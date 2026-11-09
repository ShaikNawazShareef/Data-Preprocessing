# Data Preprocessing – Bengaluru House Data

## 📌 Project Overview

This project demonstrates basic data preprocessing techniques using Python, Pandas, and NumPy. The Bengaluru House Data dataset is used to understand how to identify, handle, replace, and remove missing values in a dataset.

Data preprocessing is an important step in Machine Learning because it improves data quality and prepares raw data for further analysis.

## 🎯 Objectives

- Upload and read CSV files using Google Colab.
- Load datasets using Pandas.
- Explore datasets using `head()` and `shape`.
- Identify missing (NULL) values.
- Count missing values in individual columns and the entire dataset.
- Replace missing values with zero.
- Fill missing values using forward fill and backward fill.
- Replace missing values with custom values.
- Fill missing values using the mean.
- Remove rows containing missing values.

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Google Colab
- Bengaluru House Data (CSV)

## 📚 Practical 5 – Handling Missing Values

### 1. Import Libraries

```python
import pandas as pd
import numpy as np
from google.colab import files
```

### 2. Upload CSV File

```python
file = files.upload()
df1 = pd.read_csv('/content/Bengaluru_House_Data.csv')
```

### 3. Explore the Dataset

```python
df1.head()
df1.shape
```

- `head()` – Displays the first five rows.
- `shape` – Displays the number of rows and columns.

### 4. Identify Missing Values

```python
df1.isnull()
df1.isnull().sum()
df1.isnull().sum().sum()
```

- `isnull()` – Identifies missing values.
- `isnull().sum()` – Counts missing values in each column.
- `isnull().sum().sum()` – Counts total missing values.

### 5. Fill Missing Values with Zero

```python
df2 = df1.fillna(value=0)
```

### 6. Forward Fill (Pad)

```python
df3 = df1.fillna(method='pad')
```

Fills missing values using the previous available value.

### 7. Backward Fill

```python
df4 = df1.fillna(method='bfill')
```

Fills missing values using the next available value.

### 8. Fill Missing Values Row-wise

```python
df5 = df1.fillna(method='pad', axis=1)
df6 = df1.fillna(method='bfill', axis=1)
```

- `axis=1` – Performs filling across columns.

### 9. Fill Missing Values with Custom Values

```python
df7 = df1.fillna({
    'society': 'abcd',
    'balcony': 'defg'
})
```

Replaces missing values in specified columns with custom values.

### 10. Fill Missing Values with Mean

```python
df8 = df1.fillna(value=df1['balcony'].mean())
```

Replaces missing values using the mean of the balcony column.

### 11. Remove Missing Values

```python
df1.dropna()
df8.dropna()
```

Removes rows containing missing values.

## 📂 Dataset

**Dataset Name:** Bengaluru House Data

The dataset contains information about residential properties in Bengaluru, including:

- Area type
- Availability
- Location
- Size
- Society
- Total square feet
- Bathrooms
- Balconies
- Price

## 📖 Key Learning Outcomes

- Understanding missing values in datasets.
- Learning different methods to handle NULL values.
- Applying Pandas functions for data cleaning.
- Understanding forward fill and backward fill.
- Using mean values for missing data.
- Preparing datasets for Machine Learning.

## 🚀 Conclusion

This practical demonstrates different techniques for handling missing values using Pandas. These techniques help clean and prepare the Bengaluru House Data dataset for further data analysis and Machine Learning applications.

## 👨‍💻 Author

**Nawaz Shareef Shaik**

GitHub: https://github.com/ShaikNawazShareef
