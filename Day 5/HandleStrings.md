# Strings in datasets
Often in datasets there are strings. These strings can't be used when working with machine learning models, so you have to handle them in a different way using these techniques:

## Label Encoding
If a column contains three categories (red, green, blue), label encoding would assign the integers 0, 1 and 2 to these categories. In scikit-learn there is a LabelEncoder class: 
```
from sklearn.preprocessing import LabelEncoder

le = LabelEncoder()
df['my_column_encoded'] = le.fit_transform(df['my_column'])
```

To get back to the original data:
```
decoded_data = le.inverse_transform(encoded_data)
```

## One-Hot Encoding
Similar to Label Encoding but if a column contains three categories (red, green, blue), label binarization creates three binary columns, one for each category.

For obvious resons it could lead to too high dimensionality, that reduces the performance and increases overfitting of the models.

```
from sklearn.preprocessing import OneHotEncoder

encoder = OneHotEncoder()
df_encoded = encoder.fit_transform(df['column_name'])
```
