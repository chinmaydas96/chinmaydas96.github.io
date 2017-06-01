---
layout: post
title: Chopsticks Length Analysis
description: Analysis of chopstick using basic statistical methods.
headline: "Data Analysis Part-1"
categories: Data_Analysis
tags: 
  - Data Analysis
  - Statistics 

comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/data-analysis/chopsticks.jpg" alt="chopsticks">


# Overview

### Goal

The goal of this project is to `find the optimum length of the chopstick for the adult` and `review and analyse the paper` published regarding chopstick length from the Taiwan Institute of Technology . 	

### Dataset

I will be using the `optimum length of chopsticks` data set where researchers set out to determine the optimal length of chopsticks for children and adults. They came up with a measure of how effective a pair of chopsticks performed, called the `Food Pinching Performance`. The "Food Pinching Performance" was determined by *counting the number of peanuts picked and placed in a cup (PPPC)*.
[Link to the dataset](https://www.udacity.com/api/nodes/4576183932/supplemental_media/chopstick-effectivenesscsv/download)

### Abstract

Chopsticks are one of the most simple and popular hand tools ever invented by humans, but have not previously been investigated by ergonomists. Two laboratory studies were conducted in this research, using a randomised complete block design, to evaluate the effects of the length of the chopsticks on the food-serving performance of adults and children. Thirty-one male junior college students and 21 primary school pupils served as subjects for the experiment. The results showed that the food-pinching performance was significantly affected by the length of the chopsticks, and that chopsticks of about 240 and 180 mm long were optimal for adults and pupils, respectively. Based on these findings, the researchers suggested that families with children should provide both 240 and 180 mm long chopsticks. In addition, restaurants could provide 210 mm long chopsticks, considering the trade-offs between ergonomics and cost.
[Link to the full paper](https://www.ncbi.nlm.nih.gov/pubmed/15676839)


# Analysis

#### Independent and Dependent Variables :

`Independent variable` is what you change and isn't affected by other variables. In this problem the independent variable is the `length of the chopsticks`.

`Dependant variable`  is a variable dependent on other variables.It is affected by independent variables.In this problem the dependent variable is the `food-pinching performance`.

#### Operational definition of the dependent variable :

The study used a randomised complete block design to evaluate the effects of the length of the chopsticks on the food-serving performance. The "Food Pinching Performance" was determined by counting the number of peanuts picked and placed in a cup (PPPC).


#### Controlled Variables :

Based on the description of the experiment controlled variable are :
* The age of the participants was controlled based on the block design.
* The material of the chopsticks (wood, metal, and so on).
* The type or size of foods they pinch with chopsticks .
* Chopstick lengths : 180, 210, 240, 270, 300, and 330 mm


# Conclusion