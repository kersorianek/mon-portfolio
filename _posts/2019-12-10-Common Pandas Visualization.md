Note: visualization with Pandas

1.dataframe.plot()

2.subplots in different graphs 

3.subplots in one graph

4.add legend, xlim,ylim, xticks, xticks_labels



```python
import pandas as pd
import matplotlib.pyplot as plt
%matplotlib inline
```


```python
df=pd.read_csv("world happiness report.csv")
```


```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 153 entries, 0 to 152
    Data columns (total 12 columns):
    Country             153 non-null object
    Happiness Rank      153 non-null int64
    Happiness Score     153 non-null float64
    Economy             153 non-null float64
    Family              153 non-null float64
    Health              153 non-null float64
    Freedom             153 non-null float64
    Generosity          153 non-null float64
    Corruption          153 non-null float64
    Dystopia            153 non-null float64
    Job Satisfaction    151 non-null float64
    Region              153 non-null object
    dtypes: float64(9), int64(1), object(2)
    memory usage: 14.4+ KB
    


```python
df.head()
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Country</th>
      <th>Happiness Rank</th>
      <th>Happiness Score</th>
      <th>Economy</th>
      <th>Family</th>
      <th>Health</th>
      <th>Freedom</th>
      <th>Generosity</th>
      <th>Corruption</th>
      <th>Dystopia</th>
      <th>Job Satisfaction</th>
      <th>Region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Norway</td>
      <td>1</td>
      <td>7.537</td>
      <td>1.616463</td>
      <td>1.533524</td>
      <td>0.796667</td>
      <td>0.635423</td>
      <td>0.362012</td>
      <td>0.315964</td>
      <td>2.277027</td>
      <td>94.6</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Denmark</td>
      <td>2</td>
      <td>7.522</td>
      <td>1.482383</td>
      <td>1.551122</td>
      <td>0.792566</td>
      <td>0.626007</td>
      <td>0.355280</td>
      <td>0.400770</td>
      <td>2.313707</td>
      <td>93.5</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Iceland</td>
      <td>3</td>
      <td>7.504</td>
      <td>1.480633</td>
      <td>1.610574</td>
      <td>0.833552</td>
      <td>0.627163</td>
      <td>0.475540</td>
      <td>0.153527</td>
      <td>2.322715</td>
      <td>94.5</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Switzerland</td>
      <td>4</td>
      <td>7.494</td>
      <td>1.564980</td>
      <td>1.516912</td>
      <td>0.858131</td>
      <td>0.620071</td>
      <td>0.290549</td>
      <td>0.367007</td>
      <td>2.276716</td>
      <td>93.7</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Finland</td>
      <td>5</td>
      <td>7.469</td>
      <td>1.443572</td>
      <td>1.540247</td>
      <td>0.809158</td>
      <td>0.617951</td>
      <td>0.245483</td>
      <td>0.382612</td>
      <td>2.430182</td>
      <td>91.2</td>
      <td>Western Europe</td>
    </tr>
  </tbody>
</table>
</div>



if a field name is too long or not clear, df.rename can be use:
for instance:



```python
df.rename(columns={"Country":"Land"}).head() # inplance=True
```




