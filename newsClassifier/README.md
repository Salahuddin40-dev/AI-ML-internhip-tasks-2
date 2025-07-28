# 📰 News Topic Classifier Using BERT

This project fine-tunes a pre-trained BERT model to classify news headlines into one of four categories: **World**, **Sports**, **Business**, and **Science/Tech** using the AG News dataset. It also includes a Streamlit app for interactive predictions.

---

## 📌 Objective

Build a news topic classifier using **BERT** that can accurately predict the category of a news headline.

---

## 📊 Dataset

- **AG News Dataset** (Available on Hugging Face Datasets)
- 120,000 training samples and 7,600 test samples
- Each sample includes:
  - `text`: News headline or short description
  - `label`: One of 4 categories

---

## 📦 Requirements

Install all required libraries:

```bash
pip install transformers datasets torch scikit-learn streamlit
