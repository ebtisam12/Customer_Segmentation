# Data_Science_Final_Project

## Customer Segmentation Prediction


## Business Problem
A automobile company plans to enter new markets with its existing products. After conducting research on market behavior, they concluded that the new market behavior is similar to the current market behavior. So what they need to know now is to predict the right group of new customers in order to better target them in marketing the company's products.
Customer segmentation is the process of dividing customers into groups based on common characteristics so that companies can effectively and appropriately market each group.

## Objective
I aim for this project to apply unsupervised learning techniques to identify segments of customers based on customer behavior data or common characteristics, such as age, gender and spending scores.

## Project Outline
![Project_Outline](https://github.com/ebtisam12/Customer_Segmentation/blob/main/Project_Outline.PNG)

## Project data
The data used is provided by [Kaggle](https://www.kaggle.com/vetrirah/customer)

[Data Dictionary](8068 raws by 11 features)(https://github.com/ebtisam12/Customer_Segmentation/blob/main/%D8%A8%D9%84%D8%A7%20%D8%B9%D9%86%D9%88%D8%A7%D9%86.%20%E2%80%8BData%20Dictionary.pdf) 

## Data exploration and cleaning
### Data Cleaning
In this section, I started by understanding the data and cleaned, prepared data for analysis by checked for missing values, and cleaned it as follows:
- Drop the 'ID' column
- Filled the 'Ever_Married' null values to 'Yes' with the High Spending_Score
- Filled the 'Ever_Married' null values to 'Yes' with the Average Spending_Score
- Filled the 'Graduated' null values to 'No' with age less than 23
- Filled the 'Graduated' null values to 'Yes' with an age greater than 23
- And for these three features 'Family_Size', 'Profession','Work_Experience' filled null values by the 'mode' 

### Data Visualizations
In this section, l used seaborn plots. Histogram, pie and cat plots to visualization each of the data feature with the Segmentation(target)  column to understand easily how each feature relates to a target column 

- Pair Plot for Data Distribution 
![Project_Outline](https://github.com/ebtisam12/Customer_Segmentation/blob/main/Project_Outline.PNG)

- 


## Features Extraction
- I added two more features, as we believe that will increase model predicting accuracy. The added features are:
Age Category: classify the workers based on their age (young, mature, old) 
Education Category: classify the workers based on their education lever (general education, undergraduate, postgraduate)

- Outliers


- Categorical encoding
Getting the dummies of the dataset

- Features Scaling
- Dataset Splitting 

## Data Modeling

- [`Logistic Regression`](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html?)
- [` KNN Classifier`](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html?highlight=kneighbors#sklearn.neighbors.KNeighborsClassifier)
- [`Decision Tree Classifier`](https://scikit-learn.org/stable/modules/generated/sklearn.tree.DecisionTreeClassifier.html?highlight=decision%20tree%20classifier#sklearn.tree.DecisionTreeClassifier)
- [`Random Forest Classifier `](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html?highlight=random%20forest%20classifier#sklearn.ensemble.RandomForestClassifier)
- [`Stacking Classifier`](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingClassifier.html?highlight=stacking%20classifier#sklearn.ensemble.StackingClassifier)

## Models Validation & Optimizing
In order to have the best model, we attempted the SearchCV model selectors to optimize our applied models.
- GridSearchCV Model Selector

