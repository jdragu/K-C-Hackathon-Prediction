INTRODUCTION 

There are two parts to the Hackathon predictive model:  

1. Predictive Model: this is the predictive model itself. The purpose of this model is to predict which ideas will be viable finalists based on past data, and to interpret the model's accuracy using a confusion matrix. 

2. Confusion Matrix: this is a second confusion matrix built to identify which ideas have met, underperformed, or overperformed on their estimated dollar amount of benefit.


HOW IT WAS BUILT: 


1. Steps taken to build the Predictive Model: 

Data Preparation: Load and clean the dataset, ensuring all necessary columns are present and correctly formatted. 



Model Training: Train the model using features like idea_name, submitted_estimate, actual_benefits_wc, actual_benefits_savings, and expert_weighted_avg. This was all taken from the following two Excel files: 

- Global Hackathons Ideas Status - General Review -2023.xlsx 

- Global Hackathons Ideas Status - Judges-Experts Panel Scores-ChatGPT-Actual Estimations.xlsx 

Note: I primarily used this Excel file to build the hackathon_ideas.csv file. (a) - the general review – was mostly just a cross-check resource. 


Prediction: Use the model to predict the viability of new ideas. It is a Random Forest classification model. 


Evaluation: Evaluate the model's performance using a confusion matrix and feature importance list to visualize accuracy and which variables hold the most weight in the outcome of the prediction. 


2 . Confusion matrix steps:

Build to evaluate whether an idea fits into one of these categories: 

- True Positive: High Scored idea that delivered benefits, delivering their commitment in money or more 

- True Negative: High Scored idea that underdelivered benefits, delivered none or below commitment 

- False Positive: Low scored idea that delivered benefits 

- False Negative: Low scored idea that didn't deliver benefits 

Result Interpretation: Generate a final table summarizing each idea's score, actual benefits, and confusion matrix results. 
