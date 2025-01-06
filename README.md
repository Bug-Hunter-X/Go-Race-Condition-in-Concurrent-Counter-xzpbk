# Go Race Condition Example

This repository demonstrates a common race condition in Go, specifically in a concurrent counter.  The `bug.go` file contains code that exhibits the race condition, while `bugSolution.go` provides a corrected version using a mutex for synchronization.

## Bug Description
The issue arises from multiple goroutines accessing and modifying the `count` variable concurrently without any synchronization mechanism. This leads to incorrect results and non-deterministic behavior.

## How to Reproduce
1. Clone the repository.
2. Run `go run bug.go`.
3. Observe that the output of the program is not consistently 1000.

## Solution
The `bugSolution.go` file illustrates a correct way to solve this race condition using a mutex to protect the `count` variable from concurrent access.