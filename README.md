# Ex-01_DS_Data_Cleansing


## AIM
To read the given data and perform data cleaning and save the cleaned data to a file. 

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. 
Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information. 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Get the information about the data
### STEP 3
Remove the null values from the data
### STEP 4
Save the Clean data to the file

# CODE and OUTPUT
# For Data_set:
```
import pandas as pd
df=pd.read_csv("/content/Data_set(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()

df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()

df.head()

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()

df.isnull().sum()
```

# For Loan_data:
```
import pandas as pd
df=pd.read_csv("/content/Loan_Data(1).csv")
print(df)

df.head(5)

df.info()

df.isnull()

df.isnull().sum()

df['Loan_ID']=df['Loan_ID'].fillna(df['Education'].mode()[0])
df['Education']=df['Education'].fillna(df['Education'].mode()[0])
df['Married']=df['Married'].fillna(df['Education'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df.head()

df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].median())
df.head()

df.info()

df.isnull().sum()
```
# OUTPUT:
# For Data_set:
# Data
![Screenshot 2023-08-19 091403](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/86d1385c-b990-4354-acf8-b32b01bdf413)

![Screenshot 2023-08-19 091548](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/bcdaf428-9ab9-4b6c-84a0-f6dd0a4a68e2)

# Non null before
![Screenshot 2023-08-19 091728](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/f036454d-c4a3-4a74-9fbb-0638bb85ba2c)

![Screenshot 2023-08-19 091910](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/c958dc85-e26d-4619-b2d5-4752c0f5d1fa)

![Screenshot 2023-08-19 092046](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/b0d6bb9f-889e-410e-8db4-415b70c8d817)

# Mode
![Screenshot 2023-08-19 092217](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/8011a3d8-8949-44b9-b8e3-08280f972c10)

# Mean
![Screenshot 2023-08-19 092404](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/f2b2bd09-2965-4e39-908f-dbdad8686cd6)

# Median
![Screenshot 2023-08-19 092539](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/95b2764e-47d1-4fca-a834-b7e84a9318fd)

# Non null After
![Screenshot 2023-08-19 092743](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/897c0881-dcef-4adc-aa4a-6d23e9ddd23e)
![Screenshot 2023-08-19 092839](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/0917b064-2deb-4379-94cb-2f652ac3d36f)

# For Loan_data:
# Data
![Screenshot 2023-08-19 093053](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/159c5662-8c29-4489-af33-84097e77728f)
![Screenshot 2023-08-19 093157](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/29d78e75-f82b-4d53-a13f-25f46006ef9a)

# Non null before
![Screenshot 2023-08-19 093328](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/271f8009-d991-4772-acab-4c2779c83aeb)
![Screenshot 2023-08-19 093436](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/8b72df7a-4d41-4f19-85e0-8c825a9b24ad)
![Screenshot 2023-08-19 093541](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/0e06cf25-c217-4f40-945e-f27acd8300ad)

# Mode
![Screenshot 2023-08-19 093711](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/498724b6-f053-4e37-8811-8daef7d09e5a)

# Mean
![Screenshot 2023-08-19 093819](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/d48bd72a-3794-4c38-814a-24bd48ee0136)

# Median
![Screenshot 2023-08-19 094107](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/44760d52-dfcd-4f21-875d-a0f932645727)

# Non null After
![Screenshot 2023-08-19 094229](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/b85eb546-7a9c-4e71-8108-3fcbacea46cb)

![Screenshot 2023-08-19 094321](https://github.com/vasundrasriravi/ODD2023-Datascience-Ex01/assets/119393983/cf053ce4-e045-4318-b0c9-a549be83fffb)

# Result:
Thus the given data is read,cleansed and the cleaned data is saved into the file.
