# Chapter 1

## Objectives
- learn techniques for determining time complexity
- learn about algorithm design paradigms
- better algorithms exist
- understand NP-completeness
    - prove a problem is NP complete

## Time-complexity
- given an algorithm, what is the worst-case running time as function of problem size?
  - example: insertion sort
- what is the average-case running time as a function of problem size?
  - example: insertion sort
- what is the running time of the fastest algorithm (asymptotic, worst-case) for solving a given problem?
  - example: sorting, matrix multiplication

## Time-complexity: machine model
- to determine how long an algorithm takes, we need to know how much each primitive operation costs
    - have a machine model that is pretty close to the machines actually used
- use RAM model of computation
    - one operation occurs at a time
    - memory access (read/write) takes constant time
