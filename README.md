EXPERIMENT: DATA NORMALISATION AND DATA TYPE CONVERSION

Aim
To study and perform data analysis and preprocessing using Python (Pandas library) by creating structured datasets and applying various functions such as pd.DataFrame(), head(), tail(), info(), describe(), isnull(), dropna(), fillna(), value_counts(), groupby(), sort_values(), astype(), and apply() in order to clean, transform, organize, and analyze data efficiently.

Theory
1. Introduction to Data Analysis and Preprocessing
Data analysis is the process of examining, organizing, transforming, and interpreting data to extract useful information. Before analysis, raw data must undergo data preprocessing, which includes:
Handling missing values
Correcting data types
Organizing and sorting data
Summarizing and grouping data

The Pandas library in Python provides powerful tools to perform all these operations efficiently using DataFrames.


2. Data Structure: DataFrame
Function: pd.DataFrame()
A DataFrame is a two-dimensional labeled data structure consisting of rows and columns.
It is used to store heterogeneous data (different data types).

Importance:
Forms the base for all data operations
Allows easy manipulation and analysis
3. Data Inspection and Understanding

a) head() and tail()
head() displays the first few rows (default = 5).
tail() displays the last few rows.
 Purpose:
Quick overview of dataset
Helps verify whether data is loaded correctly

b) info()
Provides concise summary of DataFrame:
Column names
Number of non-null entries
Data types
 Importance:
Helps identify missing values
Useful for checking data consistency

c) describe()
Generates statistical summary for numerical columns:
Mean
Median (50%)
Standard deviation
Minimum and maximum
Quartiles (25%, 75%)
 Importance:
Helps understand distribution and spread of data
Useful for detecting outliers

4. Handling Missing Data
Missing data is a common issue in real-world datasets and must be handled carefully.

 a) isnull()
Detects missing values (NaN).
Returns Boolean values (True for missing).

 b) dropna()
Removes rows or columns containing missing values.

 Types:
Row-wise removal
Column-wise removal

 c) fillna()
Replaces missing values with:
Constant value
Mean/median
Forward/backward fill
 Importance:
Maintains dataset size
Prevents data loss

5. Data Transformation and Formatting
a) astype()
Converts data type of a column.

Example:
Integer → Float
String → Integer

 Importance:
Ensures compatibility for calculations
Avoids errors in analysis
 b) apply()
Applies a custom function across rows or columns.

Importance:
Enables flexible data transformation
Useful for complex operations

c) Column Renaming
Improves readability and understanding of dataset.


6. Data Analysis Techniques
a) value_counts()
Counts occurrences of unique values in a column.

Importance:
Helps analyze categorical data
Identifies most frequent values

b) groupby()
Splits data into groups based on column values.
Performs aggregate functions like:
Sum
Mean
Count

Importance:
Helps in pattern recognition
Useful for comparative analysis


7. Data Sorting
Function: sort_values()
Sorts dataset based on column values.
Types:
Ascending (default)
Descending (ascending=False)

Importance:
Helps identify highest/lowest values
Makes data organized and readable


8. Importance of Data Preprocessing
Improves data quality
Removes inconsistencies and errors
Ensures accurate results
Prepares data for visualization and modeling
Conclusion

The experiment successfully demonstrates the application of data analysis and preprocessing techniques using the Pandas library. The DataFrame structure provides an efficient way to store and manipulate data.

Functions like head(), tail(), info(), and describe() help in understanding the dataset, while isnull(), dropna(), and fillna() effectively handle missing data. Data transformation functions such as astype() and apply() ensure proper formatting and flexibility in operations.

Analytical functions like value_counts() and groupby() allow meaningful interpretation of data by identifying patterns and relationships. Additionally, sort_values() helps in organizing data systematically.

Overall, the experiment highlights the significance of data cleaning, transformation, and analysis, which are essential steps in converting raw data into meaningful insights and supporting effective decision-making in real-world applications.

