# ❤️ Coronary Heart Disease Prediction

A **Machine Learning-based web application** that predicts the risk of **Coronary Heart Disease (CHD)** using patient health and lifestyle information.

The application is built using **Python, Scikit-learn, Pandas, NumPy, and Streamlit** and provides an interactive interface where users can enter patient details and receive a predicted CHD risk probability.

---

## 📌 Project Overview

Coronary Heart Disease is one of the major cardiovascular conditions worldwide. Early identification of potential risk factors can help in better health monitoring and decision-making.

This project uses a trained **Logistic Regression model** to estimate the probability of CHD based on various patient characteristics such as:

* Age
* Gender
* Education level
* Smoking status
* Cigarettes consumed per day
* Blood pressure medication
* Previous stroke
* Hypertension
* Diabetes
* Total cholesterol
* Systolic blood pressure
* Diastolic blood pressure
* BMI
* Heart rate
* Glucose level

The trained model and scaler are loaded into a Streamlit application to generate predictions for new patient data.

---

## 🎯 Objectives

* Build a machine learning model for CHD risk prediction.
* Process and scale patient health data.
* Create an interactive web interface using Streamlit.
* Predict the probability of Coronary Heart Disease.
* Present the prediction in a simple and understandable format.

---

## 🛠️ Technologies Used

| Technology   | Purpose                          |
| ------------ | -------------------------------- |
| Python       | Programming language             |
| Pandas       | Data manipulation                |
| NumPy        | Numerical operations             |
| Scikit-learn | Machine learning                 |
| Streamlit    | Web application                  |
| Pickle       | Saving and loading trained model |
| Git & GitHub | Version control                  |

---

## 🤖 Machine Learning Model

The project uses **Logistic Regression** for binary classification.

The model predicts two possible outcomes:

```text
0 → Low Risk
1 → High Risk
```

In addition to the class prediction, the model calculates the probability of CHD using:

```python
model.predict_proba()
```

The probability is displayed as a percentage in the Streamlit application.

---

## 🔄 Project Workflow

```text
Patient Data
     ↓
Data Preprocessing
     ↓
Feature Scaling
     ↓
Trained Logistic Regression Model
     ↓
Prediction
     ↓
CHD Risk Probability
     ↓
Streamlit Web Application
```

---

## 📊 Input Features

The application accepts the following features:

| Feature            | Description                             |
| ------------------ | --------------------------------------- |
| Gender             | Female / Male                           |
| Age                | Patient's age                           |
| Education          | Education level from 1–4                |
| Current Smoker     | Current smoking status                  |
| Cigarettes Per Day | Number of cigarettes consumed daily     |
| BP Medication      | Whether the patient takes BP medication |
| Previous Stroke    | History of stroke                       |
| Hypertension       | Presence of hypertension                |
| Diabetes           | Presence of diabetes                    |
| Total Cholesterol  | Total cholesterol level                 |
| Systolic BP        | Systolic blood pressure                 |
| Diastolic BP       | Diastolic blood pressure                |
| BMI                | Body Mass Index                         |
| Heart Rate         | Heart rate in BPM                       |
| Glucose            | Blood glucose level                     |

---

## 📁 Project Structure

```text
CHD-Prediction/
│
├── app.py
├── log_CHD_model.pkl
├── scaler_log.pkl
├── requirements.txt
├── README.md
└── dataset/
    └── heart_data.csv
```

> File names can be changed according to your actual project structure.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/CHD-Prediction.git
```

### 2. Navigate to the Project Folder

```bash
cd CHD-Prediction
```

### 3. Create a Virtual Environment

```bash
python -m venv venv
```

### 4. Activate the Environment

**Windows:**

```bash
venv\Scripts\activate
```

**Mac/Linux:**

```bash
source venv/bin/activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Application

Run the following command:

```bash
streamlit run app.py
```

The application will open in your browser.

Usually, Streamlit runs at:

```text
http://localhost:8501
```

---

## 🖥️ Application Features

### 👤 Patient Information

Users can enter basic demographic information such as:

* Gender
* Age
* Education level

### 🚬 Lifestyle Information

Users can provide:

* Smoking status
* Cigarettes per day
* Diabetes status

### 🏥 Medical History

The application collects:

* BP medication status
* Previous stroke
* Hypertension

### 🩺 Health Measurements

Users can enter:

* Total cholesterol
* Systolic BP
* Diastolic BP
* BMI
* Heart rate
* Glucose

### 📊 Prediction Result

After clicking **Predict CHD Risk**, the application displays:

* Predicted risk category
* Estimated CHD probability
* Risk progress bar
* Patient information summary

---

## 📈 Example Prediction

Example output:

```text
Prediction Result

⚠️ HIGH RISK

Estimated CHD Risk

63.42%
```

The application also provides a simple interpretation of the estimated probability.

---

## 🧠 Why Feature Scaling?

The input features have different numerical ranges.

For example:

```text
Age              → 18–100
Cholesterol      → 100–700
BMI              → 10–70
Heart Rate       → 30–200
Glucose          → 40–500
```

Feature scaling helps bring numerical features to a comparable scale before passing them to the trained Logistic Regression model.

The same scaler used during model training is loaded using:

```python
with open('scaler_log.pkl', 'rb') as f:
    scaler = pickle.load(f)
```

The new patient data is then transformed using:

```python
input_scaled = scaler.transform(input_data)
```

---

## 🔐 Model and Scaler

The project uses two saved files:

### `log_CHD_model.pkl`

Contains the trained Logistic Regression model.

### `scaler_log.pkl`

Contains the feature scaler used during model training.

Both files are loaded when the Streamlit application starts.

---

## ⚠️ Disclaimer

This project is intended for **educational and demonstration purposes only**.

The prediction generated by this application should **not be considered a medical diagnosis or a substitute for professional medical advice**.

For actual medical decisions, patients should consult a qualified healthcare professional.

---

## 🚀 Future Improvements

Possible improvements include:

* Improve model accuracy through hyperparameter tuning.
* Compare Logistic Regression with Random Forest, XGBoost, and other models.
* Add model evaluation metrics.
* Add ROC-AUC visualization.
* Add confusion matrix visualization.
* Improve feature engineering.
* Add explainable AI techniques such as SHAP.
* Deploy the application online.
* Add authentication and secure patient-data handling.
* Add downloadable prediction reports.

---

## 👨‍💻 Author

**Tejashwini Dharani**

Machine Learning / Python Project

---

## ⭐ Acknowledgement

This project was developed as a Machine Learning and Streamlit application for predicting Coronary Heart Disease risk based on patient health information.

If you found this project useful, consider giving the repository a ⭐ on GitHub.
