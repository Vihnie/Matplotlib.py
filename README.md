# Matplotlib.py
Task 1: Load and Explore the Dataset
data = pd.read_csv('your_dataset.csv')

Show the first 5 rows
print(data.head())

Check for missing values
print(data.isnull().sum())

Fill missing values or drop them (example: filling missing values with the mean)
data = data.fillna(data.mean())

Task 2: Basic Data Analysis
Get basic statistics
print(data.describe())

Group by a categorical column (e.g., species) and calculate the mean of each group
grouped_data = data.groupby('species').mean()
print(grouped_data)

Task 3: Data Visualization
1. Line chart (example showing trends over time)
plt.figure(figsize=(10,6))
plt.plot(data['Date'], data['Sales'])
plt.title('Sales Over Time')
plt.xlabel('Date')
plt.ylabel('Sales')
plt.show()

2. Bar chart (example comparing numerical values across categories)
plt.figure(figsize=(10,6))
data.groupby('species')['sepal_length'].mean().plot(kind='bar')
plt.title('Average Sepal Length by Species')
plt.xlabel('Species')
plt.ylabel('Average Sepal Length')
plt.show()

3. Histogram (example showing the distribution of a numerical column)
plt.figure(figsize=(10,6))
plt.hist(data['sepal_length'], bins=10, edgecolor='black')
plt.title('Distribution of Sepal Length')
plt.xlabel('Sepal Length')
plt.ylabel('Frequency')
plt.show()

4. Scatter plot (example showing the relationship between two numerical columns)
plt.figure(figsize=(10,6))
plt.scatter(data['sepal_length'], data['petal_length'])
plt.title('Sepal Length vs Petal Length')
plt.xlabel('Sepal Length')
plt.ylabel('Petal Length')
plt.show()
```
