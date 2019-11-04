# Support_Vector_Machines-on-Amazon_Fine_Food_Reviews
Given a review, Using Svm model determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2). [Q] How to determine if a review is positive or negative? 
[Ans] We could use Score/Rating. A rating of 4 or 5 can be cosnidered as a positive review. A rating of 1 or 2 can be considered as negative one. A review of rating 3 is considered nuetral and such reviews are ignored from our analysis. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

Models used: Sklearn SGDClassifier with hinge loss and sklearn SVC model, Vectorizers used : Bow (sklearn-CountVectorizer),Tfidf(sklearn-TfidfVectorizer),Avg-W2v(trained a gensim model),Tfidf-W2v Metrics used: auc(sklearn's roc_auc) and Accurcy

Ipynb file also consits of feature importance representation using wordcloud

Obtained Results:
+------------+--------+---------+----------+----------------+------+
| Vectorizer | Model  | penalty | Accuracy | Hyperparameter | AUC  |
+------------+--------+---------+----------+----------------+------+
|    Bow     | Linear |    l2   |  92.985  |     0.001      | 0.96 |
|    Bow     | Linear |    l1   |  91.955  |     0.0001     | 0.96 |
|   Tfidf    | Linear |    l2   |  93.142  |     0.0001     | 0.97 |
|   Tfidf    | Linear |    l1   |  92.09   |     0.0001     | 0.96 |
|  Avg-W2v   | Linear |    l2   |  90.778  |     0.001      | 0.95 |
|  Avg-W2v   | Linear |    l1   |  90.608  |     0.001      | 0.94 |
| Tfidf-W2v  | Linear |    l2   |  89.277  |     0.001      | 0.92 |
| Tfidf-W2v  | Linear |    l1   |  88.96   |     0.001      | 0.92 |
+------------+--------+---------+----------+----------------+------+

+------------+-------+---------+----------+-------+-------+------+
| Vectorizer | Model | penalty | Accuracy | gamma |   C   | AUC  |
+------------+-------+---------+----------+-------+-------+------+
|    Bow     |  Rbf  |    l2   | 90.9423  |  0.01 |  1000 | 0.95 |
|   Tfidf    |  Rbf  |    l2   |  92.38   |   1   | 10000 | 0.97 |
|  Avg-W2v   |  Rbf  |    l2   |  91.179  |  0.01 |   10  | 0.95 |
| Tfidf-W2v  |  Rbf  |    l2   |  89.72   | 0.001 |   10  | 0.93 |
+------------+-------+---------+----------+-------+-------+------+
