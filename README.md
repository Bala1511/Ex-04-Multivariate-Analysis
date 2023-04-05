# Ex-04-Multivariate-Analysis

AIM:

write a python program to visualize the given data by analysing the multivariables in data

ALGORITHM:

step1: 

import the csv file using pandas package. #step2: store the data as dataframe in a variable. #step3: display the information of data sunch as datatypes,value counts,skewness #step4: display the data in the barplot,scatter plot and heatmap

CODE:

```
import pandas as pd 
import seaborn as sns
from matplotlib import pyplot as plt
df=pd.read_csv('SuperStore.csv')
df.info()
```

```
df.dtypes
df['State'].value_counts()
df.describe()
df.kurtosis()
```
```
sns.scatterplot(x=df['Postal Code'],y=df['Sales'])
```
```
sns.barplot(x=df['Postal Code'],y=df['Sales'])
```
```
df.info()
```
```
postal=df.loc[:,["Sales","Postal Code"]]
postal=postal.groupby(by=["Postal Code"]).sum().sort_values(by="Sales")
sns.barplot(x=postal.index,y="Sales",data=postal)
plt.xticks(rotation=90)
plt.xlabel=("Postal")
plt.ylabel=("Sales")
plt.show()
```
```
sns.heatmap(df.corr())
```
OUTPUT:

![ws 2 1](https://user-images.githubusercontent.com/118680410/230147684-edb7ca33-3942-442b-b92d-153444aff3e2.png)
![ws2 2](https://user-images.githubusercontent.com/118680410/230148288-b2f38752-d83e-4c83-9822-ca7e7c0a96d2.png)
![ws2 4![ws2 3](https://user-images.githubusercontent.com/118680410/230148731-2394d75b-de5e-4a1b-9ba6-183a9598810a.png)
](https://user-images.githubusercontent.com/118680410/230148307-ae9a1781-cabd-44db-8464-5dbaa314c7c8.png)
![ws2 5](https://user-images.githubusercontent.com/118680410/230148337-09acd4f0-7d4f-41a7-9080-901a39ccc328.png)
![ws2 6](https://user-images.githubusercontent.com/118680410/230148376-8d2f4fb1-c0f8-4319-bc99-e35fc5d330c5.png)
![ws2 7](https://user-images.githubusercontent.com/118680410/230148596-854cded5-f2d9-4fd3-b6a2-1335addd8581.png)
![ws2 8](https://user-images.githubusercontent.com/118680410/230148463-7930beec-bce8-4d3d-8e1f-05717204c0ac.png)
![ws2 9](https://user-images.githubusercontent.com/118680410/230148808-41d9f9b2-56f6-45e5-8092-6befe3bcc7a3.png)

RESULT:

thus the experiment executed sucessfully.
