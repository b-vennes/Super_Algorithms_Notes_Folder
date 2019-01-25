### 01/18/19
# Algorithms Lecture III: Analyzing Insertion Sort
---

## Algorothm Analysis Example
### time-complexity of insertion sort

```
insertionSort(lst) =
    if lst = null then null
    else insert(lst.head, insertionSort(lst.tail));

insert(el, lst) =
    if lst = null then el:null
    else if el <= lst.head then el:lst
    else lst.head:insert(el,lst.tail) 
```

- f(n) = maximum number of steps that insert will take for input size n
- g(n) = maximum number of steps that insertionSort will take for input-size n

- f(0) = c0
- f(n) = max(c1, c2 + f(n-1))
  - use max because we're looking at worst case

*missed some notes here*

## Correctness of insertion sort
1. prove that if the algorithm terminates, it produces correct result (partial correctness)
2. prove that the algorithhm terminates

- To prove partial correctness, need to habe a formal specification of what the algorithm is to do
  - output must be sorted

- want to prove that an call to insert(el, lst) does the following:
  1. if lst is sorted, then insert(el, lst) is also sorted
  2. the list el:lst is a permutation of insert(el,lst)

- A common way to prove tha a recursive program is correct is to use mathemtaical induction

- A list is sorted iff either:
  - its length is no greater than 1, or
  - its head is less than or equal to the second element and the tail is sorted
     - head of the list is less than the head of the tail of the list 

- Induction hypothesis is that for both 1. and 2. are satisfied for all lists of length k-1 or less.
  - want to prove that it's true for K

- to prove that the `el:lst` is a permutation of `insert(el,lst)`
  - need to define what it means to be a perumation
  - list `a` is a perm of `b` iff one of the following is true:
    - `a` and `b` are both non null
    - `a` and `b` are both non-null, `a.head=b.head` and `a.tail` is a permutation `b.tail`
    - `a` and `b` are both non-null, `a.head!=b.head` and there exists a `c` such that
      - `a.tail` is a perm of `(b.head):c` and
      - `b.tail` is a perm of `(a.head):c`

*missing proof notes*

- correctness proof for `insertionSort` is by induction and we are allowed to assume `insert` is correct as a lemma.
  - Need to prove `insertionSort(lst)` is sorted
  - need to prove that lst is a permutation of `insertionSort(lst)`

*see notes 02 for proofs*

