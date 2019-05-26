---
layout: post
mathjax: True
title:  "Learning Optimal Controllers through HJB & PMP"
date:   2019-05-26 23:12:04 +0100
categories: jekyll update
---
# Learning Optimal Controllers Through HJB & PMP

When it comes to Optimal Control Theory, two main approaches has been considered in order to solve it. On one side, the famous Hamilton-Jacobi-Bellman equation and on the other side, Pontryagin's Maximun Principle.

But first, let's formalize the problem. Assume a dynamical system

$$ \dot{x} = f(x,u,t)$$
