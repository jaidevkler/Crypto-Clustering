# CryptoClustering
In this Challenge, we apply your the K-means algorithm and principal component analysis (PCA) to classify cryptocurrencies according to their price fluctuations across various timeframes. Specifically, we examine price changes over intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days, and 1 year.

## Code Source
The code location is: [Click Here to view](https://github.com/jaidevkler/CryptoClustering)<br />

## Files
forecasting_net_prophet.ipynb [Click here to view](https://github.com/jaidevkler/CryptoClustering/blob/main/Crypto_Clustering_starter_code.ipynb)<br />

## How to run the program
Download the files and then use jupyter notebook or jupyter lab to open the Crypto_Clustering_starter_code.ipynb file.<br />

## Activity

### 1. Prepare the Data
* Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.
* Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.<br />

### 2. Find the Best Value for k Using the Original Scaled DataFrame
* Use the elbow method to find the best value for k by completing the following steps:
* Create a list with the number of k values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a for loop to compute the inertia with each possible value of k.
* Create a dictionary with the data to plot the elbow curve.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.<br />

### 3. Cluster Cryptocurrencies with K-Means Using the Original Scaled Data
* Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
* Initialize the K-means model with the best value for k.
* Create an instance of K-means, define the number of clusters based on the best value of k, and then fit the model using the original scaled DataFrame.
* Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
* Create a copy of the original data and add a new column with the predicted clusters.
* Create a scatterplot using pandas’ plot as follows:
* Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".<br />

### 4. Optimize Clusters with Principal Component Analysis
* Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
* Retrieve the explained variance to determine how much information can be attributed to each principal component and then answer the following question in your notebook:
* Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.<br />

### 5. Find the Best Value for k Using the PCA Data
* Use the elbow method on the PCA data to find the best value for k using the following steps:
* Create a list with the number of k-values from 1 to 11.
* Create an empty list to store the inertia values.
* Create a for loop to compute the inertia with each possible value of k.
* Create a dictionary with the data to plot the elbow curve.
* Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.<br />


### 6. Cluster Cryptocurrencies with K-Means Using the PCA Data
* Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
* Initialize the K-means model with the best value for k.
* Create an instance of K-means, define the number of clusters based on the best value of k, and then fit the model using the PCA data.
* Predict the clusters to group the cryptocurrencies using the PCA data.
* Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
* Create a scatte rplot using pandas’ plot as follows:
* Set the x-axis as "PC1" and the y-axis as "PC2".<br />

### 7. Determine the Weights of Each Feature on Each Principal Component
* Create a DataFrame that shows the weights of each feature (column) for each principal component by using the columns from the original scaled DataFrame as the index.

## Reference
Columbia AI Bootcamp - Module 8 Challenge
