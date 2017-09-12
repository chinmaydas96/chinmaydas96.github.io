---
layout: post
title: Understanding Linear Regression —  Part-2.1
description: "How Linear Regression works "
headline: "Machine Leaning Part-2.1"
categories: Machine_Learning 
tags: 
  - machine_learning
  - regression_model

comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/machine_learning/regrssion_intro.gif" alt="Regression image">

> Let's look at the Mathematics behind the Linear Regression model.

In Supervised Learning **Linear Regression model** is the most easy and simple model ,both to understand and apply. In the previous post I talk about the Supervised Learning .So to perform we are given a label dataset to predict. In this post I will describe how linear regeression works and the math behind the linear regression using gradient descent algorithm.

To understand the model let's visalize a dataset.

<img class="image-post" src="{{ site.url }}/images/machine_learning/dataset1.png" alt="Regression image">

So we will define a linear relationship for the amount of hour study and test score perform by the student, for which we will make a straight line in order to fit all the data and minimize the error.

`My point is just a outlier lies in below all the points , if you know what I mean.`

### Math Behind Linear Regression —>

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

<img class="image-post" src="{{ site.url }}/images/machine_learning/error.jpg" alt="Regression image">

So Cost Function is -

$$ J(\theta) = \frac{1}{2m} \sum_{i=1}^{m}(h_{\theta}(x_i) - y_i)^2$$

Where <br>
	  m = number of total examples given<br>
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

In order to reach local minima we need to reach the bottom of the figures.So that cost can be less.

#### Gradient Descent -

For the minimization technique we use `Gradient Descent` method.
So our goal is to minimize $$J(\theta)$$

The Gradient is a derivative that points in a direction. **Gradient descent** is a first-order iterative optimization algorithm for finding the minimum of a function. It is not only used in linear regression but also in general algorithm in both machine learning and deep learning.

To find a local minimum of a function using gradient descent, **one takes small steps($$\alpha$$)** proportional to the negative of the gradient (or of the approximate gradient) of the function at the current point.

In other word we apply first order derivative of cost function with respect to $$\theta$$ and substract it from initial taken $$\theta$$ values for minima condition.

We will start off by some initial guesses for the values of $$\theta_0 \mbox{ and }\theta_1$$ and then keep on changing the values according to the formula:

$$  \theta_j := \theta_j - \alpha \frac{\partial J(\theta_j)}{\partial \theta_j} $$  

$$\mbox{ Where } \alpha = \mbox{ learning rate (taken 0.0001 approximately)} $$


after apply first order partial derivative we get something like this -

$$  \theta_0 := \theta_0 -  \frac{\alpha}{m} \sum_{i=1}^{m}(h_{\theta}(x_i) - y_i) $$ 

$$  \theta_1 := \theta_1 - \frac{\alpha}{m} \sum_{i=1}^{m}(h_{\theta}(x_i) - y_i)x_i $$ 

**In general**

$$  \theta_j := \theta_j - \alpha (\frac{1}{m} \sum_{i=1}^{m}(h_{\theta}(x_i) - y_i)x_i^j )$$ 

The second part is $$ \alpha \frac{\partial J(\theta_j)}{\partial \theta_j} $$

So every time we substract it becomes more close towards local minima and when it reaches local minima it becomes constant at that point.And we get the final value of $$\theta_0 \mbox{ and }\theta_1$$.So it is appropiate to loop the substraction 500 or 1000 times depends on the initial parameters taken and on the dataset. So that it doesn't have to run forever in order to get the slope and line intercept.  


Let's look at the this image. It tries to minimize the cost and slowly it reaches the minima and then becomes constant at minimum loss.

<img class="image-post" src="{{ site.url }}/images/machine_learning/gradient_descent_exampl.gif" alt="Regression image">

Then we put it in hypothesis function and get the `result`.

<img class="image-post" src="{{ site.url }}/images/machine_learning/predict.png" alt="Regression image">


## Conclusion

* Get the data.
* choose initial $$\theta_0 \mbox{ and }\theta_1$$ and appropiate  $$\alpha$$.
* no of iteration we want to loop it.
* Compute Cost Function.
* Compute final b and final m value by applying Gradient Descent.
* Compute the prediction.
* Be happy and share your knowledge. :heart:

Full code on [Github](https://github.com/chinmaydas96/DLFND/blob/master/week-1(Linear-regrssion)/gradient_descent/Gradient%20descent.ipynb) :heart:

