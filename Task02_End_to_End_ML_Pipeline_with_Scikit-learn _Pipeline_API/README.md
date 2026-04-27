# 📊 Telco Customer Churn Prediction - End-to-End ML Pipeline

### 🎯 Project Objective
The goal of this project is to build a **production-ready machine learning pipeline** to predict customer churn for a telecommunications company. The project focuses on creating a reusable system that automates data preprocessing, model training, and hyperparameter tuning using the Scikit-learn Pipeline API.

---

### 📂 Project Structure
* **`End_to_End_ML_Pipeline.ipynb`**: Jupyter Notebook containing Exploratory Data Analysis (EDA), Data Cleaning, and the Pipeline construction.
* **`telco_churn_production_model.joblib`**: The final, optimized model file exported for deployment.
* **`WA_Fn-UseC_-Telco-Customer-Churn.csv`**: The raw dataset used for training and testing.

---

### 🛠️ Technical Stack
* **Language:** Python
* **Core Libraries:** * `Scikit-learn`: For Pipeline construction, ColumnTransformers, and ML algorithms.
    * `Pandas & NumPy`: For efficient data manipulation and cleaning.
    * `Matplotlib & Seaborn`: For statistical visualizations and outlier detection.
    * `Joblib`: For model serialization and exporting.

---

### ⚙️ Pipeline Architecture

The pipeline is designed to be modular and scalable, consisting of three primary stages:

#### 1. Automated Data Preprocessing
* **Numerical Transformation:** Applied `StandardScaler` to features like `MonthlyCharges` and `tenure` to ensure they are on a comparable scale.
* **Categorical Transformation:** Utilized `OneHotEncoder` to convert text-based features (e.g., Contract, PaymentMethod) into binary numerical format.
* **ColumnTransformer:** Combined both transformations into a single object to prevent data leakage and ensure consistency.

#### 2. Model Training & Optimization
* **Algorithm:** Implemented the `RandomForestClassifier` for its robustness in handling non-linear relationships.
* **Hyperparameter Tuning:** Used `GridSearchCV` to find the optimal settings for `n_estimators`, `max_depth`, and `min_samples_split`, optimizing the model for the **F1-Score**.

#### 3. Production Readiness
* The entire pipeline (including preprocessing and the model) is saved as a `.joblib` file. This allows for seamless integration into web applications (like Streamlit or Flask) without needing to rewrite preprocessing code.

---

### 🚀 Usage

You can load and use the production-ready pipeline with the following code snippet:

```python
import joblib

# Load the saved pipeline
model = joblib.load('telco_churn_production_model.joblib')

# Make predictions on new data
# The pipeline automatically handles the scaling and encoding
predictions = model.predict(X_new)