<div>
<style>
    .dataframe thead tr:only-child th {
        text-align: right;
    }

    .dataframe thead th {
        text-align: left;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Land</th>
      <th>Happiness Rank</th>
      <th>Happiness Score</th>
      <th>Economy</th>
      <th>Family</th>
      <th>Health</th>
      <th>Freedom</th>
      <th>Generosity</th>
      <th>Corruption</th>
      <th>Dystopia</th>
      <th>Job Satisfaction</th>
      <th>Region</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Norway</td>
      <td>1</td>
      <td>7.537</td>
      <td>1.616463</td>
      <td>1.533524</td>
      <td>0.796667</td>
      <td>0.635423</td>
      <td>0.362012</td>
      <td>0.315964</td>
      <td>2.277027</td>
      <td>94.6</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Denmark</td>
      <td>2</td>
      <td>7.522</td>
      <td>1.482383</td>
      <td>1.551122</td>
      <td>0.792566</td>
      <td>0.626007</td>
      <td>0.355280</td>
      <td>0.400770</td>
      <td>2.313707</td>
      <td>93.5</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Iceland</td>
      <td>3</td>
      <td>7.504</td>
      <td>1.480633</td>
      <td>1.610574</td>
      <td>0.833552</td>
      <td>0.627163</td>
      <td>0.475540</td>
      <td>0.153527</td>
      <td>2.322715</td>
      <td>94.5</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Switzerland</td>
      <td>4</td>
      <td>7.494</td>
      <td>1.564980</td>
      <td>1.516912</td>
      <td>0.858131</td>
      <td>0.620071</td>
      <td>0.290549</td>
      <td>0.367007</td>
      <td>2.276716</td>
      <td>93.7</td>
      <td>Western Europe</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Finland</td>
      <td>5</td>
      <td>7.469</td>
      <td>1.443572</td>
      <td>1.540247</td>
      <td>0.809158</td>
      <td>0.617951</td>
      <td>0.245483</td>
      <td>0.382612</td>
      <td>2.430182</td>
      <td>91.2</td>
      <td>Western Europe</td>
    </tr>
  </tbody>
</table>
</div>



1.use country as xaxis, plot happiness and freedom for each counrty (default is line)


```python
df.head(5).plot(x='Country',y=['Happiness Score','Freedom'])
```




    <matplotlib.axes._subplots.AxesSubplot at 0x11273edd8>




    
![png](assets/img/jupyter/output_8_1.png)
    


If we want to plot bar chart, then add a parameter kind = "bar"

If there are a lot of columns we wants to include, the index of the column can also be used.
The next two plots are the same


```python
df.head(5).plot(x='Country',y=['Happiness Score','Freedom'],kind='bar')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1130ac630>




    
![png](assets/img/jupyter/output_10_1.png)
    


The same graph, but plot the field in different plot, then you can set the parameter subplots=True inside plot()


```python
df.head(5).plot(x='Country',y=['Freedom','Happiness Rank'],kind='bar',subplots=True,layout=(2,1),figsize=(12,4))
```




    array([[<matplotlib.axes._subplots.AxesSubplot object at 0x11fb846a0>],
           [<matplotlib.axes._subplots.AxesSubplot object at 0x121b25710>]], dtype=object)




    
![png](assets/img/jupyter/output_12_1.png)
    


If want to change the default title, which is the list of value in yaxis,pass a list of new name as title



```python
df.head(5).plot(x='Country',y=['Freedom','Happiness Rank'],kind='bar',subplots=True,layout=(2,1),figsize=(12,4),title=['1','2'])
```




    array([[<matplotlib.axes._subplots.AxesSubplot object at 0x122aa3860>],
           [<matplotlib.axes._subplots.AxesSubplot object at 0x122c38198>]], dtype=object)




    
![png](assets/img/jupyter/output_14_1.png)
    



```python
df.columns
```




    Index(['Country', 'Happiness Rank', 'Happiness Score', 'Economy', 'Family',
           'Health', 'Freedom', 'Generosity', 'Corruption', 'Dystopia',
           'Job Satisfaction', 'Region'],
          dtype='object')




scatter plot




```python
#df.plot.scatter(x='Country',y='Happiness Score') warning: scatter plot requires both x,y axis are numberic values
df.plot(x='Freedom',y='Happiness Score',kind='scatter')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x113d63128>




    
![png](assets/img/jupyter/output_17_1.png)
    


change the range of xaxis and yaxis

 plot two graph together using subplot and passing the order of graph i.e., axs[0] as a parameter in plot()


```python
fig,axs = plt.subplots(1,2,figsize=(12,2))
df["Freedom"].plot(ax=axs[0],title='defaut range')
df["Freedom"].plot(xlim=(0,20),ylim=(0,100), ax=axs[1],title='set range')
```




    <matplotlib.axes._subplots.AxesSubplot at 0x1165c2e48>




    
![png](assets/img/jupyter/output_19_1.png)
    


change x,y ticks 


```python
fig,axs = plt.subplots(4,1,figsize=(8,16))
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),title='set range',ax=axs[0])
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[10,20],title='set xticks',ax=axs[1])
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[i for i in range(40)],title='set xticks to int',ax=axs[2])
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[i*10 for i in range(40)],title='set xticks to text',ax=axs[3])
axs[3].set_xticklabels(['Low','Med','High'])
#axs[3].legend(['happy'],loc='upper left')
```




    [<matplotlib.text.Text at 0x124b97198>,
     <matplotlib.text.Text at 0x124ba01d0>,
     <matplotlib.text.Text at 0x124c816a0>]




    
![png](assets/img/jupyter/output_21_1.png)
    



```python
fig,axs = plt.subplots(4,1,figsize=(8,16))
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),title='set range',ax=axs[0],label='no ticks')
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[10,20],title='set xticks',ax=axs[1],label='set xticks')
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[i for i in range(40)],title='set xticks to int',ax=axs[2],label='int xiticks')
df["Happiness Score"].plot(xlim=(0,20),ylim=(0,50),xticks=[i*10 for i in range(40)],title='set xticks to text',ax=axs[3],label='text xticks')
axs[3].set_xticklabels(['Low','Med','High'])
#axs[3].legend(['happy'],loc='upper left')
legend = [ax.legend() for ax in axs]
```


    
![png](assets/img/jupyter/output_22_0.png)
    


bar chart and line chart in one graph: passing the same ax in the plot()


```python
fig, ax = plt.subplots(figsize=(12,4))
df.head(5).plot(x='Country',y='Happiness Rank',kind='bar',color='steelblue',ax=ax)
df.head(5).plot(x='Country',y='Happiness Rank',color='orange',marker='o',markersize=8,ax=ax)
ax.legend(loc='upper left',bbox_to_anchor=(1, 1))
```




    <matplotlib.legend.Legend at 0x11575a6d8>




    
![png](assets/img/jupyter/output_24_1.png)
    


set_xticks and xticklabels use together, otherwise, the first value in the xticklabels list will be missing 
ax.set_xticks([])
ax.set_xticklabels([])


```python
fig, ax = plt.subplots(figsize=(12,4))

ax.plot(df.head(5)['Happiness Rank'],marker='o', markersize=8,color='orange')
ax.bar(df.head(5).index,df.head(5)['Happiness Rank'],width=0.5)

ax.set_xticks(range(len(df.head(5))))
ax.set_xticklabels(df.head(5)['Country'].tolist())
```




    [<matplotlib.text.Text at 0x12a9919b0>,
     <matplotlib.text.Text at 0x12a8bfc50>,
     <matplotlib.text.Text at 0x12a9ee438>,
     <matplotlib.text.Text at 0x12a9eee10>,
     <matplotlib.text.Text at 0x12a9f2828>]




    
![png](assets/img/jupyter/output_26_1.png)
    



```python

```
