The goal of this project is to create a machine learning model that is capable of classifying candidate exoplanets from a raw dataset collected by the NASA Kepler space telescope.

I trained and tested 3 models.

Model 1 used MinMaxScaling and a logistic regression and returned an acceptable score of 0.681. I attempted to optimize the model using a GridSearchCV model, unfortunately this only increased the score to 0.685.

Model 2 used MinMaxScaling and an SVC Model which returned a disapointing score of 0.432. I also attempted to optimize model 2 with a GridSearchCV model. I attempted to run the GridSearchCV several times with different parameters but each time I attempted to run the code to train the model it continued to run for an excessive amount of time (I stopped it after 6 hours). For that reason I decided to create a 3rd model with a different approach.

Model 3 used MinMaxScaling, Label Encoding, One Hot Encoding and then a Deep Learning Model with 3 layers totaling 14,103 parameters. This model had an accuracy rate of 0.738 and a prediction score of 0.624.

Models 1 and 3 both show potential for use predicting planets but need to further tuned. One possible factor that might impact the model accuracy is the skew of the data, there are nearly double the number of false positives as there are either confirmed or candidate, using a sampling model to adjust for that skew might improve the predictive accuracy of the model.
