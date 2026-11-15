# Advanced Data Analysis Techniques — Natural Language Processing (NLP)

## Overview
This repository implements **Natural Language Processing (NLP)** and **Sentiment Classification** on customer review data to extract actionable retention insights from unstructured text.

## Repository Structure
```text
├── data/
│   └── customer_reviews_nlp.csv         # Real-world style customer reviews dataset (1,200 records)
├── notebooks/
│   └── nlp_sentiment_analysis.ipynb     # Deliverable 2: Complete Python & NLP implementation
├── reports/
│   └── advanced_analysis_report.md      # Deliverable 1: Detailed technical report on NLP & application
├── README.md                            # Project documentation
└── requirements.txt                     # Required Python libraries
```

## Technique Applied
- **Text Preprocessing:** Regex cleaning, tokenization, and English stopword removal.
- **Feature Extraction:** TF-IDF Vectorization (`TfidfVectorizer` with unigrams and bigrams).
- **Supervised NLP Models:** Multinomial Naive Bayes, Logistic Regression, and Random Forest.

## How to Run
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Open and run `notebooks/nlp_sentiment_analysis.ipynb` in Jupyter Notebook or Google Colab.
