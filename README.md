# Churn Prediction Model

Predicting at-risk learners on an online course platform using engagement data.

## Objective
Predict which users are likely to churn (drop out) from an online learning platform, so at-risk users can be identified early and given personalized support.

## Dataset
500 synthetic user records (`online_learning_course_consumption_dataset.csv`) with engagement features: hours spent per week, course duration, completion percentage, satisfaction score, experience level, course type, and platform.

## Approach
- Defined churn from `Completion_Status` (Dropped = churned)
- Removed identifier and outcome-leaking columns
- One-hot encoded categorical features
- Trained and compared **Random Forest** and **Gradient Boosting**

## Results
| Metric | Random Forest | Gradient Boosting |
|---|---|---|
| Accuracy | 0.92 | 0.92 |
| Recall (Churn) | **0.97** | 0.89 |

**Random Forest** was chosen as the final model for its higher recall on churned users.

## Key Insight
`Completion_Percentage` is by far the strongest predictor of churn — early drops in course progress are the clearest early-warning signal.

## Files
- `Churn_Prediction_Model.ipynb` — full analysis notebook
- `Churn_Prediction_Model_Report.pdf` — formatted write-up
- `online_learning_course_consumption_dataset.csv` — dataset used
