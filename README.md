# Lab 3: Asymptotic Analysis

This lab focuses on understanding and analyzing the asymptotic behavior of algorithms. We will explore concepts such as Big-O, Big-$\Theta$, and Big-$\Omega$ notations, and apply them to various algorithmic problems to determine their efficiency and scalability.

**Instructions:** To complete this lab, you may work in groups, but you must write your solutions yourself. Once you have completed the lab, push your changes to your forked repository.

## Problem 1

Suppose $T(n)$ is the worst case running time of an algorithm with input size $n$, and we know that $T(n)$ is $\mathcal{O}(n^3)$ and $\Omega(n^2)$. For each of the following statements, determine whether it must be true, must be false, or could be either true or false. Give a brief justification for each. 

1. $T(n)$ is $\mathcal{O}(n^2)$.
    False. The big O of T(n) is equal to n^3. N^3 is then the upper bound. N^2 is faster than n^3 meaning it is out of its upper bound.
2. $T(n)$ is $\Theta(n^3)$.
    Could be either true or false. This is because theta falls between omega and big O (upper and lower bounds). We cannot say that it is exactly one or the other, but it could be. 
3. $T(n)$ is $\Omega(n)$.
    True. The omega is equal to n^2. N^2 is then the lower bound. N^2 is then the lower bound. N is faster than N^2 meaning it is within the lower bound area. 
4. $T(n)$ is $\Theta(n^{1.5})$.
    False. With n^3 being our upper bound and n^2 being our lower bound. N^1.5 does not fall between these bounds, but is faster than these bounds. 
5. $T(n)$ is $\mathcal{O}(n)$.
    False. The big O of T(n) is equal to n^3. N^3 is then the upper bound. N is faster than n^3 meaning it is out of its upper bound. 
6. $T(n)$ is $\Theta(n^2 \log n)$.
    Could be either true or false. The tight bound will fall between n^2 and n^3 due to the multiplication properties of theta. This means that n^2 * log n puts the time between these two bounds. 

## Problem 2
Consider the following algorithm where $f(A, i, j)$ is an unknown algorithm that takes as input an array $A$ and two indicies $i$ and $j$ and returns a number. 

```
Mystery Algorithm
Input: An array of int $A$ of length $n$.
Output: int sum
    n = |A|
    sum = 0
    for i = 1 to n:
        for j = 1 to n:
            sum += f(A, i, j)
```

Without knowing anything about $f$, what can we say about the running time of the Mystery Algorithm in terms of $n$? Justify your answer. 

Answer: 
    Based off counting the steps that the algorithm takes to complete the amount of times that f is being called is n^2. Which means that we can determine that omega and lower bound is n^2, but we cannot determine big O and upper bound because we do not know what f does. Without omega and big O, we cannot determine where theta could reside. 