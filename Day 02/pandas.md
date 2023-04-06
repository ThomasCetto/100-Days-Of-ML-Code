# Pandas

## Definitions
*Series:* one dimensional object, it's like a column of a table

*Dataframe:* two dimensional object, it's like a table

## Creation
```
serie = pd.Series([1, 2, 3, np.nan, 1, 9])

df = pd.DataFrame({
    "A": [1,2],
    "B": ["hey", "oo"],
    "C": [4.44, 3.14],
}, index = ["Row1", "Row2", "Row3"]
)

df = pd.DataFrame(data=iris.data, columns=iris.feature_names)
df['target'] = iris.target


df = pd.read_csv('data.csv')
df.to_csv("foo.csv")  # writing
```

## Visualization
```
df.head()
df.tail()
df.index  # row label
df.columns  # column labels
df.describe()  # shows information about the table
df.T  # transposition
df.sort_index(axis=)
df.sort_values(by="columnName")
```

## Indexing 
```
- label-based: 
    - df.loc("X")  # row with label X
    - df.loc(:, "X") #  values of the column with label X
- position-based:
    - df.iloc([0])  # row
    - df.iloc([:, 1])  # column
- boolean indexing:
    - df[df["A"] > 1 | df["B"] < 3]  # all rows where the column A is > 1

For single values: 
df.at(row_label, col_label)
df.iat(row_ind, col_ind)
```

## Missing data
```
df.dropna(how="any")
df.fillna(value=5)
df.isna()

# count number of na:
df.isna().sum()
```

How to get the name of each column with the corresponding number of na values in that column
```
missing_values = df.isna().sum()

for col, num_missing in missing_values.iteritems():
    print(f"{col}: {num_missing}")
```

How to get the number of rows that have at least one na
```
missing_rows = df.isna().any(axis=1).sum()
```

## Operations
```
df.mean()
df.mean(1)  # specify axis  
df.apply(lambda x: x.max() - x.min())
```

## Plotting
```
import matplotlib.pyplot as plt
df.plot(x="col", y="col", kind="scatter")  # kind = hist, bar...
```

# Remove
```
df = df.drop("age", axis='columns')  # removes the column "age"
# or
df = df.drop("age", axis=1)

df = df.drop(3) # removes the 4th row

df = df.dropna(axis=0/1, how='any/all', inplace=True, subset=["column_name"])
"""
# 0 if rows, 1 if columns
# any if you want to remove the row if it has any NA, all if every value is NA
"""
```

# Replace
```
df = df.fillna(value)
df["column_name"].fillna(value, inplace=True)
df[["B","C"]].fillna(value, inplace=True)
```