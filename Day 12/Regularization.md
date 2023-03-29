# Regularization techniques

*What:* It's a technique used in to prevent overfitting and improve the generalization performance of the model.

*Why:* Regularization helps to prevent that by adding a penalty term to the model's cost function that discourages it from learning complex or intricate patterns in the training data.

*How:* It is typically achieved by adding a regularization term to the cost function that penalizes the complexity of the model's parameters. Some of the techniques are L1 regularization (Lasso), L2 regularization (Ridge regression) and Elastic Net regulation (combination of L1 and L2 regularization).

### L1 regularization (or Lasso)

It adds a penalty term to the cost function that is proportional to the absolute value of the model's parameters. In this way, the model learns simple solutions that only use a subset of the available features.

It is used if you have a large number of features in the dataset, and you suspect that only a subset of them are important for the prediction. So it helps with selecting the features that are really relevant.


### L2 regularization (or Ridge regression)

It adds a penalty term that is proportional to the squared value of the model's parameters. In this way, the model learn small or smooth solutions that spread the weight evenly across all the features.

It is used when you want to spread the weight of the model evenly across all features, making it suitable when all the features in the dataset are potentially relevant for the prediction. 

### Net regularization

It combines L1 and L2 regularization, and provides a way to balance between the sparse and smooth solutions. It adds a penalty term that is a combination of the absolute value and squared value of the model's parameters.


*Overfitting:* it occurs when a model learns the noise and the random variation in the training data, instead of the patterns and relationships that generalize well to new data. 
