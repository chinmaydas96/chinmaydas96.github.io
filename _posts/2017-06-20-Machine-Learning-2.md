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



#### Hypothesis Function -

We represent the straight line as a hypothesis function in terms of $$\theta_{1}$$ as a slope and $$\theta_{0}$$ as a line intercept.

$$ h_{\theta}(x) = \theta_{0} + \theta_{1}x  $$

So hypothesis function is the final output function that help the model for prediction.


#### Cost function -

We can measure the *accuracy* of our hypothesis function by using a **cost function**. This takes an average difference (actually a fancier version of an average) of all the results of the hypothesis with inputs from x's and the actual output y's.

So to here is figure to visualize the cost function with figure ->

<img class="image-post" src="{{ site.url }}/images/machine_learning/cost.jpg" alt="Regression image">

So we need to calculate the distance between the real value vs predict value . In this case we need to calculate mean squared error function for the given figure as some of the will positive and some of will negetive.

So Cost Function is -

$$ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m}(h_{\theta}(x_i) - y_i)$$

Where <br>
	  m = number of total points<br>
	  $$J(\theta)$$ = Cost function<br>
	  $$h_\theta$$  = hypothesis function<br>
	  $$y_i$$ = output value<br>
	  $$x_i$$ = input value<br>

In other word cost function / squared error function / mean squared function is nothing but error in prediction value.
So our main task is to **minimize** the Cost function.

Let's visualize cost function in 2-D. So there can be case of two types of cost function. Convex cost function and another is non-convex cost function.

<img class="image-post" src="{{ site.url }}/images/machine_learning/costfun.jpg" alt="Regression image">

Convex cost function 3-D view. 
<img class="image-post" src="{{ site.url }}/images/machine_learning/costfun1.png" alt="Regression image">

Non-Convex cost function 3-D view.
<img class="image-post" src="{{ site.url }}/images/machine_learning/costfun2.png" alt="Regression image">

#### Gradient Descent -

For the minimization technique we use **gradient Descent** method.
So our goal is to to minimize $$J(\theta)$$

