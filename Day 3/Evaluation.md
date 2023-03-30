# Evaluation of a model

## Train/Test/Validation split
It's important to not train the model on the entire dataset, to prevent the possibility of overfitting to the training set. A good split is 70% for the training and 30% for the testing.

Also, you can use 20% of the dataset (60 20 20) for the validation. 
The difference between the test and validation dataset is that the validation it's used during the trining phase of a machine learning model to assess its performance and prevent overfitting. This allows the model to be tuned and optimized.
The testing is used to evaluate the final performance of a trained model. After the model is trained and optimized using validation, it is evaluated again. The testing set provides a final estimate of how well the model is likely to perform on new data.

The data needs to be shuffled for an accurate representation of the dataset.

## Classification metrics
There are 4 types of output that our classification model can give:
- True positives: it says that it belongs to a class and it's right
- True negatives: it says that it doesn't belong to a class and it's right
- False positives: it says that it does belong to a class and it's not true
- False negatives: it says that it doesn't belong to a class and it's not true

These can be plotted on a confusion matrix.

The three main metrics used to evaluate a classification model are:
- Accuracy: percentage of correct predictions for the test data
- Precision: true positives / true positives + false positives
- Recall: true positives / true positives + false negatives

Example: 1% of the popolation has diabetes and 99% has not.

If we always say that a person has not diabetes, we get an accuracy of 99%, even if the model is terrible.

Precision ensures that we're not misclassifying too many people as having the disease when they don't.

Recall ensures that we're not ovelooking the people who have the disease

### f-score
It's used to give a score to the model using it's precision and recall.

It uses a β value to change the importance of the two metrics. With β < 1 the precision is more important and else the recall is more important



## Regression metrics

- Mean squared error
- R^2 coefficient


How to print a pretty confusion matrix:
```
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.metrics import confusion_matrix

# Create a sample confusion matrix
cm = confusion_matrix(y_true, y_pred)

# Create a heatmap with the confusion matrix
sns.heatmap(cm, annot=True, cmap='Blues', fmt='g', xticklabels=['class 0', 'class 1'], yticklabels=['class 0', 'class 1'])

# Add labels and title
plt.xlabel('Predicted label')
plt.ylabel('True label')
plt.title('Confusion matrix')
plt.show()

```