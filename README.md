# Determining the Effectiveness of Various Machine Learning Classifiers

The dataset used in this project was acquired from https://github.com/MWiechmann/enron_spam_data which itself is taken from the [Enron Corpus](https://www2.aueb.gr/users/ion/data/enron-spam/readme.txt)

The classifiers being tested are:
- Support Vector Machine
- Decision Tree
- Multinomial Naive Bayes
- Random Forest
- K-Nearest Neighbors
- Logistic Regression


The performance of each classifer is evaluated on various different metrics:
-F1 Score
-Precision
-Recall
-Accuracy

Each classifier is also given a 10-fold Cross Validation Score (accuracy). These scores are used to compare how well of an estimate each model can give on unseen data.
