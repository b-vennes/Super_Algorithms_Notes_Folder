# Chapter 6

## Divide and Conquer Algorithms
- **divide** the problems into subproblems that are the same kind of problem as the original but smaller, all subproblems are approximately the same size
- **conquer** the subproblems by solving them recursively
- **combine** the subproblem solutions into a solution for the whole problem

## Strassen's Algorithm

[ A B ] [ E F ] -- [ R S ]  
[ C D ] [ G H ] -- [ T U ]  
  
P1 = A(F-H)  
P2 = (A+B)H  
P3 = (C+D)E  
P4 = D(G-E)  
P5 = (A+D)(E+H)  
P6 = (B-D)(G+H)  
P7 = (A-C)(E+F) 
  
R = P5 + P4 - P2 + P6  
S = P1 + P2  
T = P3 + P4  
U = P5 + P1 - P3 - P7  

- Strassen's algorithm is only faster when greater than 44x44