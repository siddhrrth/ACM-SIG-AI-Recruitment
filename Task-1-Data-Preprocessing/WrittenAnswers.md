# Written Answers

### 1. Why did you choose these methods to fill missing values?

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

### 3. How did you encode categorical variables?

For columns with Yes or No values, I used label encoding

For columns with more than two categories I used one hot encoding.

---

### 4. What is data leakage and where can it happen?

Data leakage happens when information from test data or future data
is used during training.

It will happen when Data is scaled before train test split , Missing values are filled using the full dataset, Target related features are used

To avoid data leakage, preprocessing should be done only
after splitting the data and using training data only.

---

### 5. How did you prepare the final cleaned dataset?


- I Removed duplicate rows, Fixed incorrect data types, Filled missing values, Handled outliers, Encoded categorical columns

Finally, I saved the cleaned dataset as a CSV file.
