---
layout: post
title: Altair Data Visualizations
subtitle: Trying Data Visualizations
cover-img: /assets/img/draft.jpg
thumbnail-img: /assets/img/draft.jpg
share-img: /assets/img/path.jpg
tags: [Altair, Lab]
author: Siddhant Jain
---

# **Graph 1: Lifespan of Cars**

![Lifespan of Cars](/assets/img/Cars.jpg)

The purpose of this data is to look at the different types of cars in the market, and showcase which of these cars has the longest potential lifespan over its entire lifetime. It is very interesting in the way the graphs were set up, from the variety in color schemes of the donut chart, to the concentric set-up, and how the ends of the charts lead to a horizontal line with the car and its values. I chose it because very interesting in the way it showed data, and I felt like it would be a good challenge for me to try and remake. 

**Marks:** 
Volume of the Pie chart 
**Channels:**
Color and Size of the Pie Chart


## **My Attempt**
I tried to replicate this graph using the actual data given on the website, but was unsuccessful. The concentric donut charts were extremely hard to generate, and I was unable to write code that accurately colored in different quadrants of the donut chart. In short, it was a failure.

Despite spending a lot of time, my efforts did not bear fruit, and I have nothing remotely similar to the actual graph. Hence, I shall not be putting an image here. My code will be on my Art of Data github repository.



# **Graph 2: Cars Exported by Germany**

![Cars Exported by Germany](/assets/img/German_Exports.png)

The purpose of this data is to look at the the amount of cars exported by Germany to different countries in the world. It is very interesting in the way the graphs were set up, and showcases just how big the U.S. mark is for german brands and how much revenue/profit they extract from the US. I chose it because very interesting in the way it showed data, and I felt like it would be an easier graph for me to make after a failed attempt at attempting an extremely had visualization. 

**Marks:** 
Rectangle

**Channels:**
Size, Position, and Color of Rectangle

## **My Attempt**
I tried to replicate this graph using some NBA data that I had generated in the past, and was successful. The sqaures, and positioning of the treemap were easier to generate than the concentric circles, and while the sizing took time to perfect, I feel like I had a decent sizing of each rectangle relative to others.

