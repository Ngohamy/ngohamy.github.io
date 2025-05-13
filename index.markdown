---
layout: page
title: Home
---

# Welcome

What Shapes Housing Prices in Copenhagen?

This site explores how housing prices have changed across Copenhagen and what might be driving those changes. From major renewal projects to the everyday amenities that make a district feel like home, we take a closer look at the patterns behind property values.

Explore the maps, interact with the charts, and see what might be shaping the city!

## Inflation-Adjusted Housing Price Trends
 
Between 2005 and recent years, housing prices across Copenhagen districts have shown varying real-term trends. This visualization tracks the year-on-year percentage change in square meter prices, corrected for inflation to reflect real purchasing power. The data includes only apartments sold through regular sales — excluding auctions, family transfers, or other non-standard transactions.

Different districts display distinct patterns over time — some experience sharp increases during certain periods, while others remain stable or even decline in real terms.

A widespread negative growth is observed around 2007–2009, reflecting the impact of the 2008 financial crisis. More recently, in 2022–2023, all districts show a downturn, followed by renewed growth.

Explore the interactive chart below by hovering over data points or muting specific districts using the legend to focus on individual trends.
 
<iframe 
  src="{{ '/assets/bokeh/inflation_adjusted_price_trends.html' | relative_url }}"
  width="100%"
  height="600"
  frameborder="0"
  loading="lazy">
</iframe>

## What Might Make Districts Desirable?

<div style="display: flex; flex-wrap: wrap; gap: 2rem; align-items: flex-start;">
  <!-- Left Column: Map -->
  <div style="flex: 2; min-width: 400px;">
    <iframe
       src="{{ '/assets/bokeh/district_poi_map.html' | relative_url }}"
       width="100%"
       height="700"
       frameborder="0"
       loading="lazy">
    </iframe>
  </div>

  <!-- Right Column: Text -->
  <div style="flex: 1; min-width: 300px; max-width: 500px; margin-top: 6rem;">
    <p>
      Besides macroeconomic factors like interest rates or inflation, the local environment can also influence housing demand — and thereby prices.
    </p>
    <p>
      To explore this, the following map visualizes the concentration of different types of facilities across Copenhagen's districts.
    </p>
    <p>
      You can use the dropdown to switch between different types of points of interest. Districts with fewer places in a selected category appear lighter on the map.
    </p>
  </div>
</div>


## Tracking Attractions and Housing Prices (2008-2017)

As Copenhagen emerged from the financial crisis, both housing markets and urban amenities underwent significant transformation. This visualization reveals how these two elements evolved together during a pivotal decade.

Watch as attractions (blue dots) appear across the city while district colors shift to reflect changing housing prices. Notice how central areas maintain their premium status while price increases gradually ripple outward to once-affordable neighborhoods.

The story unfolds differently in each district — some see dramatic price increases despite few new attractions, while others develop a rich concentration of amenities that coincides with rising property values.

<iframe 
  src="{{ '/assets/bokeh/copenhagen_housing_attractions.html' | relative_url }}"
  width="100%"
  height="650"
  frameborder="0"
  loading="lazy">
</iframe>

## Prediction of housing price with regression
This section introduces an interactive tool that predicts apartment prices across Copenhagen using a machine learning model trained on historical housing data. The model considers four key features: apartment size (sqm), number of rooms, construction year, and postal code.

To make the prediction process transparent and explorable, users can adjust each of these inputs via sliders and immediately see how the predicted price changes. The corresponding district on the map is also highlighted to give spatial context to the estimate.

Behind the scenes, the tool is powered by a trained Random Forest regression model and a standardized input pipeline. 

<iframe
  src="{{ '/assets/bokeh/copenhagen_price_projects_ml.html' | relative_url }}"
  width="100%"
  height="700"
  frameborder="0"
  loading="lazy">
</iframe>