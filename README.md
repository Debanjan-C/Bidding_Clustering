# Bidding Cluster Project

## Repository Navigation
<pre>
Technical Notebook         : <a href=https://github.com/Debanjan-C/Bidding_Clustering/blob/main/Notebooks/Technical%20Notebook.ipynb>Technical Notebook</a>
Code                       : <a href=https://github.com/Debanjan-C/Bidding_Clustering/blob/main/Notebooks/Code.ipynb>Code</a>
Data                       : <a href=https://github.com/Debanjan-C/Bidding_Clustering/blob/main/Data/Shill%20Bidding%20Dataset.csv>Data</a>
Data Web                   : <a href=https://www.kaggle.com/aishu2218/shill-bidding-dataset>Data Web</a>
</pre>

## Table of Contents
[Repository Navigation](#repository-navigation) -
[Overview](#overview) -
[Business Goals](#business-goals) -
[Motivation and Background](#motivation-and-background) -
[Data](#data) 
[Contributor](#contributor)
[Software Requirements - Packages used](#software-requirements--packages-used) -
[Reference and contribution](#reference-and-contribution)

## Overview
This project is about a Shill bidding and the dataset was retrieved from popular bids made in ebay and they made an analysis on multiple factors and assigned scores like bid ratio for each auction item, the tendency or how many times the bidder bids for a product, the number of hours for auctions, winning percentage, etc. According to those results, they use many conditions to verify if the bids are authentic or not. Shill bidding occurs when an user may mask his identity, or they would bid to a point where they could bid up to an unordinary limit and it ususally may benefit them or they can encourage others to bid at that rate. This is a new concept for me and I found it overall interesting to understand how it works and how can one be accused of shill bidding as it is not easy to evaluate. For this project, I work in a tech consulting firm that is working closely with an investigative agency to evaluate whether  Our dataset has 6321 rows and 13 columns. However, we drop one of the columns called 'action' column as that columns shows the target values and in unsupervised learning, we do not use target values in the modelling. Following that step, we check whether we have null values of duplicates for further data cleaning and preparation. The next step after this was Feature Engineering where we use label encoders to specific columns that are categorical and apply a transformation to convert all of the variables to numeric categorical values. I decided to scale our dataset to ensure our datas are in the same range and also felt that it was important to perform dimensionality reduction using Principal Component Analysis ans reduce any redundancy or additional dimensions in the dataset. I felt that would help us get a better understanding when we go to the clustering step. I chose to use 3 number of clusters as that seemed to be the cest in terms of the Kelbow Visualizer graph where we used it to measure it by the silhouette metric.  That metric is calculated by computing the difference between the mean of one cluster point with the other divided by the maximum of both mean scores. Next, I used K-Means cluster and Agglomerative Hierarchical Clustering to cluster our dataset into different types of sections to evaluate if the clusters can help identify different cases of shill bidding and if any form of unauthentic bidding took place. We used the silhouette metric to develop a Kelbow visualizer to show which cluster would be the best appropriate compared to the others. Therefore, we used silhouette scores to evaluate the better clustering algorithm amongst the two of the modelling algorithms. It seems that KMeans algorithm performed better than the Hierarchiacal clustering algorithm by 3 percentage points. Our data science goals is to identify which clustering model would return a better score in terms of how the clustering is performing and how that may reflect on how we identify whether a bidding is authentic or not. However, the overall scores are a little low and that may be troublesome when we identify cases of shill bidding. However, looking at the current scores, I felt that KMeans would be the best as it gave us a slighlty better result.



## Business Goals
For this project, I work as an ML Engineer in a tech consulting firm where they have a government contract with and investigation agency. There was a recent event where an auction had taken place on the ecommerce site - abc.com. They were auctioning all of there popular products and the investigative agency got a report of suspected shill bidding where unauthentic bidding has taken place. According to coin word, shill bidding is when the seller or any of the sellers agents will bid up to a lot and they would bid to a point where they could bid up to an unordinary limit and it ususally may benefit them indirectly or they can encourage others to bid at that rate. Many shill bidders mask there identiity and it happens often in online bids where they may use a different server, router to prevent their original ip address form being visible. Therefore, there was a supected event of that in the recent bids. The Investigation agencies retreived the data sets that contain details of individuals who conducted biddings, what price they bid and made further analysis on what items they bid for, how many times they participated in a bid, how many items they set a bid for, etc. After that step, they gave us a new dataaset with all of thsoe detailed analysis and wanted help in identifying any possible cases of shill bidding and whether certain conditions were authentic. Therefore, my role is to use unsupervised or clustering algorithms to group specific observations into clusters and that can help evaluate if a specific user is suspected of shill bidding or any sort of unauthentic forms of bidding. In order to predict help cluster the data, I would use k-means algorithm and agglomerative Hierarchical clustering to understand the ideal number of clusters and how they can be clustered. I also plan on looking into PCA to understand how the dimensions could be reduced to help us further. Following that, the investigation agency will move on to the next step of actions that they have. This dataset gives us a great understanding of how many times a user has bid on a speficic item, hi winning ratio, how logn auction was for, was a bid done early and they have many more details. They ahve also added specific ids for auction items and user id and each bidding is classified as a record id. Therefore, this dataset would give a lot of useful information and help get an idea of what a shill bidder could look like. The corresponding machine learning problem is to use k-means algorithm and agglomerative Hierarchical clustering to understand the ideal number of clusters and how they can be clustered. I also plan on looking into PCA to understand how the dimensions could be reduced to help us further. The main goal is to see which clustering algorithm could help us see a better score and understand whether the clusters would be reliable.

**Technical Goals:**
- Data Prep/Cleaning: We will be performing data cleaning and preparations, so the data would not have any missing valuess, duplicates, we will drop any features that may not be relevant to the project.
Data Vizualization and EDA: We will be doing Data Visualizations to help understand the dat in more depth and identify how a specific feature can play a role.
Feature Engineering: We will be chagning the categorical values to numericals and adding some changes to features that may help with modelling.
Clustering model: In this step, we are working on developing two clustering models and evaluating which one would suit the goals of what we are aiming to do.

## Motivation and Background
- "Whenever you see the same initials or user identification appearing alongside your bid, as in the photo above, you should be wary" (coin world)
- "Shill bidding is not allowed on eBay. It happens, though, easily enough, through different computers on different routers or Internet servers." (coin world)
- This is a dataset about shill bidding and I wanted to look into this as I was unfamiliar with the terma nd wehn I heard about this I learned that there could be many different ways of bidding where you could mask your identity, have an indirect influence on the overall price of the items being auctioned, you may use specific strategies and all also to show others that you are a genuine bidder, but your aim may be to get all the benefits for yourself. Therefore, I felt this topic and the dataset were interesting.

## Data

- The dataset used for this project was found at https://www.kaggle.com/aishu2218/shill-bidding-dataset.
- The dataset was inspired by the intial data in the UCI website: 
https://archive.ics.uci.edu/ml/datasets/Shill+Bidding+Dataset
- This dataset contains bidding information from a large number of auctions from ebay of a lot of the popular products on the website. Following that, the data was preporcessed and an evalaution was conducted on whether a bid was normal or authentic or any form of shill bidding took place. A shil bidding could be done when the user masks his identity, places bids when he or she may know the seller of the product, etc. I think this dataset is good as it can help you understand details about what type of specific characteristics or set of characteristics can be used to determine if a bid is acurate or not. We removed the target value which was evaluating if a shill bidding took place or not. However, we removed that column as we do not have targets when we use unsupervised learning techniques like clustering.


### Data Dictionary

- Record ID: (int data type), not null, unique, it contains a unique set of record ids for each bidding record in the dataset. 
- Auction ID: (int data type), not null, unique, it contains a unique set of auction ids for each  record in the dataset. 
- Bidder ID: (int data type), not null, unique, it contains a unique set of ids for each bidder in the dataset.
- Bidder Tendency: (float data type), not null, it checks a score of how many bids a bidder would participate in. If someone is shill bidding then they would participate in a few sales witht the same sellers in usual cases. 
- Bidding Ratio: (float data type), not null, this will check how frequently or the ratio of how often an individual participates in a bid. Those who participate more frequently could be shill bidders who try to elevate the auction price for other bidders who may be making authentic bids.
- Successive Outbidding: (float data type), not null, This checks a score on how much a bidder may try to outbid himself even though he may be the current winner and would want to make a small and steady increase on price. 
- Last Bidding: (float data type), not null, This will check how much an individual would be active on their last bid as a shill bidder could sometimes be inactive towardss the end when more thn 90% of the auction has gone by to lose a bid and it could be part of their strategy. 
- Auction Bids: (float data type), not null, This shows us a number of auction bids that an user may have done and a shill bidder would usually have a higher number of bids than the average bids in auctions that may be going on at the same time.
- Starting_Price_Average:(float data type), not null, This will be the starting price that each of the bidders may propose and a shill bidder may usually ask for a smaller starting price to attract all authentic biddders to come and make claims on bidding.
- Early Bidding: (float data type), not null, This will show at what percentage ofthe overall bidding time the bid was called and ashill bidders usually bid early usually within the first 25% of the time.
- Winning Ratio: (float data type), not null, This shows us the ratio of the proprion of bids that users won. Some shill bidders compete in many auctions and seem to win in barely any of them. 
- Auction Duration: (int data type), not null, The duration of how long an auction lasted for.
- Class: (int data type), not null, this is the target data type where we eill see if a bidding is considered authentic or not. Marked with 0 or 1. However, we will be dropping this column for the project as we do not use target variables in unsupervised learning algortihms.


##  Contributor
<pre>
Contributer  : <a href=https://github.com/Debanjan-C>Debanjan Chowdhury</a>
</pre>

##  Software Requirements - Packages used
<pre>
Languages    : Python
Tools/IDE    : Anaconda, Jupyter Notebook
Libraries    : pandas, matplotlib, seaborn, scikit learn
</pre>

<pre>
Last Updated : November 2020
</pre>

## Reference and contribution
<pre>
- https://www.coinworld.com/voices/gerald-tebben/beware_of_shill_bidd.html#:~:text=Shill%20bidding%E2%80%94legal%20or%20illegal,is%20not%20allowed%20on%20eBay
- Dataset: https://www.kaggle.com/aishu2218/shill-bidding-dataset
- Dataset inspired by: https://archive.ics.uci.edu/ml/datasets/Shill+Bidding+Dataset
</pre>
