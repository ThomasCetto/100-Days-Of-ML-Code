# Exploratory data analysis (EDA)

It's a process where a number of techniques are used to better understand the dataset begin used, and also to clean up a dataset.

That includes:
- Extracting the important variables and excluding the useless ones
- Identifying outliers, missing values
- Understanding relationships between variables (if there are)

The steps are:
1. Understanding the variables
2. Cleaning the dataset
3. Analyzing relationships between variables

### Undestanding the variables

- Merging values together if they are very very similar, for example "cloudy", "grey", "mostly cloudy", "cloudy with a chance of rain"... into "cloudy".


### Cleaning the dataset

- Removing redundant or useless columns
- Removing columns that have too many null values
- Removing outliers
- Removing rows with null values


### Analyzing relationships between variables

##### Correlation matrix 
```
corr = df_cleaned.corr()# plot the heatmap
sns.heatmap(corr, xticklabels=corr.columns, yticklabels=corr.columns, annot=True, cmap=sns.diverging_palette(220, 20, as_cmap=True))
```

!(heatmap)[https://miro.medium.com/v2/resize:fit:828/format:webp/0*zSbFQ2v2rkwvTbeX.png]

If the value > 0, the increase of the label on the row leads to an increment of the label on the column.

The opposite happens if value < 0.


##### Scatterplot

```
df_cleaned.plot(kind='scatter', x='odometer', y='price')


# To create catterplots between every variable

sns.pairplot(df_cleaned)
```

##### Histogram 

To explore variables by themselves

```
df_cleaned['odometer'].plot(kind='hist', bins=50, figsize=(12,6), facecolor='grey',edgecolor='black')
```
##### Boxplot
```
df_cleaned.boxplot('price')
```

