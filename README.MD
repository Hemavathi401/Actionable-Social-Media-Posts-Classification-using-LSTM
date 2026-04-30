# 📌 Actionable Social Media Posts Classification using Deep Learning (LSTM)

## 📖 Overview

This project is a **binary text classification** learning project that predicts whether a social media post is:

- **Actionable (1):** Requires attention, support, complaint handling, refund check, issue resolution, etc.
- **Non-Actionable (0):** General praise, casual comments, neutral opinions, compliments, etc.

### 🔍 What is LSTM?

**LSTM (Long Short-Term Memory)** is a type of Recurrent Neural Network (RNN) designed to learn from sequential data by remembering important past information and ignoring irrelevant details.

Unlike basic RNNs, LSTM uses memory gates to decide:

- What to remember  
- What to forget  
- What to use for the current prediction  

In this project, LSTM helps analyze text patterns in social media posts to classify whether a post is **Actionable** or **Non-Actionable**.

**Simple Idea:**  
RNN may forget older context, but **LSTM remembers selectively**, making it more effective for text classification tasks.

It was built as a practical **Deep Learning + NLP beginner project** to understand how text data can be processed and classified using **TF-IDF + LSTM Neural Network**.

This project is suitable for **job preparation**, portfolio building, and demonstrating practical machine learning workflow skills.

---

## 🎯 Problem Statement

Companies receive thousands of customer comments on social media.

Manually checking which posts need action is slow and inefficient.

The goal of this project is to automatically classify posts into:

- Needs response / support  
- No action needed

---

## 🧠 What This Project Actually Demonstrates

This project realistically shows understanding of:

- Text preprocessing
- NLP feature extraction
- Train/Test data splitting
- TF-IDF vectorization
- Deep Learning model creation using Keras
- LSTM for sequence-style input
- Binary classification
- Model evaluation using Accuracy, Precision, Recall, F1-score
- Data visualization using Matplotlib

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Regex
- Matplotlib
- Scikit-learn
- TensorFlow / Keras
- Jupyter Notebook

---

## 📁 Project Structure
├── Dataset/
       ├── actionable_social_media_posts.csv
├── Notebook/       
       ├── Actionable_Social_Media_Posts_LSTM.ipynb
└── README.md
├── requirements.txt 
└── .gitignore

## 📂 Dataset Information

**File:** `actionable_social_media_posts.csv`

### Columns

| Column Name  | Description |
|--------------|-------------|
| `post_text`  | Social media post text |
| `actionable` | Target label (0 or 1) |

### Dataset Size

- **Total Rows:** 1200
- **Classes:** Balanced practical binary dataset

---

## ⚙️ Project Workflow

### 1️⃣ Load Dataset

Reads CSV file into Pandas DataFrame.

### 2️⃣ Text Cleaning

Performed preprocessing:

- Convert text to lowercase
- Remove punctuation
- Remove numbers
- Keep alphabetic text only

### 3️⃣ Data Visualization

Bar chart used to inspect class distribution.

### 4️⃣ Train-Test Split

- 80% Training Data
- 20% Testing Data

### 5️⃣ TF-IDF Vectorization

Converted text into numeric features using:

python
TfidfVectorizer(max_features=150)

### 6️⃣ Reshape for LSTM

TF-IDF output reshaped into 3D format:

(samples, timesteps, features)

### 7️⃣ Build Deep Learning Model

Architecture:

LSTM (64 Units)
Dropout (0.3)
Dense Output Layer (Sigmoid)

### 8️⃣ Train Model
epochs = 10
batch_size = 32

### 9️⃣ Evaluate Model

Used:

Accuracy Score
Classification Report

## 🧱 Model Architecture

Sequential([
    LSTM(64),
    Dropout(0.3),
    Dense(1, activation="sigmoid")
])

## 📈 Results

Test Accuracy
69.58%
Classification Report
Class	Precision	Recall	F1-Score
0	     0.68	      0.67	  0.68
1	     0.71	      0.72	  0.71

## 📌 Honest Project Evaluation

What Is Good

✅ Complete end-to-end NLP pipeline
✅ Uses real Deep Learning model
✅ Shows preprocessing + evaluation skills
✅ Good beginner portfolio project
✅ Relevant for customer support / sentiment routing use cases

What Is Limited

⚠️ TF-IDF + LSTM is not ideal modern architecture combination
⚠️ Better methods today: Embeddings, GRU, BERT, DistilBERT, Transformers
⚠️ Small dataset limits performance ceiling
⚠️ Synthetic/simple dataset likely used for learning

This is a solid learning project, not a production-grade AI system.

## 🚀 Future Improvements

Use Word2Vec / GloVe embeddings
Replace TF-IDF with Tokenizer + Padding
Try GRU / BiLSTM
Use BERT Transformer model
Hyperparameter tuning
Deploy using Flask / Streamlit
Add real Twitter / Instagram complaint dataset


## 💼 This project can demonstrate:

NLP fundamentals
Deep learning basics
Binary classification
TensorFlow usage
Model evaluation understanding
Ability to complete ML pipeline independently

Best positioned as: Deep Learning Learning Project or NLP Text Classification Project

## ▶️ How to Run

pip install pandas numpy matplotlib scikit-learn tensorflow

Run notebook:

jupyter notebook

Open:

Actionable_Social_Media_Posts_LSTM.ipynb

## 📌 Author Note

Created as a practical project to strengthen understanding of Deep Learning + NLP workflows. Do Follow for More!