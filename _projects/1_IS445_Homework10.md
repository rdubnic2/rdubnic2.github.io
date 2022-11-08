---
name: IS445 - Homework 10
tools: [Python, HTML, vega-lite]
image: assets/jpgs/iwtb.jpg
description: Homework 10 for IS445 DataViz
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Homework 10

Here are some example vega-lite visualizations, first a look at duration of UFO sightings (in seconds) by US state (trying hovering over points for exact details!).

<vegachart schema-url="{{ site.baseurl }}/assets/json/chart1.json" style="width: 100%"></vegachart>

Next, I visualize a look at Bigfoot sightings by state, and then by humidity and temperature, for a selected state (click on the bar for the state you want to see!).

<vegachart schema-url="{{ site.baseurl }}/assets/json/dualChart.json" style="width: 100%"></vegachart>


## The Data & Methods

Below are links to some shoddy code and some less-shoddy data as buttons:
<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/ufo-scrubbed-geocoded-time-standardized-00.csv" text="The UFO Data" %}
</div>

<div class="center">
{% include elements/button.html link="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_bcubcg_fall2022/main/data/bfro_reports_fall2022.csv" text="The Bigfoot Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://raw.githubusercontent.com/rdubnic2/rdubnic2.github.io/main/python_notebooks/dubnicek-homework10.ipynb" text="The Analysis" %}
</div>

