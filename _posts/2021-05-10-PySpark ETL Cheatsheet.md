
# 🚀 Automated ETL with PySpark & dbt on Azure Synapse (2021 Edition)

This project documents how I migrated legacy Pandas-based ETL scripts into a scalable PySpark pipeline on Azure Synapse, integrating `dbt` for clean modeling and orchestration. All examples are version-compatible with **PySpark 3.0–3.1** and reflect Azure Synapse capabilities in **2021**.

---

## 🧠 Background

Originally, our data transformation logic was a mix of scattered Python scripts using Pandas—running locally, with no scheduling, no documentation, and no scalability. I rebuilt these pipelines in PySpark on Azure Synapse, and layered in `dbt` to manage transformations downstream in a modular, declarative way.

---

## 🛠 PySpark ETL Cheatsheet (2021 Safe)

Here are the most common transformations I used to replace legacy Pandas logic:

### 📅 Reading Data

```python
df = spark.read \
    .option("header", True) \
    .option("inferSchema", True) \
    .csv("abfss://mycontainer@mystorage.dfs.core.windows.net/myfile.csv")

df_parquet = spark.read.parquet("path/to/file.parquet")
```

---

### 🔍 Inspecting Data

```python
df.printSchema()
df.show(5)
df.describe().show()
df.columns
df.count()
```

---

### 🔎 Filtering Rows

```python
from pyspark.sql.functions import col

df_filtered = df.filter(col("age") > 30)
```

---

### 🧱 Selecting & Renaming Columns

```python
df = df.select("name", "age")
df = df.withColumnRenamed("old_name", "new_name")
```

---

### 🧠 Conditional Columns

```python
from pyspark.sql.functions import when

df = df.withColumn("age_group", when(col("age") < 18, "child").otherwise("adult"))
```

---

### ✂️ Dropping Columns / Nulls

```python
df = df.drop("unused_column")
df = df.dropna()
df = df.fillna({"country": "Unknown", "salary": 0})
```

---

### 📊 GroupBy & Aggregation

```python
from pyspark.sql.functions import avg, max

df_grouped = df.groupBy("department").agg(
    avg("salary").alias("avg_salary"),
    max("salary").alias("max_salary")
)
```

---

### 🔠 String Operations

```python
from pyspark.sql.functions import lower, upper, trim

df = df.withColumn("clean_name", trim(lower(col("name"))))
```

---

### 📅 Date Handling

```python
from pyspark.sql.functions import to_date, year

df = df.withColumn("join_date", to_date(col("join_ts"), "yyyy-MM-dd"))
df = df.withColumn("join_year", year(col("join_date")))
```

---

### 🔗 Joining DataFrames

```python
df_joined = df1.join(df2, on="id", how="inner")
```

---

### 📆 Writing to Azure Data Lake (Parquet)

```python
df.write \
    .mode("overwrite") \
    .parquet("abfss://mycontainer@mystorage.dfs.core.windows.net/output_folder/")
```

---

## 📦 dbt Integration (Optional but Recommended)

While PySpark handles heavy data lifting, `dbt` was used to manage the **semantic layer** and **SQL-based transformations**, such as:
- Filtering outputs into dimensional models
- Creating summary tables
- Enabling downstream BI and analytics use cases

Example `dbt` model:

```sql
-- models/clean_customer_data.sql
SELECT
    id,
    TRIM(LOWER(name)) AS clean_name,
    CAST(age AS INT) AS age
FROM {{ ref('raw_customer_data') }}
WHERE age IS NOT NULL
```

---

## ✅ Why This Upgrade Was Worth It

| Feature               | Before (Pandas Scripts) | After (PySpark + dbt)        |
|----------------------|-------------------------|-------------------------------|
| Runtime              | Manual/local            | Scalable/Synapse Spark Pools |
| Scheduling           | None                    | Orchestrated via Synapse Pipelines |
| Modularity           | Low                     | High (thanks to dbt)          |
| Schema evolution     | Manual                  | Automatic with `inferSchema` |
| Performance          | Limited by RAM          | Distributed Spark Execution  |

---

## 🧵 Next Steps

- Add CI/CD to dbt models using Azure DevOps
- Enable Delta Lake for ACID-compliant outputs
- Build alerting into Synapse pipelines

---

## 📬 Questions or Feedback?

Feel free to open an issue or reach out if you’re modernizing your ETL stack and want some war stories.
