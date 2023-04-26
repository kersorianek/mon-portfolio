# Regression part 2: Advanced Techniques

By Joe Ganser

<a href="https://github.com/JoeGanser/teaching/blob/main/Lectures/supervised_learning/regression2/regression_part2.ipynb">github link</a>

### Example 1:  OLS, Ridge & Lasso

Fit ordinary least squares, Ridge regression and Lasso regression to the following data set. (dont worry about tuning hyperparamters for ridge and lasso)

* Print their coefficients for each model
* Use the models to make predictions on the data set
* Perform the predicted calculations 'by hand' for row zero of the data set.


```python
import pandas as pd
df = pd.read_csv('lecture12_example1.csv',index_col=0)
X = df.drop('arm_length',axis=1)
y = df['arm_length']
df.head()
```


| age | height | weight | male | arm_length |
|-----|--------|--------|------|------------|
| 23.3   | 163    | 100  | 1          | 22.3 |
| 34.0   | 190    | 95   | 0          | 24.3 |
| 17.0   | 180    | 143  | 1          | 22.1 |






```python
from sklearn.linear_model import Ridge,Lasso,LinearRegression,ElasticNet

for m in [Ridge,Lasso,ElasticNet,LinearRegression]:
    m = m()
    m.fit(X,y)
    y_pred = m.predict(X)
    print(m)
    print('coefficients: ',m.coef_)
    print('intercept: ',m.intercept_)
    print('predictions: ',y_pred)
    print('\n')
```

    Ridge()
    coefficients:  [ 0.02695934  0.05870384 -0.02395133 -0.00235268]
    intercept:  14.502675925812566
    predictions:  [22.30206924 24.29764732 22.10028344]
    
    
    Lasso()
    coefficients:  [ 0.          0.0599208  -0.02923667 -0.        ]
    intercept:  15.548069696525761
    predictions:  [22.39149279 24.15553771 22.1529695 ]
    
    
    ElasticNet()
    coefficients:  [ 0.          0.06380857 -0.03038895 -0.        ]
    intercept:  14.987166308050938
    predictions:  [22.34906773 24.22384384 22.12708843]
    
    
    LinearRegression()
    coefficients:  [ 0.02701024  0.05884593 -0.02395852 -0.00235768]
    intercept:  14.476984164678683
    predictions:  [22.3 24.3 22.1]
    
    


### Example 2: Grid Searching for hyperparameters

**Using the dataset, `lecture12_example2.csv` use `GridSearchCV` to test different values of `alpha` for `Ridge()`, `Lasso()`, `ElasticNet()`.**

* Let `alpha=np.arange(0,1,0.01)`
* For the case of `ElasticNet()`, use `alpha` and also use `l1_ratio=np.arange(0,1,0.01)`


```python
import pandas as pd
data2 = pd.read_csv('lecture12_example2.csv',index_col=0)
X2 = data2.drop('target',axis=1)
y2 = data2['target']
data2.head()
```


| 0 | 1         | 2         | 3        | 4         | 5         | 6         | 7         | 8         | 9         | ...       | 301 | 302       | 303       | 304       | 305       | 306       | 307       | 308       | 309       | target    |
|---|-----------|-----------|----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| 0 | 2.330870  | -1.612841 | 1.339116 | -2.430704 | -0.093109 | -1.316382 | -0.457527 | 0.462286  | 0.810499  | 0.572844  | ... | 1.376158  | 0.542736  | -1.411426 | -1.881519 | -0.733447 | 0.651879  | -0.204618 | 1.350441  | 0.743563  | -1441.211856 |
| 1 | 0.027808  | -0.679261 | 0.871705 | 0.745946  | 0.688176  | -1.963766 | -0.254602 | 1.559677  | 1.727085  | 1.680125  | ... | 0.651409  | -1.883939 | 0.600215  | -0.506214 | 0.083978  | 0.804308  | 0.090795  | -0.573402 | -0.865638 | 91.855773    |
| 2 | 1.186985  | -0.130896 | 1.458549 | -0.629930 | -3.175641 | 1.135818  | -1.184185 | 2.579488  | 2.357140  | 0.128912  | ... | 0.612371  | 0.840436  | -2.393615 | 0.320818  | 0.158502  | -0.701265 | 0.641657  | -0.303029 | 0.078271  | -1133.264673 |
| 3 | -1.614443 | 0.410332  | 0.557796 | -0.273931 | 2.244855  | 0.303914  | 0.957551  | 0.596357  | -0.297291 | -1.785487 | ... | 0.027101  | -1.205863 | -0.781089 | -0.557228 | 1.682864  | 0.588004  | 0.771023  | 1.279060  | 0.373258  | -1084.860469 |
| 4 | -0.397127 | -2.174227 | 1.210069 | 0.805470  | 2.251384  | -0.513468 | -1.572685 | -0.690919 | -0.549232 | 0.203158  | ... | -1.027788 | -0.478835 | 1.215282  | 0.148531  | -0.449885 | 0.926758  | -0.275255 | -0.460199 | -0.826239 | -269.257935  |


