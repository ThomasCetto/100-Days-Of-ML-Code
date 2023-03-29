# Gradient Descent

It is an algorithm used to find the best values for the model's parameters (not hyperparameters) that minimize the error between the predicted output and the actual output. 

It works by starting with some randomly chosen values for the model's parameters. The it uses the data to measure how far off the predictions are from the actual output (the loss function).

It helps us adjust the values of the model's parameters to minimize the loss function. It does this by finding the slope of the loss function at the current values for the parameters. Then it uses other values for the parameters in the direction that decreases the loss function the most. It repeats this process many times, until it reaches the point where changing the parameter values won't make the loss function any smaller. 