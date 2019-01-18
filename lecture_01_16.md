### 01/16/19
# Algorithms Lecture II: Overview of Problems, Algorithms, and Time-complexity
---

## Main Topics:
- algorithm analysis
    - worst-case or avg-case
    - produce recurrence relation and solve
- exposure to clever non-intuitive alg.
    - try harder to solve tough problem
    - minimize ideas of maximum optimization

## Problems and Algorithms
- **problem** : what needs to get done
    - ex. sorting : output list should contain same as input but reordered in order
    - ex. factoring : output should be a sequence prime numbers such that the product is the original input
- **algorithm** : sequence of steps to solve a problem
- different algorithms often have different time complexities
- **time complexity** : how long an algorithm runs as a function of problem size
- difficult to determine time complexity of a problem
    - easy(ish) to determine the time complexity of an algorithm
- can find exact complexity of a problem when the upper and lower bounds are the same
- for determining upper/lower bounds, always look at the worst-case
- **upper bound** : worst-case time complexity of the algorithm with the best worst-case time complexity of the problem
    - uses big-O notation
- **lower bound** : worst-case time complexity for the best possible algorithm that could exist (must be determined mathematically)
    - uses omega notation

## Worst-case vs Average case
- time complexity based on how an algorithm performs for the worst possible case
- analyze average when:
    - all possible inputs equally likely
    - analyzing a random-distribution algorithm

## Mathematical Induction
1. prove a base case
2. prove that if the statement is true for n-1 then its also true for n
- equivalent to proving a proof exists
  - or can view as a special case of proof by contradiction