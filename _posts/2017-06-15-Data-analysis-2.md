---
layout: post
title: Bay Area Bike Share Analysis
description: Analysis of Bay Area Bike Share data 
headline: "Data Analysis Part-2"
categories: Data_Analysis
tags: 
  - Data Analysis
  - Statistics 
  - Data Visualisation
comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/data-analysis/bike-share.jpg" alt="bike-share">


# Introduction

---

[Bay Area Bike Share](http://www.bayareabikeshare.com/) is a company that provides on-demand bike rentals for customers in San Francisco, Redwood City and other cities. Users can unlock bikes from a variety of stations throughout each city, and return them to any station within the same city. Users pay for the service either through a yearly subscription or by purchasing 3-day or 24-hour passes. Users can make an unlimited number of trips, with trips under thirty minutes in length having no additional charge; longer trips will incur overtime fees.

# Goal

---

In this project, I take a look at two of the major parts of the data analysis process: data wrangling and exploratory data analysis. But before even start looking at data, if I myself was working for Bay Area Bike Share: what kinds of information would I want to know about in order to make smarter business decisions? Or if I was a user of the bike share service. What factors might influence how  would I want to use the service ? As a Data analyst I should be able to answer those questions.

## Datasets Used

---

I will be using 2014 Bay Area Bikeshare Data released in the [website](https://s3.amazonaws.com/babs-open-data/babs_open_data_year_1.zip).Here take a look at [submission winner for Best Analysis](http://thfield.github.io/babs/index.html) from Tyler Field. He made excellent visualisation almost answer all question. I won't be able to do that just now. I will be Just doing some basic visualisation in order to answer some of the questions as a junior Data Analyst .


## Key Concept
---
#### Data Wrangling

**Data wrangling** (sometimes referred to as data munging) is the process of transforming and mapping data from one "raw" data form into another format with the intent of making it more appropriate and valuable for a variety of downstream purposes such as analytics.


Now it's time to explore the data. Year-1 , Year-2 and Year-3 data privide on the Bay Area Bike Share's [Open Data](http://www.bayareabikeshare.com/open-data) website. I select `Year-1` data as many data analysist analysed on Year 1 data ,So I can a look at everyone's analysis and gain more insight knowledge on the data besides my analysis.

The data comes in two parts: the first half of Year 1 (files starting `201402`), the second half of Year 1 (files starting `201408`). There are 4 main datafiles associated with each part: `trip data` showing information about each trip taken in the system (`*_trip_data.csv`), information about the `stations data` in the system (`*_station_data.csv`), `status data` showing information on number of available bikes and docks (`*_status_data.csv`), and `daily weather data` for each city in the system (`*_weather_data.csv`).

When dealing with a lot of data, it can be useful to start by working with only a sample of the data. This way, it will be much easier to check that our data wrangling steps are working since our code will take less time to complete and easy to analyse.Then we can test that on the whole datasets.


