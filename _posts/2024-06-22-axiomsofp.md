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

# Properties of Probability

Let $S$ be a sample space. Let $A$, $B$, and $C$ be subsets of $S$. Then the following properties hold:

1. $P(A) = 1 - P(A^{\prime})$
   
   **Proof:** Using the axiomatic definition of probability:  
   Since $S = A \cup A^{\prime}$ and $A \cap A^{\prime} = \emptyset$,  
   by property 2, $P(S) = 1$.  
   Thus, $P(S) = P(A \cup A^{\prime}) = P(A) + P(A^{'})$.  
   By property 3, this can be expressed as the sum of the two probabilities.

2. $P(\emptyset) = 0$
   
   **Proof:** Using property 1 of probability. Let the event $A$ be the empty set,  
   $A = \emptyset \rightarrow A^{'} = S$.  
   Then, $P(A) = 1 - P(A^{\prime}) = 1 - 1 = 0$.  
   By property 2 of the axiomatic definition of probability, $P(A^{\prime}) = P(S) = 1$.

3. If $A \subseteq B$, then $P(A) \leq P(B)$
   
   **Proof:** Assume $A \subseteq B$. Then $B$ can be divided into two parts: $B = A \cup (B \setminus A)$, and $A \cap (B \setminus A) = \emptyset$.  
   By the axiomatic definition of probability, $P(B) = P(A \cup (B \setminus A)) = P(A) + P(B \setminus A)$.  
   Since probabilities are non-negative, $P(B \setminus A) \geq 0$, hence $P(B) \geq P(A)$.

4. $P(A) \leq 1$
   
   **Proof:** Using property 3:  
   Since $A \subseteq S$, we have $P(A) \leq P(S) = 1$.

5. $P(A \cup B) = P(A) + P(B) - P(A \cap B)$
   
   **Proof:** Let 1 be $A \setminus B$, 2 be $A \cap B$, and 3 be $B \setminus A$.  
   Then,
   
   $$ P(1 \cup 2 \cup 3) = P(A \cup B) $$
   
   can be expressed as
   
   $$ P(1 \cup 2 \cup 3) = P(A \setminus B) + P(A \cap B) + P(B \setminus A) $$
   
   Adding and subtracting $P(A \cap B)$,
   
   $$ P(1 \cup 2 \cup 3) = P(A \setminus B) + P(A \cap B) + P(B \setminus A) + P(A \cap B) - P(A \cap B) $$
   
   Rewriting the terms,
   
   $$ P(1 \cup 2 \cup 3) = P((A \setminus B) \cup (A \cap B)) + P((B \setminus A) \cup (A \cap B)) - P(A \cap B) $$
   
   Thus,
   
   $$ P(A \cup B) = P(A) + P(B) - P(A \cap B) $$