# Written Answers

### 1. Why did you choose specific imputation methods?

First, I checked which columns had missing values.  
I handled numerical and categorical columns separately.

For numerical columns, I used median to fill missing values.  
I did not use mean because some values were very large or very small.  
Median is safer and does not change much because of outliers.

For categorical columns, I used mode.  
Mode means the value that appears most often.  
This is suitable for categorical data.

---

### 2. How did you handle outliers and why?

I used the IQR (Interquartile Range) method to detect outliers.
Found Q1 (25th percentile) then Found Q3 (75th percentile) after that I Calculated IQR = Q3 − Q1

Values below Q1 − 1.5 × IQR and above Q3 + 1.5 × IQR were treated as outliers.

Instead of removing rows, I capped the outliers within the allowed range.  
It reduces the effect of extreme values without losing data.

---

## 3. Where and how might data leakage occur in this dataset?

Data leakage happens when information from test data or future data
is used during model training.

Here data leakage can happen if Scaling is done before splitting the data into training and testing sets,Missing values are filled using statistics from the full dataset,Features related to the target variable  are used incorrectly
To avoid data leakage, all preprocessing steps should be done after the train test split and only using training data.
