# Pandas

## Definitions
*Series:* one dimensional object, it's like a column of a table

*Dataframe:* two dimensional object, it's like a table

## Creation
```
serie = pd.Series([1, 2, 3, np.nan, 1, 9])

df = pd.Dataframe({
    "A": [1,2],
    "B": ["hey", "oo"],
    "C": [4.44, 3.14],
}, index = ["]
)

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
df.plot()  # kind = scatter, hist, bar
```