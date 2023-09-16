# Matrix Multiplication with OpenMP

## Code Explanation

This program performs the following steps:

1. **Command-Line Arguments**: It accepts two command-line arguments - `matrix_size` and `num_threads`. These arguments determine the size of the matrices and the number of threads to use for parallel execution.

2. **Memory Allocation**: Dynamic memory allocation is used to create three matrices `A`, `B`, and `C`. These matrices will hold the input matrices and the result of matrix multiplication.

3. **Initialization**: Matrices `A` and `B` are initialized with the value 2, while matrix `C` is initialized with zeros.

4. **Parallel Matrix Multiplication**: The core matrix multiplication operation is parallelized using OpenMP. The `#pragma omp parallel for` directive splits the work among multiple threads. Each thread calculates a portion of the result matrix `C`.

5. **Timing**: The program measures the elapsed time for the matrix multiplication using the `gettimeofday` function. This provides a measure of the program's performance.

6. **Memory Deallocation**: After the matrix multiplication is complete, memory is deallocated to prevent memory leaks.

## How to Compile and Run

To compile the program, open a terminal and navigate to the directory containing the code. Use the following command:

```bash
gcc -o matrix_multiplication matrix_multiplication.c -fopenmp
```

This command compiles the code with OpenMP support and generates an executable named matrix_multiplication.

To run the program, use the following command:
```bash
./matrix_multiplication <matrix_size> <num_threads>
```

For finding nth power of the matrix:
```bash
./matrix_multiplication <matrix_size> <exponent> <num_threads>
```

Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2
```

For nth power:
Replace <matrix_size> with the desired size of the matrices and <num_threads> with the number of threads you want to use for parallel execution.
```bash
./matrix_multiplication 512 2 4
```

This will perform matrix multiplication with matrices of size 1000x1000 using 4 threads.

## Output

The program will display the size of the matrices, the number of threads used, and the elapsed time for matrix multiplication.

Graph for the same are as below:

1. **OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/e4ec8ef1-f2cc-4db8-a749-fefc4e32f552)

     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/9e332601-97de-40b4-9fac-c5c397f1b439)

     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/828b1e02-1c37-485f-9878-2bcf9fb5ed88)


   
2. **Nth Power of Matrix with OMM ( Threads vs Elapsed Time )** :

     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/bd6e0375-47df-468b-ade6-6acfeb7fb0fa)

     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/b0414fe9-178d-4707-b558-76aa2dbbbec6)
 
     ![image](https://github.com/batul02/hpc_assign1/assets/50478830/5c42956f-2256-4a9d-97e8-742b04be1f06)


## Conclusion

This C program demonstrates how to use OpenMP to parallelize matrix multiplication, improving the performance of the computation. You can adjust the matrix size and the number of threads to observe the impact on execution time.




# Block Matrix Multiplication

```markdown
# Block Matrix Multiplication

Compile the program using a C compiler. For example:

gcc -o block_matrix_mult block_matrix_mult.c -fopenmp
```

Here, block_matrix_mult is the name of the executable.

To run the program, use the following command-line format:
```bash
./block_matrix_mult <matrix_size> <num_threads> <block_size>
```

For nth power of a matrix using BMM:
```bash
./block_matrix_mult <matrix_size> <exponent> <num_threads> <block_size>
```

<matrix_size>: The size of the square matrices (e.g., 100 for a 100x100 matrix).
<block_size>: The size of the square blocks (e.g., 10 for a 10x10 block).
For example, to multiply two 100x100 matrices using 10x10 blocks:

```bash
./block_matrix_mult 1024 6 4
```

For nth power:
```bash
./block_matrix_mult 1024 2 6 4
```

## Output
The program will display the size of the matrices, the block size, and the result of the multiplication.

1. **BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/6885d6b1-08a1-4f9b-923e-3db4d81accdf)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/2c00f04d-f66b-4787-99f7-059dc9ba5373)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/baed4569-d574-451a-a8c0-672c41a389a9)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/a1398327-af3b-4271-ad19-79ed9f33f2bc)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/a0964aff-e62f-49e9-abff-85ec349688a9)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/5f262ca2-2ad4-4dae-88e4-17570aba8cd5)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/174a423d-259b-4151-a20c-303d8cf775c1)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/df799de0-4fd2-47bd-b893-738f9e5282ff)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/9b30ff16-fc4a-4137-ade6-d87ebda448b1)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/b1d6c8ca-8efd-47bd-a0bd-cd0d3ec49a79)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/2c810fd7-af6b-4b42-bbf1-cc1c8bc82f55)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/085795fa-3f94-4180-8acd-ec0b2968b23b)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/f119837f-3b3e-49ec-8eac-44bdeb31d64a)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/778f1f9b-5853-4763-8594-999f39e8a5cb)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/b310fdbc-a15c-4098-b1eb-2270475f82b9)

   
3. **Nth Power of Matrix with BMM ( Threads vs Elapsed Time )** :

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/af554d42-d431-49ae-b388-6d3fc2ad5da9)

   ![image](https://github.com/batul02/hpc_assign1/assets/50478830/ae669fe3-0166-44bd-942c-5e4ae401ace8)


## Memory Management
The program dynamically allocates memory for matrices A, B, and C, as well as for the block buffers. It frees the allocated memory after the multiplication is complete to prevent memory leaks.
