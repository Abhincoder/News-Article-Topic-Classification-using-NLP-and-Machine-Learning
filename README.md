# 📰 News Article Classification using NLP and Machine Learning

This project focuses on the classification of news articles into four distinct categories — **World**, **Sports**, **Business**, and **Science & Technology** — using Natural Language Processing (NLP) and a suite of machine learning models.

## 📂 Dataset

The dataset contains labeled news articles with features like:
- `Title`
- `Description`
- `Class Index` (Label: 1–4)

Label Mapping:
- 1 → World
- 2 → Sports
- 3 → Business
- 4 → Science & Technology

---

## 🛠️ Preprocessing

- **Data Cleaning**:
  - Combined `Title` and `Description` into a `Summary`
  - Removed null values and unwanted characters
  - Applied lowercasing, symbol replacement, and whitespace normalization

- **Tokenization & Normalization**:
  - Tokenized text into words
  - Removed stopwords
  - Lemmatized tokens using `WordNetLemmatizer`

---

## 📈 Feature Engineering

- **Bag of Words (BoW)** and **TF-IDF Vectorization** used to convert text into numerical feature vectors.
- For LDA topic modeling, a bag-of-words matrix was created from tokenized summaries.

---

## 🤖 Models Applied

| Model               | Validation Accuracy | Test Accuracy | Notes |
|--------------------|---------------------|---------------|-------|
| Logistic Regression | ~0.719              | —             | Baseline model |
| Naive Bayes (MultinomialNB) | ~0.876 (CV)     | ~0.868        | Best performing |
| Random Forest       | ~0.814 (CV)         | —             | Good with tuning |
| XGBoost             | ~0.853 (CV)         | —             | Tuned with GridSearchCV |
| MLP Classifier      | ~0.801 (Val)        | ~0.798        | Neural network |
| SGD Classifier      | ~0.712 (Val)        | —             | Linear model baseline |

---

## 🔍 Topic Modeling (LDA)

- Applied Latent Dirichlet Allocation (LDA) to discover hidden topics.
- Identified 10 coherent topics, e.g.:

