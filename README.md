# 🏠 House Price EDA & ML Readiness Analysis

## 📌 Project Overview

This project performs a comprehensive Exploratory Data Analysis (EDA) and Machine Learning Readiness Assessment on the King County House Sales Dataset.

Rather than immediately training machine learning models, this project follows a **research-first approach**, focusing on understanding the dataset, identifying key drivers of house prices, detecting data quality issues, exploring statistical relationships, and preparing a leakage-safe preprocessing plan for future regression modeling.

The objective is to answer:

> Which structural, locational, and temporal features most strongly influence house prices?

---

## 🎯 Problem Statement

Estimate residential property prices in King County, USA using structural, locational, and sale-time attributes that would be available at or before the time of sale.

This project focuses on:

* Understanding the data generating process
* Statistical exploration
* Data quality assessment
* Feature relationship analysis
* Outlier identification
* Train-test split planning
* Preprocessing readiness

No machine learning model training is performed in this phase.

---

## 📊 Dataset Information

**Dataset:** House Sales in King County, USA

**Rows:** 21,613

**Features:** 21

**Target Variable:** `price`

### Key Features

| Feature      | Description                   |
| ------------ | ----------------------------- |
| price        | House sale price (Target)     |
| bedrooms     | Number of bedrooms            |
| bathrooms    | Number of bathrooms           |
| sqft_living  | Living area in square feet    |
| sqft_lot     | Lot area in square feet       |
| floors       | Number of floors              |
| waterfront   | Waterfront property indicator |
| view         | Quality of view               |
| condition    | Overall condition             |
| grade        | Construction/design grade     |
| yr_built     | Year built                    |
| yr_renovated | Year renovated                |
| zipcode      | Location identifier           |
| lat, long    | Geographic coordinates        |
| date         | Sale date                     |

---

## 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Google Colab

---

## 📈 Exploratory Data Analysis Performed

### Data Quality Assessment

* Dataset shape inspection
* Schema audit
* Data type verification
* Missing value analysis
* Duplicate detection
* ID uniqueness validation

### Statistical Analysis

* Mean
* Median
* Mode
* Variance
* Standard Deviation
* Skewness Analysis

### Relationship Analysis

* Correlation Matrix
* Correlation Heatmap
* Covariance Analysis
* Feature Importance Ranking

### Group-Based Analysis

* Price vs Grade
* Price vs Condition
* Price vs Waterfront
* Price vs Zipcode
* Monthly Price Trends

### Probability Analysis

* Probability of homes above median price
* Conditional probability of premium homes

### Outlier Analysis

* IQR-based outlier detection
* Extreme property identification

---

## 📍 Advanced Explorations

The project extends beyond basic EDA by investigating:

### Geographic Analysis

* Price distribution across latitude and longitude
* Neighborhood-level pricing patterns
* Location dominance over structural features

### House Age Analysis

* House age feature engineering
* Relationship between age and property value

### Renovation Impact

* Renovated vs Non-renovated property comparison
* Renovation premium estimation

### Price Per Square Foot

* Market value efficiency analysis
* Neighborhood price-per-square-foot comparison

### Luxury Home Segmentation

* Identification of top 10% premium properties
* Characteristics of luxury homes

### Waterfront Premium

* Quantification of waterfront price advantage

---

## 📊 Visualizations Created

* Price Distribution Histogram
* Log Price Distribution
* Living Area vs Price Scatter Plot
* Correlation Heatmap
* Waterfront Price Comparison
* Zipcode-Based Boxplots
* Monthly Price Trends
* Geographic Price Map
* Grade vs Condition Heatmap
* Price Per Square Foot Distribution

---

## 🔍 Key Findings

### 1. Living Area Drives Price

`sqft_living` exhibits one of the strongest positive relationships with house prices.

### 2. Construction Quality Matters

Higher-grade properties consistently command significantly higher prices.

### 3. Location Has Strong Influence

Latitude, longitude, and zipcode demonstrate substantial impact on property valuation.

### 4. Waterfront Properties Command Premium Prices

Waterfront homes are significantly more expensive than non-waterfront properties.

### 5. Target Variable Is Right-Skewed

House prices contain luxury outliers, suggesting potential benefit from log transformation during future modeling.

---

## ⚙️ Feature Engineering

Additional features created during analysis:

```python
house_age = 2015 - yr_built
price_per_sqft = price / sqft_living
total_rooms = bedrooms + bathrooms
renovated = (yr_renovated > 0)
```

---

## 🔒 Machine Learning Readiness

### Planned Preprocessing Pipeline

#### Numerical Features

* Median Imputation (if needed)
* Standard Scaling

#### Categorical Features

* One-Hot Encoding

#### Data Splitting

* 80/20 Train-Test Split
* Fixed Random State
* Leakage Prevention Strategy

### Important Rule

All preprocessing steps will be fitted only on training data to prevent data leakage.

---

## 📂 Project Structure

```text
House-Price-EDA/
│
├── House_Price_EDA.ipynb
├── kc_house_data.csv
├── README.md
└── visualizations/
```

## 📚 Learning Outcomes

Through this project, I gained practical experience in:

* Exploratory Data Analysis
* Statistical Reasoning
* Data Visualization
* Feature Engineering
* Outlier Detection
* Probability Analysis
* Data Quality Assessment
* ML Pipeline Planning
* Leakage Prevention Strategies

---

## 👨‍💻 Author

Arya

