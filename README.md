# Ransomware-Detection-System
Final year project: A system to detect ransomware activity using behavioral analysis

# 🛡️ Ransomware Detection System using Deep Learning (LSTM)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Django](https://img.shields.io/badge/Django-Web%20App-092E20)
![Deep Learning](https://img.shields.io/badge/Model-LSTM-orange)
![Security](https://img.shields.io/badge/Domain-Cybersecurity-red)
![Accuracy](https://img.shields.io/badge/Accuracy-~90%25-brightgreen)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

A deep learning-based web application that detects ransomware 
activity using behavioral analysis with a two-stage LSTM 
classification system — identifies not just whether a file is 
ransomware, but which family it belongs to, and provides 
targeted prevention advice.

---

## 🔍 Overview

Traditional antivirus software uses signature-based detection, 
which fails against new or modified ransomware variants. This 
system uses an LSTM (Long Short-Term Memory) neural network to 
learn **behavioral patterns** from dynamic analysis data — making 
it effective even against previously unseen ransomware.

---

## ⚙️ Two-Stage Detection System

### Stage 1 — Binary Classification
> Is this file **ransomware** or **goodware (safe)**?
The model outputs a yes/no decision for each uploaded sample.

### Stage 2 — Family Classification
> If ransomware, **which family** does it belong to?
Classifies across **12 ransomware families**:
`CryptoLocker` `TeslaCrypt` `Reveton` `CryptoWall` `MATSNU` 
`Kovter` `Locker` `Critroni` `Trojan-Ransom` and more.

---

## ✨ Features

- 🔐 **Login module** — secure authentication before system access
- 📂 **Data Upload** — upload CSV files directly via browser
- 🧠 **Model Creation** — view LSTM architecture and summary
- 🔎 **Ransomware Predict** — binary classification on uploaded data
- 👪 **Family Predict** — identifies specific ransomware family
- 🛡️ **Prevention Module** — gives targeted prevention advice per family
- 📊 **Visualization** — accuracy graphs and loss curves via Matplotlib

---

## 🧠 Model Architecture

| Model | Activation | Loss Function |
|-------|-----------|---------------|
| Binary Classifier | Sigmoid | Binary Cross-Entropy |
| Family Classifier | Softmax | Categorical Cross-Entropy |
| Optimizer | Adam | — |

---

## 📊 Results

| Metric | Value |
|--------|-------|
| Training & Validation Accuracy | ~90% (after 30 epochs) |
| Unit Tests Passed | 10/10 ✅ |
| Integration Tests Passed | 10/10 ✅ |
| System Tests Passed | 10/10 ✅ |

---

## 🔄 Data Pipeline

1. Input CSV with behavioral features (API calls, file system 
   events, registry accesses, entropy levels)
2. Features normalized using **StandardScaler** (zero mean, 
   unit variance)
3. Data reshaped into 3D tensors `[samples, timesteps, features]` 
   for LSTM input
4. Predictions returned with family label + prevention advice

---

## 🆚 Why This Is Better Than Existing Systems

| Existing Systems | This System |
|-----------------|-------------|
| Signature-based, fails on new variants | Learns behavioral patterns, generalizes |
| No web interface, needs technical users | Django web app, usable by anyone |
| Only detects malware, no guidance | Detects + identifies family + gives prevention advice |
| Manual preprocessing required | Fully automated pipeline |

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Backend | Python, Django |
| Frontend | HTML, CSS |
| Deep Learning | LSTM (Keras/TensorFlow) |
| Preprocessing | StandardScaler (scikit-learn) |
| Visualization | Matplotlib |
| Input Format | CSV (behavioral features) |

---

## 🚀 How to Run

1. **Clone the repository**
```bash
   git clone https://github.com/Jeevika-hub/Ransomware-Detection-System.git
   cd Ransomware-Detection-System
```

2. **Install dependencies**
```bash
   pip install -r requirements.txt
```

3. **Run the Django app**
```bash
   python manage.py runserver
```

4. **Open in browser**
5. http://localhost:8000

6. ## 📁 Project Structure
Ransomware-Detection-System/
├── Good_or_Ransomware_model_data/  # Train/test CSV datasets
├── model/                          # Trained LSTM models
├── myapp/                          # Django app & HTML templates
├── ransomeware/                    # Core detection logic
└── README.md

---

## 🔮 Future Improvements

- Attention mechanisms to highlight important behavioral features
- Transformer-based architectures for improved accuracy
- SHAP/LIME integration for model explainability
- Federated learning for privacy-preserving training
- Real-time monitoring of live systems

---

## 🎓 Academic Context

> **Final Year Project** — B.E./B.Tech in Computer Science  
> **Domain:** Cybersecurity | Deep Learning | Threat Detection  
> **Model:** LSTM-based Sequential Behavioral Analysis

---

## 👩‍💻 Author

**Jeevika** — [GitHub Profile](https://github.com/Jeevika-hub)
