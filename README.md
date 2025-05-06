# SKILL-ASSSESMENT-1
# AIM:
  To perform a comprehensive data science assessment using Python, applying key concepts such as data cleaning, analysis,
  and basic machine learning techniques.

# EXPLANATION:
Data Science involves extracting meaningful insights from structured or unstructured data using scientific methods, algorithms, and tools. Python, being a versatile programming language, provides libraries like Pandas, NumPy and  Scikit-learn that enable data manipulation, visualization, and modeling. This assessment ensures practical understanding and command over essential data science operations.

# ALGORITHM:
STEP 1: Import necessary libraries: pandas, numpy.

STEP 2: Create a dataframe with the help of pandas.

STEP 3: Perform basic data cleaning:

  - Handle missing values using .isnull(), .dropna(), or .fillna().

  - Remove duplicates using .duplicated().

  - Convert data types if necessary using .astype().

STEP 4: Perform data manipulation using pandas and numpy:

  - Filter rows or columns.

  - Apply aggregation functions (like .mean(), .sum(), etc.).

STEP 5: Display or save the results as required.

#  CODING AND OUTPUT:
```
NAME :  THILAK RAJ . P
REGISTER NUMBER : 212224040353
```
```
# creating a dataFrame
df = pd.DataFrame(
    [[1,2,3],
     [4,5,6],
     [7,8,9]],
    index=[1,2,3],
    columns = ['a','b','c']
)
print(df)
```
![image](https://github.com/user-attachments/assets/e73de0bd-ab74-4dad-b6f4-28f53c0e91bc)
```
# creating dataframe from dictionary
import pandas as pd
mydataset = {
  'cars': ["BMW", "Volvo", "Ford"],
  'passings': [3, 7, 2]
}
myvar = pd.DataFrame(mydataset)
print(myvar)
```
![image](https://github.com/user-attachments/assets/036aab73-b0ab-4ca0-8842-68af6e264f1c)

```
# Column addition
data = {'Name': ['izana', 'mikey', 'draken', 'takemichi'],  'Height': [5.1, 6.2, 5.1, 5.2], 'Qualification': ['fighter', 'fighter', 'fighter', 'fighter']} 
df = pd.DataFrame(data) 
address = ['tokyo', 'berlin', 'denver', 'newjersey'] 
df['Address'] = address 
print(df) 
```
![image](https://github.com/user-attachments/assets/42cfab1f-cd3f-4819-8ad3-54072c0d3900)

```
import pandas as pd

data = {
    'Name': ['izana', 'mikey', 'draken', 'takemichi'],
    'Age': [27, 24, 22, 32],
    'Address': ['tokyo', 'berlin', 'denver', 'newjersey'],
    'Qualification': ['fighter', 'fighter', 'fighter', 'fighter']
}

df = pd.DataFrame(data)

del df['Address']

print(df)
```
![image](https://github.com/user-attachments/assets/f1359c21-430f-4a4f-bf75-3fe66ed73a5e)

```
# column renaming
import pandas as pd

data = {
    'Name': ['izana', 'mikey', 'draken', 'takemichi'],
    'Age': [27, 24, 22, 32],
    'Address': ['tokyo', 'berlin', 'denver', 'newjersey'],
    'Qualification': ['fighter', 'fighter', 'fighter', 'fighter']
}

df = pd.DataFrame(data)
print(df)


df.rename(columns={'Address': 'place'}, inplace=True)

print(df)
```
![image](https://github.com/user-attachments/assets/ccf89f76-d589-4003-8270-8a3b3b22b5a5)

```
import pandas as pd

data = {
    'Name': ['izana', 'mikey', 'draken', 'takemichi'],
    'Age': [27, 24, 22, 32],
    'Address': ['tokyo', 'berlin', 'denver', 'newjersey'],
    'Qualification': ['fighter', 'fighter', 'fighter', 'fighter']
}

df = pd.DataFrame(data)
print(df)


df.columns = ['A', 'B', 'C', 'D']
print(df)
```
![image](https://github.com/user-attachments/assets/f9fac1f8-9e31-4e3b-9c3c-5a21ec0f4c1c)

```
# Indexing and Selecting data
import pandas as pd
data = {'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
        'age': [25, 32, 18, 47],
        'gender': ['F', 'M', 'M', 'M'],
        'height': [1.62, 1.78, 1.65, 1.83]}
df = pd.DataFrame(data)
df = df['name']
df
```
![image](https://github.com/user-attachments/assets/5340f4de-6da5-4eab-b111-f479d96507aa)

```
# Multiple column selection
import pandas as pd

data = {
    'Name': ['Jai', 'Princi', 'Gaurav', 'Anuj'],
    'Age': [27, 24, 22, 32],
    'Address': ['Delhi', 'Kanpur', 'Allahabad', 'Kannauj'],
    'Qualification': ['Msc', 'MA', 'MCA', 'Phd']
}

df = pd.DataFrame(data)

print(df[['Name', 'Qualification']])
```
![image](https://github.com/user-attachments/assets/ada0bccb-5aa9-42ae-b1c8-1de4798040f7)

```
# Finding nlargest
data = {'name': ['Alice', 'Bob', 'Charlie', 'David', 'Emily'],
        'age': [25, 30, 35, 40, 45],
        'salary': [50000, 60000, 70000, 80000, 90000]}
df = pd.DataFrame(data)

top_salaries = df.nlargest(2, columns='salary')
print(top_salaries)
```
![image](https://github.com/user-attachments/assets/16912583-b103-4079-b27b-1d5ddb2bfcc2)

```
# Handling missing values using Dropna
import pandas as pd

data = {
    'Name': ['izana', 'mikey', 'draken', 'takemichi', 'kakucho'],
    'Age': [25, 32, None, 41, 28],
    'Salary': [50000, None, 70000, 90000, 60000]
}

df = pd.DataFrame(data)
df.dropna(inplace=True)
print(df)
```
![image](https://github.com/user-attachments/assets/686878f0-a3f5-47bf-bf13-25e4c458ed98)
```
# Filling missing values
import pandas as pd
import numpy as np

data = {
    'Name': ['izana', 'mikey', 'draken', 'takemichi', 'kakucho'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}

df = pd.DataFrame(data)

df_filled = df.fillna(0)

print(df_filled)
```
![image](https://github.com/user-attachments/assets/7d67c8aa-00c3-43cc-b001-773d94fbd271)

```
# Sorting the dataframe with actual value
import pandas as pd
df = pd.DataFrame({'col1':[1,2,3,4],'col2':[444,555,666,444],
			'col3':['abc','def','ghi','xyz']})
df.sort_values(by='col2')
print(df)
```
![image](https://github.com/user-attachments/assets/92e4e605-c95e-420b-a979-b5450509c035)

```
#Sorting the dataframe with label
df = pd.DataFrame(np.random.randn(10,2),
		index=[1,4,6,2,3,5,9,8,0,7],columns = ['col2','col1'])
df
df1=df.sort_index(ascending=True)
print("Dataframe 1")
print(df1)
print("Dataframe 2")
df2=df.sort_index()
df2
```
![image](https://github.com/user-attachments/assets/935ebee2-ce25-4641-bc2f-7b16e4aaa842)

```
# Groupby commands
import pandas as pd
data = {'Company':['GOOG','GOOG','MSFT','MSFT','FB','FB'],
       'Person':['Sam','Charlie','Amy','Vanessa','Carl','Sarah'],
       'Sales':[200,120,340,124,243,350]}
df = pd.DataFrame(data)
df
```
![image](https://github.com/user-attachments/assets/2bdd983a-7415-4fa5-b1a7-31290366de3f)

```
print(df.groupby('Company')['Sales'].mean()) 
```
![image](https://github.com/user-attachments/assets/5e90c36a-60ff-4832-951a-ffc351be0b54)

```
print(df.groupby('Company')['Sales'].min()) 
```
![image](https://github.com/user-attachments/assets/4d1da329-5437-4994-854f-3a764b815003)

```
df = pd.DataFrame({'col1':[1,2,3,4],'col2':[444,555,666,444],'col3':['abc','def','ghi','xyz']})
df.head()
```
![image](https://github.com/user-attachments/assets/cb9e8e14-32b1-4ced-b084-111dc2882380)

```
df.describe()
```
![image](https://github.com/user-attachments/assets/367ea369-2e43-411e-8ba3-a1c419b13db0)

```
# Checking for missing values
df = pd.DataFrame({'A':[1,2,np.nan],
                  'B':[5,np.nan,np.nan],
                  'C':[1,2,3]})
df
```
![image](https://github.com/user-attachments/assets/62cc527e-6a0a-409b-8614-af2edfababbb)

```
df.isnull()
```
![image](https://github.com/user-attachments/assets/de1c9f67-1ae0-4af7-8a65-dad31b6b7a48)

```
df.notnull()
```
![image](https://github.com/user-attachments/assets/6e1e1330-0bca-4585-ae83-aba88176b2aa)

```
df.dropna()
```
![image](https://github.com/user-attachments/assets/3decc9c5-97a6-4f03-b722-1d9b7534cd0f)

```
df.dropna(axis=1)
```
![image](https://github.com/user-attachments/assets/54d4bb45-e930-46ef-9119-85d628cb2628)

```
#Replace NaN with a Scalar Value
df.fillna(value=10)
df['A'].fillna(value=df['A'].mean())
df
```
![image](https://github.com/user-attachments/assets/ed509e04-6524-4548-81db-48e34ef9e3d3)

```
df.fillna(method='ffill')
```
![image](https://github.com/user-attachments/assets/0c9030f3-acbe-4c39-8b6f-ee2a4c35318f)
```
# Forward and backward filling
df = pd.DataFrame({'A':[1,np.nan,2],
                  'B':[5,np.nan,3],
                  'C':[1,2,3]})
df
```
![image](https://github.com/user-attachments/assets/5f006c89-1d3a-4f1e-aed2-4f7eac5747f7)

```
# using backward filling
df.fillna(method='ffill')
```
![image](https://github.com/user-attachments/assets/4ed5b086-27d4-4c9f-9609-08e4d5df9e31)

```
# using forward filling
df.fillna(method='bfill')
```
![image](https://github.com/user-attachments/assets/fd468a1b-7261-49f6-ab36-0f0fda8b158c)

```
# DataFrame Commands
data = {
    'Name': ['John', 'Sarah', 'Mike', 'Emily', 'David'],
    'Age': [25, 31, 29, 35, 27],
    'Gender': ['M', 'F', 'M', 'F', 'M'],
    'Salary': [50000, 70000, 60000, 80000, 55000]
}
df = pd.DataFrame(data)
print("Head Values")
print(df.head(3))
print("Tail Values")
print(df.tail(3))
```
![image](https://github.com/user-attachments/assets/cb93c82f-804f-455a-a43c-efc51cfb956d)

```
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'Dave', 'Eve'],
    'Age': [25, np.nan, 35, 41, np.nan],
    'Salary': [50000, np.nan, 70000, np.nan, 60000]
}

df = pd.DataFrame(data)

# This will check for non-duplicated values
~df.duplicated()
```
![image](https://github.com/user-attachments/assets/a7a3eff5-3dc7-40ae-8d16-0e42155433b1)

```
# filtering in a dataframe
data = {
    'name': ['Alice', 'Bob', 'Charlie', 'Dave'],
    'age': [25, 32, 18, 47],
    'gender': ['F', 'M', 'M', 'M'],
    'height': [1.62, 1.78, 1.65, 1.83]
}

df = pd.DataFrame(data)

df_filtered = df[(df['gender'] == 'M') & (df['height'] > 1.7)]


print(df_filtered)
```
![image](https://github.com/user-attachments/assets/b45a97d0-445a-495e-a56a-08943e23c6ca)

# Result:
 Basic operations on the dataset were successfully performed using pandas and NumPy. The data was cleaned by handling missing values and removing duplicates.
