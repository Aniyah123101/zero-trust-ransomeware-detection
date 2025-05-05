# 🔐 Ransomware Detection Using Machine Learning (Aligned with Zero Trust Security)

This project applies supervised machine learning techniques to detect **ransomware** and **benign files** based on system behavior patterns. It supports **Zero Trust Architecture (ZTA)** by enabling real-time behavioral monitoring and threat detection to enforce data protection policies.

---

## 👩‍💻 Authors

**Aniyah Hall**  
B.S. in Computer Technology, Health Tech & Cybersecurity  
Bowie State University 

**Dajah Gordon**  
B.S. in Computer Technology  
Bowie State University

---

## 🎯 Objective

To develop machine learning models that detect ransomware activity with high accuracy and low error. This project supports **Zero Trust Security Implementation** by analyzing every file request, validating behavior before granting access, and flagging potential threats.

---

## 🧠 Machine Learning Models Used

| Model                  | Purpose              | Accuracy (Test) | Notes                                      |
|------------------------|----------------------|------------------|---------------------------------------------|
| Random Forest          | Classification       | ~99.7%           | Best-performing model across all metrics    |
| K-Nearest Neighbors    | Classification       | ~99.1%           | Strong performance, low loss                |
| Logistic Regression    | Classification       | ~87.3%           | Moderate performance                        |
| Linear Regression      | Regression (improper)| ~48.3%           | Not suitable for this classification task   |

---

## 🧪 Dataset

- **Features:** Behavioral indicators from file executions
- **Label:** `Benign` (1 = safe, 0 = ransomware)
- **Split:** 80% training, 20% testing
- **Preprocessing:** Feature scaling via `StandardScaler`, irrelevant columns removed

---

## 📊 Outputs

- Accuracy & Loss metrics printed for each model
- Confusion Matrices (for Random Forest) showing true/false positives
- Performance comparison plots (Accuracy/Loss) for all models

---

## 🛡️ Zero Trust Security Integration

This project supports **Zero Trust principles**:
- **"Never trust, always verify"**: Each file is verified with ML before classification
- **Behavioral monitoring**: Models trained on normal vs malicious patterns
- **Access control**: Output can be used to trigger access/block decisions in Zero Trust systems
- **Automated threat response**: Models can integrate into EDR/SIEM platforms

---

## 🖥️ How to Run the Project

### 1. Clone the Repository
```bash
git clone https://github.com/YOURUSERNAME/ransomware-detection-ml.git
cd ransomware-detection-ml

2. Install Dependencies
pip install -r requirements.txt
3. Run the Scripts
➤ Random Forest with Confusion Matrices

python ransomware_detection_random_forest.py
➤ Linear, Logistic, and KNN Model Comparison

python model_comparison_ransomware_detection.py
4. Output
Accuracy and loss printed in terminal
Confusion matrix plotted (Random Forest)
Accuracy/Loss comparison graphs shown for all models
