# Ex-04-Multivariate-Analysis

# AIM:

   To perform Multivariate EDA on the given data set.

# EXPLANATION:

Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

# ALGORITHM:

### STEP 1

Import the built libraries required to perform EDA and outlier removal.

### STEP 2

Read the given csv file.

### STEP 3

Convert the file into a dataframe and get information of the data.

### STEP 4

Return the objects containing counts of unique values using (value_counts()).

### STEP 5

Plot the counts in the form of Histogram or Bar Graph.

### STEP 6

Use seaborn the bar graph comparison of data can be viewed.

### STEP 7

Find the pairwise correlation of all columns in the dataframe.corr() .

### STEP 8

Save the final data set into the file.

#PROGRAM:


Program developed by :V.NAVYA
Register number : 212221230069

```
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

data=pd.read_csv("SuperStore.csv")
data

data.head()

data.info()

data.describe()

data.isnull().sum()

data.dtypes

sns.scatterplot(data['Postal Code'],data['Sales'])

states=data.loc[:,["State","Sales"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES")
plt.ylabel=("SALES") 
plt.show()

states=data.loc[:,["State","Postal Code"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Postal Code",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES") 
plt.ylabel=("Postal Code") 
plt.show()

states=data.loc[:,["Segment","Sales"]] 
states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(10,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("SEGMENT") 
plt.ylabel=("SALES") 
plt.show()

sns.barplot(data['Postal Code'],data['Ship Mode'],hue=data['Region'])

data.corr()

sns.heatmap(data.corr(),annot=True)

```

# OUTPUT:

### HEAD()

![image](https://user-images.githubusercontent.com/94165327/194203986-fbef5104-b3c3-4855-9bb0-f59e13771d7b.png)

### INFO()

![image](https://user-images.githubusercontent.com/94165327/194204042-4a1c4199-8857-4b06-80ac-4b2c5013504d.png)


### DESCRIBE()

![image](https://user-images.githubusercontent.com/94165327/194204097-c51be8a2-9ee0-4597-bcb2-776e2b3dfcc1.png)

### DATATYPE()

![image](https://user-images.githubusercontent.com/94165327/194204142-1fb99a62-77be-45f7-a8db-d2c9c4c9fb8f.png)

### ISNULL()

![image](https://user-images.githubusercontent.com/94165327/194204280-dc5debd0-db34-4a65-b8d7-d0b5449dc8dd.png)

### SCATTER PLOT

![image](https://user-images.githubusercontent.com/94165327/194204330-7d6d33eb-0c1f-4457-8ba2-2a9830830bd2.png)

### BARPLOT

![image](https://user-images.githubusercontent.com/94165327/194204412-0ac97616-e5ac-4d98-a410-e03f1371a404.png)


![image](https://user-images.githubusercontent.com/94165327/194204457-f0cd920c-59fd-47b0-9cf3-4c933d9c5ab0.png)

### SEGMENTATION

![image](https://user-images.githubusercontent.com/94165327/194204533-62b31b29-6a85-4871-b754-4c913f882303.png)

### SUBPLOTS

![image](https://user-images.githubusercontent.com/94165327/194204667-71430e60-8c1b-419f-96bd-68137d27e87f.png)

### CORRESSION

![image](https://user-images.githubusercontent.com/94165327/194204724-c951e9ff-2c04-4fc6-8f84-48b9d10acb6b.png)

### HEATMAP()

![image](https://user-images.githubusercontent.com/94165327/194204825-a691a633-2f41-48e3-a207-c7425ca0bb78.png)

# RESULT

Hence The Performance of the  Multivariate EDA on the given data set is verified.





