# Cross Validation
It's a technique used to assess the performance of a predictive model. It uses a portion of the data to train the model and the rest of the data to evaluate its performance.

## K-fold cross-validation
It's a type of cross validation; the data is divided into k equally sized folds. The model is then trained k times, each time each time using a different fold as the testing set and the remaining folds as the training set. The results from each of the k tests are then averaged to produce an overall estimate of model performance.

It can also help to identify potentail problems with overfitting, where the model performs well on the training data but poorly on the testing data.