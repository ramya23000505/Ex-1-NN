<H3>RAMYA R </H3>
<H3>212223230169 </H3>
<H3>EX. NO.1</H3>
<H3>07-03-2025</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
### Import Libraries
```py

import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
```

### Read the dataset 

```py
df=pd.read_csv("Churn_Modelling.csv")
df
```
### Checking Data
```py
df.head()
df.tail()
df.columns
```

### Check the missing data
```py
df.isnull().sum()
```

### Check for Duplicates
```py
df.duplicated()
```

### Assigning Y
```py
y = df.iloc[:, -1].values
print(y)
```

### Check for duplicates
```py
df.duplicated()
```

### Check for outliers
```py
df.describe()
```

### Dropping string values data from dataset
```py
data = df.drop(['Surname', 'Geography','Gender'], axis=1)
```
### Checking datasets after dropping string values data from dataset
```py
data.head()
```

### Normalize the dataset
```py
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(data))
print(df1)
```

### Split the dataset
```py
X=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(X)
print(y)
```

### Training and testing model
```py
X_train ,X_test ,y_train,y_test=train_test_split(X,y,test_size=0.2)
print("X_train\n")
print(X_train)
print("\nLenght of X_train ",len(X_train))
print("\nX_test\n")
print(X_test)
print("\nLenght of X_test ",len(X_test))
```
## OUTPUT:
### Data
![image](https://github.com/user-attachments/assets/60b6c086-7026-4845-9216-9773d6771b00)

### Data checking

![image](https://github.com/user-attachments/assets/a2f25808-8f26-4510-983a-c3276112828a)

### Missing Data 

![image](https://github.com/user-attachments/assets/63ea43cf-e33e-437b-ade8-0b5e4852fae4)

### Duplicates identification

![image](https://github.com/user-attachments/assets/8c5afc6b-1974-457c-ab87-d4dd46605d6a)

### Values of 'X'
![image](https://github.com/user-attachments/assets/ee6c66d2-dddd-482d-a1f2-9602f2176a2f)

### Values of 'Y'
![image](https://github.com/user-attachments/assets/32200314-e602-4510-8ed5-aebd6bc5b650)

### Outliers
![image](https://github.com/user-attachments/assets/a46ebd34-4d14-4d62-9aa6-0b68075fe623)

### Checking datasets after dropping string values data from dataset
![image](https://github.com/user-attachments/assets/f2e3d539-3ef6-4abd-8ce5-156f591651bf)

### Normalize the dataset
![image](https://github.com/user-attachments/assets/db169abd-75e1-4792-ac03-3ab7f9e4114e)

### Split the dataset
![image](https://github.com/user-attachments/assets/3d20c258-1ff8-4d64-b2bf-df22a8d165e6)

### Training and testing model
![image](https://github.com/user-attachments/assets/07d876a2-c89d-475f-9cdb-fd38c7f43db2)


## RESULT:

### Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.
