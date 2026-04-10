### Approach
The objective of this project is to predict if a customer will subscribe to a term deposit based on their banking behavior. Since this is a binary classification task (Yes/No), I used the Logistic Regression algorithm to build the predictive model.

### Methodology
I followed these steps to develop the model:
* **Data Loading:** Imported the `bank-full.csv` dataset from Google Drive using `sep=';'`.
* **Data Cleaning:** Converted binary columns like 'y', 'default', 'housing', and 'loan' from yes/no strings to 1/0 numerical values.
* **Encoding:** Used `pd.get_dummies` to transform categorical columns into a numerical format.
* **Train-Test Split:** Divided the data into an 80% training set and a 20% testing set.
* **Scaling:** Applied `StandardScaler` to normalize the numerical features.
* **Training:** Initialized and fitted the Logistic Regression model.

### Findings
* **Accuracy:** The model achieved an accuracy score of [Tomar Result].
* **Results:** The model shows a strong ability to identify customers based on the classification report.
