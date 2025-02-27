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

<h2>🛠 Implementation Details</h2>

<h3>1️⃣ Jacobi Method</h3>
<p><b>Purpose:</b> Solves a system of linear equations iteratively.</p>
<pre>
void jacobiMethod(const vector<vector<double>>& A, const vector<double>& b);
</pre>

<h3>2️⃣ Gauss-Seidel Method</h3>
<p><b>Purpose:</b> An improved iterative method for solving equations.</p>
<pre>
void gaussSeidelMethod(const vector<vector<double>>& A, const vector<double>& b);
</pre>

<h3>3️⃣ Runge-Kutta Method</h3>
<p><b>Purpose:</b> Solves differential equations using the Runge-Kutta technique.</p>
<pre>
void rungeKuttaMethod();
</pre>

<h3>4️⃣ Matrix Inversion</h3>
<p><b>Purpose:</b> Finds the inverse of a matrix using Gauss-Jordan elimination.</p>
<pre>
void matrixInversion();
</pre>

<hr>

<h2>📜 License</h2>
<p>This project is open-source. Feel free to modify, share, and contribute!</p>

<h2>🚀 Happy Coding! 😊</h2>
