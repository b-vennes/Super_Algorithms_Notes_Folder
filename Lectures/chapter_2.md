# Chapter 2


## Major CS 324 Topics
- algorithm design paradigms
    - **incremental** (insertion sort)
        - solve slightly smaller problem; then incorporate an additional piece
    - **divide and conquer** (quicksort)
        - divide problem into subproblems; combine solutions
    - **greedy** (fractional knapsack)
        - find locally optimal solutions and combine
    - **randomized** (e.g. order-statistics and median)
      - use random-number generator to get statistically high probability of an efficient or correct solution
    - **dynamic-programming** (e.g. all-pairs shortest-path)
      - reuse subproblem solutions
    - **transformation** (e.g. Vegdahl's thesis)
      - transform problem into one with a known solution
- algorithm analysis
    - worst-case or avg-case
    - produce recurrence relation and solve
- exposure to clever non-intuitive alg.
    - try harder to solve tough problem
    - minimize ideas of maximum optimization
- problem analysis
  - upper and lower bounds
  - **NP-completeness**
    - understnading what it is
    - proving it
    - efficient solutions

## Problems and Algorithms
- **problem** : what needs to get done, what a computation is supposed to do
    - ex. sorting : output list should contain same as input but reordered in order
    - ex. factoring : output should be a sequence of prime numbers such that the product is the original input
- **algorithm** : sequence of steps to solve a problem
  - often many different algorithms to solve the same problem
- different algorithms often have different time complexities
- **time complexity** : how long an algorithm runs as a function of problem size
  - difficult to determine time complexity of a problem
    - easy(ish) to determine the time complexity of an algorithm
- can find exact complexity of a problem when the upper and lower bounds are the same
- for determining upper/lower bounds, always look at the worst-case
- upper bound : worst-case time complexity of the algorithm with the best worst-case time complexity of the problem
    - uses big-O notation
- lower bound : worst-case time complexity for the best possible algorithm that could exist (must be determined mathematically)
    - uses omega notation

## Upper and Lower Bounds
- upper bound based on fastest known algorithm
- lower bound often based on a mathematical proof

## Worst-case vs Average case
- time complexity based on how an algorithm performs for the worst possible case
- analyze average when:
    - all possible inputs equally likely
    - analyzing a random-distribution algorithm
      - worst-case should never occur in practice

## Mathematical Induction
1. prove a base case
2. prove that if the statement is true for n-1 then its also true for n

## O-Notation and Friends: introduction
- general idea of O-notation is to indicate how a function grows *asymototically* (proportional to N, NlogN, N^2, etc.)
- **theta(N^2)** -- grows proportional to N^2
  - proportional to / equal to
  - f(n) = theta(N^2)
- **O(N^2)** -- grows no faster than proportional to N^2
  - upper bound
  - f(n) <= N^2
- **omega(N^2)** -- grows no slower than proportional to N^2
  - lower bound
  - f(n) >= N^2 
- **o(N^2)** -- grows slower than porportional to N^2
  - hard upper bound
  - f(n) < N^2
- **little-omega(N^2)** -- grows faster than proportioal to N^2
  - hard lower bound
  - f(n) > N^2
- technically could call any linear-time algorithm O(N^2) because its no faster than N^2
- 3N^2 + 6N + 2 = theta(N^2)
  - means that the expression on the left is an element of the set of functions that grow proportional to N^2
  - always go from most specific on left to least specific on right
    - most_specific = least_specific