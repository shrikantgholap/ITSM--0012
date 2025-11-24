🚀 ITSM-0012: Machine Learning–Driven IT Service Management Enhancement
📌 Project Reference: PM-PR-0012

🔍 Client: ABC Tech


🏢 Domain: ITSM | Machine Learning | Automation




📖 Overview

ABC Tech receives a large volume of IT incidents daily and follows ITIL best practices for managing incidents, problems, changes, and configurations. Although processes are mature, a recent customer audit highlighted inefficiencies in incident prioritization and response time.

To address this issue, this project leverages Machine Learning to automate and enhance key ITSM operations. The solution aims to increase customer satisfaction, optimize resources, reduce manual workload, and prevent service disruptions.




🎯 Project Objectives

✔ Predict high-priority tickets to enable proactive handling
✔ Forecast incident volume for quarterly & annual planning
✔ Automatically tag incoming tickets with correct priority & department
✔ Predict RFC (Request for Change) and detect possible misconfigurations




🧠 Machine Learning Solutions Developed

Module	Goal	Best Model Used

High-Priority Ticket Prediction	Predict P1/P2 incidents at ticket arrival	Gradient Boosting Classifier
Incident Volume Forecasting	Quarterly & annual forecasting	SARIMA (1,2,1)
Auto-Tagging Tickets	Correct automatic labeling to reduce reassignment time	Random Forest
RFC Prediction	Predict potential changes to prevent disruption	Bagging Classifier



---

🧪 Dataset Details

📦 Total Records: 46,606
🗄 Source: MySQL (Read-only access)
📅 Years Covered: 2012–2014




🔑 Key Fields

CI_Name, CI_Cat, CI_Subcat, Priority, Impact, Urgency, Status,
No_of_Reassignments, Open_Time, Resolved_Time, Close_Time, Closure_Code,
No_of_Related_Interactions, No_of_Related_Incidents, No_of_Related_Changes




🧹 Data Preprocessing

✔ Removed irrelevent & constant features (e.g., Alert_Status)
✔ Imputed missing values using mode/median strategy
✔ Dropped columns with 95%+ missing values (e.g., Reopen_Time)
✔ Outlier handling using IQR Method for:

No_of_Reassignments

No_of_Related_Interactions


✔ Label Encoding for categorical variables
✔ Scaling applied before model training




🧠 Model Performance Summary

📌 Best Performing Model: Gradient Boosting Classifier

Metric	Training	Testing

Accuracy	100%	99.98%
Precision	1.0000	0.9978
Recall	1.0000	0.9952
F1 Score	1.0000	0.9975





📈 Time Series Forecast Results

Model	Result

ARIMA	Baseline forecasting
SARIMA (1,2,1)	Best performing with stable residual behavior





📌 RFC Prediction Results

Model	Accuracy (Train/Test)

Bagging Classifier	99.71% / 97.61%
Random Forest	100% / 97.51%




🛠 Tech Stack

Python

Pandas, NumPy

Scikit-Learn

XGBoost, Gradient Boosting, Bagging, Random Forest

StatsModels (SARIMA/ARIMA)

Matplotlib, Seaborn

Jupyter Notebook





🚀 Impact of the System

📌 Before

❌ Manual ticket prioritization
❌ Delayed escalations
❌ Frequent SLA violations

📌 After

✅ Automated ticket intelligence
✅ Faster response time
✅ Higher customer satisfaction
✅ Data-driven ITSM decisions
