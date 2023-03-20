# Decision Trees
They are used both for regression and classification. To create a tree it's needed to decide which features to choose and what conditions to use for splitting, and also knowing when to stop.
![img](https://miro.medium.com/v2/resize:fit:640/format:webp/1*XMId5sJqPtm8-RIwVVz2tg.png)

Feature are used to split the branch in two by imposing a clause, and each feature can be used for different "splits".

Advantages:
- Simplicity
- Can handle both numerical and categorical data
- Can be used both for regression and classification
- Non-linear relationships between parameters don't affect tree performance

Disadvantages:
- Risk of overfitting with too complex trees
- Risk of creating biased trees if some classes dominate, so the data needs to be balanced