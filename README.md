### \# Operational Downtime Predictor

* Predicts equipment failure risk in industrial operations and translates
* Predictions into estimated downtime costs, helping operations teams
* Prioritise maintenance before failures occur.

\---



\##  Problem



Unplanned equipment downtime in industrial settings costs companies thousands of pounds per hour. Traditional maintenance schedules are time-based rather than condition-based, so machines are either serviced too early (wasting resources) or too late (leading to failures).



This project builds a machine learning system that uses real-time sensor data to flag at-risk equipment early, giving operations teams a window to act before failures occur.



\---



\## Dataset



* Source: AI4I 2020 Predictive Maintenance Dataset - UCI ML Repository
* Size: 10,000 records, 6 features
* Target: Binary machine failure classification
* Challenge: Severe class imbalance; only 3.39% of records are failures



\---



\## Approach



* &#x20;Conducted exploratory data analysis to understand feature distributions and failure rates
* &#x20;Handled class imbalance using SMOTE (Synthetic Minority Oversampling Technique)
* &#x20;Trained and compared three models: Logistic Regression, Random Forest, and XGBoost
* &#x20;Evaluated primarily on "recall"; missing a real failure is far costlier than a false alarm



\##  Results



| Model | Precision | Recall | F1 Score | Failures Caught |

|-------|-----------|--------|----------|-----------------|

| Logistic Regression | 0.15 | 0.81 | 0.26 | 55/68 |

| Random Forest       | 0.43 | 0.72 | 0.54 | 49/68 |

| XGBoost (selected)  | 0.37 | 0.84 | 0.51 | 57/68 |



XGBoost was selected as the final model for its highest recall, capturing 57 of 68 actual failures in the test set.



\---



\## 🛠️ Tech Stack



* Python, Pandas, Scikit-learn, XGBoost, Imbalanced-learn
* Streamlit (dashboard — coming soon)
* Deployed on Streamlit Cloud (coming soon)



\---



\## Live Demo



* Coming soon; Streamlit dashboard with real-time failure risk prediction and an estimated downtime cost calculator



\---

