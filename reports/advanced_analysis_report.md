# Project Report: Advanced Data Analysis Using Natural Language Processing (NLP)

## 1. Chosen Technique: Natural Language Processing (TF-IDF & Sentiment Classification)
Natural Language Processing (NLP) enables computers to parse, structure, and extract quantitative insights from unstructured human text. In this project, we apply **Term Frequency–Inverse Document Frequency (TF-IDF)** vectorization with unigram and bigram extraction (`ngram_range=(1, 2)`) alongside supervised text classification models to automatically categorize customer feedback into **Positive**, **Neutral**, and **Negative** sentiments.

## 2. Dataset & Application
* **Dataset:** Customer Telecom & Broadband Reviews (`data/customer_reviews_nlp.csv`, 1,200 reviews).
* **Real-World Application:** Subscription businesses receive thousands of free-text support tickets and reviews daily. Automated NLP sentiment analysis identifies dissatisfied customers experiencing network or billing issues in real time so retention teams can prioritize outreach.

## 3. Methodology & Workflow
1. **Text Normalization & Cleaning:** Converted raw review strings to lowercase, stripped punctuation and special characters via regular expressions (`re.sub`), and calculated token length distributions.
2. **Feature Engineering (TF-IDF):** Removed English stopwords and transformed text into a 500-feature numerical matrix weighting key phrases (such as *"fiber internet"*, *"billing issue"*, and *"network disconnection"*).
3. **Classification Modeling:** Trained and compared three machine learning classifiers on an 80/20 train-test split:
   * **Multinomial Naive Bayes** (probabilistic baseline tailored for word frequency features)
   * **Logistic Regression** (linear hyperplane classifier over sparse TF-IDF matrices)
   * **Random Forest Classifier** (ensemble decision trees over text features)

## 4. Key Results & Analytical Insights
* **High Classification Accuracy:** All three models achieved strong separation between positive, negative, and neutral feedback using bigram TF-IDF features.
* **Top Negative Drivers:** Bigram analysis reveals that *"network disconnection"*, *"billing issue"*, and *"hidden fees"* are the strongest predictors of 1-star and 2-star reviews.
* **Top Positive Drivers:** Phrases centered on *"fast fiber"*, *"resolved quickly"*, and *"stable connection"* strongly correlate with 5-star retention.
