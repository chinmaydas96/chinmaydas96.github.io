---
layout: post
title: What is Machine Learning and Types — Part-1
description: "Definition & Types "
headline: "Machine Leaning Part-1"
categories: Machine_Learning
tags: 
  - machine_learning
  - MOOC

comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/machine_learning/ml.png" alt="machine learning intro">

I have in been reading quite a few months about what is machine learning and how to apply it in practical application .Well the story begin when I first time read about the Google’s self driving car Waymo . Then suddenly I read about how it works . Then I heard the term `Machine Learning` . Then I attended Pycon India conference for better intuition .I just attended some talks there about machine learning .And unfortunately all were gone by the side of my ear .Then I started googling it . And in most of the blog and in quora I heard about coursera [Machine Learning](https://www.coursera.org/learn/machine-learning) course by Andrew ng  to begin with. Suddenly I jumped right into it .


In this post I will briefly mention  machine learning  defintion and types.



> What is machine learning ?


Two definitions of Machine Learning are offered.

`Arthur Samuel` described it as: *The field of study that gives computers the ability to learn without being explicitly programmed.* This is an older, informal definition.


`Tom Mitchell` provides a more modern definition: *A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E.*

#### Example :

I will make a simple example to understand better . Imagine you have some pair of numbers . Then you put only 1 number into a machine to predict the other half of the pair .

(2,4),(3,6),(4,9) . The computer program have to predict the second number for (5 , `?`)

The program first need to find the logic between the pairs and then apply the same logic to predict the number . To find that logic is called **`machine learning`** . So that after find the logic it can apply same logic to predict each number .

> Types of Machine Learning

In general there are 3 types of machine learning .

1. Supervised learning
2. Unsupervised learning
3. Reinforcement learning


### Supervised learning

In `supervised learning`, we are given a data set and already know what our correct output should look like, having the idea that there is a relationship between the input and the output.

Supervised learning problems are categorized into `regression` and `classification` problems. In a `regression problem`, we are trying to predict results within a continuous output, meaning that we are trying to map input variables to some continuous function. In a `classification problem`, we are instead trying to predict results in a discrete output. In other words, we are trying to map input variables into discrete categories.

##### Example 1:

Given data about the size of houses on the real estate market, try to predict their price. Price as a function of size is a continuous output, so this is a regression problem.

We could turn this example into a classification problem by instead making our output about whether the house “sells for more or less than the asking price.” Here we are classifying the houses based on price into two discrete categories.

##### Example 2:

(a) `Regression` — Given a picture of a person, we have to predict their age on the basis of the given picture
(b) `Classification` — Given a patient with a tumor, we have to predict whether the tumor is malignant or benign.

### Unsupervised Learning

`Unsupervised learning` allows us to approach problems with little or no idea what our results should look like. We can derive structure from data where we don’t necessarily know the effect of the variables.

We can derive this structure by clustering the data based on relationships among the variables in the data.
With unsupervised learning there is no feedback based on the prediction results.

##### Example 1:

`Clustering:` Take a collection of 1,000,000 different genes, and find a way to automatically group these genes into groups that are somehow similar or related by different variables, such as lifespan, location, roles, and so on.

`Non-clustering:` The “Cocktail Party Algorithm”, allows you to find structure in a chaotic environment. (i.e. identifying individual voices and music from a mesh of sounds at a cocktail party).

##### Example 2:

I am bad at making coffee . So one day I was decided to build a model to predict the quality of my coffee based on the quantity of sugar , milk ,coffee powder . Unfortunately that didn’t go well .But Still hope I will build a effective model on that .

### Reinforcement learning

`Reinforcement learning` is an area of machine learning inspired by behaviorist psychology, concerned with how software agents ought to take actions in an environment so as to maximize some notion of cumulative reward.

##### Example 1:

Consider teaching a dog a new trick .You cannot tell it what to do, but you can reward/punish it if it does the right/wrong thing. It has to figure out what it did that made it get the reward/punishment. We can use a similar method to train computers to do many tasks, such as playing backgammon or chess, scheduling jobs, and controlling robot limbs.

##### Example 2:

Teaching a game bot to perform better and better at a game by learning and adapting to the new situation of the game.


> That’s all for today folks .Thanks for your patience .Let me know if there are errors in the post as it’s my first post .


























