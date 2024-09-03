# Openmp-Matrix-Multiplication
Matrix multiplication is a fundamental operation in many scientific and engineering applications. 
In this project, I have implemented a matrix multiplication algorithm using OpenMP to parallelize the computation across multiple threads. 
The focus is on demonstrating how parallel programming can significantly improve performance in HPC environments.

## Project Overview
This project demonstrates the use of OpenMP for parallel matrix multiplication in a shared memory environment. The implementation showcases the performance improvement achieved by parallelizing the computation across multiple threads.

## Prerequisites
- GCC compiler with OpenMP support
- Linux environment (recommended)
- Basic understanding of C programming and OpenMP

## Matrix Multiplication Algorithm
The matrix multiplication algorithm implemented here performs the multiplication of two matrices using parallel processing with OpenMP. 
The algorithm follows these steps:

A] Initialize Matrices :
       a) Matrix A and Matrix B are initialized with random values.
       b) Matrix C will store the result of the multiplication.

B] Matrix Multiplication:
       a) Use nested loops to compute the product of Matrix A and Matrix B.
       b) For each element in Matrix C, compute the dot product of the corresponding row in Matrix A and column in Matrix B.

C] Parallel Processing:
        a) Use OpenMP to parallelize the computation.
        b) The #pragma omp parallel for directive distributes the work of computing matrix elements across multiple threads.

D] Measure Performance:
        a) Record the start and end time of the multiplication process using omp_get_wtime().
        b) Calculate the time taken for the multiplication and output it.

## Algorithm Steps
   1) Input:
          Matrix size 𝑛 (from user input).

   2) Initialization:
        Generate random values for matrices A and 𝐵.

   3) Compute Result Matrix:
        For each element 𝐶[𝑖][𝑗]
        Initialize C[i][j] to zero.
        For each element 𝑘 :
          Update C[i][j] as C[i][j]+=A[i][k]×B[k][j].
    
    4) Parallel Computation:
        Apply OpenMP parallelism to the outer loop of the matrix multiplication.

    5) Output:
        Print the time taken for the matrix multiplication process.
        

## Setup Instructions

1)  **Clone the Repository:**
       git clone https://github.com/ShrutiPravinBokare/openmp-matrix-multiplication.git
       cd openmp-matrix-multiplication

2) **Install Dependencies:**
        Ensure you have the necessary tools installed. For this project, you need gcc (GNU Compiler Collection) with OpenMP support.
        i) On Linux, you can install it using:
               sudo apt-get install build-essential
        ii) On macOS, you might use Homebrew:
               brew install gcc

3) **Create a Makefile:**
       If not already present, create a Makefile in the root of the repository.

4) **Compile the Code:**
        Run the following command to compile the code using the Makefile:
           make
    
5) **Run the Program:**
       Execute the program with a specified matrix size. For example:
           ./matrix_multiplication 500
       Replace 500 with the desired size of the matrix.
   
 6) **Clean Up:**
        To remove the compiled executable and any temporary files, run:
           make clean 


