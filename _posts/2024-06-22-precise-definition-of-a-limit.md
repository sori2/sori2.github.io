---
title: Precise Definition of a Limit
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062204_en
tags: Calculus
lang: en
---

# Limits of Function

Most readers will have encountered the concept of limits during their high school math classes. When discussing a function $f(x)$, if $x$ approaches $a$ and $f(x)$ gets *arbitrarily close* to a constant value $L$, we say that $f(x)$ converges to $L$ and denote this by $\lim_{x \rightarrow a} f(x) = L$.

Most students understand this concept superficially and move on without much thought. However, from a mathematical perspective, what does it mean to get "arbitrarily close"? If you find this expression too vague, you are ready to move beyond high school math to more rigorous thinking.

So, how can we express "arbitrarily close" in a mathematically precise and rigorous way? This problem is solved by the epsilon-delta ($ϵ,δ$) definition introduced by the 19th-century mathematician Augustin-Louis Cauchy. The epsilon-delta definition provides a formal framework for understanding limits.



# ($\epsilon,\delta$)-definition of Limit
Let $f(x)$ be a function defined on some open interval that contains the number $a$, except possibly at $a$ itself. We say that the limit of $f(x)$ as $x$ approaches $a$ is $L$, and we write $\lim_{x \to a} f(x) = L$ if for every number $\epsilon > 0$ there is a number $\delta > 0$ such that if $0 < |x - a| < \delta$, then $|f(x) - L| < \epsilon$.

This means that for every $x$ within a range of $\delta$ from $a$ but not equal to $a$, the corresponding $f(x)$ values lie within a range of $\epsilon$ from $L$. In other words, $\epsilon$ and $\delta$ serve to mathematically define how close $x$ must be to $a$ for $f(x)$ to be as close as desired to $L$.

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/sori2/sori2.github.io/master/png/pdl1.png">
  <br>
  Figure 1. An illustration of the epsilon-delta definition of a limit.
</p>

To put it more precisely, if any small interval $(L-\epsilon, L+\epsilon)$ is given around $L$, then we can find an interval $(a-\delta, a+\delta)$ around a such that $f$ maps all the points in  $(a-\delta, a+\delta)$, except possibly $a$ itself, into the interval $(L-\epsilon, L+\epsilon)$.

<p align="center">
  <img width="800" src="https://raw.githubusercontent.com/sori2/sori2.github.io/master/png/pdl2.png">
  <br>
  Figure 2. Geometric interpretation of limits can be given in terms of the graph of a
function.
</p>



One important point to note is that the epsilon-delta method is not a tool for finding the limit value $L$. Instead, it is a proof technique used to rigorously verify that $L$ is indeed the limit value, assuming we already know $L$. The goal of the epsilon-delta method is as follows: given any arbitrary $\epsilon$, no matter how small, we must find a $\delta$ that satisfies the definition of the epsilon-delta method. The $\delta$ is dependent on $\epsilon$, meaning that it is a function of $\epsilon$.



# Reference

* Stewart, J. (2018). *Calculus: Early Transcendentals*.
