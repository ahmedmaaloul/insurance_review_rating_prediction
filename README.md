# Insurance Review Rating Prediction

## 📌 Project Overview

This project aims to analyze customer reviews of insurance services using **Natural Language Processing (NLP)** techniques. The primary goal is to predict **customer ratings** based on textual feedback and extract key insights to improve insurance services. A web application is also deployed using **Streamlit** to allow users to input their reviews and receive predicted ratings.

## 🎯 Objectives

- **Classify** customer reviews into predefined categories or themes.
- **Predict ratings** from textual feedback.
- **Extract insights** from customer opinions to enhance service quality.
- **Deploy** an interactive web app for real-time predictions.

## 🗂 Dataset

- **Source**: 35 text files (~300 KB each) containing customer reviews.
- **Features**:
  - `DateTime`: Time of the review.
  - `Insurer`: Name of the insurance provider.
  - `Type`: `train` or `test` dataset.
  - `Review`: Customer feedback in **French** (translated to English).
  - `Rating`: Numeric rating associated with the review.

## 🛠️ Methodology

### 1️⃣ **Data Preprocessing & Cleaning**
- Removing URLs, HTML tags, emojis, and special characters.
- Expanding contractions (e.g., *can't* → *cannot*).
- Correcting spelling errors.
- Tokenization, stopword removal, and **lemmatization**.

### 2️⃣ **Feature Engineering**
- **N-gram Analysis**: Extracting frequent word patterns.
- **Topic Modeling**: Using **LDA** to group reviews into themes.
- **Word Embeddings**: Using **Word2Vec (W2V)** and clustering with **k-means**.

### 3️⃣ **Modeling**
- **Baseline**: TF-IDF + Logistic Regression.
- **Neural Network**: Basic NN with an embedding layer.
- **Fine-Tuned Transformer Models**:
  - **RoBERTa (GPT-2)**
  - **LLaMA 3.2 (1B parameters) with LoRA fine-tuning**
- **Final Choice**: **Basic NN** (small size, high accuracy, easy to deploy).

### 4️⃣ **Model Evaluation**
- **Metrics**: Accuracy, Precision, Recall, F1-score.
- **SHAP Analysis**: Explainability of model predictions.

### 5️⃣ **Deployment**
- **Streamlit Web App** for real-time review analysis.
- Hosted at: [Insurance Opinion Classification App](https://insurance-opinion-classification-3hv3edp8cpphd4dwgtwzcc.streamlit.app/)

## 📊 Results & Insights

- **Key Influencing Factors**:
  - Terms like **"speed"**, **"premium"**, and **"high price"** significantly impact ratings.
  - **Negative reviews** are more focused on **pricing** and **customer service** delays.
  - **Positive reviews** mention **fast claims processing** and **good customer support**.

- **Model Performance**:
  - **Selected Model**: Basic NN (Embedding + 1D Convolution)
  - **Accuracy**: ~85%
  - **Mean Distance from True Rating**: ~0.75 (good predictive capability)

## 📌 Future Improvements

- Integrating **French-specific embeddings** for better semantic understanding.
- Implementing **attention-based mechanisms** for more refined predictions.
- Expanding the dataset with **more diverse customer feedback sources**.

## 🏆 Contributors

- **Ahmed Maaloul**
- **Martin Pujol**
