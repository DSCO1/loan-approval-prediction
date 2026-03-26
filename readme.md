📊 Loan Subscription Prediction using Machine Learning

🚀 Project Overview
Loan subscription prediction is a crucial problem in the banking sector, where identifying potential customers can significantly improve marketing efficiency and business revenue.

In this project, we build a Machine Learning classification model that predicts whether a customer will subscribe to a term deposit based on their personal details, financial information, and previous marketing interactions.

By predicting customer behavior in advance, banks can optimize their marketing campaigns, reduce unnecessary calls, and improve conversion rates.

---

🎯 Objective
The primary objective of this project is:

* To predict whether a customer will subscribe to a term deposit (Yes / No)
* To analyze customer behavior patterns
* To improve identification of potential customers
* To align model performance with business goals

---

🧠 Machine Learning Type

* Supervised Learning
* Classification Problem

---

📁 Dataset Description
The dataset used is the **Bank Marketing Dataset** containing ~41,188 records.

It includes features such as:

* Demographics (age, job, marital status, education)
* Financial details (housing loan, personal loan, default)
* Marketing information (contact type, month, campaign)
* Previous interaction details (pdays, previous, poutcome)
* Target variable (`y` → subscription Yes/No)

---

🔧 Data Preprocessing & Cleaning
The following steps were performed:

* Converted target variable (`yes/no → 1/0`)
* Handled categorical variables using One-Hot Encoding
* Checked for missing values
* Ensured dataset consistency and correctness

---

⚙️ Feature Engineering

* Applied One-Hot Encoding using `pd.get_dummies()`
* Used `drop_first=True` to avoid multicollinearity
* Ensured all features are numeric
* Applied StandardScaler for feature scaling

---

📊 Exploratory Data Analysis (EDA)

Key observations:

* 📞 Call duration strongly influences subscription
* 📉 High campaign frequency reduces success rate
* 🎓 Higher education increases probability of subscription
* ⚠️ Dataset is imbalanced (more “No” than “Yes”)

---

📊 Model Building

We trained and evaluated multiple models:

🔹 Logistic Regression ✅

* Baseline model
* Improved using class balancing
* Best performance for minority class

🔹 Decision Tree

* Captures non-linear relationships
* Lower recall for positive class

🔹 Random Forest

* High accuracy
* Poor recall for actual subscribers

---

⚖️ Handling Class Imbalance

* Observed strong imbalance in dataset
* Applied:

  * `class_weight = 'balanced'`
* Improved recall significantly

---

🔥 Final Model — Logistic Regression

Reason for selection:

* Best recall for identifying actual customers
* Aligns with business objective
* More reliable for imbalanced dataset

---

📈 Model Evaluation

Metrics used:

* Accuracy
* Confusion Matrix
* Precision
* Recall
* F1-Score

---

📊 Final Performance

| Metric          | Value       |
| --------------- | ----------- |
| Accuracy        | ~86%        |
| Precision (Yes) | ~45%        |
| Recall (Yes)    | **~90% 🔥** |
| F1 Score        | ~60%        |

---

🧠 Key Insights

* Accuracy alone is misleading for imbalanced data
* Recall is the most important metric for this problem
* Logistic Regression outperformed complex models in business terms
* Feature scaling improved model stability

---

🏆 Business Impact

This model can help banks:

* Identify potential customers effectively
* Reduce unnecessary marketing costs
* Improve campaign success rate
* Enable data-driven decision making

---

⚠️ Challenges Faced

* Handling imbalanced dataset
* Choosing correct evaluation metric
* Model bias toward majority class
* Feature alignment during prediction

---

💾 Model Saving

The trained model and preprocessing objects were saved using pickle:

* `loan_model.pkl`
* `scaler.pkl`
* `columns.pkl`

---

🔮 Prediction Pipeline

A prediction function was implemented to:

* Accept user input
* Convert it into model-compatible format
* Apply scaling and encoding
* Generate prediction output

---

🛠️ Technologies Used

* Python 🐍
* Pandas
* NumPy
* Scikit-learn
* Matplotlib & Seaborn
* Jupyter Notebook

---


📌 Future Improvements

* Use Pipeline API to avoid feature mismatch
* Hyperparameter tuning
* Try advanced models (XGBoost, LightGBM)
* Deploy using Streamlit
* Improve precision using threshold tuning

---

👨‍💻 Author

Ujjawal Shrivastava
Aspiring Data Scientist | Machine Learning Enthusiast

---

⭐ If you found this project useful, don’t forget to give it a star!
