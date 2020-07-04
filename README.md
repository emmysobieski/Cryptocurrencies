# Cryptocurrencies

## Challenge

## Project overview
##Ingest and preprocess data to remove unnecessary columns as well as rows with null values
1) Remove all cryptocurrencies that aren’t trading.
2) Remove all cryptocurrencies that don’t have an algorithm defined.
3) Remove the IsTrading column.
4) Remove all cryptocurrencies with at least one null value.
5) Remove all cryptocurrencies without coins mined.
6) Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
7) Remove the CoinName column.
8) Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
9) Use the StandardScaler from sklearn (Links to an external site.) to standardize all of the data from the X DataFrame. Remember, this is important prior to using PCA and K-means algorithms.Remove the descriptive column (coin name) in order to run unsupervised ML on the data

## Use PCA to determine the best number of K values
1) I reduced Data Dimensions Using PCA
2) I used the PCA algorithm from sklearn (Links to an external site.) to reduce the dimensions of the X DataFrame down to three principal components.
3) I created the DataFrame named “pcs_df” that includes the following columns: PC 1, PC 2, and PC 3. Use the crypto_df.index as the index for this new DataFrame.

#### Clustering Cryptocurrencies Using K-means
1) I used the KMeans algorithm from sklearn to cluster the cryptocurrencies using the PCA data, using an elbow curve to find the best value for K.
2) I ran the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. 
3) Then I created a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class, and has 10 rows with the headings: 42, 404, 1337, BTC, ETH, LTC, DASH, XMR, ETC, and ZEC.

#### Visualize Results
1) I created a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. 
2) I created a data table with all the current tradable cryptocurrencies. 
3) I created a scatter plot using hvplot.scatter to present the clustered data about cryptocurrencies.
