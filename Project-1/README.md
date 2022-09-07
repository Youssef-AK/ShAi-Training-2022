Project Unsupervised Learning titled (Credit Card Customer Segmentation)

Developing a customer segmentation model to segment the credit card customer base by similar behavior and usage patterns, which allows businesses utilizing such models to form a better understanding of their customers needs and desires, closely aligning their strategy and tactics with their customers, enabling their products to be marketed and sold more effectively.

I worked with Mohammad Almasri firstly make a good EDA on our dataset and understand the features (data types, null values, distributions, etc.) and write some useful notes.
Then we noticed some problems like > null values in two columns and skewness on most of our columns/features
So, we check if there is any pattern for missing values, and concluded with some Missing not at Random so Imputed with appropriate values based on analysis,
and some values were Missing at Random so imputed with Multivariate imputer
* Remove ineffective missing (1 row )

for skewness we transform our data with Log-Transformer & Powertransformer they worked fine (as usual we tried other transformers but didn't work like log, power transformers) to make approx. all information is equality represented (as we can see from the below graph.)

Down to Clustering Algorithms we chose different clustering methods that have different inferences and computations of what constitutes a cluster and how to efficiently find them, which allows us to observe various approaches to inferring clusters from the data.

the following methods that were used :
* K-means: centroid model of clustering, fast and efficient.
  - Init: k-means++ / algorithm: auto
* Agglomerative Hierarchical: Hierarchical Model of clustering, efficient and suitable for specific kinds of data clusters
  - affinity: Euclidean / linkage: ward (variance-based)
* Meanshift: density model of clustering, computation-heavy
  - bandwidth: 3.63
* DBSCAN: density model of clustering, identifies outliers as noise
  - metric: Euclidean / algorithm: auto
* Expectation-Maximization Clustering: Distribution Model of clustering, flexible and fast
  - n_components : 4

As an Example : We can see how K-Means clustered our customers to 4 Groups and how well it is balanced.

for more information kindly check the full project on Drive : https://lnkd.in/dmQfA5sn
