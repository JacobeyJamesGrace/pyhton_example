# Nashville Housing Data Cleaning

## Project Overview

This project demonstrates a complete data cleaning workflow using **Python** and **Pandas** on the Nashville Housing dataset. The goal was to prepare the dataset for future analysis and machine learning by improving data consistency, handling missing values, and exporting a cleaned version of the data.

---

## Objectives

- Load and inspect the dataset
- Standardize column names
- Remove unnecessary columns
- Handle missing values
- Convert data types
- Standardize categorical values
- Export a cleaned dataset

---

## Technologies Used

- Python 3
- Pandas
- NumPy
- Jupyter Notebook

---

## Data Cleaning Process

### 1. Load the Dataset

- Imported the Nashville Housing dataset using Pandas.
- Displayed the first few rows to inspect the data.
- Reviewed data types and missing values using `info()`.
- Generated descriptive statistics for numeric columns.

---

### 2. Standardize Column Names

Column names were converted to **snake_case** to improve consistency and readability.

Example:

- `Sale Date` → `sale_date`
- `Sale Price` → `sale_price`

---

### 3. Remove Unnecessary Columns

Removed automatically generated index columns when present:

- `unnamed_0`
- `unnamed_0.1`
- `unnamed_0_1`

These columns do not provide analytical value.

---

### 4. Handle Missing Values

#### Sale Price

Rows with missing `sale_price` values were removed because the sale price is a critical field.

#### Bedrooms

Missing values in the `bedrooms` column were replaced using the **median** number of bedrooms, helping preserve the dataset while minimizing the impact of missing data.

---

### 5. Convert Date Columns

The `sale_date` column was converted into a proper datetime format.

Additional features were created:

- `sale_year`
- `sale_month`

These new columns make time-based analysis easier.

---

### 6. Standardize Categorical Values

The `sold_as_vacant` column was cleaned so all values are consistently represented as:

- Yes
- No

Common variations such as:

- Y / N
- True / False
- 1 / 0

were converted into a single standardized format.

---

### 7. Export Cleaned Data

The cleaned dataset was saved as:

```
nashville_housing_cleaned.csv
```

---

## Final Validation

Before exporting, the notebook verifies:

- Column names are standardized
- Missing values were handled appropriately
- `sale_date` is stored as a datetime object
- `sold_as_vacant` contains only standardized values
- The cleaned dataset is ready for analysis or machine learning

---

## Project Structure

```
.
├── clean_nashville.ipynb
├── nashville_housing_data.csv
├── nashville_housing_cleaned.csv
└── README.md
```

---

## Skills Demonstrated

- Data Cleaning
- Data Wrangling
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Missing Value Treatment
- Data Type Conversion
- Data Standardization
- Pandas
- Python

---

## Future Improvements

Potential enhancements include:

- Detecting and removing duplicate records
- Handling outliers
- Feature scaling and normalization
- Encoding categorical variables
- Preparing the dataset for predictive modeling

---

