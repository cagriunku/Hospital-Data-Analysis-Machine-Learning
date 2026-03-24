# Hospital-Data-Analysis-Machine-Learning
Hospital data analysis with SQL EDA and machine learning, exploring drivers of length of stay and limitations of predictive modeling.

Project Overview

This project explores a hospital patient dataset through a full data science workflow, including data cleaning, SQL-based exploratory analysis, and machine learning modeling.

The main objective is to understand what drives length of hospital stay (LOS) and evaluate whether it can be predicted using available patient features.

Dataset
~4,900 patient records
Features include:
Age
Gender
Diagnosis
Admission & Discharge dates
Hospital ID
Length of Stay (engineered)

The dataset was cleaned prior to analysis, including:

fixing invalid dates
handling missing values
standardizing categorical variables
Workflow
1. Data Cleaning
Corrected negative length-of-stay values caused by date errors
Standardized inconsistent diagnosis labels
Ensured data consistency before analysis
2. SQL-Based EDA

SQL was used to:

calculate average length of stay by diagnosis
explore distribution patterns
validate findings from Python analysis

Key findings:

Length of stay ranges between 1–10 days
Most common stay is around 5 days
Diagnosis is a stronger driver than age alone

A critical insight:

Age does not directly determine hospital stay —
its effect depends on the diagnosis (feature interaction).

3. Machine Learning
Regression (Predict LOS)
Linear Regression
Random Forest

Result:

Both models performed close to baseline

Conclusion:

Available features have limited predictive power.

Classification (Long-Stay Risk)

Target:

LongStay = 1 if LOS ≥ 6 else 0

Models:

Logistic Regression
Random Forest

Result:

Performance close to baseline
4. Error Analysis (Confusion Matrix)
TN = 274 | FP = 237  
FN = 272 | TP = 207

Insight:

High false negatives
Model often misses long-stay patients

This makes the model unreliable for real-world risk detection.

5. Clustering (Unsupervised Learning)

K-Means clustering identified 3 patient groups:

Young / short-stay
Young / long-stay
Elderly / moderate-stay

Key insight:

Similar patients can have very different outcomes →
hidden factors are missing from the dataset.

Key Takeaways
Data quality issues can significantly affect analysis results
Aggregated trends can be misleading without proper segmentation
Feature interactions are more important than individual variables
Limited features → limited predictive power
Technologies Used
Python
Pandas
NumPy
Scikit-learn
SQL

Author

Çağrı 
