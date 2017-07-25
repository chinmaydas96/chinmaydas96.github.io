---
layout: post
title: Understanding Linear Regression —  Part-2
description: "How Linear Regression works "
headline: "Machine Leaning Part-2"
categories: Machine_Learning 
tags: 
  - machine_learning
  - regression_model

comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/machine_learning/regrssion_intro.jpg" alt="Regression image">

> Let's predict future with Machine Learning Linear Regression model.

In Supervised Learning **Linear Regression model** is the most easy and simple model ,both to understand and apply. In the previous post I talk about the Supervised Learning .So to perform we are given a label dataset to predict. In this post I will describe how linear regeression works and use it to predict on a real world dataset.

To understand the model let's visalize a dataset.

<img class="image-post" src="{{ site.url }}/images/machine_learning/dataset1.png" alt="Regression image">

So we will define a linear relationship for the amount of hour study and test score perform by the student, for which we will make a straight line in order to fit all the data and minimize the error.

#### Math Behind Linear Regression —>

***
##### Straight line -

So in order to plot a stright line we need to have slope and line intercept for the straight line .
<p>$$y = mx +c $$ </p>


<img class="image-post" src="{{ site.url }}/images/machine_learning/line.jpg" alt="Regression image">



##### Hypothesis Function -

We represent the straight line as a hypothesis function in terms of $$\theta_{1}$$ as a slope and $$\theta_{0}$$ as a line intercept.

$$ h_{\theta}(x) = \theta_{0} + \theta_{1}x  $$

So hypothesis function is the final output function that help the model for prediction.