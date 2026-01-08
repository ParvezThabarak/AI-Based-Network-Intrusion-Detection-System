# 🛡️ AI-Based Network Intrusion Detection System

This project implements an **AI-Based Network Intrusion Detection System (NIDS)** using **Machine Learning (Random Forest)** and **Generative AI (Groq LLM)**.  
It is developed as an **academic student project** to demonstrate how artificial intelligence can be applied to **cybersecurity threat detection and analysis**.

---

## 📌 Project Overview

Network Intrusion Detection Systems are used to monitor network traffic and identify malicious activities such as **DDoS attacks**, **abnormal packet behavior**, and **suspicious flows**.

In this project:
- A **Random Forest Classifier** is trained on real network traffic data
- The model classifies traffic as **BENIGN** or **ATTACK**
- A **Streamlit dashboard** provides an interactive interface
- **Groq AI (LLM)** is optionally used to generate human-readable explanations for predictions

The project uses a subset of the **CIC-IDS2017 dataset** focused on DDoS traffic.

---

## 🎯 Objectives

- Understand how Machine Learning can detect network intrusions
- Train and evaluate a Random Forest model on real traffic data
- Simulate live packet analysis
- Generate explainable AI insights using an LLM
- Build an interactive cybersecurity dashboard using Streamlit

---

## 🧠 Technologies Used

- **Python 3**
- **Streamlit** – Web dashboard
- **Pandas & NumPy** – Data processing
- **Scikit-learn** – Machine Learning
- **Groq API (LLM)** – AI explanations (optional)
- **CIC-IDS2017 Dataset** – Network traffic data

---


### File Description

- **app.py**  
  Main Streamlit application containing data loading, model training, prediction, and Groq AI integration.

- **Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv**  
  Dataset file (CIC-IDS2017 DDoS traffic subset).

- **requirements.txt**  
  List of Python libraries required to run the project.

- **README.md**  
  Project documentation.

---

## ⚙️ System Workflow

### 1️⃣ Dataset Loading
- The CSV dataset is loaded automatically
- Missing and infinite values are removed
- Columns are cleaned for consistency

### 2️⃣ Model Training
- Selected network flow features are used
- A **Random Forest Classifier** is trained
- Model accuracy is calculated and displayed

### 3️⃣ Traffic Simulation
- A random packet is selected from the test dataset
- The model predicts whether the packet is **BENIGN** or an **ATTACK**

### 4️⃣ AI Explanation (Optional)
- If a **Groq API key** is provided:
  - Packet data is sent to the Groq LLM
  - The AI explains why the traffic appears normal or malicious
  - If no API key is provided, detection still works normally

---

## 🚀 How to Run the Project

### 1️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
### 2️⃣ Run the Application
```bash
streamlit run app.py
```
### 3️⃣ Open in Browser
```bash
http://localhost:8501
```
## 🔑 Groq API Key (Optional)
Used only for AI-generated explanations

Detection works without the API key

Free API keys can be obtained from:
https://console.groq.com/keys

Paste the key into the sidebar input field in the application.

## 🚀 How to Use
1. **Enter API Key:** Paste your Grok API key in the sidebar (optional, for AI explanations).
2. **Train Model:** Click the "Train AI Model" button. The system loads the `Friday-WorkingHours...` dataset automatically.
3. **Simulate:** Click "Simulate Random Packet" to pick a real network packet from the test set.
4. **Analyze:** See if the model flags it as **BENIGN** or **DDoS**, and ask Grok to explain why.

## 📊 Features & Output

Machine Learning based intrusion detection

Real dataset (CIC-IDS2017) usage

Accuracy score after training

Random packet simulation

BENIGN vs ATTACK classification

Explainable AI using Groq LLM

Interactive Streamlit dashboard

## 🎓 Academic Disclaimer

This project is developed strictly for educational purposes.
It demonstrates the integration of traditional machine learning and large language models in cybersecurity.

It is not intended for real-world production deployment.

## 📌 Conclusion

This project successfully demonstrates:

Practical application of AI in network security

Detection of malicious network traffic using ML

Explainable AI for security analysis

End-to-end AI-powered cybersecurity workflow
