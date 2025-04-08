# Absenteeism Analysis Project

## 📌 Project Overview
This project aims to analyze employee absenteeism patterns using logistic regression. It also introduces a reusable machine learning module that can handle preprocessing, prediction, and data transformation for similar datasets.

The project is divided into two main pipelines:
1. **Detailed Pipeline:** Step-by-step data preprocessing, feature engineering, and machine learning.
2. **Reusable Module Pipeline:** A self-contained Python module for applying the ML model on any similar dataset.

---

## 📁 Project Structure

```bash
Absenteeism Analysis Project
│
├── Absenteeism_data.csv                # Raw data
├── Absenteeism_preprocessed.ipynb      # Preprocessing and feature engineering
├── Absenteeism_preprocessed.csv        # Cleaned dataset
│
├── Absenteeism_logistic_regression.ipynb  # ML model training & evaluation
├── model/                              # Saved logistic regression model
├── scaler/                             # Saved custom scaler object
│
├── Absenteeism_module.ipynb           # Creating reusable module
├── Absenteeism_module.py              # Final Python module
│
├── Absenteeism_new_data.csv           # New data to test the module
├── Absenteeism_module_exercise.ipynb  # Using module on new data
├── Absenteeism_predictions.csv        # Final predictions
│
├── Absenteeism.twb                    # Tableau workbook (basic)
├── Tableau_workbook.twbx              # Tableau packaged workbook
```

---

## ⚙️ Installation & Setup

### Requirements
Make sure to install the following libraries:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

To run the module-based workflow:
```bash
pip install joblib
```

For visualization:
- Tableau Desktop (or Tableau Public)

---

## 🔬 Technical Process

### Part 1: Data Cleaning & Preprocessing
- Handled missing values
- Mapped categorical features (e.g., Reason for Absence)
- Feature scaled numerical columns
- Created new features (e.g., 'Month value', 'Day of the week')

### Part 2: Machine Learning
- Applied logistic regression to predict probability of being absent
- Used feature importance to understand key drivers
- Model & scaler saved using `joblib`

### Part 3: Module Creation
- Converted the pipeline into a reusable module (`Absenteeism_module.py`)
- Can be applied to new data without re-writing ML logic

### Part 4: Module Execution on New Data
- Loaded `Absenteeism_new_data.csv`
- Applied the reusable module
- Created `Absenteeism_predictions.csv` with predicted probabilities

### Part 5: Tableau Visualization
- Visualized insights using the predicted probability data:
  - Age vs Probability
  - Reason for absence vs Probability
  - Transportation expenses and number of children vs Probability

---

## 📊 Business Impact
This project helps HR and management to:
- Identify employees with high risk of frequent absenteeism
- Understand which features (age, distance, reasons, etc.) drive absenteeism
- Take proactive steps in improving employee attendance and well-being

---

## ✅ Usage
To reuse the module:
```python
from Absenteeism_module import AbsenteeismModel
model = AbsenteeismModel()
model.load_and_clean_data('your_data.csv')
model.predict_probabilities()
model.save_predictions('your_output.csv')
```

---

## 🧠 Author
This project was developed as part of a structured machine learning pipeline using Python and Tableau. This is my first project so there may be many impprovements and problems with the project .

