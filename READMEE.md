
# Zomato Data Cleaning and Preprocessing

This project involves cleaning and preprocessing a dataset from Zomato to prepare it for exploratory data analysis or machine learning applications. The notebook handles missing values, transforms columns, and standardizes formats to make the dataset analysis-ready.

## 📁 Dataset

The dataset contains restaurant-related information such as:
- Restaurant names
- Locations
- Cuisines
- Ratings
- Costs
- Online delivery and booking options

## 🛠️ Key Steps Performed

### 1. **Importing Libraries**
Standard libraries for data manipulation and visualization were imported:
- `pandas`
- `numpy`
- `matplotlib.pyplot`
- `seaborn`

### 2. **Reading the Dataset**
```python
df = pd.read_csv("zomato.csv", encoding="latin-1")
```

### 3. **Initial Exploration**
- Inspected column names and null values.
- Checked the shape and sample entries of the dataset.

### 4. **Dropping Unnecessary Columns**
Removed columns that were not helpful or had too many missing values:
- `url`, `address`, `phone`, `dish_liked`, `reviews_list`, `menu_item`

### 5. **Handling Missing Values**
- Dropped rows with null values in critical columns like `rate` and `cuisines`.

### 6. **Cleaning Columns**
- Removed `/5` and other unwanted characters from the `rate` column.
- Removed commas and converted `approx_cost(for two people)` to integers.
- Cleaned the `rate` column and handled inconsistencies like "NEW" and "nan".

### 7. **Converting Columns**
- Transformed cost and rate to numeric types.
- Created a new column `cost_category` for different ranges of costs.

### 8. **Encoding Categorical Variables**
- Used Label Encoding for categorical features such as `location`, `rest_type`, `cuisines`, etc.

### 9. **Outlier Removal**
- Removed extreme outliers based on cost and rating thresholds.

## 📊 Final Output

The cleaned dataset is ready for:
- Visualizations
- Clustering
- Recommendation systems
- Predictive modeling

## 📌 Notes
- The project primarily focuses on preprocessing.
- Next steps could include feature engineering or model building for restaurant recommendations or rating predictions.

## 🧠 Author
This notebook was developed as part of a data science workflow to prepare real-world data for analysis.
