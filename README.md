# 💳 Fraud Detection System
A machine learning project focused on detecting fraudulent financial transactions using engineered features and traditional classification models. This system helps in identifying suspicious patterns in large volumes of transactions, reducing the risk of financial loss.

🧾<b> Project Objective</b>
<br>The goal is to build a reliable fraud detection system that can:<br>
Accurately classify transactions as fraudulent or genuine.<br>
Minimize false positives (flagging a normal transaction as fraud).<br>
Improve recall, especially for the rare fraud cases, by using engineered features that reveal hidden patterns.<br>
This project simulates a real-world financial fraud scenario using synthetic data that closely mimics actual banking transaction behavior.

<b>📁 Dataset Description:</b>
<br>The dataset contains millions of transactions, each represented by multiple features. Below are the original columns in the dataset:<br>
<b>step:</b> Time step in hours since the beginning of data collection.<br>
<b>type:</b> Type of transaction (e.g., TRANSFER, CASH_OUT).<br>
<b>amount:</b> Transaction amount.<br>
<b>nameOrig:</b> ID of the transaction initiator.<br>
<b>oldbalanceOrg:</b> Sender’s account balance before the transaction.<br>
<b>newbalanceOrig:</b> Sender’s balance after the transaction.<br>
<b>nameDest:</b> ID of the transaction recipient.<br>
<b>oldbalanceDest:</b> Recipient’s account balance before the transaction.<br>
<b>newbalanceDest:</b> Recipient’s balance after the transaction.<br>
<b>isFraud:</b> 1 if the transaction is fraudulent, otherwise 0.<br>
<b>isFlaggedFraud:</b> 1 if the system flagged it, regardless of whether it was actually fraud.

🧠 <b>Feature Engineering:</b>
<br>To enhance the model’s performance, the following derived features were added:<br>
<b>balance_change_orig:</b> Change in the sender’s account balance.<br>
<b>balance_change_dest:</b> Change in the recipient’s account balance.<br>
<b>is_nonzero_oldbalance_orig:</b> Whether the sender had funds before the transaction (binary).<br>
<b>is_nonzero_oldbalance_dest:</b> Whether the recipient had funds before the transaction (binary).<br>
<b>hour:</b> Extracted hour from the time step (step % 24), to capture time-based patterns in fraud.<br>
These features help highlight unusual activity — for example, sending money from an empty account, or receiving funds into an account that had no previous activity.

📊 <b>Model Training & Evaluation</b>
<br>Machine learning algorithms used:
<br>Models are trained using train-test split or cross-validation, depending on configuration.

<b>Evaluation Metrics:</b>
<br>Because fraud cases are rare, we focus on metrics suited for imbalanced classification:<br>
<b>Precision:</b> How many flagged frauds are actually fraud.<br>
<b>Recall:</b> How many actual frauds are detected.
<b>F1-Score:</b> Balance between precision and recall.
<b>ROC-AUC:</b> How well the model distinguishes between fraud and non-fraud.

🔍<b> Challenges Addressed:</b>
<br>Class imbalance: Fraud cases make up a very small percentage of total transactions.
<b>Feature leakage:</b> Ensured no future information was used for prediction.
<b>Scalability:</b> Optimized the code for working with large datasets.

🛠 <b>Technologies Used:</b>
<br>Python 3.10+<br>
Pandas, NumPy<br>
scikit-learn<br>
logistic regression<br>
Matplotlib, Seaborn<br>
Jupyter Notebook for data exploration

📌 <b>Project Highlights:</b>
<br>Accurate fraud detection using simple and interpretable features.<br>
Clear preprocessing and feature engineering steps.<br>
Designed to scale for large datasets in financial systems.<br>
Easily extendable to include deep learning or real-time fraud detection.

🧠<b> Key Learnings:</b>
<br>How to deal with imbalanced datasets in classification problems<br>
The importance of feature engineering in structured data<br>
Evaluating models beyond just accuracy (e.g., F1, ROC-AUC)<br>
Making machine learning pipelines scalable and modular<br>
Translating business rules into features and model logic

📌<b> Use Cases:</b>
<br>This type of fraud detection system can be adapted for:<br>
Online banking platforms<br>
E-commerce payment gateways<br>
Mobile money transfer systems<br>

Credit card fraud monitoring

