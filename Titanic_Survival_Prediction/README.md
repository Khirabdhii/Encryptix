# 🚢 Titanic Survival Prediction

## 🎯Objective

This project aims to predict whether a passenger on the Titanic survived or not based on various features such as age, gender, class, and more.

## ⓘ  About the Data 

The dataset used contains information about passengers from the Titanic ship. It consists of the following columns:

- **PassengerId** : Passenger ID which is unique for each passenger.
- **Pclass**: Socio-economic class of the passenger (1 = Upper class; 2 = Middle class; 3 = Lower class)
- **Name**: Name of the passenger.
- **Sex**: Sex of the passenger.
- **Age**: Age of the passenger.
- **SibSp**: Number of siblings and spouses of the passenger aboard the Titanic.
- **Parch**: Number of parents and children of the passenger aboard the Titanic.
- **Ticket**: Ticket Number of the passenger.
- **Fare**: Fare paid by the passenger.
- **Embarked**: Port of embarkation of the passenger (C = Cherbourg; Q = Queenstown; S = Southampton)
- **Cabin**: Cabin number of the passenger.
- **Survived**: Outcome of survival (0 = No; 1 = Yes)

# Project Workflow 📚

## Importing Libraries

In this project, we **import essential libraries** that play a pivotal role in enhancing data manipulation and visualization capabilities:

- **pandas**: A versatile library for data manipulation and analysis, enabling me to handle tabular data structures effectively.
- **numpy**: A fundamental library for numerical operations and computations, empowering me with efficient mathematical operations on arrays.
- **seaborn**: A powerful data visualization library based on matplotlib, simplifying the creation of informative statistical graphics.
- **matplotlib.pyplot**: A widely used library for creating plots and charts, crucial for visualizing my data and analysis results effectively.

## Loading Data

The project begins with **loading data** from the **CSV** **file** using the **pandas** library. This dataset contains crucial information about the Titanic passengers, forming the foundation of my analysis.

## Data Preprocessing

Data preprocessing is crucial for preparing the dataset for modeling. This step involves handling missing values, dealing with outliers, converting categorical variables into numerical format, etc. Data cleaning ensures that the dataset is ready for analysis and modeling.

### Taking Care Of Missing Data

- We discover that almost **77%** of **data** is **missing** in the '**Cabin**' column and thus, we drop it.
- We will fill in the missing values of the '**Age**' and '**Embarked**' columns with the **median** and **modal** value, respectively.

### Encoding Categorical Data
- First, we **split the dataset** into the **independent variable matrix (X)** and **dependent variable vector (y)**. y consists of the target variable which is 'Survived'. X consists of all the remaining columns except the 'Name' and 'Ticket' columns as they are unlikely to yield any useful information.
- Then we proceed to encode the 'Sex' and 'Embarked' columns through OneHotEncoding.

### Feature Scaling
The next step in our project is feature scaling through standardization, also called Z-score normalization, which is an important preprocessing step for many machine learning algorithms. It involves rescaling each feature such that it has a standard deviation of 1 and a mean of 0.

Even if tree based models are (almost) not affected by scaling, many other algorithms require features to be normalized.
## Model Testing

With the preprocessed dataset, we proceed to rigorous **model testing** to determine the best approach for predicting passenger survival on the Titanic. We evaluate multiple machine learning classification models, including **Logistic Regression**, **Decision Tree**, **Random Forest**, **K-Nearest Neighbor**, **Naive Bayes** and **Support Vector Machine**, using metrics like **accuracy**, **precision**, **recall**, and **F1-score**. 

## Conclusion

- The best results were obtained from  **SVM Algorithm**  with an **accuracy** of  **84%**.

- The **precision** of the model is **87%** which means that out of all the passengers that the model predicted would survive, only 87% actually did.

- The **recall** of the model is **71%** which indicates that out of all the passengers that actually survived, the SVM model only predicted this outcome correctly for 71% of those passesngers.

- Moreover, the **F1 score** of the model comes out to be **0.78** which is moderately close to 1. This tells us that the model does a decent job of predicting whether or not passengers survived.
