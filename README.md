# Off-by-One Error in C++ Vector Iteration

This repository demonstrates a common off-by-one error when iterating through a `std::vector` in C++.  The error occurs due to an incorrect loop condition that attempts to access an element beyond the vector's valid index range.

## The Bug

The file `bug.cpp` contains code that iterates through a vector using a loop with the condition `i <= vec.size()`. This is incorrect; it should be `i < vec.size()`. The consequence of using `<=` is accessing the element at index `vec.size()`, which is out of bounds, resulting in undefined behavior (often a crash or unexpected output).

## The Solution

The file `bugSolution.cpp` provides the corrected code with the loop condition changed to `i < vec.size()`.  This ensures that the loop only iterates through valid indices of the vector.

## How to reproduce

1. Clone this repository.
2. Compile `bug.cpp` and run the executable. Observe the error (crash or incorrect output).
3. Compile `bugSolution.cpp` and run the executable. Observe the correct output.