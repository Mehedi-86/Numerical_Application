<h1>📌 Numerical Methods in C++</h1>

<p>This project implements various <b>Numerical Methods</b> such as:</p>
<ul>
  <li><b>Jacobi Method</b> - Solving linear equations iteratively.</li>
  <li><b>Gauss-Seidel Method</b> - Improved iterative method for solving equations.</li>
  <li><b>Runge-Kutta Method</b> - Numerical method for solving ODEs.</li>
  <li><b>Matrix Inversion</b> - Gauss-Jordan elimination.</li>
  <li><b>Checking Infinite or No Solutions</b> - Determines system consistency.</li>
</ul>

<hr>

<h2>📂 File Structure</h2>
<pre>
📁 Numerical_Methods/
│── 📄 main.cpp      # Main program file
│── 📄 jacobi.cpp    # Implements Jacobi method
│── 📄 gauss.cpp     # Implements Gauss-Seidel method
│── 📄 runge.cpp     # Implements Runge-Kutta method
│── 📄 matrix.cpp    # Implements matrix inversion
│── 📄 utils.cpp     # Helper functions
│── 📄 README.md     # Documentation
</pre>

<hr>

<h2>🚀 How to Run the Program</h2>
<h3>🔹 Prerequisites</h3>
<ul>
  <li>Install a <b>C++ compiler</b> (e.g., g++).</li>
  <li>Basic knowledge of numerical methods.</li>
</ul>

<h3>🔹 Compilation Steps</h3>
<ol>
  <li>Open <b>Terminal/Command Prompt</b>.</li>
  <li>Navigate to the project directory: <br> <code>cd path/to/Numerical_Methods</code></li>
  <li>Compile the program: <br> <code>g++ -o numerical_methods main.cpp jacobi.cpp gauss.cpp runge.cpp matrix.cpp -std=c++11</code></li>
  <li>Run the compiled program: <br> <code>./numerical_methods</code></li>
</ol>

<hr>

<h2>🛠 Implementation Details</h2>
<h3>1️⃣ Jacobi Method</h3>
<p><b>Purpose:</b> Solves a system of linear equations iteratively.</p>
<p><b>Function Signature:</b></p>
<pre>
void jacobiMethod(const vector<vector<double>>& A, const vector<double>& b);
</pre>
<p><b>Algorithm:</b></p>
<ol>
  <li>Assume an initial guess for the solution.</li>
  <li>Iteratively update the values using:
  <pre>x_i^(k+1) = (b_i - Σ(A_ij * x_j^(k))) / A_ii</pre>
  </li>
  <li>Stop when the difference between successive iterations is below a threshold.</li>
</ol>

<hr>

<h2>🔍 Debugging and Common Issues</h2>
<table border="1">
  <tr>
    <th>Problem</th>
    <th>Solution</th>
  </tr>
  <tr>
    <td>🚨 Incorrect results</td>
    <td>Check input matrix values and precision.</td>
  </tr>
  <tr>
    <td>🚨 Non-converging Jacobi/Gauss-Seidel</td>
    <td>Ensure the matrix is <b>diagonally dominant</b>.</td>
  </tr>
  <tr>
    <td>🚨 Division by zero</td>
    <td>Ensure the diagonal elements are non-zero.</td>
  </tr>
</table>

<hr>

<h2>📜 License</h2>
<p>This project is <b>open-source</b>. Feel free to modify, share, and contribute!</p>

<h2>🚀 Happy Coding! 😊</h2>
