---
layout: post
title: Lab 3-Individual Datasets
subtitle: Statistics of IPL 2024 and their Impact on the 2025 Mega Auction
cover-img: /assets/img/IPL.jpg
thumbnail-img: /assets/img/Auction.jpeg
share-img: /assets/img/path.jpg 
author: Siddhant Jain
---
# **The Impact of a Player's 2024 Indian Premier League (IPL) Performance on their 2025 Mega Auction Bid**

## **Which dataset did you work with? Where did you get it from?**
The Indian Premier League (IPL) is a franchise-based cricket league that takes place in India every year from Late-March to Late-May. The league consists of 10 different teams that all compete to be crowned the champions. Unlike the American leagues, the IPL does not have a contract system, nor does it have a draft. Instead, it has an auction, where players are sold to the highest bidder. In most years, there is a mini-auction, where teams can release players who did not perform well in the previous year, and bid for new talent. However, every 3 years, there is a Mega-Auction. In this Mega-Auction, teams can only retain up to 6 players or less, with the rest of their squad (usually 25 players) heading to the auction. 

The 2025 IPL Auction was a Mega-Auction. My work combines 2 different datasets to conduct this analysis. I have a file that details the statistics for ***Batter*** and his winning bid in the auction, and another file with statistics for ***Bowlers***.

## **Which aspect of this dataset are you interested in? What do you hope to learn from analyzing this dataset?**

The purpose of this analysis was to understand the relationship between the Winning Bid (Salary) of a player in the Mega Auction and his production in the 2024 IPL season. As a sportsman, I wanted to learn what key statistics IPL teams look at when they evaluate players, and understand the premise behind paying them that particular salary. 


## **3. Discuss your analysis of the dataset**
### **The variables you looked at**

For Battters, I looked at *Runs* and *Average* and their relationship to the winning bid.
For Bowlers, I looked at *Wickets* and *Strike Rate* and their relationship to the winning bid.

### **Distributions of variables (center and variability, e.g. std.dev or IQR)**

**Batters**

*Winning Bid vs Batting Average*
/assets/img/Batter:Winning_Bid_vs_Avg.png

*Winning Bid vs Runs*
/assets/img/Batter:Winning_Bid_vs_Runs.png

There is little to no correlation between Runs and Avg and the Winning Bid as shown above. However, there is a fundamental error with this calculation. This code graphs these statistics versus only Batters who average more than 25 runs in the Batters.csv file. Bowlers also have to bat in the IPL. The very best bowlers usually go for high prices, but they are not good batters, and hence do not score many runs. However, their high price and mere presence in the dataset skews the data towards 0, as most bowlers bat late in the game. By only looking at Batters who have averages greater than 25, we are looking at players whose main job is to bat, limiting the dataset to better understand the value of a batter. Here are the updated calculations based on these parameters:

*Winning Bid vs Batting Average*
/assets/img/Filtered:Winning_Bid_vs_Avg.png

*Winning Bid vs Runs*
/assets/img/Filtered:Winning_Bid_vs_Runs.png

### **Visualizations of the dataset**

### **Limitations of your analysis and the dataset?**


## **What conclusions can you draw about this dataset? What is your supporting evidence?**
