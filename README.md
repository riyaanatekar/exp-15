AIM

The aim of this experiment is to study and implement various data normalization techniques and data type conversion methods using Python libraries such as Pandas, NumPy, and Scikit-learn.
The experiment focuses on transforming raw data into a structured and standardized format by applying:

Min-Max Normalization
Z-Score Normalization
Decimal Scaling
Label Encoding
One-Hot Encoding
Dummy Encoding

It also aims to understand how these techniques improve data quality, consistency, and suitability for data analysis and machine learning models.

THEORY
1. Data Normalization

Data normalization is the process of scaling numerical data into a specific range or distribution so that different features contribute equally to analysis. It is essential when dealing with datasets having varying scales.

a) Min-Max Normalization
Min-Max normalization transforms data into a fixed range between 0 and 1 .

In the experiment:
Applied on the Price column individually
Applied on multiple columns like Price, Units_Sold, Discount

Functions used:
df['Price'].min()
df['Price'].max()
Vectorized operations in Pandas

Purpose:
Scales all values proportionally
Useful when the distribution is not Gaussian

b) Z-Score Normalization (Standardization)

Z-score normalization converts data into a distribution with mean = 0 and standard deviation = 1:

In the experiment:
Applied to Units_Sold
Also applied to multiple columns

Functions used:
df['Units_Sold'].mean()
df['Units_Sold'].std()

Purpose:
Handles outliers effectively
Suitable for statistical analysis and ML models

c) Decimal Scaling

Decimal scaling normalizes data by dividing values by powers of 10:

Where j is chosen such that the maximum value becomes less than 1.

In the experiment:
Price divided by 10000
Units_Sold divided by 100

Purpose:
Simple normalization method
Based on magnitude of values


2. Data Type Conversion
Categorical data must be converted into numerical form for machine learning algorithms.

a) Label Encoding
Label encoding assigns integer values to categories.

Example:
Male → 1
Female → 0

Functions used:
LabelEncoder()
fit_transform()

Characteristics:
Assigns values based on alphabetical order
Can be reversed
Suitable for ordinal data

b) One-Hot Encoding
One-hot encoding creates binary columns for each category.

Example:
Payment methods → COD, Credit Card, Debit Card, UPI
Each becomes a separate column with 0 or 1

Functions used:
pd.get_dummies()

Characteristics:
Avoids ordinal relationship
Increases dimensionality

c) Dummy Encoding (Drop First)
Dummy encoding is a reduced version of one-hot encoding where one column is dropped to avoid redundancy.

Functions used:
pd.get_dummies(drop_first=True)

Purpose:
Prevents dummy variable trap
Reduces multicollinearity

3. Working with External Datasets
The experiment also applies normalization and encoding on real datasets:
Amazon Dataset
Min-Max normalization on Price, Units_Sold, Rating, Reviews
Z-score normalization on multiple columns
Decimal scaling on Price and Reviews
Student Dataset
Label encoding for Placement_Status
One-hot encoding for Department
Dummy encoding for reduced feature set

4. Libraries Used
Pandas (pd) → Data manipulation and DataFrame operations
NumPy (np) → Numerical computations
Scikit-learn (LabelEncoder) → Encoding categorical data

CONCLUSION
In this experiment, various techniques of data normalization and data type conversion were successfully implemented and analyzed using Python.
Min-Max normalization scaled data within a fixed range, making it easier to compare different features. Z-score normalization standardized the data and proved effective in handling outliers by centering values around the mean. Decimal scaling provided a simple approach to reduce large numerical values based on their magnitude.
For categorical data, label encoding converted text data into numerical form but introduced ordinal relationships. One-hot encoding resolved this issue by creating independent binary columns, while dummy encoding further optimized the dataset by reducing redundancy and avoiding multicollinearity.
The use of functions such as min(), max(), mean(), std(), fit_transform(), and pd.get_dummies() demonstrated how Python libraries simplify complex data preprocessing tasks.
Overall, the experiment highlighted the importance of preprocessing in data analysis. Proper normalization and encoding ensure that datasets are clean, consistent, and suitable for statistical analysis and machine learning models, ultimately improving accuracy and performance.

