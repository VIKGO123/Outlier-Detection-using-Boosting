# Project Title

Product Range Determination using Efficient Boosting Method

## Project Description

Determination of Minimum and Maximum Prices of 100 category items based on given conditions, using the method of Boosting for removing outliers and then finding minimum and maximum prices for different categories.Also finding three most common prices for different categories unit-wise using python's collection library.
 
 Outlier Detection Unsupervised Methods employed 



## Authors
1.[Vikash Pathak](https://vikgo123.github.io/)

2.[Kiran Kumar](https://github.com/Apollo9999)


### Prerequisites

IndiaMART Phase2 Dataset

 [Phase2 Dataset Link](https://drive.google.com/open?id=1WdCNbjhlZgGkVnGvfforOJhS0961MMd6)


### Efficient Boosting for Outlier Elimination

```
Boosting ensemble technique with two models has been used for outlier detection and removal.

The two models are:
1. Inter-quartile range(IQR) also called Box-Plot method 
2. Isolation Forest method

Dataset is first passed through IQR model and then through Isolation forest model.
The maximum and minimum from the outlier removed data is found to get the range of price 
for a particular category based on the conditions imposed. 
```

### Inter-Quartile Range(IQR) Model
![IQR Method Example](https://github.com/VIKGO123/Outlier-Detection-using-Boosting/blob/master/raw%20images/IQR%20Method%20Example.png)

```
def outliers_iqr(ys):
    quartile_1, quartile_3 = np.percentile(ys, [25, 75])
    iqr = quartile_3 - quartile_1
    lower_bound = quartile_1 - (iqr * 1.5)
    upper_bound = quartile_3 + (iqr * 1.5)
    result=[]
    for i in ys:
      if(i<=upper_bound and i>=lower_bound):
        result.append(i)
    return result
```
### Isolation Forest Model
![Isolation Forest Model](https://github.com/VIKGO123/Outlier-Detection-using-Boosting/blob/master/raw%20images/IQR%20Method%20Example.png)

```
from sklearn.ensemble import IsolationForest
def isolationForest(ys):
  clf = IsolationForest(max_samples=100, random_state=42)

  clf.fit(ys)
  output_table =(clf.predict(ys))
  c=0
  result=[]
  for i in output_table:
    if(i!=-1):
      result.append(ys[c,0])
    c=c+1
  return result
```


### Category-Unit wise three most common prices


Counter function of python's Collection module is used on outlier removed data to get category-unit
wise three most common prices.
```
import collections
def mostcommon(a):
  counter=collections.Counter(a)
  l=counter.most_common(3)
  
```


### Models Used

Ensemble Technique - Boosting

```
Models used in Boosting (For Outlier Elimination)

1. Inter-quartile Range or Box-Plot Method
2. Isolation Forest Method
```
### Tech Stack

#### Programming Language
```
1.Python
```
#### Development Environment
```
1.Google Colaboratory Notebook
2.Python 3.x

```
#### Python Libraries
```
1.Numpy
2.Pandas
3.Sklearn
4.Collections

```

### Model Architecture
![Model Architecture](https://github.com/VIKGO123/Outlier-Detection-using-Boosting/blob/master/raw%20images/model_arch.JPG)


### Initial Dataset
![intial dataset](https://github.com/VIKGO123/Outlier-Detection-using-Boosting/blob/master/raw%20images/initial_dataset.JPG)


### Final Result
![final result](https://github.com/VIKGO123/Outlier-Detection-using-Boosting/blob/master/raw%20images/final_result.JPG)







