### 01/21/2019
## Algorithms Lecture IV: Median Fidning Algorithm
### Notes 02:27 -

### Median Finding Algorithm:
- non-intuitive, surprisingly efficient algorithm
  - solution of a non-trivial recurrence relation
  - Algorithm: 
    - find nth smallest element in an unsorted M-element list
    ```
        1 ... 17  ... 32
              ^^ finds 17th element
    ```
    - find a key element that is numerically in the middle 40% of elements
    ```
        | 30% | 40% | 30% |
                ^^^ element guranteed to be in here
                ^^^ key taken from this group
        ^^^ elements less than key >= 30%
                    ^^^ elements greater than key >= 30% 
    ```
    - split into elements less than key (lowList) and those greater than key (hiList) (neither list will be larger than 70% of our orig list)
    ```
        find (21, list)
        15 | < key |
        1 | = key |
        45 | > key | << 21st element must be in this list --- then call find(5, <list of 45 elements>
    ```
    - two issues:
      - how to find a key guaranteed to be in middle 40%
      - this looks like a recursive call with a logarithmic number of recursive levels (nlgn algorithm)
    - finding a middle 40%
    ```
        group into 5 element groups and find median of each
        call find recursively on the medians
        |   |   |   |   |   |   |   |
        call find on the set of medians to find the medians of medians
    ```
    - Example:
    ```
        1. number list: 13 42 11 2 17 73 3 94 47 86 22 33 1 12 7 9 28 8 1337 19 14 4 15 64 31
        2. chunk into groups of 5: (call find(13, origList))
        | 13 42 11 2 17 | 73 3 94 47 86 | 22 33 1 12 7 | 9 28 8 1337 19 | 14 4 15 64 31 |
         13              73              12             19               15             = newList
        3. call find(3, newList) = 15
        4. split into lessList, equalList, and greaterList
        lessList = 13 11 2 3 1 12 7 9 8 14 4
        equalList = 15
        greaterList = 42 17 73 94 47 86 22 33 28 19 6431
        5. get rid of the lessList since the number of elements in lessList is less than 13
        6. toss out equal list because 1 + 11 < 13
        7. chunk up greaterList into sets of 5 (call find(1,greaterList))
        | 42 17 73 94 47 | 86 22 33 28 1337 | 19 64 31 |
        47 33 31
        >> 33
        8. group into less, equal greater with key 33
        less = 17 22 28 19 31
        equal = 
        greater = 
        9. toss out equal and greater since we are looking for 1st smallest element
        10. fewer than 10 elements so we use inspection to find smallest from list
        >> 17
    ```
  - Showing the algorithm is linear time
    - call to find on a list of N has the following components
      - a call to find on a list whose size is N/5 (find median of medians)
      - a call to find on a list whose size is between 3N/10 and 7N/10 (split things up)
        - assume 7N/10 for worst case
      - do O(N) operations (splitting elements into groups of 5, finding each median, splitting elements based on being greater or less than the key)
      - yields following recurrecne relation
        - T(1) = C_0
        - T(N) = T(N/5) + T(7N/10) + C_1\*N
        - See notes 2:30 for additional notes on this