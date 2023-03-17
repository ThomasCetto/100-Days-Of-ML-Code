# Introduction to Machine Learning
*Artificial Intelligence:* The goal is to simulate human behaviour.

*Machine Learning:* Resolves problems by making predictions and classifications using some data.

## Types of Machine Learning
*Supervised learning:* data does have labels associated (e.g. classify images of animals).

*Unsupervised learning:* data does not have labels and learns about patterns in data (e.g. understand that a group of image have something in common).

*Reinforcement learning:* the model learns with rewards and penalties (e.g. with videogames).

## Data
*Feature vector:* the model's input data

Input (Feature Vector): 
- *Categorical (or qualitative):* finite number of categories (e.g. gender or nationality)
    - Nominal data: no inherent order (the values are different from eachother, one-hot encoding [0, 1, 0, 0])
    - Ordinal data: inherent order (e.g. how happy are you from 1 to 10)
- *Quantitative (or numerical):* a number

Output (target)
- In supervised learning: 
    - Classification: multiclass (pizza, ice cream, pasta) or binary (pizza or not pizza)
    - Regression: predict values (e.g. stocks, temperature...)


## Performance

### Error 
The difference between our output and the real values 
- L1 loss (mean absolute error): loss = sum(|yreal - ypredicted|)
- L2 loss (mean squared error): loss = sum((yreal - ypredicted) ^ 2)
- Binary cross-entropy loss

### Accuracy
Percentage of how many output we got right.
