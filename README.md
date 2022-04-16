# Cryptocurrencies

## Overview :
Accountability Accounting is interested in offering a new crypocurrency investment portfolio for its customer. We had to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

### Preprocessing the Data for PCA:
The following five preprocessing steps were performed on the crypto_df DataFrame:
* All cryptocurrencies that were not being traded were removed. 

    ![image](./IMAGES/nontrading.PNG)

* The IsTrading column was dropped. 

    ![image](./IMAGES/istrading_removed.PNG)

* All the rows that have at least one null value were removed. 

    ![image](./IMAGES/NaN.PNG)

* All the rows that do not have coins being mined were removed. 

    ![image](./IMAGES/no_coin.PNG) 
    
* The CoinName column was dropped. 

    ![image](./IMAGES/coin_removed.PNG)

* Created CoinName Dataframe:

    ![image](./IMAGES/coin_df.PNG)

### Reducing Data Dimensions Using PCA:

* Applied PCA to reduce the features to 3 principal components.

* Created DataFrame with column PC 1, PC 2, PC 3 & index from Crypto dataframe.

    ![image](./IMAGES/pca.PNG)

### Clustering Cryptocurrencies Using K-means :

* Created elbow curve to find the best K. 

    ![image](./IMAGES/elbow.png)

* Used the PCA dataframe to run the K-means algorithm to make the prediction pf the K clusters for the cryptocurrencies' data.

* Created new dataframe by merging the crypto dataframe & pca dataframe. Added the index, CoinName & class to the dataframe. 

    ![image](./IMAGES/clustered_df.PNG)

### Visualizing Cryptocurrencies Results :

* Created 3D scatter plot.

    ![image](./IMAGES/3Dscatter.png)

* Created a table using hvplot.table() & calculated the total number of rows.

    ![image](./IMAGES/hvplot_table.PNG)

* Using MinMaxScaler.fit_transform, created new dataframe.

    ![image](./IMAGES/plot_df.PNG)

* Created the scatter plot. 

    ![image](./IMAGES/scatter.png)
    





