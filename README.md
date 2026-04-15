Dual Intelligence Fraud Detection System
With Temporal Drift Awareness and Explainable AI

Abstract
A research-level fraud detection system combining Deep Neural Network (DNN) and Autoencoder for dual-intelligence detection. The system incorporates temporal drift awareness, adversarial robustness testing, uncertainty quantification, and bank-style explainable AI

Live Demo
🔗 [Hugging Face Space](https://huggingface.co/spaces/nandinireddybtech24/credit)

Key Results
| Model | Accuracy | ROC-AUC | False Alarms |
|-------|----------|---------|--------------|
| Logistic Regression | 98% | 0.9863 | 880  |
| TabNet | 100% | 0.9705 | 5|
| **DNN + Autoencoder (Ours)| 99% | 0.9121| 509|

 System Architecture
Transaction CSV
↓
StandardScaler
↓
┌─────────────────────────┐
│  DNN (Supervised)       │ → Fraud Probability
│  Autoencoder (Unsup)    │ → Anomaly Score
└─────────────────────────┘
↓
Risk Score = (0.7 × DNN) + (0.3 × Anomaly)
↓
Normal / Suspicious / Fraud
↓
Bank-Style Explanation

Research Contributions
1. Dual Intelligence System — DNN + Autoencoder combined
2. Temporal Drift Awareness — 9.7% AUC drop confirmed
3. Adversarial Robustness — 85% catch rate vs 76% DNN alone
4. Uncertainty Quantification — 3 zone classification
5. Explainable AI — Bank style human readable decisions

Setup Instructions ---
 Option 1 —  open Jupyter Notebook or google collab
1. Open `notebooks/fraud_detection.ipynb` in Google Colab/Jupyter notebook
2. Upload `creditcard.csv` from Kaggle
3. Run all cells in order
4. Launch Gradio UI in last cell

Dataset
- Source: [Kaggle Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- Transactions: 284,807
- Fraud cases: 492 (0.17%)
- Features: Time, V1-V28 (PCA), Amount
- 
TECH STACK 
Python — Core programming language
PyTorch — Deep learning models (DNN + Autoencoder)
Scikit-learn — Preprocessing & baseline models
SHAP — Explainable AI
Gradio — User interface
Hugging Face Spaces — Deployment
