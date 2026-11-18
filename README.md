# SMS Spam Detection

A machine learning project that classifies SMS messages as spam or ham (legitimate). I trained and compared five models on 5,500+ messages to find the one that catches spam best without flagging too many real messages.

## How it works

1. **Clean the text:** lowercase everything, remove punctuation, handle URLs.
2. **Normalize numbers:** replace them with a `num` token so the model doesn't memorize specific values.
3. **Extract features:** TF-IDF with unigrams and bigrams, so phrases like "call now" and "free entry" are captured.
4. **Train and test:** 80% of the data for training, 20% held out for testing.

## Models compared
- Linear SVM
- Logistic Regression
- Multinomial Naive Bayes
- Random Forest
- XGBoost

I used F1-score as the main metric, since spam is much rarer than normal messages and accuracy alone can be misleading.

## Result
**Linear SVM** came out on top, with 98.92% accuracy and an F1-score of 0.96. Random Forest and Naive Bayes had perfect precision, but they missed more spam. The SVM had the best balance of the two, and it trains in under 0.1 seconds.

## Built with
Python, Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, ipywidgets

## Author
   Israr Hussain
