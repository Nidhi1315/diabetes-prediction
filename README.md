# 🩺 Diabetes Prediction using Machine Learning

A machine learning project that predicts whether a person is diabetic or not based on diagnostic health measurements, using the **PIMA Indians Diabetes Dataset** and a **Support Vector Machine (SVM)** classifier.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Project Workflow](#project-workflow)
- [Model Performance](#model-performance)
- [How to Run](#how-to-run)
- [Sample Prediction](#sample-prediction)

---

## 📌 Overview

This project builds a binary classification model to predict diabetes. Given a set of medical input features, the model outputs whether the person is **diabetic** or **not diabetic**.

---

## 📊 Dataset

- **Name:** PIMA Indians Diabetes Dataset
- **File:** `diabetes.csv`
- **Features (8 input variables):**

| Feature | Description |
|---|---|
| Pregnancies | Number of times pregnant |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure (mm Hg) |
| SkinThickness | Triceps skin fold thickness (mm) |
| Insulin | 2-Hour serum insulin (mu U/ml) |
| BMI | Body mass index |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age in years |

- **Target:** `Outcome` — `0` (Not Diabetic), `1` (Diabetic)

---

## 🛠️ Tech Stack

- Python 3
- NumPy
- Pandas
- Scikit-learn (SVM, StandardScaler, train_test_split, accuracy_score)
- Google Colab / Jupyter Notebook

---

## 🔄 Project Workflow

1. **Import Dependencies** — NumPy, Pandas, Scikit-learn
2. **Load Dataset** — Read `diabetes.csv` into a Pandas DataFrame
3. **Exploratory Data Analysis** — Shape, statistics, value counts
4. **Data Preprocessing** — Separate features (`X`) and labels (`Y`); apply `StandardScaler`
5. **Train-Test Split** — 80% training / 20% testing (`stratify=Y`)
6. **Model Training** — SVM with linear kernel
7. **Model Evaluation** — Accuracy score on training and test sets
8. **Predictive System** — Input custom data to get a prediction

---

## 📈 Model Performance

| Dataset | Accuracy |
|---|---|
| Training Data | ~78.66% |
| Test Data | ~77.27% |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/diabetes-prediction.git
   cd diabetes-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install numpy pandas scikit-learn
   ```

3. **Add the dataset**
   Place `diabetes.csv` in the project root directory (or update the path in the notebook).

4. **Run the notebook**
   Open `Project_Diabetes_Prediction.ipynb` in Jupyter Notebook or Google Colab and run all cells.

---

## 🔍 Sample Prediction

```python
import numpy as np

input_data = np.array([5, 166, 72, 19, 175, 25.8, 0.587, 51])
input_data_reshaped = input_data.reshape(1, -1)
std_data = scaler.transform(input_data_reshaped)

prediction = classifier.predict(std_data)

if prediction[0] == 0:
    print("The person is not diabetic")
else:
    print("The person is diabetic")
```

**Output:** `The person is diabetic`

---

## 📁 Project Structure

```
diabetes-prediction/
│
├── diabetes.csv                        # Dataset
├── Project_Diabetes_Prediction.ipynb   # Main notebook
└── README.md                           # Project documentation
```

---

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you'd like to change.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
