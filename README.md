# Project Title

Range Determination using Boosting

## Project Description

Determination of Minimum and Maximum Prices of 100 category items based on given conditions, using the method of Boosting for removing outliers and then finding minimum and maximum prices for different categories.Also finding three most common prices for different categories unit-wise using python's collection library.


## AUTHORS
1.[Vikash Pathak](https://vikgo123.github.io/)
2.


### Prerequisites

IndiaMART Phase2 Dataset

 [Phase2 Dataset Link](https://drive.google.com/open?id=1WdCNbjhlZgGkVnGvfforOJhS0961MMd6)


### Boosting for Outlier Elimination

```
Boosting ensemble technique with two models has been used for outlier detection and removal.

The two models are:
1. Inter-quartile range(IQR) also called Box-Plot method
2. Isolation Forest method

Dataset is first passed through IQR model and then through Isolation forest model.
The maximum and minimum from the outlier removed data is found to get the range of price 
for a particular category based on the conditions imposed. 
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





