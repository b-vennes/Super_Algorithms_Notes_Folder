### 01/14/19
# Algorithms Lecture I: Syllabus Day
---

## Objectives
- learn techniques for determining time complexity
- learn about algorithm design paradigms
- better algorithms exist
- understand NP-completeness
    - prove a problem is NP complete

## Assignment 0
- send email with the following:
    - why I’m taking this course
    - what I expect to get out of this course
    - what math courses I’ve taken beyond Calculus 2
    - love of math on a scale of 0 to 10
    - digital or paper slides

## Time-complexity
- given an algorithm, what is the worst-case running time as function of problem size?
- what is the average-case running time as a function of problem size?
- what is the running time of the fastest algorithm for solving a given problem?


## Time-complexity: machine model
- to determine how long an algorithm takes, we need to know how much each primitive operation costs
    - have a machine model that is pretty close to the machines actually used
- use RAM model of computation
    - one operation occurs at a time

## Major CS 324 Topics
- algorithm design paradigms
    - incremental (insertion sort)
        - solve slightly smaller problem; then incorporate an additional piece
    - divide and conquer (quicksort)
        - divide problem into subproblems; combine solutions
    - greedy (fractional knapsack)
        - find locally optimal solutions and combine
