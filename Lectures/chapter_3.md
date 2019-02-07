# Chapter 3

## **Theta-Notation and Friends**
- f(n)=theta(n^2) means that f(n) grows in proportion to n^2
  - it doesn't grow faster and it doesn't grow slower
  - there exists constants c_1, c_2, and n_0 such that 0 <= c_1\*n^2 <= f(n) <= c_2\*n^2 for all n > n_0
  - f(n) = theta(g(n)) iff f(n) = O(g(n)) and f(n) = omega(g(n))