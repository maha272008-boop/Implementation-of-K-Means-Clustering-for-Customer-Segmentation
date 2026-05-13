# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries such as Pandas, NumPy, and sklearn.
2.Load or create the customer dataset.
3.Select relevant features for clustering.
4.Choose number of clusters (K value).
5.Apply K Means algorithm and fit the model.
6.Predict clusters and visualize the results.
## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: MAHALAKSHMI P
RegisterNumber:212225100024
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

# Dataset
data = {
    'CustomerID': [1,2,3,4,5,6,7,8,9,10],
    'AnnualIncome': [15,16,17,18,19,20,21,22,23,24],
    'SpendingScore': [39,81,6,77,40,76,94,3,72,15]
}

df = pd.DataFrame(data)

# Features
X = df[['AnnualIncome', 'SpendingScore']]

# K Means Model
model = KMeans(n_clusters=3, random_state=42)
df['Cluster'] = model.fit_predict(X)

# Print clustered data
print(df)

# -------- Visualization --------
plt.scatter(df['AnnualIncome'], df['SpendingScore'], c=df['Cluster'], cmap='viridis')
plt.scatter(model.cluster_centers_[:,0], model.cluster_centers_[:,1], s=200, c='red', marker='X')
plt.title("Customer Segmentation using K Means")
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.show() 
*/
```

## Output:
<img width="701" height="717" alt="{1892F147-B225-4DAA-9F25-77ABFB977324}" src="https://github.com/user-attachments/assets/bb2d39e8-194f-41bb-849c-13f1c63b6df4" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
