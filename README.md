# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
# data.csv
```
import pandas as pd   
import seaborn as sbn 
df=pd.read_csv("/content/data.csv") 
df.info() 
df.isnull().sum()
from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() 
df['Ord_2'] = le.fit_transform(df['Ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Ord_2'])
from sklearn.preprocessing import OneHotEncoder 
enc = OneHotEncoder() 
enc = enc.fit_transform(df[['City']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
df = pd.concat([df, encoded_colm], axis=1) 
df = df.drop(['City'], axis=1) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_2'], columns=['Ord_2']) 
df.head(10) 
df = pd.get_dummies(df, prefix=['Ord_1'], columns=['Ord_1']) 
df.head(10)
```
# encoding.csv
```
import pandas as pd 
import seaborn as sbn 
data=pd.read_csv("/content/Encoding Data.csv") 
data.info() 
data.isnull().sum() from sklearn.preprocessing import LabelEncoder 
le = LabelEncoder() data['ord_2'] = le.fit_transform(data['ord_2']) 
sbn.set(style ="darkgrid") 
sbn.countplot(data['ord_2']) from sklearn.preprocessing import OneHotEncoder 
en = OneHotEncoder() 
en = en.fit_transform(data[['nom_0']]).toarray() 
encoded_colm = pd.DataFrame(en) 
data= pd.concat([data, encoded_colm], axis=1) 
data= data.drop(['nom_0'], axis=1) 
data.head(10) 
data = pd.get_dummies(df, prefix=['bin_2'], columns=['bin_2']) 
data.head(10)
```
# titanic.csv
```
import pandas as pd 
import seaborn as sbn 
dt=pd.read_csv("/content/titanic_dataset.csv") 
dt.info() 
dt.isnull().sum() 
dt['Age']=dt['Age'] . fillna(dt ['Age'].mean()) 
dt ['Cabin']=dt['Cabin']. fillna(dt['Cabin']. mode() [0]) 
dt ['Embarked']=dt['Embarked'] . fillna(df ['Embarked'].mode( )[0]) 
dt.isnull().sum( ) from sklearn.preprocessing import LabelEncoder 
lc = LabelEncoder() 
df['Sex'] = lc.fit_transform(df['Sex']) 
sbn.set(style ="darkgrid") 
sbn.countplot(df['Sex']) from sklearn.preprocessing import OneHotEncoder 
enc= OneHotEncoder() 
enc= enc.fit_transform(dt[['Name']]).toarray() 
encoded_colm = pd.DataFrame(enc) 
dt= pd.concat([dt, encoded_colm], axis=1) 
dt= dt.drop(['Name'], axis=1) 
dt.head(10) 
dt = pd.get_dummies(dt, prefix=['Ticket'] ,columns=['Ticket']) 
df.head(10) 
dt = pd.get_dummies(dt, prefix=['Embarked'] ,columns=['Embarked']) 
df.head(10)
```
# OUPUT
# Data.csv
![image](https://user-images.githubusercontent.com/128348968/232307982-dc8388db-b07d-4397-8613-0ea965368fb1.png)

![image](https://user-images.githubusercontent.com/128348968/232308008-6b01a632-cdbb-49c7-bbbe-6ac83a3b6d54.png)

![image](https://user-images.githubusercontent.com/128348968/232308017-712bc7aa-0a31-4bbb-89c9-2d9416b897a3.png)

![image](https://user-images.githubusercontent.com/128348968/232308032-3e13fac7-501e-48dd-9f1d-599eb2e58670.png)

![image](https://user-images.githubusercontent.com/128348968/232308051-1a290032-2647-4fa8-a436-840582b346a5.png)
# Encoding.csv
![image](https://user-images.githubusercontent.com/128348968/232308136-515e58fd-b33d-4537-a3f1-524f42f9b27c.png)

![image](https://user-images.githubusercontent.com/128348968/232308145-a3f233f4-7a13-452a-9193-3d682dfee570.png)

![image](https://user-images.githubusercontent.com/128348968/232308150-bf2121c5-dd6f-4066-89c1-1c74b601da4a.png)

![image](https://user-images.githubusercontent.com/128348968/232308155-79e2da01-0615-410c-873d-9d37b11bd73c.png)
# Titanic.csv
![image](https://user-images.githubusercontent.com/128348968/232308196-74841eff-9ea0-48aa-9a86-403e3c29afc5.png)

![image](https://user-images.githubusercontent.com/128348968/232308205-3ba98bd2-ed76-4d5a-ac3a-21234b3a3aac.png)

![image](https://user-images.githubusercontent.com/128348968/232308219-bee02838-706c-460a-b288-cf77ee33693f.png)

![image](https://user-images.githubusercontent.com/128348968/232308233-d11cbfdf-5b5f-4951-94f2-1e9de4d5e5f5.png)

![image](https://user-images.githubusercontent.com/128348968/232308252-b55e19e5-c482-4cb4-a940-09e1abb7d05c.png)

![image](https://user-images.githubusercontent.com/128348968/232308272-b30bf1c4-d9ca-4edc-9aa5-4c41f2969849.png)
# RESULT:
Thus the program for Feature Generation is executed successfully.

