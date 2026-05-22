# SMS / Email Spam Classifier

A machine learning system that classifies SMS and email messages as **Spam** or **Ham** (not spam), built with an ensemble of multiple classifiers and deployed as an interactive web app.

___

## 📌 What This Project Does

Takes a raw SMS or email message as input, processes the text, and predicts whether it is spam or legitimate — with 97% accuracy on the test dataset.

___

## ⚙️ Tech Stack

| Category | Tools |

| Language | Python |
| ML Library | Scikit-learn |
| NLP | NLTK, TF-IDF Vectorizer, Wordcloud |
| Data | Pandas, NumPy |
| Web App | Streamlit |

___

## 🔍 How It Works

**1. Data Cleaning & Preprocessing**
- Removed duplicates and null values from the Kaggle SMS Spam dataset
- Lowercased text, removed punctuation, stopwords, and applied stemming using NLTK

**2. Text Vectorization**
- Converted cleaned text into numerical features using TF-IDF Vectorizer

**3. Model Training**
- Trained and compared multiple classifiers: SVM, Decision Tree, Extra Trees
- Combined them using a **Voting Classifier** to improve overall robustness and accuracy

**4. Model Evaluation**
- Evaluated using accuracy, precision, and confusion matrix
- Applied hyperparameter tuning to optimize performance

___

## 📊 Results

| Metric | Score |

| Accuracy | **97%** |
| Best Model | Voting Classifier (SVM + Decision Tree + Extra Trees) |
| Dataset | Kaggle SMS Spam Collection |

___

## 🚀 How to Run Locally

```bash
# 1. Clone the repo
git clone https://github.com/Kirtisharma2000/sms-spam-classifier.git
cd sms-spam-classifier

# 2. Install dependencies
pip install scikit-learn nltk streamlit pandas numpy wordcloud

# 3. Run the app
streamlit run app.py
```

Then open `http://localhost:8501` in your browser, paste any message, and hit Predict.

___

## 📁 File Structure

```
sms-spam-classifier/
├── app.py                      # Streamlit web app
├── sms_spam_classifier.ipynb   # Full model training notebook
├── model.pkl                   # Saved trained model
├── vectorizer.pkl              # Saved TF-IDF vectorizer
├── spam.csv                    # Dataset
└── nltk.txt                    # NLTK dependencies
```
