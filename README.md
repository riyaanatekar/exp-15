AIM
To perform exploratory data analysis and data visualization using Python, 
and to understand how to analyze datasets and represent them graphically using libraries such as Pandas, Matplotlib, and Seaborn.

THEORY
1. Exploratory Data Analysis (EDA)
EDA is the initial step in data analysis where datasets are explored to understand their structure, patterns, and relationships.

Helps to:
Summarize main characteristics
Identify trends and outliers
Prepare data for further analysis

Functions used:
df.head(), df.tail(), df.info(), df.describe()

2. Data Cleaning
Data cleaning ensures accuracy and consistency.
Handling missing values:
df.dropna()
df.fillna()

Removing duplicate entries:
df.drop_duplicates()
Changing data types:
df.astype()

3. Data Aggregation
Aggregation helps in summarizing data.
Using groupby():
df.groupby('Category').sum()
df.groupby('Category').mean()

Useful for:
Category-wise comparison
Extracting meaningful insights

4. Data Visualization
Visualization represents data graphically for better understanding.

Types of graphs:
Bar Chart

Used for comparing categories
df['Category'].value_counts().plot(kind='bar')
Line Chart
Shows trends over time
Histogram
Displays distribution of data
Scatter Plot
Shows relationship between variables
Pie Chart
Represents proportions

5. Libraries Used
Pandas → Data manipulation
Matplotlib → Basic plotting
Seaborn → Advanced visualization

6. Importance
Simplifies complex data
Helps in decision making
Reveals hidden patterns


CONCLUSION
The experiment successfully demonstrated the use of data analysis and visualization techniques in Python. By applying functions such as grouping, cleaning, and plotting, raw data was converted into meaningful insights.
Visualization made it easier to:
Understand patterns and trends
Compare different categories
Communicate results effectively
Thus, EDA and visualization are essential tools in data science and play a crucial role in real-world data analysis tasks.
