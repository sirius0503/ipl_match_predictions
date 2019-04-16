# ipl_match_predictions

Project on predicting which team will win the match
Machine Learning , Python, Jupyter Notebook, Scikit-Learn · It predicts the result of cricket match played between two teams :
Team1 and Team2, .ie, who wins? 

There are total 10 teams in the competition and are playing in round robin format just like the IPL with away and home matches.


The dataset has features such as City of Match, Day, Avg Wind Speed, Avg Humidity, Inn 1 Team 1 Total 4s, Inn 1 Team 1 Total 6s
, Inn 1 Team 2 wickets taken_catches_runout and other similar stats for the two teams. In total 29 features are present.

Firstly since their were 29 different features, I started to plot different pandas, matplotlib, seaborn plots like correlation
maps, density distribution plots (kde), etc to find out which categorical variables are correlated to the target labels, heat
maps weren't useful enough since the number of variables were too large, then since the dataset was balanced, I used accuracy 
as the metric for classification success. I used random forest classifier to understand which features were the most important; then reduced the number of features according to the variance of the variables using SelectModel. I then used 5-fold cross validation, to understand the worst performance of the model and the average performance expected.

I used k-nearest neighbors as a reasonable baseline model. Then used SVM with rbf kernel, and parameter gamma searched using
gridsearch. I got a classification accuracy of 92%. Also, used logistic regression classifier to get the
likelihood(probabilities) for the matches using predict_proba method.
