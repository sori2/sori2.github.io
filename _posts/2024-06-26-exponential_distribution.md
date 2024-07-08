---
title: Exponential Distribution
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062601_en
tags: Probability
lang: en
---

# Relationship to Poisson Process

Let $N(t)$ be the number of customers coming at a bank in an interval of length $t$. Assuming it following Poisson process with a rate $\lambda$ per each interval of length $1$. Then $N(t) ∼ Poisson(λt)$.

Let $X_1$ be the waiting time until the **first** customer arrives at the bank. We need to find its cumulative distribution function (CDF), probability density function (PDF), and the expected waiting time.

Since the waiting time is nonnegative the cdf of $X_1$ is $F(t)=0$ when $t<=0$, where $t$ is an waiting time. Given $t>0$,

$$
\begin{align*}
F(t) &= P(\text{waiting time is less than } t) = P(X_1 \leq t) = 1 - P(X_1 > t) \\
&= 1 - P(\text{there is no event until } t)
\end{align*}
$$

Define $N(t)$ be the number of customers coming at the bank in an interval of length $t$. Then $N(t) ∼ Poisson(λt)$ and $F(t)$ becomes 

$$
\begin{align*}
&= 1-P(N(t)=0) \\
&= 1 - e^{-\lambda t}.
\end{align*}
$$

Therefore, the waiting time for the first customer has CDF  $1 - e^{-\lambda t}$. Then the probability density function of $X_1$ is 

$$
f(t) = 
\begin{cases} 
\lambda e^{-\lambda t} & \text{if } t > 0 \\
0 & \text{otherwise}
\end{cases}
$$

The **expected waiting time** until the first customer is

$$
\begin{align*}
E(X_1) &= \int_{-\infty}^{\infty} x f(x) \, dx \\
&= \int_{0}^{\infty} x \lambda e^{-\lambda x} \, dx \\
&= \left[ -\frac{1}{\lambda} x e^{-\lambda x} \right]_0^{\infty} + \int_{0}^{\infty} e^{-\lambda x} \, dx \\
&= \left[ 0 + \frac{1}{\lambda} e^{-\lambda x} \right]_0^{\infty} \\
&= 0 + \left( \frac{1}{\lambda} e^{-\lambda \cdot \infty} - \frac{1}{\lambda} e^{-\lambda \cdot 0} \right) \\
&= \frac{1}{\lambda}
\end{align*}
$$

# Exponential Distributions

## Exponential Distributions

The continuous random variable $X$ follows an exponential distribution if its probability density function is: 

$$
f_X(x)=\lambda e^{-\lambda x}
$$

for $\lambda>0$ and $x\ge0$. We denote $X ∼ Exp(λ)$.



## Exponential Properties

Let $X ∼ Exp(λ)$.

- The **mean** is  

  $$
  \mu_X = E(X) = \frac{1}{\lambda}
  $$

- The **variance** is 

  $$
  \sigma^2 = \operatorname{Var}(X) = \frac{1}{\lambda^2}
  $$

- The **moment generating function is** 

  $$
  M(t)=\frac{\lambda}{\lambda-t}
  $$

  for $t < \lambda$.



## Cumulative Distribution Function

Let $X$ have an exponential distribution with mean $μ = 1/λ$. Then the **cdf** of X is:

$$
F_X(x) = 
\begin{cases} 
1- e^{-\lambda x} & \text{for } 0 \le x < \infty \\
0 & \text{for } -\infty < x < 0
    \end{cases}
$$

- When $X ∼ Exp(λ)$,

  $$
  P(X>x)=1-F_X(x)=1-(1-e^{-\lambda x})=e^{-\lambda x}
  $$

  when $x>0.$



## Memoryless Property

One of the most interesting properties of the exponential distribution is its memoryless property, which states that for $X ∼ Exp(λ)$.

$$
P(X ≥ t + t_0 \mid X ≥ t_0)=P(X≥t).
$$

This means that the probability of waiting at least an additional $t$ units of time, given that $t_0$ units of time have already passed, is the same as the probability of waiting $t$ units of time from the start.