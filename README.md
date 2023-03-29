# Ex03-Univariate-Analysis
# Aim
To read the given data and perform the univariate analysis with different types of plots.

# Explanation
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# Algorithm
# Step1:
Read the given data.

# Step2:
Get the information about the data.

# Step3:
Remove the null values from the data.

# Step4:
Mention the datatypes from the data.

# Step5:
Count the values from the data.

# Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

# Program:
```python
Developed by : s.thirisha
Registration Number : 212222230160
import pandas as pd
import numpy as np
import seaborn as snb
df = pd.read_csv('/content/SuperStore.csv')
df.head(10)
df.info()
df.describe()
df.dtypes
df.isnull().sum()
df['Postal Code'] = df["Postal Code"].fillna(df['Postal Code'].mode()[0])
df.isnull().sum()
df['Postal Code'].value_counts()
snb.boxplot(x="Sales",data=df)
snb.countplot(x="Sales",data=df)
snb.distplot(df["Sales"])
snb.histplot(x="Sales",data=df)
df.skew()
df.kurtosis()
snb.histplot(x="Postal Code",data=df)
snb.displot(x="Postal Code",data=df)
snb.boxplot(x="Postal Code",data=df)
snb.boxplot(x="Row ID",data=df)
snb.histplot(x="Ship Mode",data=df)
snb.countplot(x="Category",data=df)
```
# output
# EDA - SuperStore.csv:
![Screenshot 2023-03-29 133148](https://user-images.githubusercontent.com/120380280/228467415-6939a5ea-5012-47ad-804a-8c92da04e51c.png)
# Displaying information about Dataset:
![image](https://user-images.githubusercontent.com/120380280/228467854-aeb1ce33-0408-4de3-a8d4-104d91c3f74a.png)
# Finding null values and cleaning it:
![image](https://user-images.githubusercontent.com/120380280/228468288-b2775698-2fce-4a93-a6d4-7c2391114351.png)
# Value counts of "Postal Code":
![image](https://user-images.githubusercontent.com/120380280/228468539-879069d0-b5d2-4150-a1e6-60959195269e.png)
# Distribution of Data:
![image](https://user-images.githubusercontent.com/120380280/228468632-6bf821b1-1e53-43bb-ac35-721bf42f03fd.png)
# Univariate Analysis:
![image](https://user-images.githubusercontent.com/120380280/228468796-eafb86c8-c06a-4176-bf59-88d95a0f20df.png)
![image](https://user-images.githubusercontent.com/120380280/228468932-4c230200-5710-4045-8cd0-17d5d7a406b6.png)
![image](https://user-images.githubusercontent.com/120380280/228468982-14d29c94-b8ab-4db3-be01-b4af228e0a08.png)
![image](https://user-images.githubusercontent.com/120380280/228469049-150c46e2-1a4f-44a5-affa-be51d516b330.png)
![image](https://user-images.githubusercontent.com/120380280/228469096-5fd3aaa8-6cd4-4baa-b8d3-b8d2cc3a7102.png)
# RESULT:
Thus the program to perform EDA on the given data set is successfully executed

