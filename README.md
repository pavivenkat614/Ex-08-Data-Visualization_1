# Data-Visualization-

## AIM
To Perform Data Visualization on the given dataset and save the data to a file. 

# Explanation
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature generation and selection techniques to all the features of the data set
### STEP 4
Apply data visualization techniques to identify the patterns of the data.


# CODE
import pandas as pd

import seaborn as sns

df=pd.read_csv("/content/SuperStore.csv")

df.info()

df.isnull().sum()

import matplotlib.pyplot as plt

import numpy as np

sns.distplot(df['Sales'])

plt.axvline(x=np.mean(df['Sales']), c='red', ls='--', label='mean')

plt.axvline(x=np.percentile(df['Sales'],25),c='green', ls='--', label = '25th percentile:Q1')

plt.axvline(x=np.percentile(df['Sales'],75),c='orange', ls='--',label = '75th percentile:Q3' )

plt.legend()

sns.boxplot(x=df['Segment'], y=df['Sales'])

sns.scatterplot(x=df['City'], y=df['Sales'])

sns.boxplot(df['Region'], df['Sales'])


# OUPUT
![image](https://user-images.githubusercontent.com/95408674/201485223-e2964966-45d5-4d20-998d-bd330cb2e025.png)

![image](https://user-images.githubusercontent.com/95408674/201485259-5171e370-dd53-489e-8396-daf8c8e7dfd5.png)

![image](https://user-images.githubusercontent.com/95408674/201485295-426e6497-ecd0-415e-b135-322e874577dc.png)

![image](https://user-images.githubusercontent.com/95408674/201485323-e0566fe7-3d83-455b-ae88-47c8d2e09b02.png)

![image](https://user-images.githubusercontent.com/95408674/201485364-16dd99aa-3bc0-4440-a6c6-eef442014d93.png)



