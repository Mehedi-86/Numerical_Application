<h1>📌 Numerical Methods in C++</h1>

<p>This project implements various <b>Numerical Methods</b> using C++. The implemented methods include:</p>
<ul>
  <li><b>Jacobi Iterative Method</b></li>
  <li><b>Gauss-Seidel Iterative Method</b></li>
  <li><b>Gauss Elimination Method</b></li>
  <li><b>Gauss-Jordan Elimination</b></li>
  <li><b>LU Factorization</b></li>
  <li><b>Root Finding Methods</b> (Bi-section, False Position, Secant, Newton-Raphson)</li>
  <li><b>Runge-Kutta Method</b> (Solving Differential Equations)</li>
  <li><b>Matrix Inversion</b></li>
</ul>

<hr>

<h2>📂 File Structure</h2>
<pre>
📁 Numerical_Methods/
│── 📄 main.cpp        # Main entry point
│── 📄 2107100.hpp     # Header file 1
│── 📄 2107086.hpp     # Header file 2
│── 📄 2107102.hpp     # Header file 3
│── 📄 README.md       # Documentation
</pre>

<hr>

<h2>🚀 How to Run the Program</h2>

<h3>🔹 Prerequisites</h3>
<ul>
  <li>A C++ compiler (g++ recommended)</li>
  <li>Basic understanding of numerical methods</li>
</ul>

<h3>🔹 Compilation Steps</h3>
<ol>
  <li>Open a terminal and navigate to the project directory: <br>
      <code>cd path/to/Numerical_Methods</code></li>
  <li>Compile the program: <br>
      <code>g++ -o numerical_methods main.cpp -std=c++11</code></li>
  <li>Run the compiled program: <br>
      <code>./numerical_methods</code></li>
</ol>

<hr>

<h2 id="jacobi">🔹 Jacobi Iterative Method</h2>

The **Jacobi Method** is an **iterative algorithm** used to solve systems of **linear equations**. It starts with an initial guess and iteratively updates the solution using:

\[
x_i^{(k+1)} = \frac{b_i - \sum_{j \neq i} a_{ij} x_j^{(k)}}{a_{ii}}
\]

✅ **Advantages**:
- Works well for **diagonally dominant matrices**.
- **Parallelizable**, as updates don’t depend on previous iterations.

❌ **Disadvantages**:
- **Slow convergence** for large matrices.
- Might **not converge** if the matrix is not diagonally dominant.

---

<h2 id="gauss-seidel">🔹 Gauss-Seidel Iterative Method</h2>

An **improvement** over the Jacobi method. It updates each variable **immediately**, using the latest computed values:

\[
x_i^{(k+1)} = \frac{b_i - \sum_{j < i} a_{ij} x_j^{(k+1)} - \sum_{j > i} a_{ij} x_j^{(k)}}{a_{ii}}
\]

✅ **Advantages**:
- **Faster convergence** than Jacobi.
- Uses **previously updated values**, improving accuracy.

❌ **Disadvantages**:
- **Sequential**, so harder to parallelize.
- Might not converge for **non-diagonally dominant** matrices.

---

<h2 id="gauss-elimination">🔹 Gauss Elimination Method</h2>

A **direct method** that systematically eliminates variables to solve linear equations using row operations.

### Steps:
1️⃣ Convert the system into **Upper Triangular Form**.  
2️⃣ Perform **back-substitution** to get the solution.

✅ **Advantages**:
- Efficient for **small to medium-sized** systems.
- Works for **any square system**.

❌ **Disadvantages**:
- Computationally expensive **\(O(n^3)\)** for large matrices.
- Prone to **numerical instability**.

---

<h2 id="gauss-jordan">🔹 Gauss-Jordan Elimination</h2>

An **extension of Gauss Elimination**, where the system is transformed into **Reduced Row Echelon Form (RREF)**.

### Steps:
1️⃣ Convert the matrix into an **identity matrix**.  
2️⃣ The remaining matrix contains the solution.

✅ **Advantages**:
- Finds **exact solution** directly.
- Can be used for **matrix inversion**.

❌ **Disadvantages**:
- **More computationally expensive** than Gauss Elimination.
- **Not practical** for very large systems.

---

<h2 id="lu-factorization">🔹 LU Factorization</h2>

Decomposes a matrix **A** into **lower (L) and upper (U) triangular matrices**, where:

\[
A = LU
\]

### Steps:
1️⃣ Solve **Ly = b** using forward substitution.  
2️⃣ Solve **Ux = y** using back substitution.

✅ **Advantages**:
- Efficient for **multiple linear systems** with the same **A** but different **b**.
- Reduces computational complexity.

❌ **Disadvantages**:
- Requires **matrix decomposition**, which adds overhead.
- Not always stable for **ill-conditioned matrices**.

---

<h2 id="root-finding">🔹 Root Finding Methods</h2>

Finding the **roots of a function \( f(x) = 0 \)** is essential in numerical methods.

### 1️⃣ Bi-Section Method
- **Bracket-based method**: Requires two points where **\( f(a) \cdot f(b) < 0 \)**.
- Repeatedly **halves the interval** until the root is found.

✅ **Always converges**, but **slow**.

### 2️⃣ False Position (Regula Falsi)
- Uses **linear interpolation** to approximate the root.

✅ **Faster than Bi-section**, but may converge **slowly for some functions**.

### 3️⃣ Secant Method
- Uses **two previous points** to approximate the derivative.

✅ **No need for derivative calculations**.

### 4️⃣ Newton-Raphson Method
- Uses the **first derivative** to iteratively refine the root:

\[
x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}
\]

✅ **Fast convergence** for well-behaved functions.

❌ **Fails for non-differentiable functions**.

---

<h2 id="runge-kutta">🔹 Runge-Kutta Method (Solving Differential Equations)</h2>

A powerful method for solving **Ordinary Differential Equations (ODEs)** of the form:

\[
\frac{dy}{dx} = f(x, y)
\]

**4th Order Runge-Kutta** uses:

\[
y_{n+1} = y_n + \frac{h}{6} (k_1 + 2k_2 + 2k_3 + k_4)
\]

where:

\[
k_1 = h f(x_n, y_n)
\]
\[
k_2 = h f(x_n + h/2, y_n + k_1/2)
\]
\[
k_3 = h f(x_n + h/2, y_n + k_2/2)
\]
\[
k_4 = h f(x_n + h, y_n + k_3)
\]

✅ **More accurate** than **Euler’s Method**.  
✅ Suitable for **non-linear** ODEs.  

❌ **Computationally expensive**.

---

<h2 id="matrix-inversion">🔹 Matrix Inversion</h2>

Used to find the **inverse of a matrix** \( A^{-1} \), such that:

\[
A A^{-1} = I
\]

**Using Gauss-Jordan Method**:
1️⃣ Append **identity matrix** to \( A \).  
2️⃣ Perform **row operations** to convert \( A \) into **identity matrix**.  
3️⃣ The result is \( A^{-1} \).

✅ **Used for solving simultaneous equations**.

❌ **Computationally expensive for large matrices**.

---

## 📜 Summary

These **numerical methods** are widely used in **engineering and science** for solving complex equations efficiently. 

If you have any **suggestions or contributions**, feel free to **fork this project and create a pull request! 🚀**

---

## 📝 References:
📌 Numerical Methods in Engineering  
📌 Applied Mathematics Textbooks  

---
<h2>📜 License</h2>
<p>This project is open-source. Feel free to modify, share, and contribute!</p>

<h2>🚀 Happy Coding! 😊</h2>
