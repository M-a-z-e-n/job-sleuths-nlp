# Job Sleuths: Detecting Fraudulent Job Postings Using Hybrid NLP Architectures

This project introduces a deep learning-based fraud detection system for job postings. By integrating textual data (via BERT embeddings) with structured metadata (e.g., telecommuting, salary), we improve fraud detection accuracy and robustness.

## 🎯 Objective

Current fraud detection methods often overlook structured metadata and focus solely on job text. We propose a hybrid model that combines:

- **Textual embeddings** from a pre-trained BERT model  
- **Structured features** (e.g., salary, telecommuting, company profile)  
- **LSTM layer** for sequential modeling

---

## 📦 Dataset

- Source: Kaggle Fake Job Postings Dataset  
- Features: Job title, description, benefits, telecommuting flag, salary, company info  
- Task: Binary classification (fraudulent vs legitimate)

---

## 🧹 Preprocessing

- Text cleaning (lowercasing, punctuation removal)
- Tokenization & padding for BERT
- Handling missing values (e.g., imputation)
- Class imbalance mitigation using data augmentation and undersampling

---

## 📊 Exploratory Data Analysis

- Word clouds for real vs fake job descriptions
- Class distribution analysis
- Correlation of structured fields with fraud label

---

## 🧠 Model Architecture

- **Text Encoder**: BERT for contextual word embeddings
- **Structured Input**: Concatenated with BERT output
- **Classifier**: LSTM + Dense layers
- **Loss**: Binary Cross-Entropy  
- **Optimizer**: Adam  
- **Metrics**: Accuracy, Precision, Recall, F1, AUC-ROC

---

## ✅ Preliminary Results

- 7% F1-score increase over BERT-only baseline
- Significant improvement in handling class imbalance
- Metadata features like salary and company profile add predictive value

---

## 🔮 Future Work

- Explore transformer alternatives: Job-BERT, RoBERTa, DistilBERT
- Deploy model via real-time API
- Generalize to other NLP tasks using structured + unstructured data

---

## 👨‍💻 Team

- Kai Park  
- Mazen Moustafa  
- Evana Matulula  
- Angie Sanchez  
- Gregori Moreira  
