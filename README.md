
# 📊 Sales Data Analyzer (Python)

## Overview
This project is a **menu-driven Sales Data Analysis tool** built using **Python, Pandas, NumPy, Matplotlib, and Seaborn**.  
It allows users to **load CSV data**, **clean it**, **analyze it**, and **visualize insights** interactively through a terminal-based menu.

This tool is ideal for:
- Data Analysis mini-projects
- College assignments (AI / ML / Data Analytics)
- Beginners learning Pandas & Visualization

---

## 🛠 Technologies Used
- **Python 3**
- **Pandas** – Data handling & analysis
- **NumPy** – Numerical operations
- **Matplotlib** – Plotting
- **Seaborn** – Statistical visualizations

---

## 📂 Features Explained

### 1️⃣ Load Dataset
Loads a CSV file into a Pandas DataFrame.
- Converts data into a NumPy array
- Handles file not found errors

### 2️⃣ Explore Data
View:
- First & last 5 rows
- Column names
- Data types
- Dataset info

### 3️⃣ Data Cleaning
- Remove duplicate rows
- Handle missing values:
  - Show missing values
  - Fill with mean
  - Drop missing rows

### 4️⃣ DataFrame Operations
- Convert DataFrame to NumPy array
- Search values in columns
- Sort data
- Filter numeric data
- Aggregate functions (sum, mean, count)
- Statistical analysis (std, variance, quantiles)

### 5️⃣ GroupBy & Transform
- Group data by a column (e.g., Region)
- Aggregate using sum / mean / count
- Calculate percentage contribution within groups

### 6️⃣ Descriptive Statistics
- Numeric statistics
- Categorical statistics
- Pivot table generation

### 7️⃣ Data Visualization
Supports:
- Bar plot
- Box plot
- Scatter plot
- Histogram
- Heatmap
- Pie chart
- Stack plot

### 8️⃣ Save Visualization
- Saves the last generated plot as an image file

---

## ▶ How to Run the Project

```bash
python visualizer.py
```

### Input Required:
- CSV file path
- Column names for analysis & visualization
- Numeric values where applicable

---

## 📌 Example Dataset Columns
Typical dataset may contain:
- Region
- Product
- Category
- Sales
- Revenue
- Discount

---

---

## 1. load_data()
```python
self.data = pd.read_csv(file_path)
self.numpy_array = self.data.to_numpy()
```
**Explanation:**
- Loads CSV file into Pandas DataFrame
- Converts DataFrame to NumPy array for numerical operations

---

## 2. remove_duplicates()
```python
self.data.drop_duplicates(inplace=True)
```
**Explanation:**
- Removes duplicate rows
- `inplace=True` updates original dataset

---

## 3. handle_missing_data()
```python
self.data.fillna(self.data.mean(numeric_only=True), inplace=True)
```
**Explanation:**
- Replaces missing values with column mean
- Prevents errors in analysis

---

## 4. groupby_and_transform()
```python
self.data.groupby(group_col)[num_col].agg("sum")
```
**Explanation:**
- Groups data by a column
- Performs aggregation like sum or mean

---

## 5. Bar Plot
```python
sns.barplot(x=x, y=y, data=self.data)
```
**Use:** Compare values across categories

---

## 6. Box Plot
```python
sns.boxplot(x=x, y=y, data=self.data)
```
**Use:** Shows data spread and outliers

---

## 7. Scatter Plot
```python
sns.scatterplot(x=x, y=y, data=self.data)
```
**Use:** Shows relationship between two variables

---

## 8. Histogram
```python
sns.histplot(self.data[col], bins=30, kde=True)
```
**Use:** Shows data distribution

---

## 9. Heatmap
```python
sns.heatmap(corr, annot=True, cmap="coolwarm")
```
**Use:** Shows correlation between numeric columns

---

## 10. Pie Chart
```python
plt.pie(values, labels=labels, autopct="%1.1f%%")
```
**Use:** Shows percentage contribution

---
## 📈 Learning Outcomes
- Hands-on Pandas operations
- Data cleaning techniques
- GroupBy & pivot tables
- Real-world data visualization
- Menu-driven Python programming

---

## ✅ Best Use Case
✔ Academic projects  
✔ Data analysis practice  
✔ Beginner-friendly analytics tool  

---

## 👩‍💻 Author
**Rituu Poonjani**  
_Data Analysis Project_

---

⭐ If you like this project, feel free to improve or extend it!
