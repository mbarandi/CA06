# CA06
Customer Segmentation Analysis
This project aims to perform customer segmentation analysis on a dataset of mall customers using K-means clustering algorithm. The dataset used in this analysis is obtained from the following URL: "https://github.com/ArinB/MSBA-CA-Data/raw/main/CA06/Mall_Customers.csv".

Dataset and Attributes
The dataset contains information about mall customers and has the following attributes:

CustomerID: Unique identifier for each customer
Genre: Gender of the customer (Male or Female)
Age: Age of the customer
Annual Income (k$): Annual income of the customer in thousands of dollars
Spending Score (1-100): Score indicating customer's spending behavior (1-100, higher score indicating higher spending)
Data Preprocessing, Feature Selection, and Scaling
The following steps were taken for data preprocessing, feature selection, and scaling:

The CSV file was read into a pandas DataFrame using the provided URL.
Descriptive statistics (mean, median, standard deviation, etc.) were calculated using the describe() function to understand the spread of the data.
The size of the dataset was determined using the shape attribute to get the number of rows and columns.
The data types of each column were checked using the dtypes attribute.
Missing values in the dataset were checked using the isnull() function and no missing values were found.
Histograms were created for each variable using the histplot() function from Seaborn library to visualize the distribution of data.
Boxplots were created for each variable using the boxplot() function from Seaborn library to identify any outliers or anomalies in the data.
The 'Annual Income (k$)' and 'Spending Score (1-100)' columns were scaled using StandardScaler from Scikit-learn library to normalize the data.
Determining Optimal Number of Clusters
The optimal number of clusters was determined using the Silhouette method. The following steps were taken:

A loop was used to fit KMeans models with varying number of clusters (ranging from 2 to 10).
For each model, the average Silhouette score was computed using the silhouette_score() function from Scikit-learn library.
The Silhouette scores were stored in a list.
The number of clusters with the highest Silhouette score was considered as the optimal number of clusters.
Clustering and Cluster Characteristics
The KMeans clustering algorithm was used to cluster the customers into different segments. The following steps were taken:

A KMeans model was initialized and fitted with the optimal number of clusters determined earlier.
Cluster assignments were predicted for each data point using the predict() function.
A scatterplot was created using Seaborn library to visualize the clusters, with 'Annual Income (k$)' on x-axis, 'Spending Score (1-100)' on y-axis, and cluster assignments represented by different colors.
Cluster characteristics were calculated by taking the mean of 'Annual Income (k$)' and 'Spending Score (1-100)' for each cluster using the groupby() function.
Insights and Recommendations
Based on the analysis, the following insights and recommendations can be made:

The optimal number of clusters for customer segmentation is 5, as determined by the highest Silhouette score.
Cluster 0 has customers with low annual income and low spending score, indicating potential for low-spending customers.
Cluster 1 has customers with high annual income and low spending score, indicating potential for high-income but low-spending customers.
Cluster 2 has customers with moderate annual income
