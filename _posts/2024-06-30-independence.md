---
title: Independence
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024063003_en
tags: Probability
lang: en
---

# Independence

Two events $A$ and $B$ are **independent** if the occurrence or non-occurrence of event $B$ does not affect the probability of event $A$. That is,

$$
P(A \mid B) = P(A)
$$

In this case, the two events $A$ and $B$ are said to be independent. This can also be expressed as

$$
P(A \cap B) = P(A)P(B).
$$

In other words, whether $A$ and $B$ occur or do not occur, they do not affect each other. That is, they are unrelated events.

Independence can also be denoted using the following symbol: $A\perp\kern-5pt \perp B$
{:.info}

From this, the following proposition can be derived.

- If $A$ and $B$ are independent, then $A$ and $B^{\complement}$ are independent.
  
  **Proof:** Suppose $A$ and $B$ are independent. Since $A = (A \cap B) \cup (A \cap B^{\complement})$ and $A \cap B$ and $A \cap B^{\complement}$ are mutually exclusive, we have
  
  $$
  \begin{aligned}
P(A) &= P(A \cap B) + P(A \cap B^{\complement}) \\
&= P(A)P(B) + P(A \cap B^{\complement}) \\
\end{aligned}
  $$
  
  By rearranging the equation, we get
  
  $$
  \begin{aligned}
P(A \cap B^{\complement}) &= P(A) - P(A)P(B) \\
&= P(A)(1 - P(B)) \\
&= P(A)P(B^{\complement}) \\
\end{aligned}
  $$
  
  Therefore, $A$ and $B^{\complement}$ are independent.

We can extend the concept of independence from two events to three events. The definition of mutual independence for three events $A$, $B$, and $C$ is as follows.

Three events $A$, $B$, and $C$ are said to be **mutually independent** if they satisfy the following conditions:

1. $A$, $B$, and $C$ are pairwise independent:
   
   $$
   P(A \cap B) = P(A)P(B), \quad P(A \cap C) = P(A)P(C), \quad P(B \cap C) = P(B)P(C)
   $$

2. The probability of the intersection of all three events is the product of their probabilities:
   
   $$
   P(A \cap B \cap C) = P(A)P(B)P(C)
   $$

For example, this means that $A$ is independent of any event composed of $B$ and $C$.

$$
\begin{aligned}
P[A \cap (B \cup C)] &= P[(A \cap B) \cup (A \cap C)] \\
&= P(A \cap B) + P(A \cap C) - P(A \cap B \cap C) \\
&= P(A)P(B) + P(A)P(C) - P(A)P(B \cap C) \\
&= P(A)[P(B) + P(C) - P(B \cap C)] \\
&= P(A)P(B \cup C)
\end{aligned}
$$

## Pairwise Independent vs Mutually Independent

Here, it is necessary to distinguish between pairwise independence and mutual independence.

- **Pairwise Independent Events**
  
  When there are multiple events, pairwise independence means that each pair of events is independent. That is, for $A_i$ and $A_j$ ($i \neq j$), the following holds:
  
  $$
  P(A_i \cap A_j) = P(A_i)P(A_j)
  $$
  
  For each pair of events, the occurrence of one event does not affect the occurrence of the other event.

- **Mutually Independent Events**
  
  Pairwise independence implies that each pair of events is independent, but it does not necessarily mean that the entire set of events is independent. On the other hand, mutual independence means that all combinations of events are independent. That is, for any $k$ events ($2 \le k \le n$) chosen from $n$ general events $A_1, A_2, \dots, A_n$, the following holds for all permutations $i_1, i_2, \dots, i_k$ of $1, 2, \dots, k$:
  
  $$
  P\left(\bigcap_{j=1}^k A_{i_j}\right) = \prod_{j=1}^k P(A_{i_j})
  $$
  
  The left-hand side represents the probability that events $A_{i_1}, A_{i_2}, \dots, A_{i_k}$ occur simultaneously, and the right-hand side is the product of the probabilities of each event $A_{i_1}, A_{i_2}, \dots, A_{i_k}$ occurring. This equation must hold for all possible combinations of events. This means that the same independence applies to three or more events, not just pairs of events.

Pairwise independence indicates that subsets of events are independent, but it does not guarantee mutual independence of the entire set of events. That is, if events are mutually independent, they are necessarily pairwise independent, but the converse is not true.

The most important takeaway is this: If $A_1, A_2, \dots, A_n$ are mutually independent, then

$$
P(A_1 \cap A_2 \cap \cdots \cap A_n) = P(A_1)P(A_2) \cdots P(A_n).
$$

# Conditional Independence

In probability theory, conditional independence is an important concept. Unlike general independence, conditional independence holds when a specific event $C$ is given. If event $A$ is independent of event $B$ given event $C$, we say that events $A$ and $B$ are **conditionally independent**. This can be expressed mathematically as follows:

$$
P(A \mid B \cap C) = P(A \mid C)
$$

or,

$$
P(A \cap B \mid C) = P(A \mid C)P(B \mid C)
$$

- The proof of $P(A \mid B \cap C) = P(A \mid C)$ is as follows.
  
  We can transform $P(A \mid B \cap C) = P(A \mid C)$ into the following equation:
  
  $$
  \frac{P(A \cap B \cap C)}{P(C)} = \left(\frac{P(A \cap C)}{P(C)}\right)\left(\frac{P(B \cap C)}{P(C)}\right)
  $$
  
  Multiplying both sides by $P(C)$ gives:
  
  $$
  P(A \cap B \cap C) = \frac{P(A \cap C)P(B \cap C)}{P(C)}
  $$
  
  Dividing both sides by $P(B \cap C)$, we get:
  
  $$
  \frac{P(A \cap B \cap C)}{P(B \cap C)} = \frac{P(A \cap C)}{P(C)}
  $$
  
  By the definition of conditional probability, this shows the definition of conditional independence, $P(A \mid B \cap C) = P(A \mid C)$.

Conditional independence is denoted by the following symbol (note that it should be interpreted as $(A \perp\kern-5pt \perp B) \mid C$):

$$
A \perp\kern-5pt \perp B \mid C
$$

In summary, conditional independence means that $A$ and $B$ are independent given $C$. This means that knowing $C$, the occurrence of $B$ does not affect the probability of $A$. In other words, conditional independence indicates that $A$ and $B$ are independent only when the condition $C$ is given.

# Reference

* Ross, S. (2010). *A First Course in Probability (8th ed.)*. Pearson.
* Hogg, R. V., McKean, J. W., & Craig, A. T. (2020). *Introduction to mathematical statistics*. Pearson. 
