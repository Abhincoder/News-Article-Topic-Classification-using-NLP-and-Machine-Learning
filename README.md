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

| Model           
|--------------------|---------------------|---------------|-------|
| Logistic Regression 
| Naive Bayes (MultinomialNB)
| Random Forest       
| XGBoost             
| MLP Classifier      
| SGD Classifier      

---

## 🔍 Topic Modeling (LDA)

- Applied Latent Dirichlet Allocation (LDA) to discover hidden topics.
- Identified 10 coherent topics, e.g.:
Topic 0: ap game season new night win team lead ared year
Topic 1: president bush election minister ap prime iraq vote leader afp
Topic 2: microsoft window darfur talk sudan city peace government security eu
Topic 3: court case ap new judge india year trial federal lawsuit
Topic 4: areuters china drug nuclear new space ap state iran say
Topic 5: new search google apple music web world intel open computer
Topic 6: world champion cup gold win team olympic athens united england
Topic 7: company new software service corp plan deal dollar business microsoft
Topic 8: dollar oil areuters price stock new percent sale profit share
Topic 9: iraq killed people palestinian police areuters attack baghdad iraqi official

