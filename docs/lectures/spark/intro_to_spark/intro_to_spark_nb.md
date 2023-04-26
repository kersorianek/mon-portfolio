# Intro to Spark with Python

by Joe Ganser

<a href="https://github.com/JoeGanser/teaching/blob/main/Lectures/Spark/Intro_to_spark.ipynb">Github Repo Link</a>

## Beginning a Py-Spark session

The begin working with spark on a local machine (with Python), we should import the `SparkSession` package and use it's `.getOrCreate()` method to develop a spark work flow.


```python
try:
    from pyspark.sql import SparkSession
except:
    !pip install pyspark
    from pyspark.sql import SparkSession

spark = SparkSession.builder.appName("Python Spark SQL basic example")\
                            .config("spark.some.config.option", "some-value")\
                            .getOrCreate()
```



## Load a data frame

Heres a a simple example of loading a dataframe from a source on <a href="https://github.com/JoeGanser/Spark-The-Definitive-Guide/blob/master/data/flight-data/csv/2015-summary.csv">Github</a>.

* Add the remote file to our spark context using `spark.sparkContext.addFile(url)`
* Use the `SparkFiles` method to access temporarily downloaded csv file to our `SparkSession`
* Tell spark we want to look for the dataframes header by specifying `header=True`
* Tell spark to infer the schema (figure out the column name data types), etc using `inferSchema=True`.
* Show the first 20 rows uing the `.show()` method


```python
url = 'https://raw.githubusercontent.com/JoeGanser/Spark-The-Definitive-Guide/master/data/flight-data/csv/'
csv_file = "2015-summary.csv"
url = url+csv_file
from pyspark import SparkFiles
spark.sparkContext.addFile(url)

flightData2015 = spark.read.csv("file://"+SparkFiles.get(csv_file), header=True, inferSchema= True)
flightData2015.show()
```

    +--------------------+-------------------+-----+
    |   DEST_COUNTRY_NAME|ORIGIN_COUNTRY_NAME|count|
    +--------------------+-------------------+-----+
    |       United States|            Romania|   15|
    |       United States|            Croatia|    1|
    |       United States|            Ireland|  344|
    |               Egypt|      United States|   15|
    |       United States|              India|   62|
    |       United States|          Singapore|    1|
    |       United States|            Grenada|   62|
    |          Costa Rica|      United States|  588|
    |             Senegal|      United States|   40|
    |             Moldova|      United States|    1|
    |       United States|       Sint Maarten|  325|
    |       United States|   Marshall Islands|   39|
    |              Guyana|      United States|   64|
    |               Malta|      United States|    1|
    |            Anguilla|      United States|   41|
    |             Bolivia|      United States|   30|
    |       United States|           Paraguay|    6|
    |             Algeria|      United States|    4|
    |Turks and Caicos ...|      United States|  230|
    |       United States|          Gibraltar|    1|
    +--------------------+-------------------+-----+
    only showing top 20 rows
    


## printSchema( ) method

Schemas are an important part of working with Spark. They tell use the column names, data types and if the column can contain null values. We can save computational power by telling Spark the schema of data source before loading it. If we want to take a look at a dataframe's schema we use the `.printSchema()` method.


```python
flightData2015.printSchema()
```

    root
     |-- DEST_COUNTRY_NAME: string (nullable = true)
     |-- ORIGIN_COUNTRY_NAME: string (nullable = true)
     |-- count: integer (nullable = true)
    


## Selecting a specific columns

To select a specific column you use the `.select(columnname1, columnname2..)` method on the dataframe object.


```python
selection = flightData2015.select('DEST_COUNTRY_NAME','count')
selection.show()
```

    +--------------------+-----+
    |   DEST_COUNTRY_NAME|count|
    +--------------------+-----+
    |       United States|   15|
    |       United States|    1|
    |       United States|  344|
    |               Egypt|   15|
    |       United States|   62|
    |       United States|    1|
    |       United States|   62|
    |          Costa Rica|  588|
    |             Senegal|   40|
    |             Moldova|    1|
    |       United States|  325|
    |       United States|   39|
    |              Guyana|   64|
    |               Malta|    1|
    |            Anguilla|   41|
    |             Bolivia|   30|
    |       United States|    6|
    |             Algeria|    4|
    |Turks and Caicos ...|  230|
    |       United States|    1|
    +--------------------+-----+
    only showing top 20 rows
    


## Selecting with SQL like expressions

We can select specific columns and even pass aggregation functions (e.g. `count`,`max`,`sum`) using the `selectExpr()` method on Spark dataframes.


```python
flightData2015.selectExpr('DEST_COUNTRY_NAME', 'count').show(5)
```

    +-----------------+-----+
    |DEST_COUNTRY_NAME|count|
    +-----------------+-----+
    |    United States|   15|
    |    United States|    1|
    |    United States|  344|
    |            Egypt|   15|
    |    United States|   62|
    +-----------------+-----+
    only showing top 5 rows
    



```python
flightData2015.selectExpr('count(DEST_COUNTRY_NAME)', 'max(count)').show()
```

    +------------------------+----------+
    |count(DEST_COUNTRY_NAME)|max(count)|
    +------------------------+----------+
    |                     256|    370002|
    +------------------------+----------+
    


