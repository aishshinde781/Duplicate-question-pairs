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

We have creted 23 features from the questions.

1.we have created q1_len and q2_len to know the character length of both questions.

2.we have created q1_num_words and q2_num words to know the character count of both the questions.

3.we have created common_words feature which is count of total words in both questions.

4.we have created total_words feature which is count of total unique words in both questions.

5.we have created word_share feature which is equal to word common divided by word total.

6.we have also created some token features i.e cwc_min: this is the ration of the number of common words to the length of the smaller questions.

7.cwc_max: this is the ratio of the number of common words to the length of the larger questions.

8.csc_min: this is the ratio of the number of common stopwords to the smaller stopwords count among the two questions.

8.ccs_max: this is the ratio of the number of common stopwords to the larger stopwords count among the two questions.

9.ctc_min: this is the ratio of number of common tokens to the smaller token count among the two questions.

10.ctc_max: this is the ratio of number of common tokens to the larger token count among the two questions.

11.last_word_eq: 1 if the last word in the both questions is same, otherwise 0

12.first_word_eq: 1 if the first word in the both questions is same, otherwise 0

13.mean_lem: mean of the length of the two questions.

14.abs_len_diff: absoluate difference between the length of the two questions.

15.longest_substr_ratio: ratio of length of the longest substring among the two questions to the length of smaller question.

16.then we have extracted fuzz ratio,fuzz partial ratio, fuzz token set ratio, fuzz token sort ratio feature with fuzzywuzzy string matching tool.

4.EDA :

If the fist and last word is the same then there is a high chance that the question pairs are duplicates.
![Screenshot (65)](https://user-images.githubusercontent.com/105923718/227157778-e88ed56c-2535-4973-ae2e-9049950444ff.png)





