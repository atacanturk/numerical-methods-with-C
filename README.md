---
# Numerical Analysis with C 

This project is a console application written in C, containing fundamental algorithms learned in a numerical analysis course. It provides an interactive menu for the user to explore and apply various numerical methods.

---

## Contents

This project includes the following numerical analysis methods:

1.  **Bisection Method:** Used to find the roots of non-linear equations.
2.  **Regula-Falsi (False Position) Method:** Similar to the Bisection method for finding roots of non-linear equations, but can converge faster.
3.  **Newton-Raphson Method:** An iterative method used to quickly find the roots of a function.
4.  **Inverse of an NxN Matrix:** Calculates the inverse of a square matrix using Gauss-Jordan elimination.
5.  **Gauss Elimination (Gauss-Jordan):** Used to solve systems of linear equations.
6.  **Gauss-Seidel Method:** An iterative method used to solve systems of linear equations.
7.  **Numerical Differentiation (Central, Forward, and Backward Differences):** Numerically calculates the derivative of a function at a specific point.
8.  **Simpson's 1/3 Rule:** A method used to numerically calculate definite integrals.
9.  **Trapezoidal Rule:** Another method used to numerically calculate definite integrals.
10. **Gregory-Newton Interpolation:** Used to estimate the function value at an unknown point given a set of known points.

---

## How to Compile and Run

To compile and run this project, you will need a C compiler (e.g., GCC).

1.  **Save the Source Code:**
    Save the C code provided above into a file named `main.c` (if you use project.c directly, replace `main.c`  to `project.c` given below).

2.  **Compile:**
    Compile the code using the following command in your terminal or command prompt:
    ```bash
    gcc main.c -o numerical_analysis -lm
    ```
    * `gcc main.c`: Compiles the `main.c` file.
    * `-o numerical_analysis`: Specifies the name of the compiled executable as `numerical_analysis` (or `numerical_analysis.exe` on Windows).
    * `-lm`: Links the math library (`m`) for mathematical functions like `pow()` from `math.h`.

3.  **Run:**
    Once compiled successfully, you can run the application with the following command:
    * **Linux/macOS:**
        ```bash
        ./numerical_analysis
        ```
    * **Windows:**
        ```bash
        numerical_analysis.exe
        ```

---

## Usage

When the application starts, a menu will be displayed. Enter the corresponding number for the desired numerical analysis method and press Enter. Each function will prompt you for its specific inputs (e.g., function coefficients, interval, initial values).

---

## Functions

* **`Fx(float x, int derece, float katsayilar[])`**: Calculates the value of a polynomial at point `x` based on the given degree and coefficients.
* **`F1x(float x, int derece, float katsayilar[])`**: Calculates the derivative of a polynomial at point `x` based on the given degree and coefficients.
* Other functions (Bisection, Regula\_Falsi, etc.) implement the numerical analysis methods listed above.

---

## Notes

* The program uses `system("cls")` and `system("pause")` commands, which are primarily designed for Windows operating systems. These commands might not behave as expected or could produce errors on Linux/macOS systems. Consider replacing them with platform-independent clearing or pausing mechanisms for broader compatibility.
* For matrix operations (`matris_Tersi`, `Gauss_Jordan`), there are certain constraints, such as the diagonal elements of the matrix not being zero. The program checks for this condition and provides an error message if violated.
* Parameters like epsilon (error tolerance) and the number of iterations are requested from the user.
* Gregory-Newton Interpolation requires a constant difference (`h`) between the `x` values.
