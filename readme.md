 # Alzheimer's Disease Prediction System

## Overview
This project is a full-stack Alzheimer's disease risk prediction system that combines exploratory data analysis, preprocessing, machine learning model comparison, and a web-based assessment interface. The goal is to help estimate a patient's risk level from structured clinical and lifestyle inputs and present the result in a simple, interpretable format.

The application collects patient information through a guided form, sends the data to a Python prediction script through a Next.js API route, and returns a risk score and category. The system also includes clinical adjustment rules so the final score reflects both model output and important risk factors such as age, family history, memory complaints, and cognitive symptoms.

## Project Objective
The main objective of the project is to support early Alzheimer’s risk screening using machine learning. The system is designed to:

- gather relevant clinical and lifestyle information from a patient
- preprocess the data into a model-ready format
- compare multiple classification models
- select the best-performing model for deployment
- provide a clear risk score and risk category for interpretation

## Technologies Used

### Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- React Hook Form
- React Hot Toast

### Backend and Prediction Layer
- Next.js API routes
- Node.js child process integration
- Python
- Pandas
- NumPy
- joblib
- XGBoost
- scikit-learn

### Development and Analysis
- Jupyter notebooks
- CSV and JSON output files
- model evaluation reports

## Key Features

### 1. Multi-step patient assessment
The app includes a guided clinical form that collects information about:

- personal details
- physical health
- lifestyle factors
- medical history
- cognitive symptoms

### 2. Automatic preprocessing
The input data is transformed into the format required by the trained model. The pipeline handles:

- numeric conversion
- symptom counting
- cognitive decline scoring
- feature selection

### 3. Risk score calculation
The system converts the model probability into a simple risk score on a 0 to 10 scale and classifies the result as low, moderate, or high risk.

### 4. Clinical adjustment rules
The final score is adjusted using clinically relevant factors such as:

- advanced age
- low MMSE score
- family history of Alzheimer's disease
- multiple cardiovascular risks
- high symptom count

### 5. Model comparison
Several machine learning models were trained and evaluated, including:

- Decision Tree
- XGBoost
- Random Forest
- SVM
- Logistic Regression

### 6. Real-time inference
The web app sends data to the API, which launches the Python prediction script and returns the result immediately.

## Model Selection Summary
XGBoost was selected as the final deployment model because it provided a strong balance of accuracy, ROC-AUC, F1-score, cross-validation stability, and prediction speed.

## Results
The project produced a working prediction pipeline with clear outputs, performance reports, and saved model artifacts. The evaluation process showed that XGBoost delivered strong predictive performance and low inference time, making it suitable for deployment.

## Project Workflow

1. Collected and explored the dataset
2. Cleaned and preprocessed the data
3. Engineered features for model training
4. Trained and compared multiple models
5. Selected the best model based on evaluation criteria
6. Built the prediction API
7. Created the front-end assessment form
8. Added risk score interpretation and output display

## Folder Structure

- `app/` - Next.js routes and application pages
- `components/` - Reusable React components
- `api/python/` - Python prediction script and dependencies
- `notebooks/` - EDA, preprocessing, and model training notebooks
- `outputs/` - Saved model artifacts, metrics, reports, and prediction files

## Setup

### Frontend
```bash
npm install
npm run dev
```
<img width="1367" height="952" alt="image" src="https://github.com/user-attachments/assets/1d612dbc-13f7-4718-8ea3-8dc9473de8c0" />
<img width="1211" height="875" alt="image" src="https://github.com/user-attachments/assets/228ff92b-3192-4f72-91bc-aa12dcb3b3f5" />
<img width="1163" height="987" alt="image" src="https://github.com/user-attachments/assets/d91e5d1c-b764-4f3e-a198-c8e2414108be" />
<img width="1193" height="707" alt="image" src="https://github.com/user-attachments/assets/59449c75-ebeb-46a6-a4ab-2b31c9370950" />
<img width="1191" height="990" alt="image" src="https://github.com/user-attachments/assets/dbc7b486-6953-4f63-916a-c67d85bc9393" />
<img width="1196" height="817" alt="image" src="https://github.com/user-attachments/assets/0fb95b5d-7533-4710-8312-77fe61427422" />

### Python Environment
```bash
pip install -r requirements.txt
```

## Disclaimer
This project is intended for educational and research purposes only. It should not replace professional medical advice, diagnosis, or treatment. Any clinical use should be reviewed by qualified healthcare professionals.

