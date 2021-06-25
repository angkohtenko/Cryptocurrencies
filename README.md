# Overview of the analysis
I got a dataset with cryptocurrency retrieved from [CryptoCompare]( https://min-api.cryptocompare.com/data/all/coinlist). The goal of the project was to cluster cryptocurrencies using unsupervised machine learning algorithm.

To complete the project I’ve used python with pandas, sklearn, hvplot and plotly lybraries.


# Results
First of all, I preprocessed data: removed null values, dropped insignificant columns and created variables for the two text features using ```pd.get_dummies()```

![preprocessed_data](https://github.com/angkohtenko/Cryptocurrencies/blob/main/Images/preprocessed_data.png)

Next, I reduced data dimensions using CPA from 98 features to 3 principal components.

![3_PCs](https://github.com/angkohtenko/Cryptocurrencies/blob/main/Images/3_PCs.png)

I defined the best number of clusters plotting elbow curve.

![elbow_curve](https://github.com/angkohtenko/Cryptocurrencies/blob/main/Images/elbow_curve.png)

Then, I initialized the K-Means model and predicted a cluster for each cryptocurrency.

![predicted_class](https://github.com/angkohtenko/Cryptocurrencies/blob/main/Images/predictred_class.png)

To visualize clusters I’ve plotted 3D scatter plot with principal components as axises.

![cluster_viz](https://github.com/angkohtenko/Cryptocurrencies/blob/main/Images/cluster_viz.png)
