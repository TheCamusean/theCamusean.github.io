---
layout: post
mathjax: True
title:  "Learning Optimal Controllers through HJB & PMP"
fields: "optimalcontrol"
extra: "Optimal Control"
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

Let's apply dynamic programming approach on the value function. The value function can be represented in dependence on the previous instant. Rewritting Eq. \ref{eq:value_func}

\begin{equation}
\begin{split}
  V(x,t) = \min_u(r(t,x,u)dt + V(t+dt,x+f(x,u,t)dt))\approx \\
  min_u(r(t,x,u)dt + J(x,t) + \partial_t J(x,t)dt + \partial_x J(x,t)f(x,u,t)dt)
  \label{HJB001}
\end{split}
\end{equation}

where in the second line a Taylor expansion of the dynamic programming has been done. From Eq. \ref{HJB001}, we can obtain the Hamilton-Jacobi-Bellman equation

\begin{equation}
  -\partial_t J(x,t) = \min_u (r(x,t,u) + \partial_x J(x,t)f(x,u,t))
  \label{HJBEQ}
\end{equation}

As it will be used in the future for computing by PMP, The Hamiltonian is represented in right-hand side

\begin{equation}
  H = r(x,t,u) + \partial_x J(x,t)f(x,u,t)
  \label{Hamilton}
\end{equation}

The optimal controller will be obtained when the derivative of the Hamiltonian equals 0 $\frac{dH}{du}=0$.

In order to compute the optimal controller and so, solve the optimal control problem some assumptions must be done on the dynamic system $f(x,u,t)$ and the cost function $r(x,u,t)$.

## Pontryagin's Minimum Principle
