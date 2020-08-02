# Cryptocurrencies Challenge Module 18
## Summary
The idea with this challange is to provide how cryptocurrencies could be grouped to create a classification for development a new investment product for a Bank.  The dataset includes the coin name, algorithm, if the coin is trading, proof type, total coins mined and total coin supply.  Since there is no known output, we will use unsupervised machine learning models, in this case we use PCA and clustering using K-means.

## Data Processing
- We prepared the data to run the PCA and clustering using K-means.
- We removed all cryptocurrencies that are not trading, with at least one null value, without coins mined.  We removed the trading column and set a new index, in this case the "Symbol" columns was assigned as new Index.  Finally we dropped the coin name column.
- We created the dummies variables using the get_dummies for the no numeric columns.  We got 100 columns.
- We used the StandardScaler from sklearn to standardize all of the data.
- We applied the PCA algorithm from sklearn to reduce the dimensions of the DataFrame with 100 columns down to three principal components.
- After getting the 3 main components from PCA algorithm, we used the K-means algorithm from sklearn to cluster the cryptocurrencies using the PCA data. 
