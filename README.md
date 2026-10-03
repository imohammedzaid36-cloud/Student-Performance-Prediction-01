# Student-Performance-Prediction-01
Student Performance Prediction
Slide 1 — Title
Student Performance Prediction Using Python and Machine Learning
Tools used:
•	Python 
•	Jupyter Notebook 
•	Pandas 
•	NumPy 
•	Matplotlib 
•	Scikit-learn 
Presented by: Your Name
Class: Your Class
Date: Your Date
________________________________________
Slide 2 — Objective of the Project
Objective
The aim of this project is to analyze student data and build a simple model that predicts a student's Final Score based on Study Hours.
We also examined:
•	Attendance 
•	Previous Score 
•	Sleep Hours 
•	Final Score 
What I wanted to learn
"I wanted to understand how student-related factors are connected to final scores and use a simple regression model to make predictions."
________________________________________
Slide 3 — Dataset
We used a dataset containing 10 students and 5 variables.
Column	Meaning
Study_Hours	Number of hours studied
Attendance	Attendance value in the dataset
Previous_Score	Previous academic score
Sleep_Hours	Sleep value in the dataset
Final_Score	Final academic score
Dataset size: 10 rows × 5 columns
You can show your Jupyter output for:
df.shape
which gave:
(10, 5)
________________________________________
Slide 4 — Data Checking
I checked whether the dataset contained missing values.
I used:
df.isnull().sum()
The result was:
Study_Hours       0
Attendance        0
Previous_Score    0
Sleep_Hours       0
Final_Score       0
Result
There were no missing values in the dataset.
This means we could continue our analysis without having to fill or remove missing data.
________________________________________
Slide 5 — Descriptive Statistics
I used:
df.describe()
Some important averages were:
Variable	Average
Study Hours	4.9
Attendance	80.2
Previous Score	69.1
Sleep Hours	6.6
Final Score	69.0
This helped us understand the general characteristics of our dataset.
________________________________________
Slide 6 — Correlation Analysis
I used:
df.corr()
The correlations with Final Score were:
Variable	Correlation
Study Hours	0.9917
Attendance	0.9979
Previous Score	0.9920
Sleep Hours	0.9220
What does this mean?
A correlation closer to +1 indicates a strong positive linear relationship in this dataset.
For example, Study Hours had a correlation of approximately 0.992 with Final Score.
Important: This is a very small dataset of only 10 students, so these correlations should not be treated as evidence that the same relationships will hold for a larger population.
________________________________________
Slide 7 — Visualization
I created a scatter plot:
Study Hours vs Final Score
Show your graph here.
Then I added a regression trend line.
You can explain:
"The points generally follow an upward pattern, and the trend line summarizes the relationship between Study Hours and Final Score in this dataset."
________________________________________
Slide 8 — Regression Model
The regression equation we obtained was:
Final Score=6.6869(Study Hours)+36.2340\boxed{Final\ Score = 6.6869(Study\ Hours) + 36.2340} 
What does this mean?
The slope is approximately:
6.69
So, according to this fitted model, increasing Study Hours by one hour corresponds to an estimated increase of about 6.69 Final Score points.
The intercept is approximately:
36.23
This is the model's estimated score when Study Hours is zero.
________________________________________
Slide 9 — Example Prediction
We tested the model with:
Study Hours = 6
The prediction was:
6.6869(6)+36.23406.6869(6)+36.2340 
= 76.36
So the model predicted:
Final Score ≈ 76.36
Your dataset actually contains a student with 6 Study Hours and a Final Score of 90.
This is a good example to explain that a prediction is not necessarily the same as the actual score.
________________________________________
Slide 10 — Model Evaluation
We calculated three evaluation measures.
Measure	Result
R²	0.9834
MAE	1.2687
RMSE	1.5772
Simple explanation
R² = 0.9834
The model explains about 98.34% of the variation in Final Score within this dataset.
MAE = 1.27
The predictions differ from the actual scores by about 1.27 points on average, using absolute error.
RMSE = 1.58
This is another measure of prediction error that gives more weight to larger errors.
________________________________________
Slide 11 — Actual vs Predicted
Show your Actual vs Predicted Final Scores graph here.
You can say:
"This graph compares the scores produced by the model with the actual Final Scores. The closer the predicted values are to the actual values, the better the model is fitting this particular dataset."
________________________________________
Slide 12 — Prediction Function
We also created a function:
def predict_score(study_hours):
    return m * study_hours + b
For example:
predict_score(6)
gave:
76.35562310030394
This means the model can be used to make a prediction for a specified number of Study Hours.
________________________________________
Slide 13 — Conclusion
Conclusion
"In this project, I used Python and machine-learning techniques to analyze student performance data. I cleaned and examined the dataset, calculated statistics and correlations, visualized the data, created a linear regression model, and evaluated its predictions using R², MAE, and RMSE."
"For this particular 10-student dataset, Study Hours showed a strong positive linear relationship with Final Score. The model produced an R² of 0.9834 and an MAE of about 1.27 points."
Limitation
"The dataset contains only 10 students, so the results are specific to this dataset and should not be generalized to all students. A larger and more representative dataset would be needed for stronger conclusions."
That last point is important and will make your presentation more scientifically responsible.
________________________________________
1. Dataset
df
Show the 10 students and the five original columns.
2. Data checking
df.isnull().sum()
Show that every column has 0 missing values.
3. Graph
Show your:
Study Hours vs Final Score graph with the trend line.
4. Model results
Show:
R-squared: 0.9833720722331486
Mean Absolute Error: 1.2686930091185418
Root Mean Squared Error: 1.5771930743954499
5. Live prediction
Run:
predict_score(6)
and show:
76.35562310030394
________________________________________
"My project is Student Performance Prediction. I created a dataset containing study hours, attendance, previous score, sleep hours and final score. I used Pandas to analyze the data and checked that there were no missing values. I then calculated correlations and created graphs using Matplotlib. I built a simple linear regression model using Study Hours to predict Final Score. The regression equation was Final Score = 6.6869 × Study Hours + 36.2340. For 6 study hours, the model predicts a score of about 76.36. I evaluated the model using R², MAE and RMSE. The R² was 0.9834 and the MAE was about 1.27 points. However, because my dataset contains only 10 students, these results should not be generalized to a larger population."
