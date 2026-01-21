# Task 3 – Regression Reasoning (Learning Notes)

In this task, I learned when to use Linear Regression and Logistic Regression and how to apply them on a dataset.

---

## Dataset used
I used the **House Prices – Advanced Regression Techniques** dataset from Kaggle.  
This dataset consists of different details about houses and their selling prices.

---

## First step: After loading the dataset, I checked:
- The shape of the dataset
- The first few rows using `head()`

This helped me understand what columns are available.

---

## Targets used in this task

### 1. House Price
- I used the column `SalePrice` as the target variable.
- Its value was continuous so I used linear regression

### 2. BuyHouse
- The dataset did not have a BuyHouse column.
- So I created one based on the price.
- If `SalePrice > 200000`, I marked it as 1 (Buy) or else I marked as 0.

Used logistic regression because it was a yes/no type problem.

---

## Feature selection
- LotArea
- YearBuilt
- OverallQual
- GrLivArea
- FullBath
- TotRmsAbvGrd

I chose these because they looked important for house prices and were easy to work with.

---

## Train and test split
I split the dataset into training and testing parts.
- 80% data for training
- 20% data for testing

Did this bcz the model is tested on data it has not seen before.

---

## Handling missing values
- I used mean imputation to fill missing values.
- I fitted the imputer only on training data.
- Then I applied it to test data.

This avoids using test data information while training.

---

## Next did was Feature scaling

I used StandardScaler to scale the features.
- When I learned about this part I got to know that scaling is needed bcz it helps the model to learn better and deal values with different range..

---

## Linear Regression model
- I trained a Linear Regression model to predict house prices and I evaluated the model using RMSE.
- RMSE tells how much the predicted price differs from the actual price.

---

## Logistic Regression model
- I trained a Logistic Regression model to predict BuyHouse.
- I tried to evaluate it using accuracy.
- Accuracy tells how many predictions were correct.

---

## What I learned about overfitting

- Overfitting happens when model performs well on training data but not that good in test data

- I used a train-test split it helped in checking this.

---

## Final understanding
- Linear Regression is used for continuous values.
- Logistic Regression is used for binary classification.
- Preprocessing steps like scaling and imputation.

---

## Conclusion
As a beginner doing this helped me to learn about what regression models are and using them.
