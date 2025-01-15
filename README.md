# Crypto Clustering
**Overview**
The Crypto Clustering project aims to predict if cryptocurrencies are affected by 24-hour or 7-day price changes using unsupervised learning techniques, specifically K-means clustering. Additionally, the project explores the impact of dimensionality reduction using Principal Component Analysis (PCA) on clustering.

Dependencies
Python, pandas, NumPy, scikit-learn, hvPlot

Steps
1.Load and preprocess the data.
The raw data we used are returns from different periods and differenct crypto-currencies, as can be spot in the figure below. These returns are standarized before starting the analysis.
2.Scale the data using StandardScaler.
3.Find the best value for k using the elbow method.
Using K-Means, we find different levels of inertia associted to different number of clusters (k), and plot results in a line plot. Then apply the Elbow rule to decide which is the more appropiate and more efficient number of clusters in which to classify the data. In this case, k=4 is the best choice, since after that the reduction in inertia for applying a new cluster get significantly reduced.
4.Cluster cryptocurrencies with K-means using the original scaled data.
5.Perform PCA to reduce the features to three principal components.
6.Find the best value for k using the PCA data.
7.Cluster cryptocurrencies with K-means using the PCA data.
8.Visualize and compare the results using hvPlot.
Clusters are colored, and compared between original data and principal components for several terms. 

Results
The project includes the following visualizations:

1.Returns for several holding periods.
2.Elbow curve for the original data.
3.Elbow curve for the PCA data.
4.Scatter plot of cryptocurrency clusters based on the original data.
5.Scatter plot of cryptocurrency clusters based on the PCA data.

Note: Plots are saved in the plots folder

**Conclusion**
Our analysis of the dataset suggests that k=4 is the most suitable number of clusters for this dataset, as supported by the elbow method plot and scatter plot analysis.
The top three principal components account for approximately 90% of the total variance, and clustering by fewer components results in more well-defined clusters. 
Plotting the resulting clusters on the principal component analysis clarifies the separation between the second and third clusters, which were initially overlapped in the full feature plot. However, clustering by fewer components also loses focus on specific timeframes of interest. 
Ultimately, selecting the ideal number of clusters is subjective and requires domain knowledge and discretion.
