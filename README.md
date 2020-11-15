# Bidding_Clustering

## Repository Navigation
<pre>
Technical Notebook         : <a href=></a>
Code                       : <a href=></a>
Data                       : <a href=></a>
Data Web                   : <a href=https://www.kaggle.com/kabure/german-credit-data-with-risk>Data Web</a>

## Table of Contents
[Repository Navigation](#repository-navigation) -
[Overview](#overview) -
[Business Goals](#business-goals) -
[Motivation and Background](#motivation-and-background) -
[Data](#data) - https://www.kaggle.com/aishu2218/shill-bidding-dataset
[Contributor](#contributor)
[Software Requirements - Packages used](#software-requirements--packages-used) -
[Reference and contribution](#reference-and-contribution)

## Overview


## Business Goals

## Motivation and Background

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
https://www.kaggle.com/aishu2218/shill-bidding-dataset
https://archive.ics.uci.edu/ml/datasets/Shill+Bidding+Dataset
</pre>
