# Matrix Multiplication with Threading

## Methodology

### Objective

The objective of this experiment is to evaluate the performance gain obtained by using multiple threads for matrix multiplication tasks. The experiment involves multiplying a constant matrix `A` of size `(1000, 1000)` with 100 randomly generated matrices of size `(3000, 3000)` using different numbers of threads.

### Implementation

#### Dependencies
- `numpy`: For numerical computations and matrix operations.
- `threading`: For creating and managing threads.
- `time`: For measuring the execution time of the thread-based matrix multiplication.
- `tabulate`: For displaying the results in a table format.
- `matplotlib.pyplot`: For plotting the results graphically.

#### Procedure

1. Initialize a constant matrix `A` of size `(1000, 1000)` and generate 100 random matrices of size `(3000, 3000)`.
2. Define a `matrix_multiply` function that performs matrix multiplication between matrix `A` and a given matrix from the list of random matrices.
3. Implement the `run_with_threads` function to create and manage threads for matrix multiplication.
4. Measure the execution time of matrix multiplication using different numbers of threads (1 to 10).
5. Tabulate the results and plot a graph to visualize the performance gain with increasing number of threads.



## Result Graph

The graph below illustrates the relationship between the number of threads and the time taken for matrix multiplication.
![image](https://github.com/tanejanikhil3638/Multithreading/assets/98747035/fc7df82b-7c9d-4d8e-8a5d-318b0e34f6f9)


### Observations

- As the number of threads increases, the execution time initially decreases, indicating a performance gain.
- After reaching a certain point (in this case, around 4 threads), the execution time starts to increase. This can be attributed to the overhead associated with creating and managing a large number of threads, which can outweigh the benefits of parallelization.

## Conclusion

The experiment demonstrates that while using multiple threads can significantly improve the performance of matrix multiplication tasks, there is an optimal number of threads beyond which the performance may degrade due to increased overhead. Therefore, it is essential to carefully choose the number of threads based on the nature of the task and the underlying hardware architecture to achieve optimal performance.