## DataFrame analytics

We can describe the dataframe using the `.describe()` method.


```python
flightData2015.describe().show()
```

    +-------+-----------------+-------------------+------------------+
    |summary|DEST_COUNTRY_NAME|ORIGIN_COUNTRY_NAME|             count|
    +-------+-----------------+-------------------+------------------+
    |  count|              256|                256|               256|
    |   mean|             null|               null|       1770.765625|
    | stddev|             null|               null|23126.516918551915|
    |    min|          Algeria|             Angola|                 1|
    |    max|           Zambia|            Vietnam|            370002|
    +-------+-----------------+-------------------+------------------+
    


We can combine this method with the `select()` in a code chain to act only on specific columns.


```python
flightData2015.select('DEST_COUNTRY_NAME','ORIGIN_COUNTRY_NAME')\
              .describe()\
              .show()
```

    +-------+-----------------+-------------------+
    |summary|DEST_COUNTRY_NAME|ORIGIN_COUNTRY_NAME|
    +-------+-----------------+-------------------+
    |  count|              256|                256|
    |   mean|             null|               null|
    | stddev|             null|               null|
    |    min|          Algeria|             Angola|
    |    max|           Zambia|            Vietnam|
    +-------+-----------------+-------------------+
    


## Group by aggregation

We can group by specific columns using the `.groupby()` and `.agg()` functions.

For every origin country in the data set, count the number of destination countries. Sort the values in decreasing order.


```python
from pyspark.sql.functions import count,col
flightData2015.groupby('ORIGIN_COUNTRY_NAME')\
              .agg(count(col('DEST_COUNTRY_NAME')))\
              .orderBy("count(DEST_COUNTRY_NAME)",ascending=False)\
              .show()
```

    +--------------------+------------------------+
    | ORIGIN_COUNTRY_NAME|count(DEST_COUNTRY_NAME)|
    +--------------------+------------------------+
    |       United States|                     132|
    |            Paraguay|                       1|
    |            Anguilla|                       1|
    |              Russia|                       1|
    |              Guyana|                       1|
    |             Senegal|                       1|
    |              Sweden|                       1|
    |            Kiribati|                       1|
    |               Palau|                       1|
    |         Philippines|                       1|
    |           Singapore|                       1|
    |            Malaysia|                       1|
    |                Fiji|                       1|
    |              Turkey|                       1|
    |             Germany|                       1|
    |              Jordan|                       1|
    |Turks and Caicos ...|                       1|
    |              France|                       1|
    |              Greece|                       1|
    |British Virgin Is...|                       1|
    +--------------------+------------------------+
    only showing top 20 rows
    


## Adding a new column to the dataset

If we want to add a new column to our dataframe, we can use the `.withColumn(column_name, column_data)` method, where `column_name` and `column_data` are the arguments.

In this example we create a columnd `double the count` that takes the values of the `count` column and doubles them.


```python
flightData2015 = flightData2015.withColumn('double the count',flightData2015['count']*2)
flightData2015.show()
```

    +--------------------+-------------------+-----+----------------+
    |   DEST_COUNTRY_NAME|ORIGIN_COUNTRY_NAME|count|double the count|
    +--------------------+-------------------+-----+----------------+
    |       United States|            Romania|   15|              30|
    |       United States|            Croatia|    1|               2|
    |       United States|            Ireland|  344|             688|
    |               Egypt|      United States|   15|              30|
    |       United States|              India|   62|             124|
    |       United States|          Singapore|    1|               2|
    |       United States|            Grenada|   62|             124|
    |          Costa Rica|      United States|  588|            1176|
    |             Senegal|      United States|   40|              80|
    |             Moldova|      United States|    1|               2|
    |       United States|       Sint Maarten|  325|             650|
    |       United States|   Marshall Islands|   39|              78|
    |              Guyana|      United States|   64|             128|
    |               Malta|      United States|    1|               2|
    |            Anguilla|      United States|   41|              82|
    |             Bolivia|      United States|   30|              60|
    |       United States|           Paraguay|    6|              12|
    |             Algeria|      United States|    4|               8|
    |Turks and Caicos ...|      United States|  230|             460|
    |       United States|          Gibraltar|    1|               2|
    +--------------------+-------------------+-----+----------------+
    only showing top 20 rows
    


## Dropping columns

We can drop columns using the `.drop()` method.


```python
flightData2015 = flightData2015.drop('double the count')
flightData2015.show()
```

    +--------------------+-------------------+-----+
    |   DEST_COUNTRY_NAME|ORIGIN_COUNTRY_NAME|count|
    +--------------------+-------------------+-----+
    |       United States|            Romania|   15|
    |       United States|            Croatia|    1|
    |       United States|            Ireland|  344|
    |               Egypt|      United States|   15|
    |       United States|              India|   62|
    |       United States|          Singapore|    1|
    |       United States|            Grenada|   62|
    |          Costa Rica|      United States|  588|
    |             Senegal|      United States|   40|
    |             Moldova|      United States|    1|
    |       United States|       Sint Maarten|  325|
    |       United States|   Marshall Islands|   39|
    |              Guyana|      United States|   64|
    |               Malta|      United States|    1|
    |            Anguilla|      United States|   41|
    |             Bolivia|      United States|   30|
    |       United States|           Paraguay|    6|
    |             Algeria|      United States|    4|
    |Turks and Caicos ...|      United States|  230|
    |       United States|          Gibraltar|    1|
    +--------------------+-------------------+-----+
    only showing top 20 rows
    


