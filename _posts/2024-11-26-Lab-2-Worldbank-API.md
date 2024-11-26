---
layout: post
title: Lab 2-Worldbank API
subtitle: Exploring Global Development Indicators with World Bank Data
cover-img: /assets/img/worldbank.png
thumbnail-img: /assets/img/worldbank.png
share-img: /assets/img/path.jpg 
author: Siddhant Jain
---

# **Introduction**
In a world driven by data, understanding global development trends requires analyzing key indicators that reflect the economic, social, and infrastructural health of nations. The World Bank provides a treasure trove of such data, allowing us to examine critical metrics that shape the trajectory of countries around the globe. In this blog, I dive into a selection of these indicators to uncover meaningful patterns and insights.  

The analysis spans a diverse set of countries—India, the United States, China, Brazil, and Russia—and focuses on the years 2015 to 2023, a transformative decade marked by global upheavals and recoveries. From population growth and GDP trends to education spending and access to electricity, the indicators paint a vivid picture of development progress and challenges.  

But why these particular metrics? Why these countries? And why this timeframe? In this post, I’ll walk you through my choices and explain how filtering the data helped streamline the analysis while ensuring depth and relevance. Let’s explore how these indicators tell the story of global growth, inequality, and resilience.



## **What indicators from the World Bank did you choose to look at besides population, life expectancy, and GDP per capita? Why?**

In addition to the core indicators of population, life expectancy, and GDP per capita, I chose to include the following indicators for a broader and deeper analysis of development:

**GDP (USD):**
While GDP per capita provides a measure of average economic output per person, looking at total GDP gives insight into the overall scale of a country’s economy. It highlights the nation’s position in global trade and investment, its capacity for international influence, and its ability to fund large-scale infrastructure or social programs. This indicator helps contextualize how economic resources are distributed within and across nations.

**Unemployment Rate (%):**
This metric reveals the proportion of the labor force without jobs but actively seeking work. It serves as a critical barometer for economic health, social stability, and government policy effectiveness. High unemployment rates often signal structural problems, while lower rates indicate strong economic performance.

**Access to Electricity (%):**
Electricity is a basic necessity for modern living, and this indicator reflects how accessible this resource is to the population. It is a direct measure of a country’s infrastructure and economic development. In nations with low access, the data reveals areas needing investment, while in developed economies, near-universal access showcases established systems.

**Mortality Rate (Per 1,000):**
Mortality rate provides essential insight into healthcare infrastructure, nutritional standards, and the impact of diseases on a population. This indicator helps assess the quality of life and public health initiatives in a country. Tracking this over time can reveal the effectiveness of health interventions and changing living conditions.

**Government Expenditure on Education (%):**
Education is central to a country’s long-term development. By measuring the percentage of GDP allocated to education, this indicator showcases the importance placed on human capital development. It helps to identify countries prioritizing education as a tool for economic and social progress.

**Children in Employment, Female and Male (%):**
Child labor reflects broader socio-economic issues. These indicators illustrate the pressures on families and the effectiveness of laws protecting children’s rights. Disparities between genders can also highlight cultural norms and inequalities within societies.


## **Did you filter any countries out? How, and why?**
Yes, instead of analyzing all countries, I limited the dataset to five key nations: **India**, **United States**, **China**, **Brazil**, and **Russia**. 

These countries were chosen based on the following rationale:
**Diversity in Development Levels:** These nations range from *developing economies (India, Brazil)* to *developed economies (United States)*, with *China* and *Russia* occupying intermediate positions.
**Geographic Representation:** By selecting countries from Asia, the Americas, and Europe, the analysis captures a global perspective on development trends.
**Economic Significance:** These nations are among the world’s largest economies, making their data highly relevant for understanding global economic and social dynamics.
While limiting the countries meant excluding some regions, it allowed for a more focused analysis of development trends among representative economies with varied challenges and strengths.

### **Code**
  if __name__ == "__main__":
      # Define countries
      countries = [
  {"code": "IND", "name": "India"},
  {"code": "USA", "name": "United States"},
  {"code": "CHN", "name": "China"},
  {"code": "BRA", "name": "Brazil"},
  {"code": "RUS", "name": "Russia"},
  ]


## **Did you filter any years out? How, and why?**
Yes, the analysis is focused on the years 2015 to 2024. 

This period was chosen for several reasons:
**Relevance to Current Trends:** This timeframe captures recent global events, including the economic disruptions of COVID-19, recovery efforts, and the impact of technological advances. It ensures that the insights are relevant to current policy and academic discussions.
**Consistency Across Indicators:** The World Bank's data availability varies across indicators and countries. Selecting this range ensures that most indicators have sufficient data points for meaningful comparisons.
**Avoiding Historical Bias:** Older data, while valuable for long-term trends, can be less reflective of current conditions due to shifts in policy, technology, and international dynamics.

By focusing on this decade, the analysis highlights contemporary issues and progress, offering insights into how countries are adapting to modern challenges like climate change, health crises, and economic inequality.

### **Code**
The start_year and end_year are passed as parameters to the API request, which is made through the following line of code:
*response = requests.get(
    base_url.format(country_code=country["code"], indicator=indicator_code),
    params={"format": "json", "date": f"{start_year}:{end_year}"}, 
)*
The date parameter in the API request ensures that only data from the years 2015 to 2024 is fetched. The API returns data only within this range.

*for entry in api_data[1]:
    year = entry["date"]
    if entry["value"] is not None:
        ...*
This loop iterates over the data returned by the World Bank API, and each entry in the api_data[1] list corresponds to a specific year. The entry["date"] field contains the year, and the code checks if this year falls within the defined range (2015 to 2024). If an entry’s year is within the specified range and has a valid value (entry["value"] is not None), it is added to the data list.




