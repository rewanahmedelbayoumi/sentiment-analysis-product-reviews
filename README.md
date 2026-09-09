# Sentiment Analysis on IMDb Reviews

An end-to-end Natural Language Processing project for classifying movie reviews as **positive** or **negative** using classical machine learning techniques.

This project uses the **Large Movie Review Dataset (IMDb)** released by researchers at **Stanford University**, a widely used benchmark dataset for sentiment classification.

## Project Overview

The goal of this project is to build a complete sentiment analysis pipeline that transforms raw natural language text into numerical features and trains a machine learning classifier to detect sentiment polarity.

The complete pipeline includes:

- Dataset loading and inspection
- Text preprocessing and normalization
- Label encoding
- Train-test splitting
- TF-IDF feature extraction
- Logistic Regression classification
- Model evaluation
- Confusion matrix analysis
- Custom sentiment prediction
- Frequent word analysis
- Naive Bayes comparison

## Dataset

This project uses the:

**Large Movie Review Dataset (IMDb)**  
**Stanford University**

The dataset contains:

- 25,000 labeled training reviews
- 25,000 labeled testing reviews
- Balanced positive and negative sentiment classes

The original dataset is provided as individual text files organized into positive and negative review directories.

Dataset source:

https://ai.stanford.edu/~amaas/data/sentiment/

## NLP Pipeline

Raw IMDb Reviews
        ↓
Text Cleaning
        ↓
Text Preprocessing
        ↓
Label Encoding
        ↓
Train-Test Split
        ↓
TF-IDF Vectorization
        ↓
Logistic Regression
        ↓
Sentiment Prediction
        ↓
Model Evaluation


## Text Preprocessing

The raw review text is cleaned before model training.

The preprocessing pipeline includes:

* Lowercasing
* HTML tag removal
* URL removal
* Special character removal
* Whitespace normalization

This reduces noise and produces a cleaner representation of the review text.

## Feature Extraction

The project uses **TF-IDF (Term Frequency-Inverse Document Frequency)** to convert textual reviews into numerical feature vectors.

TF-IDF helps emphasize words that are important within a review while reducing the influence of extremely common words across the dataset.

The vocabulary is limited to the most informative features for efficient model training.

## Classification Model

The primary classifier is:

**Logistic Regression**

The model learns the relationship between TF-IDF features and sentiment labels:

```text
Negative = 0
Positive = 1
```

Logistic Regression was selected because it is a strong baseline for high-dimensional sparse text classification problems.

## Model Evaluation

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

These metrics provide a more complete understanding of model performance than accuracy alone.

## Custom Sentiment Prediction

The project includes a custom prediction function that allows new reviews to be classified directly.

Example:

```python
predict_sentiment(
    "This movie was absolutely amazing and I enjoyed every minute."
)
```

Output:

```text
Positive
```

## Bonus Experiments

### Frequent Word Analysis

The most frequent words in positive and negative reviews are extracted and visualized.

### Naive Bayes Comparison

A Multinomial Naive Bayes classifier is trained using the same TF-IDF features and compared against Logistic Regression.

This provides a direct comparison between two classical machine learning approaches for text classification.

## Technologies Used

* Python
* Pandas
* NumPy
* Regular Expressions
* Matplotlib
* Scikit-learn
* NLTK
* Jupyter Notebook
* Git
* GitHub

## Project Structure

```text
sentiment-analysis-product-reviews/
│
├── data/
│   └── aclImdb/
│
├── images/
│
├── notebooks/
│   └── sentiment_analysis.ipynb
│
├── src/
│
├── .gitignore
├── README.md
└── requirements.txt
```

## Installation

Clone the repository:

```bash
git clone https://github.com/rewanahmedelbayoumi/sentiment-analysis-product-reviews.git
```

Enter the project directory:

```bash
cd sentiment-analysis-product-reviews
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install the project dependencies:

```bash
pip install -r requirements.txt
```

## Dataset Setup

Download the Stanford IMDb Large Movie Review Dataset and extract the `aclImdb` folder into:

```text
data/aclImdb/
```

Expected structure:

```text
data/
└── aclImdb/
    ├── train/
    │   ├── pos/
    │   └── neg/
    └── test/
        ├── pos/
        └── neg/
```

## Key Learning Outcomes

This project demonstrates practical experience with:

* Natural Language Processing
* Text preprocessing
* Feature engineering for text
* TF-IDF
* Binary classification
* Supervised machine learning
* Logistic Regression
* Naive Bayes
* Model evaluation
* Confusion matrix analysis
* Git and GitHub workflow
* Reproducible machine learning project structure

```
```
