# Chapter 5

## Solving Recurrences
- Three Techniques
  - substitution (induction)
  - iteration/expansion
  - master method
- goal is to turn a recurrence to a closed form

## Iteration/Expansion (recursion tree)
- sometimes you can expand out the recurrence and see a pattern

## Master Method
- can be used to find the asymptotic value when the recurrence divides the problem into equal sized problems
- recurrence is in the form of T(n) = aT(n/b) + f(n)
- key is to look at which of n^log(a,base=b) or f(n) grows faster
- if f(n) = little-omega(n^log(a,base=b)), then complexity is theta(f(n))
- if f(n) = theta(n^log(a,base=b)), then the complexity is theta(f(n)log(n))
- if f(n) = o(n^log(a,base=b)), then the complexity is theta(n^log(a,base=b))