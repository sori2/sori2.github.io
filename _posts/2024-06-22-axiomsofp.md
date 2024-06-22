---
title: Axiom of Probability
sidebar:
  nav: docs-en
aside:
  toc: true
key: 2024062203_en
tags: Probability
lang: en
---

# Axiom of Probability

Probability theory is a branch of mathematics that deals with the likelihood of events occurring. The foundation of probability theory is built on three fundamental axioms, which provide a rigorous basis for defining and working with probabilities. These axioms ensure that probabilities are assigned in a consistent and logical manner.

A function $P$ is called a **probability function** if it satisfies the following three axioms, and $P(A)$ is the probability of event $A$.

1. **Non-negativity**: The probability of any event is a non-negative number.

   $$P(A) \ge 0$$

2. **Normalization**: The probability of the entire sample space $S$ is 1. 

   $$P(S) = 1$$

3. **Additivity**: For any **mutually exclusive** events $A_1, A_2, \ldots$ in the sample space $S$,

   $$P(\bigcup_{k=1}^{\infty}A_k)=\sum_{k=1}^{\infty}P(A_k)$$

The probability function $P$ is defined as a mapping

$$P: \{A \subseteq S\} \rightarrow [0,1] \subseteq \mathbb{R}$$

where $S$ is the sample space and $A$ is any event within $S$.

These axioms serve as the foundation for probability theory, allowing us to model and analyze random phenomena in a consistent way. By adhering to these axioms, we ensure that the probabilities assigned to events behave in a logical and predictable manner.