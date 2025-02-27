<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - Numerical Methods in C++</title>
</head>
<body>

    <h1>📌 Numerical Methods in C++</h1>
    <p>
        This project implements various <strong>Numerical Methods</strong> such as 
        <strong>Jacobi Method, Gauss-Seidel Method, Runge-Kutta Method, and Matrix Inversion</strong> 
        using C++. It is designed for solving linear equations, ordinary differential equations, 
        and checking system consistency.
    </p>

    <h2>📜 Features</h2>
    <ul>
        <li>✅ <strong>Jacobi Method</strong> - Iterative method for solving linear equations.</li>
        <li>✅ <strong>Gauss-Seidel Method</strong> - Improved iterative method for solving equations.</li>
        <li>✅ <strong>Runge-Kutta Method</strong> - Numerical method for solving ODEs.</li>
        <li>✅ <strong>Matrix Inversion</strong> - Gauss-Jordan elimination method.</li>
        <li>✅ <strong>Checking Infinite or No Solutions</strong> - Determines system consistency.</li>
    </ul>

    <h2>📂 File Structure</h2>
    <pre>
    📁 Numerical_Methods/
    │── 📄 main.cpp      # Main program file
    │── 📄 jacobi.cpp    # Implements Jacobi method
    │── 📄 gauss.cpp     # Implements Gauss-Seidel method
    │── 📄 runge.cpp     # Implements Runge-Kutta method
    │── 📄 matrix.cpp    # Implements matrix inversion
    │── 📄 utils.cpp     # Helper functions
    │── 📄 README.html   # Documentation
    </pre>

    <h2>🚀 How to Run the Program</h2>
    <h3>🔹 Prerequisites</h3>
    <ul>
        <li>Install a <strong>C++ compiler</strong> (g++ recommended).</li>
        <li>Ensure you have <strong>basic knowledge of numerical methods</strong>.</li>
    </ul>

    <h3>🔹 Compilation Steps</h3>
    <ol>
        <li>Open <strong>Terminal/Command Prompt</strong>.</li>
        <li>Navigate to the project directory:
            <pre><code>cd path/to/Numerical_Methods</code></pre>
        </li>
        <li>Compile the program:
            <pre><code>g++ -o numerical_methods main.cpp jacobi.cpp gauss.cpp runge.cpp matrix.cpp -std=c++11</code></pre>
        </li>
        <li>Run the compiled program:
            <pre><code>./numerical_methods</code></pre>
        </li>
    </ol>

    <h2>🛠 Implementation Details</h2>

    <h3>1️⃣ Jacobi Method</h3>
    <p><strong>Purpose:</strong> Solves a system of linear equations iteratively.</p>
    <p><strong>Function Signature:</strong></p>
    <pre><code>void jacobiMethod(const vector&lt;vector&lt;double&gt;&gt;& A, const vector&lt;double&gt;& b);</code></pre>
    <p><strong>Algorithm:</strong></p>
    <ol>
        <li>Assume an initial guess for the solution.</li>
        <li>Iteratively update the values using:<br>
            <code>x_i^(k+1) = (b_i - Σ(A_ij * x_j^(k))) / A_ii</code></li>
        <li>Stop when the difference between successive iterations is below a threshold.</li>
    </ol>

    <h3>2️⃣ Gauss-Seidel Method</h3>
    <p><strong>Purpose:</strong> Improved iterative method for solving linear systems.</p>
    <p><strong>Function Signature:</strong></p>
    <pre><code>void gaussSeidelMethod(const vector&lt;vector&lt;double&gt;&gt;& A, const vector&lt;double&gt;& b);</code></pre>
    <p><strong>Algorithm:</strong></p>
    <ul>
        <li>Similar to Jacobi, but updates variables immediately after computation.</li>
    </ul>

    <h3>3️⃣ Runge-Kutta Method</h3>
    <p><strong>Purpose:</strong> Solves Ordinary Differential Equations (ODEs).</p>
    <p><strong>Function Signature:</strong></p>
    <pre><code>void rungeKuttaMethod();</code></pre>
    <p><strong>Algorithm:</strong></p>
    <ol>
        <li>Compute intermediate values:
            <pre><code>
            k1 = h * f(x, y);
            k2 = h * f(x + h/2, y + k1/2);
            k3 = h * f(x + h/2, y + k2/2);
            k4 = h * f(x + h, y + k3);
            </code></pre>
        </li>
        <li>Update the value using:
            <pre><code>y_next = y + (1/6) * (k1 + 2*k2 + 2*k3 + k4);</code></pre>
        </li>
    </ol>

    <h3>4️⃣ Matrix Inversion</h3>
    <p><strong>Purpose:</strong> Finds the inverse of a square matrix using Gauss-Jordan elimination.</p>
    <p><strong>Function Signature:</strong></p>
    <pre><code>void matrixInversion();</code></pre>
    <p><strong>Algorithm:</strong></p>
    <ol>
        <li>Form an augmented matrix <code>[A | I]</code>.</li>
        <li>Apply row operations to convert <code>[A]</code> into an identity matrix.</li>
        <li>The result on the right-hand side <code>[I]</code> becomes <code>A^-1</code>.</li>
    </ol>

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
            <td>Ensure the matrix is <strong>diagonally dominant</strong>.</td>
        </tr>
        <tr>
            <td>🚨 Division by zero</td>
            <td>Ensure the diagonal elements are non-zero.</td>
        </tr>
    </table>

    <h2>📜 License</h2>
    <p>This project is <strong>open-source</strong>. Feel free to modify, share, and contribute!</p>

    <h2>📌 Conclusion</h2>
    <p>
        This project demonstrates various <strong>numerical methods in C++</strong>, including 
        <strong>iterative solvers for linear systems, differential equations, and matrix operations</strong>. 
        It serves as a useful tool for students and engineers working with numerical computations.
    </p>

    <h2>🚀 Happy Coding! 😊</h2>

</body>
</html>
