---
name: IS445 Final Project - Liverpool and Man City 2018-2019
tools: [Python, HTML, vega-lite]
image: assets/pngs/trent1819.png
description: Looking at Liverpool FC and Manchester City FC scoring in 2018-2019 PL season
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Final Project: Liverpool FC and Manchester City FC - Goals and Refs

For my final project, I decided to look into Liverpool FC and Manchester City FC scoring in the 2018-2019 season. As a Liverpool fan, I would've preferred the next season, where Liverpool won the title instead of Man City, but alas, the data wasn't easily available online. This is yet another reminder of the compromises we make in data analysis, and the practical limitations that have nothing to do with technical expertise or resources. Here are the main sets of data I have:
* **Performances for each club, by match date.** This includes which teams were home and away, how many goals they scored, the half time score, the full time score, shots, fouls, the referee, bookings, etc.
* **Player season stats for both clubs.** This includes goals, assists, minutes played, and lots of other soccer nerd stats like xG (expected goals), a new stat created in the age of big data that evaluates each goal chance and assigns it a likelihood of being a goal (on paper).

For both sets, I am using relatively low-tech data for practical reasons, both for me (I am still learning!) and for you (you might not know such strange stats, or care!)

First up, let's just take a look at each club's goals scored, by match date. First, Liverpool:

<vegachart schema-url="{{ site.baseurl }}/assets/json/lfc_goals_t.json" style="width: 100%"></vegachart>


And for Manchester City:

<vegachart schema-url="{{ site.baseurl }}/assets/json/city_goals_t_.json" style="width: 100%"></vegachart>


Both clubs scored a lot of goals, as you'd expect for two historically good season performances! But we can also see who scored the goals for each club, again first with Liverpool:

<vegachart schema-url="{{ site.baseurl }}/assets/json/lfc_pg.json" style="width: 100%"></vegachart>


And for Manchester City:

<vegachart schema-url="{{ site.baseurl }}/assets/json/mcfc_pg.json" style="width: 100%"></vegachart>

Manchester City had slightly better scoring balance, with more players over 6 goals than Liverpool, who instead had two elite goalscorers in Mohammed Salah and Sadio Mane, each ending the season with 22 goals (and sharing the top scorer prize in the Premier League). However, Manchester City did also have one elite goalscorer in Sergio Aguero, who scored 21 goals for the season.

But what if we want to investigate if anything is fishy about Man City's season? Perhaps we could glean some insights by looking at referee assignment for each match day, and see if there is a correlation between which referees are assigned to each club and how it aligns with their performances? After all, a referee can create or hinder goal scoring with fouls, corners, playing advantage or, of course, awarding penalties. Here, we have two interactive bar charts, with the same data as in our initial line charts, but now interactive. If you click on a bar that corresponds to the match, the referee name will be returned. If you don't click any bar, you'll see the referees for the entire season. First, let's look at Liverpool:

<vegachart schema-url="{{ site.baseurl }}/assets/json/lfc_g_r.json" style="width: 100%"></vegachart>

Hmmmmm.... DEFINITELY nothing fishy here, and I am 110% confident that Liverpool earned each and every one of their 97 points.

But let's look at Manchester City:

<vegachart schema-url="{{ site.baseurl }}/assets/json/mcfc_g_r.json" style="width: 100%"></vegachart>

Strange! It looks Paul Tierney and Andre Marriner reffed a lot of City matches, though, in their defense, the biggest wins for City are generally refereed by different officials. Though the data doesn't show it here, I am confident there might be impropriety about the season still, just not in this data ;)

### The Data & Underlying Code

Below are links to a GitHub folder with the underlying data as well as to the Python notebook that was used to create these visualizations.
<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/rdubnic2/rdubnic2.github.io/tree/main/finalproject-data" text="The Data (directory of 4 files)" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/rdubnic2/rdubnic2.github.io/blob/main/python_notebooks/dubnicek-homework10.ipynb" text="The Notebook" %}
</div>

