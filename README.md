# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
```
import pandas as pd
df=pd.read_csv("sampleids.csv")
print(df)
```
<img width="967" height="790" alt="image" src="https://github.com/user-attachments/assets/b7c500ed-b364-4ee9-977c-be80385ce650" />


```
df.dropna(axis=1)
```

<img width="233" height="678" alt="image" src="https://github.com/user-attachments/assets/472a60b2-7820-41ef-8f2c-a2c472a826ad" />

```
dfs = df[df['TOTAL']>270]
dfs
```

<img width="744" height="306" alt="image" src="https://github.com/user-attachments/assets/ad74a1da-9bb4-4a22-b360-ee57a94666ab" />

```
dfs=df[df['NAME'].str.startswith(('A','c'))& (df['TOTAL']>250)]
dfs
```

<img width="582" height="47" alt="image" src="https://github.com/user-attachments/assets/6fbc1f3c-8944-4064-9fd1-c4cd0fa3775c" />

```
df.iloc[:4]
```

<img width="730" height="163" alt="image" src="https://github.com/user-attachments/assets/98b3dbf9-1caa-4d5b-a5fb-50ccbe84778a" />

```
df.iloc[0:4,1:4]
```

<img width="232" height="150" alt="image" src="https://github.com/user-attachments/assets/c5a99667-fdc3-4d09-8fb4-45d21799f0df" />

```
df.iloc[[1,3,5],[1,3]]
```

<img width="172" height="130" alt="image" src="https://github.com/user-attachments/assets/b0118005-21b7-4128-8084-2b9a744a10d5" />

```
df
```

<img width="755" height="670" alt="image" src="https://github.com/user-attachments/assets/47d41275-66d7-4cbb-bde3-30405fb239d3" />

```
dff = df.fillna(0)
dff
```

<img width="751" height="671" alt="image" src="https://github.com/user-attachments/assets/127d9c07-6b19-4fc5-b08f-9f670dad2b6a" />

```
df['TOTAL'].fillna(value=df['TOTAL'].mean())
```

<img width="230" height="385" alt="image" src="https://github.com/user-attachments/assets/6f617062-4630-4fe6-8f8e-22cae01f5d36" />

```
df.fillna(method='ffill')
```

<img width="741" height="665" alt="image" src="https://github.com/user-attachments/assets/47af38f8-273c-4d38-9d30-cb9f9e83ff42" />

```
df.fillna(method='bfill')
```

<img width="744" height="651" alt="image" src="https://github.com/user-attachments/assets/623743bd-46f3-4e90-92ff-18dbbcf866c5" />

```
df['TOTAL'].fillna(value=df['TOTAL'].mean(),inplace=True
df
```

<img width="748" height="675" alt="image" src="https://github.com/user-attachments/assets/1d8cd89f-2d24-444b-af77-fcc5beecea78" />







# Result
          <<include your Result here>>
