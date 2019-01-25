### 01/23/19
# Algorithm Lecture V: O, Theta, and Omega Notation
### Notes 02:31 - 03:09

## **O-Notation and Friends**
- general idea of O-notation is to indicate how a function grows *asymototically* (proportional to N, NlogN, N^2, etc.)
- `theta(N^2)` -- grows proportional to N^2
- `O(N^2)` -- grows no faster than proportional to N^2
- `omega(N^2)` -- grows no slower than proportional to N^2
- `o(N^2)` -- grows slower than porportional to N^2
- `little-omega(N^2)` -- grows faster than proportioal to N^2
- technically could call any linear-time algorithm O(N^2) because its no faster than N^2
- `3N^2+6N+2=theta(N^2)`
  - means that the expression on the left is an element of the set of functions that grow proportional to N^2
  - always go from most specific on left to least specific on right
    - most_specific=least_specific

## **Theta-Notation and Friends**
- `f(n)=theta(n^2)` means that f(n) grows in proportion to n^2
  - it doesn't grow faster and it doesn't grow slower
  - there exists constants c_1, c_2, and n_0 such that `0 <= c_1\*n^2 <= f(n) <= c_2\*n^2`
  - f(n) = theta(g(n)) iff f(n) = O(g(n)) and f(n) = omega(g(n))

## Mathematical definitions
- **Monotonicity**
  - monotonically increasing -- f(n) does not decrease as n increases
  - strictly increasing -- f(n) increases as n increases
  - monotonically decreasing -- f(n) does not increase as n increases
  - strictly decreasing -- f(n) decreases as n increases
- **Logarithms**
  - log x -- logarithm of x, base unpecified
  - log_a x -- logarithm of x base a
  - log_2 x = log_10 x / log_10 2