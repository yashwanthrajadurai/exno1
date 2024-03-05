# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanationa
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## Data cleaning
<table>
  <tr>
    <td width=50%>

### 1) Read and display DataFrame
```Python
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 160011](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/374817ca-588d-4ce9-ad1b-8898275ff330)


</td>
</tr>
<tr>
  <td width=50%>
              
### 2) Display head
```Python
df.head(4)
```
  </td>
  <td>

              
#### OUTPUT:

![Screenshot 2024-02-27 160858](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/7ff8dc08-e462-47de-90f6-3f15d23a7bc4)

</td>
</tr>
<tr>
  <td width=50%>

### 3) Display tail
```Python
df.tail(4)
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 160909](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/cc5835ee-8e45-4d9b-8186-a0a9555e5ee2)

</td>
</tr>
<tr>
  <td width=50%>

### 4) Info of datafram
```Python
df.info(3)
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 161613](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/bd98f185-b0f7-4aa0-aad5-34cf0de4f7ce)


</td>
</tr>
<tr>
  <td width=50%>

### 5) Describe about the dataframe
```Python
df.describe()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 161734](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/1244543f-1efa-4de8-a814-193dac11da80)


</td>
</tr>
<tr>
  <td width=50%>

### 6) Shape of the datafram
```Python
df.shape
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 161817](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/3c12a861-c592-45d8-84e6-ef6711d22f74)

</td>
</tr>
<tr>
  <td width=50%>

### 7) Checking tha NUll values
```Python
df.isnull().sum()
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 161904](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/89d06b3b-8d22-4de3-ac75-34294024389e)

</td>
</tr>
<tr>
  <td width=50%>

### 8) Drop the Null values
```Python
df.nunique()

```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 162113](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/836eb8b4-c9d7-447a-ab98-f541110f727d)

</td>
</tr>
<tr>
  <td width=50%>

### 9) Finding the mean value
```Python
mn=df.TOTAL.mean()
mn
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 171508](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/c4e865f3-9c77-4f1a-b03d-66e29cc36ba2)


</td>
</tr>
<tr>
  <td width=50%>

### 10) Fill Null value with Mean value
```Python
df.TOTAL.fillna(mn,inplace=True)
df
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 171720](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/7616aa46-2fdf-45bf-a321-39b8e6e2b441)


</td>
</tr>
<tr>
  <td width=50%>
    
### 11) Finding minimum value
```Python
mn=df.M4.min()
mn
```
  </td>
  <td>
              
#### OUTPUT:


![Screenshot 2024-02-27 171831](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/7a7bf6ee-daa7-480a-ae1b-d67bebd22e2b)



</td>
</tr>
<tr>
  <td width=50%>

### 12) Printing only Date of Birth
```Python
df['cd']=pd.to_datetime(df['DOB'])
df['cd']
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-02-27 172720](https://github.com/BALUREDDYVELAYUDHAMGOWTHAM/exno1/assets/119559905/2da7285f-ead4-4a60-8bad-f430c407ee64)



</td>
</tr>
<tr>
  <td width=50%>

# Result:
  Thus the program for data cleaning using python has executed successfully.
