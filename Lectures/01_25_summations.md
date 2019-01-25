### 01/25/19
# Algorithms Lecture VI: Summations
### Notes 3:10 - 

## Operations/Identities on Summations
- when encountering a summation, one goal is to transform it to closed form (no sum or product symbol)
- Change index-variable (3.12)
- Explicitly list leading terms (3.12)
  - `sum(k^2\*x^k, k>=0) = 0^2\*x^0 + 1^2*x^1 + sum(k^2\*x^k, k >=2)`
- Swapping order of sums
  - see 03:13 on how to do this, too many number to write down
  - reverses order of sums as long as all the same pairs of values are being added it (not missing anything)
- Factoring out independent sums
  - see 03:13 on how to do this ... too many numbers again

## Known Summations
- listed in 03:14 notes set
- Arithmetic Series
  - `Sum(c_0 + c_1 * k, 0 <= k <= n) = c_0 * n + ([c_1 * n * (n-1)] / 2)`
- Geometric Series
- Binomial Expansions
  - `Sum((m+k)choose(k), 0 <= k <= n) = (m+n+1)choose(n)`
- Finite Sums

## Divergent Sums
- The identities in the *Known Summations* section only work as long as the summations converge

## Summary of Summations
- dealing with summations is like dealing with integrals in calculus
- certain kinds of manipulationsare legal
- the trick is to come up with the right combo that leads to a closed-form result
- Getting good at reaching closedforms takes experience and knowledge of closed-form formulas

## Bounding Summations
- often don't just case about the exact value of a summation, but rather just want to get the asymptotic bound
  - also sometimes a reasonably tight bound on the leading coefficient
- several techniques to be tried
  - mathematical inductioon with inequalities (settings bounds)
  - approximation by integrals
- See notes 04:02 about how to do some of these proofs (way too many values to type here)


# Solving Recurrences