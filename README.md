# Salary Prediction Using Explainable AI

A full-stack Machine Learning web application that predicts salaries based on factors such as experience, education, and job title, while using Explainable AI (XAI) to show why the model made a particular prediction.

## 📌 Project Overview

Salary prediction systems can provide estimated salaries, but many Machine Learning models work like a "black box" and do not explain how the prediction was made.

This project addresses this problem by combining Machine Learning with Explainable AI. The application predicts a user's expected salary and provides visual explanations showing how individual features contribute to the final prediction.

## 🎯 Objectives

- Predict salary based on user-provided information.
- Provide transparent explanations for salary predictions.
- Show how features such as experience, education, and job title affect the prediction.
- Provide model performance metrics.
- Build an interactive web application using a full-stack architecture.

## ✨ Key Features

- Salary Prediction based on user inputs.
- Explainable AI using SHAP values.
- SHAP Waterfall Charts showing feature contributions.
- Interactive visualizations.
- Model performance metrics including R², MAE, and RMSE.
- Streamlit frontend connected to a FastAPI backend.
- Real-time salary prediction based on user-provided information.

## 🧠 Machine Learning Model

The project uses **Linear Regression** for salary prediction.

Linear Regression was selected because it provides an interpretable approach for predicting continuous values such as salary.

### Data Processing

Categorical features are processed using:

- Column Transformer
- One-Hot Encoding

The dataset is divided into:

- 80% Training Data
- 20% Testing Data

A fixed random seed is used for reproducibility.

## 🔍 Explainable AI

The project uses **SHAP (SHapley Additive exPlanations)** to explain the model's predictions.

The explanation starts from a baseline salary and shows how individual features contribute to the final predicted salary.

For example:

Base Salary  
↓  
Experience Contribution  
↓  
Education Contribution  
↓  
Job Title Contribution  
↓  
Final Predicted Salary

### SHAP Waterfall Chart

The SHAP Waterfall visualization helps users understand which features increase or decrease the predicted salary and by how much.

## 🏗️ System Architecture

The application follows a client-server architecture.

User Input  
↓  
Streamlit Frontend  
↓  
REST API Request  
↓  
FastAPI Backend  
↓  
Data Preprocessing  
↓  
Linear Regression Model  
↓  
Salary Prediction  
↓  
SHAP Explanation  
↓  
Results and Visualizations  
↓  
Streamlit Frontend

## 🛠️ Technologies Used

### Machine Learning and Data Processing

- Python
- Scikit-learn
- Pandas
- SHAP

### Backend

- FastAPI
- Uvicorn
- Requests

### Frontend and Visualization

- Streamlit
- Matplotlib

## 📊 Model Performance

The model achieved the following performance:

| Metric | Result |
|---|---:|
| R² Score | 0.9918 |
| MAE | ~$3,338 |
| RMSE | ~$4,168 |

The R² score indicates that the model explains approximately **99.1% of the variance** in the salary data.

## 🚀 Applications

This system can be useful for:

- Career guidance for students and professionals.
- Salary benchmarking for HR departments.
- Educational demonstrations of Machine Learning and Explainable AI.
- Workforce planning and decision-support systems.

## 🔮 Future Enhancements

Future improvements could include:

- Integration of advanced models such as Random Forest and XGBoost.
- Use of larger and real-time salary datasets.
- Cloud deployment using AWS or Azure.
- User authentication and profile-based predictions.
- Region-specific salary estimation.


## 📌 Conclusion

This project demonstrates how Machine Learning and Explainable AI can be combined to build a transparent salary prediction system.

By using SHAP-based explanations, the application not only predicts a salary but also helps users understand **why the model arrived at that prediction**.
