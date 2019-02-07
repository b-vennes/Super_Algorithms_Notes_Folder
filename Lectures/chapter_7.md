# Chapter 7

## Parallel Algorithms
- Reasons why there isn't always linear speedup
  - communication cost
  - synchronization cost
  - data dependency issues
  - contention
  - overhead of spawning parallel processes/threads

## Definitions
- **spawn** -- a running computation creates a new thread and runs it. At this point there are two computations running in parallel
- **join** -- a computation waits for another thread to complete
- **sync** -- a computation waits for all threadsthat it has spawned in the current function to complete
- **parallel loop** -- a loop in which all iterations of the loop execute simultaneously
- **deadlock** -- when computation comes to a halt due to threads waiting for eachother
- **strand** -- a group of instructions that execute sequentially, often within a single function
- **thread** -- a group of functions that execute sequentially
- **MIMD** -- multiple instruction multiple data -- computation model where each thread independently executes its own set of instructions
- **SIMD** -- single instruction multiple data -- all threads executing the same instructions on their own set of data
- **work** -- total amount of computations performed during an algorithm
- **span** -- total amount of time a computation would take if run in parallel on an infinite number of processors
- **slackness** -- factor by which the parallelism of a computation exceedsthe number of processors -- work/(P*span)
- **speedup** -- amount of work divided by time the processor parallel algorithm takes -- work/span