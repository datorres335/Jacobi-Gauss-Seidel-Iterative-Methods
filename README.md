# Solving Linear Systems Using Jacobi and Gauss-Seidel Methods

## Overview
This program solves a system of linear equations (up to **n = 10**) using **Jacobi Iterative Method** and **Gauss-Seidel Method**. It ensures that the input matrix is **strictly diagonally dominant** to guarantee convergence.

## Implementation Details
This program is implemented in **Java** using a single main file:
1. **Main.java** - Handles user input, reads the matrix from a file or manual input, and applies the chosen numerical method.

## Input Format
The user chooses how to input the system of equations:
1. **Manually enter the equations**
2. **Provide a file path** containing the augmented coefficient matrix

### Example Input File
For a system of 3 equations:
```
5 -1 0 7
-1 3 -1 4
0 -1 2 5
```
This represents the system:
- **5x - y = 7**
- **-x + 3y - z = 4**
- **-y + 2z = 5**

## Program Output
1. **Checks if the matrix is diagonally dominant**
2. **Asks the user for a desired stopping error**
3. **Iterates using Jacobi or Gauss-Seidel method**
4. **Prints the solution at each iteration in the format:**
   ```
   [2.0870 3.4348 4.2174]T
   ```
5. **Stops when the L2 norm of the difference between successive iterations is less than the given error or reaches 50 iterations**

## Example Run
### **Option 1: Manually Entering the Matrix**
Upon running the program, the user is prompted to **either create the system manually or load from a file.**

```
Choose input method:
1. Enter equations manually
2. Load from file
```
If the user selects **Option 1**, they enter the matrix coefficients and b values row by row:

```
Enter number of equations: 3
Enter row 1: 5 -1 0 7
Enter row 2: -1 3 -1 4
Enter row 3: 0 -1 2 5
```
The program then checks **diagonal dominance** and proceeds to solve using the selected iterative method.

### **Option 2: Loading a File**
If the user selects **Option 2**, they are prompted to enter the file path:

```
Enter the path to your matrix file: matrix.txt
```
The program reads the file and proceeds with **Jacobi or Gauss-Seidel iteration**, displaying the steps and final solution.

## Java Code Structure
### **Main.java**
- Prompts the user for input method (manual entry or file-based input).
- Reads matrix from user input or file.
- Checks if the matrix is **diagonally dominant**.
- Asks for the **desired error tolerance** and **initial guess**.
- Solves using **Jacobi or Gauss-Seidel method**.
- Displays **iteration steps and convergence results**.

## Notes
- The program ensures numerical stability by checking **diagonal dominance** before attempting iteration.
- The **L2 norm** is calculated after each iteration to determine stopping criteria.
- The final output presents the computed values of **x, y, z, ...** for the given system.

## Example Output
```
Iteration 1:
[2.0000 3.0000 4.0000]T

Iteration 2:
[2.0870 3.4348 4.2174]T

Solution converged!
```
If the error tolerance isn't reached in **50 iterations**, the program prints:
```
Sorry the desired error wasn't achieved in 50 iterations. Here is the value at the 50th iteration:
[2.0870 3.4348 4.2174]T
```

## Usage Instructions
1. **Compile the program**:
   ```bash
   javac Main.java
   ```
2. **Run the program**:
   ```bash
   java Main
   ```
3. **Follow the prompts** to enter data manually or provide a file.
4. **Select the desired method** (Jacobi or Gauss-Seidel).
5. **View the step-by-step solution and final computed results.**

## License
This project is open-source and available for modification and use.

---
Let me know if you need any modifications! 🚀

