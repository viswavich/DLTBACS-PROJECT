# 🧠 Deep Learning Based Access Control System (DLBAC)

This project implements an AI-powered access control system using deep learning in Google Colab. It replaces manual rule-based models like RBAC and ABAC with an intelligent model that learns from user and resource metadata to predict access decisions (Grant or Deny).

---

## 🎯 Objective

To develop an intelligent and automated access control system using deep learning techniques that can predict whether access should be granted or denied, based on user and resource metadata.

---

## ❓ Problem Statement

Traditional access control models like RBAC and ABAC are static and require manual policy creation. They fail to scale in dynamic environments like cloud systems or organizations with changing roles, devices, and contexts. This project addresses the issue by introducing a neural network-based model that learns from historical access data.

---

## 🔧 Project Modules

- **1. Data Collection & Preprocessing:**  
  Collect user and resource metadata, handle null values, encode categorical fields, and normalize data.

- **2. Model Training:**  
  Train a lightweight neural network using Keras with user-resource metadata to predict access.

- **3. Access Prediction Engine:**  
  Takes input (EMP_ID and RESOURCE_ID), fetches metadata, and predicts access (Grant or Deny).

- **4. Explainability Layer (XAI):**  
  Uses SHAP to explain why a decision was made — shows which features influenced the result.

- **5. Adversarial Testing:**  
  Adds noise to inputs to simulate fake access requests and tests if the model can detect them.

- **6. Deployment (optional):**  
  Use Flask or Streamlit to build a simple UI or API for real-time predictions.

---

## 🤖 Neural Network Configuration

- **Input Layer:** Encoded metadata
- **Hidden Layers:** 2 Dense layers (ReLU)
- **Output Layer:** Sigmoid (binary classification)
- **Loss Function:** Binary Crossentropy
- **Optimizer:** Adam
- **Training Split:** 80% training, 20% validation

---

## 📌 Project Features

- Uses employee and resource metadata for prediction
- Lightweight neural network built in Keras
- Real-time access prediction from user input
- Explainable AI (XAI) using SHAP
- Adversarial testing for tamper protection
- Runs fully in Google Colab

---

## 🔧 Technologies Used

- Python 3
- Google Colab (Jupyter Notebook)
- Keras / TensorFlow
- Pandas / NumPy
- SHAP (for explainability)
- Matplotlib / Seaborn

---

## 📁 Dataset Used

A synthetic dataset simulating an IT company's employee access records.

**Sample Columns:**
- `EMP_ID`
- `ROLE`
- `DEPARTMENT`
- `ACCESS_TIME`
- `DEVICE_TRUST`
- `RESOURCE_TYPE`
- `SENSITIVITY_LEVEL`
- `ACCESS_GRANTED` (Label: 0/1)

---

## 📊 Evaluation Metrics

- Accuracy  
- Precision  
- Recall  
- F1-score  
- Confusion Matrix  
- SHAP visual explanations

---

## 🚀 Steps to Run in Google Colab

1. Upload the dataset CSV file to Colab.
2. Run all cells in the notebook (`DLBAC_Colab.ipynb`).
3. The notebook will:
   - Preprocess the data
   - Train a lightweight neural network
   - Predict access for input values
   - Show explanations using SHAP

---

## ✅ Sample Input

```python
emp_id = 1005
resource_id = 203
```

## 🔍 Sample Output

```
Access: GRANTED
Reason: Normal access time, trusted device
```

---

## 📊 Explainability Output

- SHAP visual plots to explain decisions
- Shows most influential features for the result

---

## 🔐 Security Layer

- Adversarial inputs tested by adding random noise
- Ensures the model is resistant to fake or tampered inputs

---

## 🎯 Future Scope

- Add Multi-Factor Authentication (MFA)
- GUI with Streamlit or Flask
- Integration with real-time API systems
- Federated learning for distributed data

---

## 👨‍💻 Developed By

**Project Title:** Deep Learning Techniques Based Access Control System  
**Platform:** Google Colab  
**Tools:** Keras, SHAP, Python  
**Use Case:** Smart, Automated, adaptive access control for organizations
