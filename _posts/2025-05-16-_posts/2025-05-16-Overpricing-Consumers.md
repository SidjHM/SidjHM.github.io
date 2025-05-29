---
layout: post
title: Overpricing Consumers
subtitle: Dynamic Pricing and its Impact
cover-img: 
thumbnail-img: 
share-img: 
tags: [Cars]
author: Siddhant Jain
---

# **Introduction**
Uber, and Lyft, the 2 giants of the taxi industry, have often employed a tactic that many would see as unfair: Dynamic Pricing. The purpose of this is to help these companies boost up prices during high demand, which in turn forces the consumers to pay an exorbitant amount because they simply have no other option. As somebody who has fallen victim to this tactic many times, I wanted to use this project as an opportunity to understand this environment and see if I could build a model that would be able to predict price based on a myriad of factors. 

# **Data**
The dataset used for this project was sourced from [**Kaggle**](https://www.kaggle.com/datasets/ravi72munde/uber-lyft-cab-prices) and focuses on ride-sharing data collected in Boston during November 2018. It includes detailed information on both Uber and Lyft trips, capturing a range of variables that influence pricing. These factors include distance, cab type (Uber or Lyft), time of day, day of the week, surge pricing multipliers, weather conditions, and ride categories (such as UberX or Lyft Premier). The dataset provides a valuable snapshot of how dynamic pricing played out in a real-world urban setting, allowing for a deeper analysis of the pricing models these companies use and the external conditions that might drive fare increases.

## **Limitations**
The dataset does not differentiate based on the day of the week that you are taking a cab. In doing so, it avoids the fact that prices tend to be much cheaper on friday, saturday, and sunday because there are not as many drivers and there are more people who want to use cabs because of the party nature of these days. 




# **Graphs**


# **Findings**
Surge multiplier is unaffected by the time of the day or the day that you took the cab on. This indicates that the most likely factor is where you book a cab from, suggesting that places where demand is higher (heavily crowded spaces), the prices are higher.


In the span on this dataset in 2018, lyft was more expensive than uber, and as such, people took uber for long journeys (6+ miles).

