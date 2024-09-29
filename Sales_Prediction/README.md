# Sales Prediction Based on Advertising Expenditure

## Objective
This project aims to predict sales based on advertising data using machine learning techniques. It analyzes the relationship between advertising spending across different media channels (TV, radio, newspaper) and the resulting sales figures.

## Dataset
The dataset contains information about advertising budgets for TV, radio, and newspaper, along with corresponding sales figures.

# Project Workflow 📚

##  Importing Libraries
The project starts by importing essential libraries such as NumPy, Pandas, Matplotlib and Seaborn.

## Loading Data
The advertising dataset is loaded from a CSV file using Pandas.

## Data Inspection and Cleaning

Basic statistical analysis is performed to understand the structure of the dataset. The absence of missing and duplicated values is confirmed.

## Exploratory Data Analysis (EDA)

Pair plots and a heatmap are generated to visualize relationships and correlations between different variables.

### Observations
-   **TV Ads**: A strong positive correlation between TV ads and sales suggests that increasing TV advertising significantly impacts sales. This should be prioritized in marketing efforts.
-   **Radio Ads**: While not as impactful as TV ads, radio ads still contribute positively to sales. They can be a supplementary strategy for increasing sales.
-   **Newspaper Ads**: Since newspaper ads show little to no clear relationship with sales, they may not be a cost-effective medium for driving sales.

## Data Preprocessing

Data preprocessing is crucial for preparing the dataset for modeling. This step involves handling missing values, dealing with outliers, converting categorical variables into numerical format, etc. 

### Splitting the data into test set and training set
----
We split the dataset into the independent variable matrix (**X**) and dependent variable vector (**y**).

**y**  consists of the target variable which is 'Sales' &  **X**  will consist of all the remaining columns in the dataset.

### Feature Scaling
-----
The next step in our project is feature scaling through standardization, also called Z-score normalization, which is an important preprocessing step for many machine learning algorithms. It involves rescaling each feature such that it has a standard deviation of 1 and a mean of 0.

Even if tree based models are (almost) not affected by scaling, many other algorithms require features to be normalized.

## Model Testing

With the preprocessed dataset, we proceed to rigorous **model testing** to determine the best approach for estimating sales. We evaluate multiple regression models, including **Linear Regression**, **Decision Tree**, **Random Forest** and **Support Vector Machine**, using metrics like **R²** and **Mean Squared Error**.

# **Conclusion**
**Random Forest Regression** model delivered the best performance based on the following key factors:

-   **Lowest Mean Squared Error (MSE):** The model exhibited the lowest MSE of 1.74, indicating minimal prediction errors and a strong fit to the data.
-   **Highest R² Score:** With an R² score of 0.92, Random Forest Regression explained a substantial portion of the variance in the target variable, suggesting a highly reliable model.
-   **Excellent Model Fit:** The R² score, approaching 1, is a clear indicator of a strong model fit, implying that the model can accurately estimate the target variable based on the given features.
