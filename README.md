[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JipkpgEHOkEoybPXGLBUO_ADa7oEy1Ts)

# 🕵️‍♂️ Detecting Fraudulent Job Postings

**Project Title:** Fraud Detection in Job Postings Using Hybrid NLP Architectures with Structured Metadata Integration

**Team:** Kai Park, Mazen Moustafa, Gregori Moreira, Evana Matulula, Angie Sanchez

---

## 📌 Overview

Online job portals face increasing fraudulent postings, compromising user safety and platform integrity. Traditional approaches focus solely on unstructured text, often ignoring valuable metadata such as salary, location, or telecommuting flags. Our goal was to build a hybrid model that integrates:

* 🔤 Context-sensitive BERT-based text embeddings
* 📊 Structured metadata (e.g., salary, company logo, employment type)

This project achieved improved detection accuracy and robustness across class imbalance.

---

## 📁 Folder Structure

```
├── assets/                  # Screenshots & architecture visualizations
│   ├── acc plot.png
│   ├── loss plot.png
│   ├── confusion matrix.png
│   ├── Model Architecture.png
│   ├── fake wordcloud.png
│   └── real wordcloud.png
├── eda.ipynb               # Exploratory data analysis notebook
├── model.ipynb             # BERT + LSTM hybrid model implementation
├── README.md               # Project documentation (this file)
```

---

## 🧪 Dataset

* **Source**: [Kaggle Job Posts Dataset](https://www.kaggle.com/datasets/shivamb/real-or-fake-fake-jobposting-prediction)
* **Features**: Title, Description, Company Profile, Salary, Telecommuting, etc.
* **Problem**: Highly imbalanced classes (Real vs. Fake)

⚠️ Note: Dataset not uploaded due to size. Please download from Kaggle manually.

---

## 🧼 Data Preprocessing

* Missing value handling (imputation / dropping)
* Lowercasing & punctuation removal
* Tokenization & padding for BERT
* Class imbalance handled via:

  * Undersampling majority class
  * Synonym replacement (via `eda-python`)

---

## 🔍 Exploratory Data Analysis

* Word Clouds: Visualize common terms in fake vs. real jobs
* Metadata Correlation: Weak correlation with individual structured features, but combined they provide additive value

---

## 🧠 Model Architecture

* BERT for text embedding
* LSTM layer to capture sequence context
* Concatenation with structured metadata
* Dense layers for final binary classification

---

## 🏋️ Training Strategy

* **Loss**: Binary Crossentropy
* **Optimizer**: Adam
* **Evaluation**: Accuracy, Precision, Recall, F1-score, AUC-ROC

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

## 📌 Results

* **7% increase in F1-score** over BERT-only baseline
* **Improved robustness** to class imbalance
* **Additive value from metadata** like salary & telecommuting flag

---

## 🚀 Future Work

* Try advanced transformer variants (RoBERTa, DistilBERT, JobBERT)
* Real-time API deployment
* Investigate SHAP/LIME for model explainability

---

## 🤝 Contact

For any queries or collaboration:

* 📧 [mazen110.net@gmail.com](mailto:mazen110.net@gmail.com)
* 💼 [LinkedIn](https://www.linkedin.com/in/mazen-abdel-tawwab/)

---

> "Fake job posts are everywhere … we're here to change that."
> — *AI Sleuths for the Job Truths*
