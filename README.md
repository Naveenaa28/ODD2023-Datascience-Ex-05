## Ex:05 Feature Generation
## AIM :
To read the given data and perform Feature Generation process and save the data to a file.

## EXPLANATION :
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM :
STEP 1 : Read the given Data

STEP 2 : Clean the Data Set using Data Cleaning Process

STEP 3 : Apply Feature Generation techniques to all the feature of the data set

STEP 4 : Save the data to the file

## PROGRAM :
```
NAVEENAA V.R
212221220035
```
## bmi.csv
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```
## data.csv
```
import pandas as pd
df1 = pd.read_csv("/content/data (1).csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
## Encoding.csv
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data (1).csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
## OUTPUT:
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/5c48cba6-9fe8-4c56-b0e2-008290bf70f0)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/1ca853ca-b4ef-4a96-93ca-e15df3ec711d)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/c6295ebb-9182-4878-ac14-55d29c17686c)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/c3f760c6-f0ad-4931-b3ec-7ffce93a2fa8)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/5b334368-9ecb-4e8e-bf8d-3f50054b3a64)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/6ec05858-991d-4be1-864d-999007c21132)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/b3dc39e2-d836-4196-882f-2e8be233eeba)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/8dbed0a1-4d1a-452f-8f83-6d11b5e02599)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/8a652f0d-acb3-41ad-a619-47872b80fa88)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/ea57b6ff-c763-4be7-bd6c-62c50af06f9e)
![image](https://github.com/Naveenaa28/ODD2023-Datascience-Ex-05/assets/131433133/2fd56f1e-e3ab-4bab-97fa-8d0f1ea462fb)
## RESULT:
The Feature Generation process was performed and saved the data to a file.


