EXPERIMENT: DATA NORMALISATION AND DATA TYPE CONVERSION

AIM
To implement data normalisation techniques (Min-Max, Z-score, Decimal Scaling) and data type conversion using encoding methods (Label Encoding, One-Hot Encoding, Dummy Encoding) in Python using Pandas and Scikit-learn.

THEORY 
1. Creating Dataset using Pandas
A dataset of products is created using:
pd.DataFrame(data)
It contains:
Product names
Price
Units Sold
Discount
This step is used to store structured data in tabular form for further processing.

2. Min-Max Normalisation
a) Price Normalisation
df['Price_MinMax'] = (df['Price'] - df['Price'].min()) / (df['Price'].max() - df['Price'].min())
Converts price into range 0 to 1
Example:
Max price → 1
Min price → 0

b) Discount Normalisation
df['Discount_MinMax'] = (df['Discount'] - df['Discount'].min()) / (df['Discount'].max() - df['Discount'].min())
  Same formula applied to another column → shows column-wise normalization

c) Multiple Column Normalisation
cols = ['Price','Units_Sold','Discount']
df_norm = (df[cols] - df[cols].min()) / (df[cols].max() - df[cols].min())
  This step normalizes multiple columns at once using vectorized operations.

3. Z-Score Normalisation

a) Price Z-score
df['Price_Zscore'] = (df['Price'] - df['Price'].mean()) / df['Price'].std()
Centers data around mean
Uses standard deviation

b) Units Sold Z-score
df['Units_Zscore'] = (df['Units_Sold'] - df['Units_Sold'].mean()) / df['Units_Sold'].std()

c) Discount Z-score
df['Discount_Zscore'] = (df['Discount'] - df['Discount'].mean()) / df['Discount'].std()

d) Multiple Column Z-score
df_zscore = (df[cols] - df[cols].mean()) / df[cols].std()
  This step applies standardization on multiple features simultaneously

4. Decimal Scaling
df['Price_Decimal'] = df['Price'] / 100000
Reduces magnitude by shifting decimal
Example: 55000 → 0.55
  Used for simple scaling without complex calculations

5. Second Dataset Creation
A new dataset is created with:
Order ID
Gender
Payment Method
Product Category
City
Order Value
   This dataset is used for categorical data conversion (encoding)
6. Label Encoding
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
df['Customer_Gender_Encoded'] = le.fit_transform(df['Customer_Gender'])
Converts categories into numbers
Example:
Male → 1
Female → 0
  Used when categories are binary or ordinal

7. One-Hot Encoding
df_encoded = pd.get_dummies(df, columns=['Payment_Method'])
Converts categories into separate columns
Each category becomes True/False
  Prevents misinterpretation of numeric relationships

8. Encoding Multiple Columns
df_multi = pd.get_dummies(df, columns=['Product_Category','City'])
  Encodes multiple categorical features at once

9. Dummy Encoding (Drop First)
df_dummy = pd.get_dummies(df, columns=['Payment_Method'], drop_first=True)
Removes one column to avoid:
Dummy Variable Trap
Multicollinearity


CONCLUSION
The experiment successfully demonstrated data normalisation and data type conversion techniques using Python.
Min-Max normalization scaled values between 0 and 1
Z-score normalization standardized data based on mean and standard deviation
Decimal scaling reduced magnitude of values


Overall, these preprocessing techniques help in:
Improving data quality
Making data suitable for machine learning
Ensuring accurate and efficient analysis

