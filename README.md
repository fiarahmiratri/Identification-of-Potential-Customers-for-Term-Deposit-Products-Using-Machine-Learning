# Identification-of-Potential-Customers-for-Term-Deposit-Products-Using-Machine-Learning
Predicting potential term deposit customers using LightGBM with business-driven threshold optimization.


📌 Identification of Potential Customers for Term Deposit Products Using Machine Learning
📖 Project Overview

This project aims to identify potential customers who are likely to subscribe to a term deposit product in a bank marketing campaign.

Instead of focusing solely on accuracy, this project emphasizes business-driven model evaluation, incorporating campaign cost and potential revenue to determine the optimal classification threshold.

The objective is to maximize campaign profit rather than traditional machine learning metrics.

🎯 Business Problem

Banks spend significant resources on marketing campaigns. Offering a term deposit product to all customers may:

Increase operational cost

Reduce campaign efficiency

However, failing to offer to potential customers leads to lost revenue.

Key question:

Should the bank target all customers or use machine learning to optimize campaign efficiency?

💰 Business Assumptions

For simulation purposes:

Campaign Cost per Customer: Rp100,000

Revenue per Successful Deposit: Rp500,000

False Negative (missed potential depositor) is 5x more expensive than False Positive

This cost ratio heavily influences threshold optimization.

🛠 Methodology
1. Data Preprocessing

Handling categorical and numerical features

Encoding & scaling

Pipeline integration

2. Model Training

Models evaluated:

Logistic Regression

KNN

Decision Tree

Random Forest

XGBoost

LightGBM (Best performing model)

3. Hyperparameter Tuning

LightGBM tuned using cross-validation.

4. Threshold Optimization

Instead of using default threshold (0.5), multiple thresholds were evaluated:

0.15

0.30

0.50

Evaluation metric shifted from accuracy to expected profit.

📊 Key Results
Default Threshold (0.5)

High precision

Lower recall

Significant potential revenue loss

Threshold 0.15

Very high recall (98%)

Almost all customers targeted

Similar to offering to everyone

Threshold 0.30 (Balanced Strategy)

Recall: 86%

Reduced campaign cost

Slightly higher net profit compared to no-model strategy

💡 Business Insight

When campaign cost is significantly lower than potential revenue:

Optimizing for recall is more important than precision.

Cost-sensitive threshold adjustment improves profitability.

Machine learning should be evaluated using financial metrics, not only accuracy.

📈 Conclusion

Using LightGBM with threshold optimization provides:

Improved campaign efficiency

Controlled marketing cost

Data-driven targeting strategy

However, if campaign cost is relatively low, offering to all customers may yield similar profit.

Final recommendation depends on:

Operational capacity

Campaign budget

Cost-revenue ratio

🚀 Tech Stack

Python

Pandas

Scikit-learn

LightGBM

Matplotlib / Seaborn

📂 Project Structure
├── data/
├── notebook/
├── models/
├── README.md
👩‍💻 Author

Luthfia Rahmiratri
Machine Learning & Business Analytics Enthusiast
