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

#### Python Code :

```python
import pandas as pd
dataFrame = pd.read_csv('chopstick-effectiveness.csv')
dataFrame.head()
```
**output :**
<div style="padding-left: 200px">
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Food.Pinching.Efficiency</th>
      <th>Individual</th>
      <th>Chopstick.Length</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>19.55</td>
      <td>1</td>
      <td>180</td>
    </tr>
    <tr>
      <th>1</th>
      <td>27.24</td>
      <td>2</td>
      <td>180</td>
    </tr>
    <tr>
      <th>2</th>
      <td>28.76</td>
      <td>3</td>
      <td>180</td>
    </tr>
    <tr>
      <th>3</th>
      <td>31.19</td>
      <td>4</td>
      <td>180</td>
    </tr>
    <tr>
      <th>4</th>
      <td>21.91</td>
      <td>5</td>
      <td>180</td>
    </tr>
  </tbody>
</table>
</div>


Let's do a basic statistical calculation on the data using code! Run the block of code below to calculate the average "Food Pinching Efficiency" for all 31 participants and all chopstick lengths.

```python
dataFrame['Food.Pinching.Efficiency'].mean()
```
**output :**
    25.00559139784947

This number is helpful, but the number doesn't let us know which of the chopstick lengths performed best for the thirty-one male junior college students. Let's break down the data by chopstick length. The next block of code will generate the average "Food Pinching Effeciency" for each chopstick length. Run the block of code below.

```python
meansByChopstickLength = dataFrame.groupby('Chopstick.Length')['Food.Pinching.Efficiency'].mean().reset_index()
meansByChopstickLength

# reset_index() changes Chopstick.Length from an index to column. Instead of the index being the length of the chopsticks, the index is the row numbers 0, 1, 2, 3, 4, 5.
```
**output :**
<div style="padding-left: 200px">
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Chopstick.Length</th>
      <th>Food.Pinching.Efficiency</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>180</td>
      <td>24.935161</td>
    </tr>
    <tr>
      <th>1</th>
      <td>210</td>
      <td>25.483871</td>
    </tr>
    <tr>
      <th>2</th>
      <td>240</td>
      <td>26.322903</td>
    </tr>
    <tr>
      <th>3</th>
      <td>270</td>
      <td>24.323871</td>
    </tr>
    <tr>
      <th>4</th>
      <td>300</td>
      <td>24.968065</td>
    </tr>
    <tr>
      <th>5</th>
      <td>330</td>
      <td>23.999677</td>
    </tr>
  </tbody>
</table>
</div>

**From the table we can see that chopsticks of length 240 performed best as it has highest Food Pinching Efficiency**

```python
# Causes plots to display within the notebook rather than in a new window
%pylab inline

import matplotlib.pyplot as plt

plt.scatter(x=meansByChopstickLength['Chopstick.Length'], y=meansByChopstickLength['Food.Pinching.Efficiency'])
plt.xlabel("Length in mm")
plt.ylabel("Efficiency in PPPC")
plt.title("Average Food Pinching Efficiency by Chopstick Length")
plt.show()
```
<img class="image-post" src="{{ site.url }}/images/data-analysis/output_13_1.png" alt="png">


**Based on the scatter plot created from the code above,It is seen that Food pinching efficiency increase till it reaches the length 240 mm and then it decreases with increasing length in chopstick.
Highest efficiency seen at the 240 mm length chopsticks.**


# Conclusion
**In the abstract the researchers stated that their results showed food-pinching performance was significantly affected by the length of the chopsticks, and that chopsticks of about 240 mm long were optimal for adults. But I think we need more data in order to know the optimal length.**


# Try the whole code here.

{% include trinket-open %}
print "hello world"
{% include trinket-close %}

	