<p>5 rows × 311 columns</p>





```python
import warnings
warnings.filterwarnings('ignore')
from sklearn.model_selection import train_test_split, GridSearchCV
alpha = np.arange(0,1,0.01)
for m in [Ridge,Lasso,ElasticNet]:
    if m!=ElasticNet:
        parameters = {'alpha':alpha}
    else:
        parameters = {'alpha':alpha,'l1_ratio':alpha}
    gs = GridSearchCV(m(),parameters)
    gs.fit(X2,y2)
    print(gs.best_estimator_)
    print(gs.best_score_)
    print('\n')
```

    Ridge(alpha=0.0)
    0.603656993865098
    
    
    Lasso(alpha=0.03)
    0.4571337721470381
    
    
    ElasticNet(alpha=0.08, l1_ratio=0.84)
    0.6041495435590333
    
    


### Example 3: Grid Search & Stochastic Gradient Descent

* `SGDRegressor` can use `Ridge`, `Lasso` or `ElasticNet` as it's regression protocol.
* Let the parameters cycled through be 
    * `sgd_params = {'penalty':['l1','l2'],'alpha':np.arange(0,1,0.1),'l1_ratio':np.arange(0,1,0.1)}`


```python
import pandas as pd
import numpy as np
df3 = pd.read_csv('lecture12_example3.csv',index_col=0)
X3 = df3.drop('target',axis=1)
y3 = df3['target']
df3.head()
```

| 0 | 1         | 2         | 3         | 4         | 5         | 6         | 7         | target    |
|---|-----------|-----------|-----------|-----------|-----------|-----------|-----------|-----------|
| 0 | 0.440476  | -0.539437 | -0.741995 | 0.222795  | -0.174341 | 0.286436  | -0.930370 | 0.270159  | -8.406421   |
| 1 | -1.194987 | -0.162277 | -1.511640 | 0.726551  | 1.905424  | -0.084078 | -0.075408 | -1.097597 | -17.903971  |
| 2 | -0.754477 | -1.311020 | 0.494098  | -1.356511 | -0.893744 | -1.901495 | -0.354791 | -1.292560 | -212.767631 |
| 3 | -1.551001 | 0.273258  | 0.111347  | -0.161415 | -0.491677 | -1.181606 | -0.669466 | -3.642809 | -200.496421 |
| 4 | 1.270708  | -0.786369 | -0.577232 | 1.197173  | 0.013121  | 0.612230  | 0.011464  | 2.359498  | 165.434211  |



```python
from sklearn.linear_model import SGDRegressor
from sklearn.model_selection import GridSearchCV


sgd_params = {'penalty':['l1','l2'],'alpha':np.arange(0,1,0.1),'l1_ratio':np.arange(0,1,0.1)}
gs_sgd = GridSearchCV(SGDRegressor(loss='squared_loss'),param_grid=sgd_params)
gs_sgd.fit(X3,y3)
print(gs_sgd.best_estimator_)
print(gs_sgd.best_score_)
```

    SGDRegressor(alpha=0.0, l1_ratio=0.7000000000000001)
    0.9999999999763147