<div id="vis"></div>
  <script>
    (function(vegaEmbed) {
      var spec = {"config": {"view": {"continuousWidth": 300, "continuousHeight": 300, "stroke": "transparent"}, "axis": {"grid": false, "labels": false, "ticks": false}, "title": {"anchor": "middle", "color": "white", "font": "Georgia", "fontSize": 18, "fontWeight": "bold"}}, "data": {"name": "data-8fccb3fd7bf476b9346511f56a248cfd"}, "mark": {"type": "rect"}, "encoding": {"color": {"field": "WS", "type": "quantitative"}, "size": {"field": "normalized_WS", "type": "quantitative"}, "tooltip": [{"field": "Name", "type": "nominal"}, {"field": "WS", "type": "quantitative"}], "x": {"field": "x", "type": "quantitative"}}, "height": 200, "title": "Top 25 Players by Win Shares", "width": 800, "$schema": "https://vega.github.io/schema/vega-lite/v5.20.1.json", "datasets": {"data-8fccb3fd7bf476b9346511f56a248cfd": [{"Name": "Nikola Jokic", "Age": 28, "WS_Now": 17.0, "Experience": 9, "WS": 13.2, "normalized_WS": 0.05223585278986941, "x": 0.026117926394934706, "y": 0}, {"Name": "Shai Gilgeous-Alexander", "Age": 25, "WS_Now": 14.6, "Experience": 6, "WS": 12.5, "normalized_WS": 0.049465769687376336, "x": 0.07696873763355758, "y": 0}, {"Name": "Luka Doncic", "Age": 24, "WS_Now": 12.0, "Experience": 6, "WS": 11.3, "normalized_WS": 0.04471705579738821, "x": 0.12406015037593984, "y": 0}, {"Name": "Domantas Sabonis", "Age": 27, "WS_Now": 12.6, "Experience": 8, "WS": 11.2, "normalized_WS": 0.0443213296398892, "x": 0.16857934309457853, "y": 0}, {"Name": "Giannis Antetokounmpo", "Age": 29, "WS_Now": 13.2, "Experience": 11, "WS": 11.1, "normalized_WS": 0.043925603482390184, "x": 0.21270280965571825, "y": 0}, {"Name": "Jalen Brunson", "Age": 27, "WS_Now": 11.2, "Experience": 6, "WS": 10.7, "normalized_WS": 0.04234269885239414, "x": 0.2558369608231104, "y": 0}, {"Name": "Chet Holmgren", "Age": 21, "WS_Now": 8.9, "Experience": 2, "WS": 10.5, "normalized_WS": 0.04155124653739612, "x": 0.29778393351800553, "y": 0}, {"Name": "Anthony Edwards", "Age": 22, "WS_Now": 7.5, "Experience": 4, "WS": 10.4, "normalized_WS": 0.041155520379897115, "x": 0.33913731697665217, "y": 0}, {"Name": "Anthony Davis", "Age": 30, "WS_Now": 11.8, "Experience": 12, "WS": 10.3, "normalized_WS": 0.0407597942223981, "x": 0.3800949742777998, "y": 0}, {"Name": "Jayson Tatum", "Age": 25, "WS_Now": 10.4, "Experience": 7, "WS": 10.3, "normalized_WS": 0.0407597942223981, "x": 0.42085476850019793, "y": 0}, {"Name": "Victor Wembanyama", "Age": 20, "WS_Now": 3.7, "Experience": 1, "WS": 10.1, "normalized_WS": 0.039968341907400076, "x": 0.461218836565097, "y": 0}, {"Name": "Tyrese Haliburton", "Age": 23, "WS_Now": 9.0, "Experience": 4, "WS": 10.1, "normalized_WS": 0.039968341907400076, "x": 0.501187178472497, "y": 0}, {"Name": "Paolo Banchero", "Age": 21, "WS_Now": 5.3, "Experience": 2, "WS": 9.7, "normalized_WS": 0.03838543727740404, "x": 0.5403640680648992, "y": 0}, {"Name": "Tyrese Maxey", "Age": 23, "WS_Now": 8.1, "Experience": 4, "WS": 9.6, "normalized_WS": 0.037989711119905026, "x": 0.5785516422635537, "y": 0}, {"Name": "Jalen Williams", "Age": 22, "WS_Now": 7.3, "Experience": 2, "WS": 9.6, "normalized_WS": 0.037989711119905026, "x": 0.6165413533834587, "y": 0}, {"Name": "Jarrett Allen", "Age": 25, "WS_Now": 10.7, "Experience": 7, "WS": 9.4, "normalized_WS": 0.03719825880490701, "x": 0.6541353383458648, "y": 0}, {"Name": "Devin Booker", "Age": 27, "WS_Now": 9.2, "Experience": 9, "WS": 9.4, "normalized_WS": 0.03719825880490701, "x": 0.6913335971507718, "y": 0}, {"Name": "Joel Embiid", "Age": 29, "WS_Now": 7.5, "Experience": 10, "WS": 9.3, "normalized_WS": 0.036802532647408, "x": 0.7283339928769292, "y": 0}, {"Name": "Alperen Sengun", "Age": 21, "WS_Now": 6.9, "Experience": 3, "WS": 9.3, "normalized_WS": 0.036802532647408, "x": 0.7651365255243372, "y": 0}, {"Name": "Isaiah Hartenstein", "Age": 25, "WS_Now": 8.1, "Experience": 6, "WS": 9.2, "normalized_WS": 0.03640680648990898, "x": 0.8017411950929957, "y": 0}, {"Name": "Daniel Gafford", "Age": 25, "WS_Now": 7.8, "Experience": 5, "WS": 9.2, "normalized_WS": 0.03640680648990898, "x": 0.8381480015829047, "y": 0}, {"Name": "Zion Williamson", "Age": 23, "WS_Now": 7.5, "Experience": 5, "WS": 9.2, "normalized_WS": 0.03640680648990898, "x": 0.8745548080728137, "y": 0}, {"Name": "Derrick White", "Age": 29, "WS_Now": 8.5, "Experience": 7, "WS": 9.1, "normalized_WS": 0.036011080332409975, "x": 0.9107637514839731, "y": 0}, {"Name": "Franz Wagner", "Age": 22, "WS_Now": 6.4, "Experience": 3, "WS": 9.0, "normalized_WS": 0.03561535417491096, "x": 0.9465769687376336, "y": 0}, {"Name": "Bam Adebayo", "Age": 26, "WS_Now": 7.2, "Experience": 7, "WS": 9.0, "normalized_WS": 0.03561535417491096, "x": 0.9821923229125445, "y": 0}]}};
      var embedOpt = {"mode": "vega-lite"};

      function showError(el, error){
          el.innerHTML = ('<div style="color:red;">'
                          + '<p>JavaScript Error: ' + error.message + '</p>'
                          + "<p>This usually means there's a typo in your chart specification. "
                          + "See the javascript console for the full traceback.</p>"
                          + '</div>');
          throw error;
      }
      const el = document.getElementById('vis');
      vegaEmbed("#vis", spec, embedOpt)
        .catch(error => showError(el, error));
    })(vegaEmbed);

