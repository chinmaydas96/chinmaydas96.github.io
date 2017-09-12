---
layout: post
title: Understanding Logistic Regression —  Part-3.1
description: "Math Behind Logistic Regression Works"
headline: "Machine Leaning Part-3.1"
categories: Machine_Learning 
tags: 
  - machine_learning
  - classification_model

comments: true
mathjax: null
featured: true
published: true 
---

<img class="image-post" src="{{ site.url }}/images/machine_learning/lr2.jpg" alt="Classification image">

> Let's look at the Mathematics behind the **Logistic Regression** model.

In both Supervised and Unsupervised machine learning `Classfication` is widely applied in pretty much every fields. From Separating Dogs and Cats to Traffic sign recognition in Self Driving Cars , Classification models are used everywhere.

So there are two classification model. One is `Binary Classification` (classify between two things) and another is `Multiclass Classification`.

In this post I will write about one of the Supervised Classification Algorithm called Logistic Regression algorithm. It is the simplest and most basic Classification algorithm. 

> And NO, Logistic Regression is not a Regression algorithm.

It is derived from Linear Regression algorithm that's why it is called so. I mentioned in Part-1 about Supervised Classification
method. So we are given a lebeled input data with features and we need to derived a model to classify on other example.

So let's visualise a datasets.  