## Renaming Columns

We can rename columns using the `.withColumnRenamed(old_column_name, new_column_name)` method


```python
flightData2015.withColumnRenamed('DEST_COUNTRY_NAME','DEST')\
              .withColumnRenamed('ORIGIN_COUNTRY_NAME','ORIGIN')\
              .show()
```

    +--------------------+----------------+-----+
    |                DEST|          ORIGIN|count|
    +--------------------+----------------+-----+
    |       United States|         Romania|   15|
    |       United States|         Croatia|    1|
    |       United States|         Ireland|  344|
    |               Egypt|   United States|   15|
    |       United States|           India|   62|
    |       United States|       Singapore|    1|
    |       United States|         Grenada|   62|
    |          Costa Rica|   United States|  588|
    |             Senegal|   United States|   40|
    |             Moldova|   United States|    1|
    |       United States|    Sint Maarten|  325|
    |       United States|Marshall Islands|   39|
    |              Guyana|   United States|   64|
    |               Malta|   United States|    1|
    |            Anguilla|   United States|   41|
    |             Bolivia|   United States|   30|
    |       United States|        Paraguay|    6|
    |             Algeria|   United States|    4|
    |Turks and Caicos ...|   United States|  230|
    |       United States|       Gibraltar|    1|
    +--------------------+----------------+-----+
    only showing top 20 rows
    


## Filtering Columns for specific row values

We can filter the dataframe to display only rows yielding specific values using the `.filter()` method. The arguments use a SQL like syntax


```python
flightData2015.filter("DEST_COUNTRY_NAME = 'United States'")\
              .show()
```

    +-----------------+--------------------+-----+
    |DEST_COUNTRY_NAME| ORIGIN_COUNTRY_NAME|count|
    +-----------------+--------------------+-----+
    |    United States|             Romania|   15|
    |    United States|             Croatia|    1|
    |    United States|             Ireland|  344|
    |    United States|               India|   62|
    |    United States|           Singapore|    1|
    |    United States|             Grenada|   62|
    |    United States|        Sint Maarten|  325|
    |    United States|    Marshall Islands|   39|
    |    United States|            Paraguay|    6|
    |    United States|           Gibraltar|    1|
    |    United States|Federated States ...|   69|
    |    United States|              Russia|  161|
    |    United States|         Netherlands|  660|
    |    United States|             Senegal|   42|
    |    United States|              Angola|   13|
    |    United States|            Anguilla|   38|
    |    United States|             Ecuador|  300|
    |    United States|              Cyprus|    1|
    |    United States|            Portugal|  134|
    |    United States|          Costa Rica|  608|
    +-----------------+--------------------+-----+
    only showing top 20 rows
    


## Using SQL to query dataframe values

We can run sql queries on a dataframe using `spark.sql( query text )` method. But before we can do that, we must first register the table as one that can be queried using sql. This is done using the `.registerTempTable(tablename)` method.


```python
#Writing in SQL example
flightData2015.registerTempTable("flightData2015")

spark.sql("select distinct DEST_COUNTRY_NAME from flightData2015 order by DEST_COUNTRY_NAME ASC")\
     .show(20)
```

    /usr/local/lib/python3.7/dist-packages/pyspark/sql/dataframe.py:229: FutureWarning: Deprecated in 2.0, use createOrReplaceTempView instead.
      warnings.warn("Deprecated in 2.0, use createOrReplaceTempView instead.", FutureWarning)


    +--------------------+
    |   DEST_COUNTRY_NAME|
    +--------------------+
    |             Algeria|
    |              Angola|
    |            Anguilla|
    | Antigua and Barbuda|
    |           Argentina|
    |               Aruba|
    |           Australia|
    |             Austria|
    |          Azerbaijan|
    |             Bahrain|
    |            Barbados|
    |             Belgium|
    |              Belize|
    |             Bermuda|
    |             Bolivia|
    |Bonaire, Sint Eus...|
    |              Brazil|
    |British Virgin Is...|
    |            Bulgaria|
    |        Burkina Faso|
    +--------------------+
    only showing top 20 rows
    



```python

```

## Sources

Some of the notes here were taken from the following text book, in conjunction to examples written by myself.

* Spark: The Definitive Guide Big Data Processing Made Simple, Bill Chabers & Matel Zaharia, O'Reilly Publications 2018
    * Purchase here: <a href='https://www.amazon.com/s?k=spark+the+definitive+guide&crid=2VERI00ZCPTLK&sprefix=spark+the+definitive+guide%2Caps%2C107&ref=nb_sb_noss_1'>Amazon Link</a>.


```python

```
