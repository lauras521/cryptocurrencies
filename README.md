# Cryptocurrency Analysis

## Overview

### Purpose
Martha is a senior manager for the Advisory Services Team at Accountability Accounting.  This client is a prominent investment bank and wants to offer a new cryptocurrency investment portfolio for its customers.  This project will create a report to include cryptocurrencies that are on the marked now and how they can be grouped and classified for new investments.  

## Analysis and Results

### Analysis
This project uses unsupervised learning to process and cluster cryptocurrency data for 532 tradeable currencies.  A dataset of cryptocurrencies was read in from a CSV file and the Pandas library was used to clean the data.  Data was transformed and scaled for analysis.  Data dimensions were reduced to 3 principal components using PCA.  An elbow curve was generated to determine the optimal number of groups and data was displayed using 3D and 2D scatter plots.  

### Results
The Elbow curve showed 4 groups should be created.  

<p align="center">
  <img src = https://github.com/lauras521/cryptocurrencies/blob/30c858ac5384d057644e5399cf035461b18fed72/Resources/elbow_curve.PNG>
</p>

Hvplot_table was used to have a user friendly view of the raw data.

<p align="center">
  <img src = https://github.com/lauras521/cryptocurrencies/blob/30c858ac5384d057644e5399cf035461b18fed72/Resources/hvplot_table.PNG>
</p>

A 3D scatter plot was created for the 3 principal components to visualize all 4 classes. 
<p align="center">
  <img src = https://github.com/lauras521/cryptocurrencies/blob/30c858ac5384d057644e5399cf035461b18fed72/Resources/3D_PCA_Scatter_Plot.PNG>
</p>

A 2D scatter plot was created for the scaled Total Coin Supply and Total Coin Mined data to visualize all 4 classes. 
<p align="center">
  <img src = https://github.com/lauras521/cryptocurrencies/blob/30c858ac5384d057644e5399cf035461b18fed72/Resources/D4_scatter_plot.PNG>
</p>


### Summary
The elbow curve indicates 4 classes of data.  Classes 1 and 3 do not have many points (i.e. class 1 = 1 point and class 3 = 2 points).  Visualizations of the classes were displayed using different plotting techniques.  I would recommend further reviewing the following Coin Names to ensure their data is accurate.

* LCC = LitecoinCash = Class 3
* WAVES = Waves = Class 3
* BTT = BitTorrent = Class 1
* TRTL = TurtleCoin = Class 2 (highest point on total_coin_supply_scaled y-axis, right up by 1)

Without these 4 points it would be interesting to see how the data is modeled.  Currently the PCA explained variance is low and it would be good to know if that increases or changes without these points.  

## Resources
[link to code](https://github.com/lauras521/cryptocurrencies/blob/aacfb4bef9bb33d145d47081f9cd1447125c89c5/crypto_clustering.ipynb)
