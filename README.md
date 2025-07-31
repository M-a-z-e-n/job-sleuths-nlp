# 🕵️‍♂️ Detecting Fraudulent Job Postings Using Hybrid NLP Architectures

This project aims to detect fraudulent job advertisements by combining **context-aware text embeddings** with **structured metadata features**, creating a hybrid deep learning architecture for improved accuracy and robustness.

## ✨ Project Highlights

- 📄 Dataset from Kaggle: [Fake Job Postings](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)
- 📚 Hybrid model combining **BERT embeddings** + **LSTM classifier** + **structured metadata**
- 🔍 Performed thorough **EDA** and visualizations
- 🎯 Tackled **class imbalance** using undersampling and data augmentation
- 📈 Achieved significant performance improvement over BERT-only baseline

---

## 🧑‍💻 Team Members

- **Kai Park**
- **Mazen Moustafa Sayem Abdel-tawwab**
- **Gregori Moreira**
- **Evana Matulula**
- **Angie Sanchez**

---

## 🚀 Try it on Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JipkpgEHOkEoybPXGLBUO_ADa7oEy1Ts)

---

## ⚙️ Methodology Overview

1. **Text Preprocessing**  
   - Lowercasing, punctuation removal  
   - Tokenization and padding for BERT  
   - Data augmentation to handle class imbalance

2. **Text Representation**  
   - Used pre-trained **BERT** to obtain embeddings

3. **Model Architecture**  
   - **LSTM** classifier for sequence modeling  
   - Concatenated metadata features (e.g., telecommuting, salary) to BERT outputs

4. **Training**  
   - Loss: Binary Cross-Entropy  
   - Optimizer: Adam  
   - Evaluation: Accuracy, Precision, Recall, F1-Score, AUC-ROC

---

## 📊 Visualizations & Model Insights

### 🧠 Model Architecture
![Model Architecture](assets/Model%20Architecture.png)

---

### ☁️ Word Clouds

**🔴 Fake Job Posts**
![Fake Word Cloud](assets/fake%20wordcloud.png)

**🟢 Real Job Posts**
![Real Word Cloud](assets/real%20wordcloud.png)

---

### 📈 Training Progress

**✅ Accuracy Over Epochs**
![Accuracy Plot](assets/acc%20plot.png)

**📉 Loss Over Epochs**
![Loss Plot](assets/loss%20plot.png)

---

### 📊 Evaluation

**🧾 Confusion Matrix**
![Confusion Matrix](assets/confusion%20matrix.png)

---

## 🔚 Conclusion & Future Work

✅ Integrating structured metadata alongside text representations significantly improves fraud detection performance.  
🔄 Future work includes:

- Experimenting with alternative transformers (e.g., RoBERTa, DistilBERT, JobBERT)
- Real-time deployment via a REST API
- Expanding feature engineering from metadata

> 🧠 Fake job posts are everywhere — we're here to change that.  
> 💼 AI Sleuths for the Job Truths.

---

## 📁 Repository Structure

```bash
.
├── assets/                     # All screenshots and visualizations
├── notebook/                  # Colab notebooks (linked or exported)
├── README.md                  # Project documentation
└── requirements.txt           # (Optional) Dependencies
