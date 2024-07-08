---
title: "Conditional Probability"
categories: [Probability]
tag: [Probability]
toc: true
toc_sticky: true
author_profile: true
---

# Conditional Probability

One of the most important concepts in probability theory is **conditional probability**. The importance of the concept of conditional probability lies in two main aspects:

- It allows us to calculate probabilities when partial information about the outcome of an experiment is available.
- It simplifies the calculation of probabilities even when partial information is not available.

The formal definition of conditional probability is the probability of one event occurring given that another event has already occurred. Mathematically, it is expressed as follows:

The conditional probability of $A$ given $B$ is defined by

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

if $P(B) > 0$.

Here, $\mid$ is often read as "given". This is often referred to as an *updated probability* because it updates the existing probability with more information.

Additionally, conditional probability can be understood as **reducing the sample space**. For two events $A$ and $B$ in the sample space $S$, the conditional probability $P(A \mid B)$ considers event $B$ as the new sample space and represents the probability that $A \cap B$ occurs within this new sample space.

For example, let's calculate the probability of rolling a 2 given that an even number has been rolled on a die. The condition here is "given that an even number has been rolled". Let $B$ be the event that an even number is rolled, and let $A$ be the event that a 2 is rolled. Originally, the sample space for rolling a die is $\\{1, 2, 3, 4, 5, 6\\}$. Given that an even number is rolled, the sample space reduces to $B = \\{2, 4, 6\\}$. Within this new sample space, the event $A \cap B$ is $\\{2\\}$. Thus, $P(A \mid B) = \frac{1}{3}$. Alternatively, we can use the formula directly. The probability of rolling a 2 within the original sample space is $P(A \cap B) = \frac{1}{6}$, and the probability of rolling an even number is $P(B) = \frac{1}{2}$. Thus, $P(A \mid B) = \frac{P(A \cap B)}{P(B)} = \frac{1/6}{1/2} = \frac{1}{3}$.

According to the above formula, we obtain the following results:

1. $P(B \mid A) \ge 0$
2. $P(A \mid A) = 1$
3. If $B_1, B_2, \cdots$ are mutually exclusive events, then $P\left(\bigcup_{n=1}^\infty B_n \mid A\right) = \sum_{n=1}^\infty P(B_n \mid A)$

The proof for property $(3)$ is as follows. (Proofs for $(1)$ and $(2)$ are straightforward.)

If the sequence of events $B_1, B_2, \cdots$ are mutually exclusive, then for $i \neq j$,

$$
(B_i \cap A) \cap (B_j \cap A) = \emptyset
$$

holds. Therefore,

$$
\begin{aligned}
P\left(\bigcup_{n=1}^\infty B_n \mid A\right) &= \frac{P\left[\bigcup_{n=1}^\infty (B_n \cap A)\right]}{P(A)} \\
&= \sum_{n=1}^\infty \frac{P(B_n \cap A)}{P(A)} \\
&= \sum_{n=1}^\infty P(B_n \mid A)
\end{aligned}
$$

- Note: $\left(\bigcup_{n=1}^\infty B_n\right) \cap A = (B_1 \cup B_2 \cup \cdots) \cap A = (B_1 \cap A) \cup (B_2 \cap A) \cup \cdots = \bigcup_{n=1}^\infty (B_n \cap A)$

## Multiplication Rule of Probability

By the definition of conditional probability, we can write

$$
P(A \cap B) = P(B)P(A \mid B)
$$

known as the multiplication rule (if $P(B) > 0$).

Also, generalizing this for an arbitrary number of events, the formula for the probability of their intersection is as follows:

$$
\begin{aligned}
P(A_1 \cap A_2 \cap \cdots \cap A_k) &= P(A_1)P(A_2 \mid A_1)P(A_3 \mid A_1 \cap A_2) \cdots P(A_k \mid A_1 \cap A_2 \cap \cdots \cap A_{k-1}) \\
&=\prod_{i=1}^kP\left(A_i\mid\bigcap_{j=1}^{i-1}A_j\right)
\end{aligned}
$$

if $P(A_1 \cap A_2 \cap \cdots \cap A_{k-1}) > 0$.

To prove the multiplication rule, we apply the definition of conditional probability to the right-hand side:

$$
P(A_1 \cap A_2 \cap \cdots \cap A_k) = P(A_1) \cdot \frac{P(A_1 \cap A_2)}{P(A_1)} \cdot \frac{P(A_1 \cap A_2 \cap A_3)}{P(A_1 \cap A_2)} \cdots \frac{P(A_1 \cap A_2 \cap \cdots \cap A_k)}{P(A_1 \cap A_2 \cap \cdots \cap A_{k-1})}
$$

# References

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 