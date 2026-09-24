\# Student Performance Analytics \& Prediction using Machine Learning



\## Project Overview



This project analyzes student performance data to identify factors associated with examination scores and develops machine learning models for predicting student exam performance.



The project follows a complete data analytics workflow:



\*\*Data Collection → Data Cleaning → Exploratory Data Analysis → Insights → Machine Learning → Model Evaluation → Recommendations\*\*



\## Dataset



The project uses the \*\*Student Performance Factors\*\* dataset containing 6,607 student records and 20 variables.



\*\*Dataset Source:\*\*  

https://www.kaggle.com/datasets/ayeshaseherr/student-performance



The dataset contains academic, behavioral, family, school, and demographic factors such as:



\- Hours Studied

\- Attendance

\- Previous Scores

\- Sleep Hours

\- Tutoring Sessions

\- Motivation Level

\- Parental Involvement

\- Access to Resources

\- Teacher Quality

\- Peer Influence

\- Family Income

\- School Type

\- Exam Score



\## Data Cleaning



The original dataset contained 235 missing values across:



\- Teacher Quality

\- Parental Education Level

\- Distance from Home



Missing categorical values were replaced using the most frequent category.



After cleaning:



\- Rows: 6,607

\- Columns: 20

\- Missing values: 0

\- Duplicate rows: 0



A potential data-quality anomaly was identified because one Exam Score value was 101 while the observed minimum and maximum range otherwise suggests a score scale ending at 100. The observation was retained rather than removed without justification.



\## Exploratory Data Analysis



Important findings include:



\- Average Exam Score: 67.24

\- Average Attendance: 79.98%

\- Average Study Hours: 19.98

\- Average Previous Score: 75.07

\- Attendance correlation with Exam Score: 0.58

\- Hours Studied correlation with Exam Score: 0.45



Categorical analysis also showed differences in average exam scores across groups such as Access to Resources and Parental Involvement.



These relationships represent associations in the dataset and should not be interpreted as proof of causation.



\## Machine Learning



Three regression models were evaluated:



1\. Linear Regression

2\. Random Forest Regression

3\. Gradient Boosting Regression



\### Model Comparison



| Model | MAE | MSE | RMSE | R² |

|---|---:|---:|---:|---:|

| Linear Regression | 0.4524 | 3.2560 | 1.8044 | 0.7696 |

| Random Forest | 1.0841 | 4.6904 | 2.1657 | 0.6682 |

| Gradient Boosting | 0.7918 | 3.7699 | 1.9416 | 0.7333 |



Based on the tested evaluation metrics, Linear Regression was selected as the final model.



\### Final Model Performance



\- MAE: 0.4524

\- MSE: 3.2560

\- RMSE: 1.8044

\- R²: 0.7696



The final model was trained on the cleaned dataset and saved as:



`student\_performance\_final\_model.pkl`



A sample prediction produced an actual exam score of \*\*65\*\* and a predicted score of \*\*64.59\*\*, resulting in an absolute prediction error of \*\*0.41\*\* for that sample.



The model provides predictive information about exam scores and should be used as a decision-support tool rather than as a replacement for educator judgment.



\## Recommendations



Based on the analysis:



\- Identify students with lower attendance and provide appropriate academic follow-up.

\- Encourage structured and consistent study schedules.

\- Improve access to learning resources for students with limited resources.

\- Encourage constructive family engagement with students' learning.

\- Use model predictions as a supporting signal alongside educator judgment.



\## Technologies Used



\- Python

\- Pandas

\- NumPy

\- Matplotlib

\- Seaborn

\- Scikit-learn

\- Jupyter Notebook

\- Joblib



\## Project Structure



```text

project/

│

├── data/

│   ├── StudentPerformanceFactors.csv

│   └── StudentPerformanceFactors\_cleaned.csv

│

├── notebooks/

│   └── Student\_Performance\_Analytics.ipynb

│

├── report/

│

├── student\_performance\_final\_model.pkl

├── requirements.txt

├── .gitignore

└── README.md

