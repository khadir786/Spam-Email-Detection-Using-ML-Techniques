# Determining the Effectiveness of Various Machine Learning Classifiers in Spam Detection

## Dataset
The dataset used in this project was acquired from https://github.com/MWiechmann/enron_spam_data which itself is taken from the [Enron Corpus](https://www2.aueb.gr/users/ion/data/enron-spam/readme.txt).
The dataset contains a total of 33716 emails. 17171 emails are spam and 16545 emails are ham(not spam). 

The relevant data in the dataset are data that falls under the Subject, Message and Spam/Head columns. Considering the subject and the message are the features, the data is processed to drop any rows that do not have any data in either column.

## Feature Extraction

The nature of this project is categorised under Natural Language Processing (NLP) and so a the Bag of Words model was used which is a common feature-extraction technique. The technique vectorized the data in the Message and Subject column (which was conacatenated to 'Email Content') which is to say that it converted the text data into numerical features. 

Before this, the data is normalised via tokenization and lemmatization. This makes it so that the number of words are reduced by collapsing similar word forms into a single representation.

These processes made it so that the number of features is reduced from 156081 to 149269 which represents the number of unique words in the data.

The classifiers being tested are:
- Support Vector Machine
- Decision Tree
- Multinomial Naive Bayes
- Random Forest
- K-Nearest Neighbors
- Logistic Regression

Each classifier is given a 10-fold Cross-Validation Score (accuracy). These scores are used to compare how well of an estimate each model can give on unseen data.

The performance of each classifer is also evaluated on various different metrics given by a classification report, which is itself is generated based on 5-fold cross-validated data.
These metrics are:
- F1 Score
- Precision
- Recall
- Accuracy

The following is an explanation of what each of these values mean taken from the [sklearn metrics documentation](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.precision_recall_fscothere_support.html#sklearn.metrics.precision_recall_fscore_support)

> The precision is the ratio tp / (tp + fp) where tp is the number of true positives and fp the number of false positives. The precision is intuitively the ability of the classifier not to label a negative sample as positive.
> The recall is the ratio tp / (tp + fn) where tp is the number of true positives and fn the number of false negatives. The recall is intuitively the ability of the classifier to find all the positive samples.
> The F-beta score can be interpreted as a weighted harmonic mean of the precision and recall, where an F-beta score reaches its best value at 1 and worst score at 0.
> The F-beta score weights recall more than precision by a factor of beta. beta == 1.0 means recall and precision are equally important.
> The support is the number of occurrences of each class in y_true.



