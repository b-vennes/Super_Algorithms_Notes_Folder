### 01/30/19
### Notes 05:07 - 
# Algorithms Lecture VIII: Solving Recursions, Introduction to Divide and Conquer

## Master Method
- used to find the asymptotic value when recurrence is of a standard form
- see notes 05:07

## Induction: dealing with ceilings or floors
- Ceilings (and floors in general) can cause problems
  - This problem does not occur with master theorem

## Divide and Conquer Algorithms
- many algorithms can be split into subproblems, which can then be recursively solved

## Strassen's Algorithm
- computes matrix multiplication in about O(n^lg(2.87)) time
- Uses 7 multiplications and 18 additions

## Parallel Algorithms
- Increases the speed of an algorithm
- Ideally we can get N linear speed up by adding more cores
- Less speedup in practice
  - communication cost
  - synchronization cost
  - data dependency issues
  - contention
  - overhead of spawning parallel processes/threads

## Parallel Programming Models

