# Cryptocurrencies
Data Bootcamp week 19 - Unsupervised Machine Learning

## Overview of Project
This independent challenge exercise involved processing data before running unsupervised machine learning models and producing visualizations of that data, which was information about various cryptocurrencies.

Specific steps consisted of:

* Loading data provided in [this csv file](https://github.com/larabjork/cryptocurrencies/blob/main/crypto_data.csv);
* Cleaning the data by dropping rows with at least one null value, dropping columns that did not pertain to the analysis, and creating a new dataframe to save the names of cryptocurrencies separately, for later use;
* Using StandardScaler to standardize all features;
* Reducing the dimensions of the data with Principal Component Analysis;
* Using the K-means algorithm to create an elbow curve to find the best K value, then using that value to predict K clusters in the data;
* Concatenating the scaled dataframe with the dataframe that held coin names; 
* Creating a 3D scatter plot of the clustered and scaled data, plotting Total Coin Supply against Total Coins Mined, ordered by Class, showing the Coin Name and Algorithm on hover; and
* Creating a 2D scatter plot of the clustered and scaled data, plotting Total Coin Supply against Total Coins Mined, ordered by Class, showing the Coin Name on hover.

## Results
Before data clean-up, there were 1,252 rows of data; after all processing steps were complete, 532 remained.

The elbow curve revealed that the best value for K in the K-means algorithm was 4, as shown below:

![screenshot of line graph with sharp bend at x=4](https://github.com/larabjork/cryptocurrencies/blob/main/images/elbowcurve.png)

Using plotly.express to generate a 3D scatter plot resulted in the following:

![screenshot of 3D scatter plot, showing data in four clusters](https://github.com/larabjork/cryptocurrencies/blob/main/images/3dplot.png)

Using pandas.hvplot to generate a 2D scatter plot resulted in the following:

![screenshot of 2D scatter plot, showing data from four classes](https://github.com/larabjork/cryptocurrencies/blob/main/images/scatter_plot.png)

## Summary

The stated aim of this challenge was to produce a report summarizing what cryptocurrencies are on the trading market and how they could be grouped to create a classification system. Using unsupervised machine learning was a viable strategy to produce the needed information, because at the outset, it was not known how many groups there should be or what criteria should be used to create them. 
