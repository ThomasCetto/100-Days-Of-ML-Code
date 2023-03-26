# Unsupervised learning
Used when data has not pre-defined labels, and we want to classify by finding some commonality in the features.
It's main goal is to study the intrinsic structure of the data.

It is used for:
- Dividing datasets by some shared attributes
- Detecting anomalies that don't fit to any group
- Simplifing datasets by aggregating variables with similar attributes

It solves two kind of problems: 
- Clustering
- Dimensionality Reduction

## Clustering Analysis

The goal is to find different groups within the elements in the data. To do so, clustering algorithms find the structure in the data so that elements of the same cluster are more similar to each otehr than to those from different clusters.

![Visual example](https://miro.medium.com/v2/resize:fit:828/format:webp/1*UrTFgcUrxq5C-wOUFvxCkQ.png)

These algorithms are useful for real world problems such as anomaly detection, recommending systems, documents grouping or finding customers with common interests based on their purchases.

Some algorithms are:
- K-means
- Hierarchichal Clustering
- Density Based Scan Clustering of Applications with Noise (DBSCAN)
- Gaussian Clustering Model

### K-Means Clustering

These algorithms are very efficient, but are not very good to identify classes when dealing with groups that do not have a spherical distribution shape.

They aim to find and group in classes the data points that have high similarity between them. The closer the data points are, the more similar and more likely to belong to the same cluster they will be.

*Squared Euclidean Distance:*

![formula](https://miro.medium.com/v2/resize:fit:640/format:webp/1*svzWIVVO4k0tSu14pzSuFA.png)

*Cluster Inertia:*

The sum of Squared Errors within the clustering context

![formula](https://miro.medium.com/v2/resize:fit:640/format:webp/1*jO8AEM1Ttkc46ea7bIEl0Q.png)

Where μ(j) is the centroid for cluster j, and w(i,j) is 1 if the sample x(i) is in cluster j and 0 otherwise.

K-Means tries to minimize the cluster inertia factor.


Algorithm Steps:
1. First, we need to choose k, the number of clusters that we want to be finded.
2. Then, the algorithm will select randomly the the centroids of each cluster.
3. It will be assigned each datapoint to the closest centroid (using euclidean distance).
4. It will be computed the cluster inertia.
5. The new centroids will be calculated as the mean of the points that belong to the centroid of the previous step. In other words, by calculating the minimum quadratic error of the datapoints to the center of each cluster, moving the center towards that point
6. Back to step 3.


Problems:
- The output for any training won't always be the same, because the initial centroids are set randomly, and that influences the whole process.
- It's not suitable when dealing with clusters that have non-spherical shapes.

What to do before using it:
- Features must be measured on the same scale, by performing z-score.standardization or max-mmin scaling.
- When dealing with categorical data, we will use the get dummies function.
- Exploratory Data Analysis (EDA) is very helpful to have an overview of the data and determine if K-means is the most appropiate alogirthm.
- The minibatch method is useful when there are many columns, but it's less accurate.

How to choose the right K number:
- field knoledge
- Elbow method (better)

##### Elbow method

It is used for determining the correct number of clusters in a dataset. It works by plotting the ascending values of K versus the total error obtained when using that K.

% Variance = Variance between groups / Total variance

The goal is to find the k that for each cluster will not rise significantly the variance.
![explainatory image](https://miro.medium.com/v2/resize:fit:828/format:webp/1*86R1OByRi6JoLq1JPAUnpQ.png)

In this case above, K=3 is the best choice, because it's where the elbow is located.

![Examples of effects on different datasets](https://miro.medium.com/v2/resize:fit:828/format:webp/1*ykyaNxEi1QhICv8gbdI8aw.png)


### Hierarchical Clustering
The difference with the previous one is that it finds the K by itself. 

There are two approaches to this type of clustering:
- Divisive: it englobes all datapoints in one single cluster. The it splits the cluster iteratively into smaller ones until each one of them cnotains only one sample 
- Agglomerative: each sample is a different cluster and then it merges them by the ones that are closer from each other until there is only one cluster.

Algorithms used for agglomerative hierarchical clustering:
- *Single Linkage:* it computes the distances between the most similar members for each pair of clusters and merge the two clusters for which teh distance between the most similar members is the smallest.
- *Complete Linkage:* it compares the most dissimilar datapoints of a pair of clusters to perform the merge

Disadvantages of hierarchical clustering:
- They are very sensitive to outliers, and the model performance decreases significantly.
- They are computationally expensive

Comparison between K-means and Single Link Hierarchical
![k-means vs single link hierarchical](https://miro.medium.com/v2/resize:fit:1100/format:webp/1*HUOYokgnLlokcYvT2C4stg.png)

### Density-Based Spatial Clustering of Applications with Noise (DBSCAN)
It's another clustering algorithm useful to correctly identify noise in data.

It is based on a number of points with a specified radius and a special label assigned to each datapoint.

The logic of the algorithm:
1. Identify a core poiint and make a group for each one, or for each connected group of core points
2. Identify and assign border points to their respective core points

![Visualization](https://miro.medium.com/v2/resize:fit:640/format:webp/1*USv6WLj3A-9De9D7am2iZQ.png)

Advantages:
- No need to specify the number of clusters
- High flexibility in the shapes and sizes that the clusters may adopt
- Very useful to identify and deal with noise data and outliers

Disadvantages:
- Difficulties when dealing with border points that are reachable by two clusters
- Doesn't find well clusters of varying densities

Comparison between K-means and DBSCAN
![K-means vs BDSCAN](https://miro.medium.com/v2/resize:fit:828/format:webp/1*x48iVUvrWtYY31WEsVLdeQ.png)


### Gaussian Mixture Models (GMM)

...


## Clustering Validation
To evaluate the result of a cluster we apply cluster validation indices. There are 2 ways:
- External indices
- Internal indices


