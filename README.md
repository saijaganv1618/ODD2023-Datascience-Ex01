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

# CODE
### LOAN_DATA.CSV
````
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
df.info()
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()

df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()

df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()

df.info()
df.isnull().sum()
````
### DATA_SET.CSV
````
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
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

df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()

df.info()
df.isnull()
df.isnull().sum()
````
# OUTPUT
### FOR LOAN_DATA:
### DATA
````
import pandas as pd
df=pd.read_csv("Loan_data.csv")
print(df)
df.head(10)
````
![1](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/e56346b9-5358-4755-9fa9-0731384d7875)
### NON NULL BEFORE
````
df.info()
````
![2](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/bcdd59da-892b-4b61-aea5-90c31b7fdff5)
### MODE
````
df['Loan_ID']=df['Loan_ID'].fillna(df['Dependents'].mode()[0])
df['Dependents']=df['Dependents'].fillna(df['Dependents'].mode()[0])
df['Education']=df['Education'].fillna(df['Dependents'].mode()[0])
df['Self_Employed']=df['Self_Employed'].fillna(df['Self_Employed'].mode()[0])
df['Gender']=df['Gender'].fillna(df['Gender'].mode()[0])
df.head()
````
![3](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/219a6d74-2cf9-4385-9a10-e2612b3bc28f)
### MEAN
````
df['ApplicantIncome']=df['ApplicantIncome'].fillna(df['ApplicantIncome'].mean())
df['Loan_Amount_Term']=df['Loan_Amount_Term'].fillna(df['Loan_Amount_Term'].mean())
df['LoanAmount']=df['LoanAmount'].fillna(df['LoanAmount'].mean())
df.head()
````
![4](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/326bd78c-ea1c-4502-a090-0c858b90392c)
### MEDIAN
````
df['Credit_History']=df['Credit_History'].fillna(df['Credit_History'].median())
df.head()
````
![5](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/ff17ebcb-2b94-4fc1-a3cd-e6de2825a5e4)
### NON NULL AFTER
````
df.info()
````
![6](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/8b3d8ad9-670e-4765-b931-fd8f17896b07)
````
df.isnull().sum()
````
![7](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/bd92664f-5dda-4fb8-a785-24bfe8f23830)
### FOR DATA_SET:
### DATA
````
import pandas as pd
df=pd.read_csv("Data_set.csv")
print(df)
df.head(10)
````
![8](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/f088086c-bab3-4a3b-a14a-407209394c15)
### NON NULL BEFORE
````
df.info()
````
![9](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/19b2df64-70aa-4b25-a0c4-e01864623991)
````
df.isnull()
````
![10](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/0ce02807-0898-4881-96e9-c0a05b4c3275)
````
df.isnull().sum()
````
![11](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/f82ae558-0de5-4473-9f26-f57036bef55c)
### MODE
````
df['show_name']=df['show_name'].fillna(df['aired_on'].mode()[0])
df['aired_on']=df['aired_on'].fillna(df['aired_on'].mode()[0])
df['original_network']=df['original_network'].fillna(df['aired_on'].mode()[0])
df.head()
````
![12](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/6a6b6c93-f4a9-4839-89a2-8c4e04f03772)
### MEAN
````
df['rating']=df['rating'].fillna(df['rating'].mean())
df['current_overall_rank']=df['current_overall_rank'].fillna(df['current_overall_rank'].mean())
df.head()
````
![13](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/d45490eb-f685-4b1d-8fbc-f2d9d32188ae)
### MEDIAN
````
df['watchers']=df['watchers'].fillna(df['watchers'].median())
df.head()
````
![14](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/ec53fe34-539b-4abf-8a49-3a0770f1b8b6)
### NON NULL AFTER
````
df.info()
````
![15](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/f38ef5d5-af1b-4c19-bd5d-14ee0427ac08)
````
df.isnull()
````
![16](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/4634d6c5-51ab-4972-a742-4b158c40d670)
````
df.isnull().sum()
````
![17](https://github.com/Aakash0407/ODD2023-Datascience-Ex01/assets/118799103/4611191e-159e-4a17-9170-8bdc523d8c93)

# RESULT
Thus,the given data is read,cleansed and the cleaned data is saved into the file.




