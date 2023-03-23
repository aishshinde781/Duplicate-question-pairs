# Duplicate-question-pairs

1.Introduction:

One of the many problems that quora face is the duplication of questions. Duplication of question ruins the experience for both the questioner and the answerer. Since the questioner is asking duplicate questopn, we can just show him/her the answers to the previous question. And the answerer doesn't have to repeat his/her answer for essentially the same questions.

The dataset is available on kaggle

2.Data Overview:

Available columns: id, qid1, qid2, question1, question2, is_duplicate
Class labels: 0,1
Total training data/No of rows: 404290
No of columns: 6
is_duplicate is the dependent variable.

3.Data Cleaning

1.Replace certain special charcters with their string equvivalents.
2.We have removed contractions
3.Replacing some numbers with string equvivalents.
4.We have  removed HTML tags.
5.We have removed  punctuations.

3.Feature Extraction:

We have creted 14 features from the question.

1.



