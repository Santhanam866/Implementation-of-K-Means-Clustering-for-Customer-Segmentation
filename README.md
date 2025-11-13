# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import dataset and print head,info of the dataset
2.check for null values
3.Import kmeans and fit it to the dataset
4.Plot the graph using elbow method
5.Print the predicted array
6.Plot the customer segments

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SANTHANAM S
RegisterNumber:  212224040293


import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans

wcss=[]

for i in range(1,11):

kmeans=KMeans(n_clusters=i,init="k-means++")

kmeans.fit(data.iloc[:,3:])

wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)

plt.xlabel("No_of_Clusters")

plt.ylabel("wcss")

plt.title("Elbow Method")

km=KMeans(n_clusters=5)

km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])

y_pred

data["cluster"]=y_pred

df0=data[data["cluster"]==0]

df1=data[data["cluster"]==1]

df2=data[data["cluster"]==2]

df3=data[data["cluster"]==3]

df4=data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()

plt.title("Customer Segment") 
*/
```

## Output:
## 1.DATA.HEAD():

<img width="750" height="223" alt="image" src="https://github.com/user-attachments/assets/9823f477-7e6b-4c41-89cd-9faa6ee027df" />

## 2.DATA.INF0():

<img width="652" height="275" alt="image" src="https://github.com/user-attachments/assets/1969d275-3af3-4c51-a565-73c5a534307c" />

## 3.DATA.ISNULL().SUM():

<img width="397" height="144" alt="image" src="https://github.com/user-attachments/assets/0f232e23-7a92-41fb-ae2d-57f66ecb27cb" />

## 4.PLOT USING ELBOW METHOD:

<img width="926" height="604" alt="image" src="https://github.com/user-attachments/assets/6b7956da-9a7b-487b-ba51-97864c6ff155" />

## 5.K-MEANS CLUSTERING:

<img width="363" height="84" alt="image" src="https://github.com/user-attachments/assets/29e12425-5091-4410-992c-e2ecc3d2eff7" />

## 6.Y_PRED ARRAY:

<img width="842" height="225" alt="image" src="https://github.com/user-attachments/assets/191f1de3-424c-4fcc-b02f-6d7fd7b5c8bd" />

## 7.CUSTOMER SEGMENT:

<img width="720" height="594" alt="image" src="https://github.com/user-attachments/assets/0d69f516-150d-460c-ab7e-89060e8f43af" />











## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
