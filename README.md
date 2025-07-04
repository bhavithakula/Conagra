# Conagra
📊 Customer Churn Prediction – Group 14
This project focuses on predicting customer churn in the telecommunications sector using machine learning. Churn prediction is a critical business need: retaining customers is far more cost-effective than acquiring new ones. Our analysis helps identify customers at high risk of leaving, enabling the business to take proactive retention measures.

🎯 Project Purpose
Customer churn directly affects a company's revenue and growth. Our objective was to:

Understand patterns and behaviors that lead to customer churn.

Develop predictive models that accurately identify customers likely to leave.

Deliver actionable insights to drive strategic decisions for customer retention.

This project simulates a real-world data science workflow used in the telecom industry, from raw data to business recommendations.

📂 Files in This Repository
bash
Copy
Edit
Group_14/
├── Churn_Prediction_Group_14.ipynb    # Main Jupyter Notebook with code and visualizations
├── churn.csv                          # Cleaned and prepared dataset for model training
└── README.md                          # You are here!
🧠 Machine Learning Models Applied
To approach the classification problem, we implemented and compared multiple supervised learning algorithms:

Algorithm	Why We Chose It
Logistic Regression	Baseline model – interpretable, easy to implement
Decision Tree	Good for visualizing decision paths
Random Forest	Handles overfitting better by averaging multiple trees
K-Nearest Neighbors	Simple and intuitive, distance-based classifier
Naive Bayes	Effective for categorical data and high-dimensional datasets
Gradient Boosting	Ensemble technique that builds strong learners from weak ones
AdaBoost	Focuses on misclassified instances to improve performance
XGBoost	Optimized boosting, often top performer in structured data ML

All models were evaluated using a standardized pipeline with the following metrics:

Accuracy: Overall correctness

Precision: How many predicted churns were actual churns

Recall (Sensitivity): How many actual churns were detected

F1 Score: Harmonic mean of precision and recall

Confusion Matrix: Visual breakdown of predictions vs actuals

🔬 Data Exploration & Feature Engineering
Our dataset, churn.csv, consists of customer records with demographic, account, and usage information. We performed:

Null Value Handling: Cleaned missing entries and removed unnecessary columns

Encoding Categorical Data: Used label encoding and one-hot encoding

Correlation Analysis: Identified the strongest indicators of churn

Visualization: Used Seaborn and Matplotlib to explore distributions and relationships

Key features impacting churn:
Contract type (Month-to-month contracts churn more)

Tech Support (Lack of tech support increases churn)

Internet Service (Fiber optic users have higher churn risk)

Monthly Charges (Higher bills correlate with churn)

📈 Modeling Strategy
We split the data into training and testing sets (typically 70/30), applied standard scaling, and trained each model. The best-performing models were:

XGBoost – High accuracy and excellent recall

Gradient Boosting – Balanced performance with lower variance

Random Forest – Robust to noise and overfitting

Sample Evaluation (XGBoost):
Accuracy: 82%

Recall: 78%

F1 Score: 80%

Confusion Matrix: Detected most churn cases with low false positives

🔧 Tools and Libraries Used
Tool/Library	Purpose
Python	Core programming language
Pandas, NumPy	Data cleaning, manipulation, transformation
Matplotlib, Seaborn	Data visualization
Scikit-learn	ML algorithms, preprocessing, model evaluation
XGBoost	High-performance gradient boosting model
Jupyter Notebook	Interactive development environment

📊 Business Insights & Takeaways
Contract type and tenure are top churn predictors—month-to-month contracts show high churn risk.

Support services (tech support, online backup) significantly impact retention.

Boosting models (XGBoost, Gradient Boosting) are more reliable for classification tasks in imbalanced datasets like churn.

These insights can inform targeted retention strategies, such as:

Offering incentives for long-term contracts

Bundling support services to enhance satisfaction

Alerting account managers when high-risk customers are detected

🚀 Future Enhancements
Deploy the model as a REST API using Flask or FastAPI

Add model explainability using SHAP or LIME

Integrate with a real-time dashboard (Power BI / Streamlit)

Tune hyperparameters using GridSearchCV for optimization

