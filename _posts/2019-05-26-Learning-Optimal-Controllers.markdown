---
layout: post
mathjax: True
title:  "Learning Optimal Controllers through HJB & PMP"
date:   2019-05-26 23:12:04 +0100
categories: jekyll update
---
# Learning Optimal Controllers Through HJB & PMP

When it comes to Optimal Control Theory, two main approaches has been considered in order to solve it. On one side, the famous Hamilton-Jacobi-Bellman equation and on the other side, Pontryagin's Maximun Principle.

But first, let's formalize the Optimal Control problem. Assume a dynamical system


\begin{equation}
    \dot{x} = f(x,u,t)
\end{equation}

and a Value function

\begin{equation}
V(x,u,t) = \int_{0}^{\inf} r(x,u,t) dt.
\end{equation}

The objective is to minimize the value function

\begin{equation}
    V^{*}(x,u,t) = \arg \min_u \int_{0}^{\inf} r(x,u,t) dt
    \label{eq:value_func}
\end{equation}

In order to solve this problem, two main paths has been studied. On one side, extending the work of [Hamilton & Jacobi](https://en.wikipedia.org/wiki/Hamilton%E2%80%93Jacobi_equation), Bellman developed the [Hamilton-Jacobi-Bellman equation](http://fourier.dur.ac.uk/Ug/projects/highlights/PR4/Smears_HJB_report.pdf)(HJB) in the decade of the 60's. On the other hand, Pontryagin's approach is also well known as the Pontryagin's Maximun Principle(PMP).

## Hamilton-Jacobi-Bellman equation

Based on the previous work on Dynamic Programming, Bellman found an extension on the Hamilton-Jacobi equation in order to solve the Optimal Control problem.

Let's apply dynamic programming approach on the value function. The value function can be represented in dependence on the previous instant. Rewritting Eq. \cite{eq:value_func}

\begin{equation}
  
\end{equation}
