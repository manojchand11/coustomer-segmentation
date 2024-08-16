# Customer-Segmentation-using-Kmeans
### Overview
This project performs customer segmentation on a dataset using the K-Means clustering algorithm. Customer segmentation is crucial for businesses to target specific groups and allocate marketing resources effectively. By analyzing historical customer data, we can group customers with similar characteristics, allowing businesses to tailor their strategies for different customer segments

### Pre-processing
##### Feature Selection:
- The Address and Customer Id columns are dropped as they are not useful for clustering.
- The Address is a categorical variable, and Customer Id is just an identifier.
##### Normalization:
- Data is standardized using StandardScaler to ensure that all features contribute equally to the clustering process. This is crucial because K-Means is distance-based, and features on different scales can bias the results.
##### Handling Missing Values:
- NaN values are replaced with 0, and infinity values are replaced with the largest or smallest finite numbers.
### Modeling
##### Choosing the Number of Clusters:
- Elbow Method: This method helps determine the optimal number of clusters by plotting the within-cluster sum of squares (inertia) against the number of clusters and identifying the "elbow" point where inertia starts decreasing more slowly.
- Silhouette Score: This metric evaluates the quality of clusters by measuring how similar a data point is to its own cluster compared to other clusters. A higher silhouette score indicates better-defined clusters.
##### K-Means Clustering:
Applied K-Means with the optimal number of clusters determined from the Elbow Method and Silhouette Score.
Evaluated the clustering results using inertia and silhouette score for different numbers of clusters.

### Results
##### Cluster Labels:
Each customer is assigned a cluster label indicating the segment to which they belong.
##### Cluster Profiles:
Average feature values for each cluster are computed to understand the characteristics of each segment.
##### Visualizations:
Scatter plot and 3D plot are provided to visualize the distribution of customers based on key features such as Age, Income, and Education.
### Insights
Based on the clustering results, customers can be grouped into distinct segments with common demographic characteristics. For example, segments might include:
- Affluent, Educated, and Old-Aged: Customers with higher income, education levels, and older age.
- Middle-Aged and Middle Income: Customers with moderate income and age.
- Young and Low Income: Younger customers with lower income.
###### These profiles can help in tailoring marketing strategies and improving customer targeting.
