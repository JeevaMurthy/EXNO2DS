# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
REG NO: 212223230090
NAME : JEEVA K
```

```python
import pandas as pd
df=pd.read_csv('/content/titanic_dataset.csv')
df
```

![alt text](<Screenshot 2024-09-11 092318.png>)


```python
df.shape
```


![alt text](<Screenshot 2024-09-11 092327.png>)


```python
df.isnull().sum()
```

![alt text](<Screenshot 2024-09-11 092334.png>)



```python
df.dropna(inplace=True)
```
```python
df.isnull().sum()
```


![alt text](<Screenshot 2024-09-11 092343.png>)



```python
df.info()
```


![alt text](<Screenshot 2024-09-11 092350.png>)



```python
df.shape
```

![alt text](<Screenshot 2024-09-11 092355.png>)



```python
df.set_index("PassengerId",inplace=True)
```





```python
df.describe()
```

![alt text](<Screenshot 2024-09-11 092402.png>)


```python
df
```

![alt text](<Screenshot 2024-09-11 092409.png>)


```python
df.nunique()
```

![alt text](<Screenshot 2024-09-11 092416.png>)

```python
df["Survived"].value_counts()
```

![alt text](<Screenshot 2024-09-11 092422.png>)


```python
per=(df["Survived"].value_counts()/df.shape[0]*100).round(2)
per
```

![alt text](<Screenshot 2024-09-11 092427.png>)



```python
import matplotlib.pyplot as plt
import seaborn as sns
```


```python
sns.countplot(data=df,x="Survived")
```

![alt text](<Screenshot 2024-09-11 092444.png>)



```python
df
```

![alt text](<Screenshot 2024-09-11 092452.png>)


```python
df.Pclass.unique()
```

![alt text](<Screenshot 2024-09-11 092458.png>)

```python
sns.catplot(x="Sex",col="Survived",kind="count",data=df,height=5,aspect=.7)
```

![alt text](<Screenshot 2024-09-11 092505.png>)


```python
sns.catplot(x='Survived',hue="Sex",data=df,kind="count")
```

![alt text](<Screenshot 2024-09-11 092513.png>)



```python
sns.catplot(data=df,col="Survived",x="Sex",hue="Pclass",kind="count")
```

![alt text](<Screenshot 2024-09-11 092528.png>)

# RESULT
The Exploratory Data Analysis on the given data set has been performed.

