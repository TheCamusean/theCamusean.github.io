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

and a Cost function

$$ J(x,u,t) = \int_{0}^{\inf} r(x,u,t) dt$$.

The objective is to minimize the value function

\begin{equation}
    V(x,u,t) = \arg \max_u \int_{0}^{\inf} r(x,u,t) dt
\end{equation}

In equation \eqref{eq:sample}, we find the value of an
interesting integral:

\begin{equation}
  \int_0^\infty \frac{x^3}{e^x-1}\,dx = \frac{\pi^4}{15}
  \label{eq:sample}
\end{equation}

not appears :(
