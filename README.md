# Sentiment Analysis of Flipkart Product Reviews Using NLP and Machine Learning

## 📌 About the Project

This project focuses on analyzing customer reviews from Flipkart and classifying them into different sentiment categories using Natural Language Processing (NLP) and Machine Learning.

The system processes customer review text, converts the text into numerical features using TF-IDF, and applies machine learning algorithms to predict whether a review is Positive, Neutral, or Negative.

The main aim of this project is to understand customer opinions from product reviews and automatically identify the sentiment expressed in the reviews.

---

## 🎯 Problem Statement

Online shopping platforms receive a large number of customer reviews every day. Manually analyzing these reviews to understand customer opinions can be time-consuming.

This project aims to develop an NLP-based sentiment analysis system that can automatically classify Flipkart product reviews into Positive, Neutral, and Negative categories.

---

## 🎯 Objectives

- Analyze customer reviews from Flipkart.
- Clean and preprocess the review text.
- Convert text data into numerical features using TF-IDF.
- Train different machine learning models for sentiment classification.
- Compare the performance of different models.
- Select the best-performing model.
- Evaluate the model using suitable performance metrics.
- Predict the sentiment of new customer reviews.

---

## 📊 Dataset

The dataset used in this project is the **Flipkart Product Reviews with Sentiment Dataset**.

**Source:** Kaggle

**Dataset:** Flipkart Product Reviews with Sentiment Dataset

**Number of Records:** 205,052

**Number of Columns:** 6

### Dataset Columns

| Column | Description |
|--------|-------------|
| `product_name` | Name of the product |
| `product_price` | Price of the product |
| `Rate` | Customer rating |
| `Review` | Customer review text |
| `Summary` | Short summary of the review |
| `Sentiment` | Sentiment category of the review |

The `Review` column is used as the main input text, while the `Sentiment` column is used as the target variable.

### Sentiment Classes

- Positive
- Neutral
- Negative

---

## 🔄 Methodology

The project follows the following workflow:

**Flipkart Dataset**  
↓  
**Data Cleaning**  
↓  
**Text Preprocessing**  
↓  
**TF-IDF Feature Extraction**  
↓  
**Train-Test Split**  
↓  
**Machine Learning Models**  
↓  
**Prediction**  
↓  
**Evaluation**  
↓  
**Model Comparison**  
↓  
**Final Model – Linear SVM**

---

## 🧹 Data Preprocessing

The dataset was cleaned and prepared before applying machine learning models.

The following preprocessing steps were performed:

- Removed rows with missing review values.
- Removed duplicate records.
- Converted review text to lowercase.
- Removed special characters and unnecessary symbols.
- Removed extra spaces from the text.
- Created a `Cleaned_Review` column containing the processed review text.

These preprocessing steps helped prepare the review text for feature extraction and machine learning.

---

## 🔢 Feature Extraction Using TF-IDF

Since machine learning models cannot directly process raw text, the cleaned review text was converted into numerical features.

**TF-IDF (Term Frequency-Inverse Document Frequency)** was used for feature extraction.

The TF-IDF vectorizer was configured with:

- Maximum features: 5000
- N-gram range: 1 to 2

This means both individual words and pairs of consecutive words were considered as features.

TF-IDF helps identify words and phrases that are important in the review dataset.

---

## ✂️ Train-Test Split

The dataset was divided into training and testing sets.

- **80%** of the data was used for training.
- **20%** of the data was used for testing.
- Stratified splitting was used to maintain the distribution of sentiment classes.

A random state of `42` was used to make the results reproducible.

---

## 🤖 Machine Learning Models

Three machine learning models were trained and compared:

### 1. Logistic Regression

Logistic Regression was used as one of the classification models for predicting the sentiment of customer reviews.

### 2. Naive Bayes

Multinomial Naive Bayes was used because it is suitable for text classification tasks and works with TF-IDF features.

### 3. Linear SVM

Linear Support Vector Machine was also trained for sentiment classification.

Linear SVM performed slightly better than the other models and was selected as the final model.

---

## 📈 Model Evaluation

The models were evaluated using classification accuracy.

The project also uses evaluation measures such as:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

These metrics help understand the performance of the classification models.

---

## 📊 Model Comparison

The performance of the three machine learning models was compared.

| Model | Accuracy |
|-------|----------|
| Logistic Regression | 90.26% |
| Naive Bayes | 89.44% |
| Linear SVM | **90.27%** |

Among the three models, **Linear SVM achieved the highest accuracy of 90.27%**.

Therefore, Linear SVM was selected as the final model for this project.

---

## 🏆 Final Model – Linear SVM

Linear SVM was selected as the final model because it achieved the highest accuracy among the tested models.

The final model uses:

**Review Text → Text Preprocessing → TF-IDF → Linear SVM → Sentiment Prediction**

The model can classify new customer reviews into:

- Positive
- Neutral
- Negative

---

## 🔍 Testing with New Customer Reviews

After training the model, new customer reviews can be entered into the system.

The review is first cleaned using the same preprocessing steps and then converted into TF-IDF features.

The trained Linear SVM model then predicts the sentiment of the new review.

### Example

**Input Review:**
> "The product quality is excellent and I am very happy with the purchase."

**Predicted Sentiment:**
> Positive

---

## 📉 Confusion Matrix

A confusion matrix was generated to analyze the prediction performance of the Linear SVM model.

It shows the relationship between the actual sentiment classes and the sentiments predicted by the model.

The confusion matrix helps identify correctly classified reviews as well as misclassified reviews.

---

## 📸 Project Screenshots

Important screenshots of the project implementation and results are included in the `screenshots` folder.

The screenshots include:

- Dataset Overview
- Data Cleaning
- Sentiment Distribution
- Text Preprocessing
- TF-IDF Feature Extraction
- Logistic Regression Results
- Linear SVM Results
- Linear SVM Confusion Matrix
- Model Accuracy Comparison

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Natural Language Processing
- TF-IDF
- Logistic Regression
- Naive Bayes
- Linear SVM
- Google Colab
- GitHub

---

