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

import pandas as pd
import numpy as np
import seaborn as sns
df=pd.read_csv("/content/titanic_dataset.csv")
df 

<img width="1570" height="573" alt="image" src="https://github.com/user-attachments/assets/93ca5f54-5edc-4d2b-8e41-2bc8a4826257" />

df.info()

<img width="453" height="468" alt="image" src="https://github.com/user-attachments/assets/1f78ee48-7615-4a18-8f21-9b38e92009d1" />

df.describe()

<img width="940" height="405" alt="image" src="https://github.com/user-attachments/assets/45c67131-7983-46f4-ad63-13bb6b0b6520" />

df.dtypes

<img width="228" height="619" alt="image" src="https://github.com/user-attachments/assets/e297d895-8c33-484e-80e1-2d6fe871d281" />

df.shape

<img width="117" height="43" alt="image" src="https://github.com/user-attachments/assets/ab21b65a-8a90-4b8c-8b6d-e14342c09cd6" />

df.value_counts()

<img width="1643" height="670" alt="image" src="https://github.com/user-attachments/assets/fa8807df-74b5-424a-aea2-ddcd5caff234" />

df['Age'].value_counts()

<img width="195" height="665" alt="image" src="https://github.com/user-attachments/assets/9fed2218-6a03-4c23-9c55-e10dd7349a41" />

df.set_index("PassengerId",inplace=True)

<img width="1342" height="336" alt="image" src="https://github.com/user-attachments/assets/9a4dd2cb-7be7-47f9-b69e-512a0eeba774" />

df

<img width="1623" height="615" alt="image" src="https://github.com/user-attachments/assets/37e01c8e-5702-4175-b10b-8177cb064765" />

df.nunique()

<img width="231" height="576" alt="image" src="https://github.com/user-attachments/assets/faf1df48-9829-4fef-8a7e-7c9cd9b87772" />

sns.countplot(data=df,x='Age')

<img width="795" height="646" alt="image" src="https://github.com/user-attachments/assets/7a869f77-10ee-4ca9-9063-bdacede7271b" />

df.rename(columns={'Sex':'Gender'},inplace=True)
df

<img width="1630" height="611" alt="image" src="https://github.com/user-attachments/assets/747e6b8a-ecd9-49b4-a3f0-222bc9988196" />

sns.catplot(x='Gender',col='Survived',kind='count',data=df,height=5,aspect=.7)

<img width="945" height="696" alt="image" src="https://github.com/user-attachments/assets/237a7833-5176-4b5f-b29b-80154a20467a" />

df.boxplot(column='Age',by='Survived')

<img width="778" height="668" alt="image" src="https://github.com/user-attachments/assets/7f432fdf-fc48-4f6e-8511-87241647c34c" />

sns.scatterplot(x=df['Age'],y=df['Fare'])

<img width="793" height="625" alt="image" src="https://github.com/user-attachments/assets/d5f89349-1a55-48fe-95c4-d09eacf733d5" />

plt=sns.boxplot(x='Passenger Class',y='Age',hue='Gender',data=df)

<img width="785" height="620" alt="image" src="https://github.com/user-attachments/assets/43660804-c02b-42b8-8e6a-eb46da16ecca" />

sns.catplot(x='Passenger Class',y='Age',hue='Gender',col='Survived',data=df,kind='box')

<img width="1538" height="705" alt="image" src="https://github.com/user-attachments/assets/ac9fb0c5-1818-4408-9c45-299d2b1c18cf" />

corr=df.corr(numeric_only=True)

sns.heatmap(corr,annot=True,cmap='coolwarm')

<img width="962" height="741" alt="image" src="https://github.com/user-attachments/assets/515e9e8d-c251-478c-84a7-d14750aadf58" />


# RESULT
Exploratory Data Analysis is performed and verified on the given data set.        
