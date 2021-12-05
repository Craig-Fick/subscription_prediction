# subscription_prediction
Kaggle challenge
link: https://www.kaggle.com/c/nyu-shbigb-7311


This ia a project that is on kaggle that anyone can enter. The date has past for the chance to be ranked, but you can still submit your submissions for a score.

My Approach
I ran all of my models off of one file so I could tweak arguments faster. It is pretty sloppy, but here is a list of basically what was tested.

- Feature selection
- forward/backward elimination
- information gain using Caret and Boruta packages
- PCA using python
- models
-boosting
-stacking/ensemble - with a variety of looped arguments
- rf - with a variety of trees for testing
- svm
- naive bayes
- adaboost
- decision tree
- logistic regression
- rf/xgboost
- splitting tested
- train/test splits
-50:50, 70:30, 80:20, 90:10, 95:5
- Cross Validation - 10 folds
- balancing
- undersampling
- 1540:1540
- 1540:4000
- 1540:6000



Task Description
Website XYZ, a music-listening social networking website, follows the “freemium” business
model. The website offers basic services for free, and provides a number of additional premium 
capabilities for a monthly subscription fee. We are interested in predicting which people would be 
likely to convert from free users to premium subscribers in the next 6 month period, if they are 
targeted by our promotional campaign. You have a dataset (provided on the course Canvas
site) from the previous marketing campaign which targeted a number of non-subscribers.
Specifically, the labeled dataset contains 86,682 records, each record representing a different user 
of the XYZ website who was targeted in the previous marketing campaign. Each record is 
described with 25 attributes. Here is a brief description of the attributes (attribute
name/type/explanation):
• adopter / binominal (0 or 1) / whether a user became a subscriber within the 6 month period 
after the marketing campaign (this is the outcome variable!)
• user_id / integer / unique user id (obviously, this is not a predictive feature, just a unique 
identifier)
• age / integer / age in years
• male / integer (0 or 1) / 1 – male, 0 – female
• friend_cnt / integer / numbers of friends that the current user has
• avg_friend_age / real / average age of friends (in years)
• avg_friend_male / real (between 0 and 1) / percentage of males among friends
• friend_country_cnt / integer / number of different countries among friends of the current 
user
• subscriber_friend_cnt / integer / number of friends who are subscribers of the premium 
service
• songsListened / integer / total number of tracks this user listened (or reported as listened)
• lovedTracks / integer / total number of different songs that the user “liked”
• posts / integer / number of forum or discussion board posts made by the user
• playlists / integer / number of playlists created by the user
• shouts / integer / number of wall posts received by the user
• good_country / integer (0 or 1) / country type of the user: 0 – countries where free usage is 
more limited, 1 – less limited
• tenure / integer / number of months since the user has registered on the website.
• There are also a number of attributes with the following names: delta_<attrname>, where 
<attrname> is one of the attributes mentioned in the above list. Such attributes refer not to 
the overall number, but the change to the corresponding number over the 3-month period 
before the marketing campaign. For example, consider attribute delta_friend_cnt. If, for 
some user, friend_cnt = 50, and delta_friend_cnt = –5, it means that the user had 50 friends 
at the time of the previous marketing campaign, but this number reduced by 5 during the 3 
months before the campaign (i.e., user had 55 friends 3 months ago).
The general task is to build the best predictive model for the next marketing campaign, i.e., for
predicting likely adopters (that is, which current nonsubscribers are likely to respond to the 
marketing campaign and sign up for the premium service within 6 months after the campaign).
Feel free to use any techniques, methodologies, and approaches that you learned in the class. Here
are some basic guidelines:
• Make sure to follow the standard practice in building and evaluating predictive machine 
learning models, i.e., training-validation split, training-validation-testing split, or cross-validation;
• Explore different modeling techniques. For each modeling technique, explore different 
parameter combinations;
• Consider feature selection;
• Note that this is an imbalanced dataset, i.e., the adopters only account for less than 2% of 
the population. Therefore, you may also consider sampling techniques to deal with 
imbalanced data;
• A starter R Script is also provided, which contains a very simple Naïve Bayes model that 
achieves F-measure of 0.0986 for the “adopter = 1” class. This baseline should be fairly 
easy to beat.
Model Performance Assessment
To assess the out-of-sample performance of your model, you will also be provided with an 
unlabeled dataset of another set of 86,681 users with the same attributes as described above, 
except this dataset does not have the outcome labels. No more than once per calendar day, you 
can use your current best model to predict outcomes in this dataset and email the predictions to the 
instructor. Your predictions should come in a .csv file named “X-Submission.csv” (replace X with 
your name) with two columns: user_id and prediction, where the user_id column must match the 
user IDs in the unlabeled dataset, and prediction column contains binary (0/1) predictions for each 
user. Prediction files that do not follow this format will not be scored.
Upon receiving your predictions, the instructor will score your prediction against actual outcome 
labels and will email you back your model’s performance. The best-to-date performance will be 
continuously updated on the leaderboard page on Canvas. The scoring metric used for this 
project is the F-measure for the “adopter = 1” class. The individual predictions will be accepted 
by the instructor until end-of-day on December 5th.
Evaluation: 15 points total
• Performance: This is based on two aspects: (1) the final performance achieved by your best 
reported model, and (2) the diversity of techniques, methodologies, and approaches you have tried 
(i.e., there will be a penalty if you only tried a small number of models)
