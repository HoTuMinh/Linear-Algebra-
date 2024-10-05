## LINEAR EQUATION

- **a linear equation in $2$ variables** has the form $a_1x+a_2y=b$
- $a_1,a_2,b$ are **constants**
- a **linear equation in $n$ variables** has the form $a_1x_1+a_2x_2+...+a_nx_n=b$
- $a_1,a_2,...,a_n$ are real numbers, called **coefficients**
- the **constant term** $b$ is a real number
- $a_1$ is the **leading coefficient**
- $x_1$ is the **leading variable**
- *linear equations have no products, roots of variables, and no variables involved trigonometric, exponential, or logarithmic functions*
- all the variables appear to only the first power <br/>

## THE SOLUTION OF A LINEAR EQUATION 

- the **solution of a linear equation in $n$ variables** is a sequence of $n$ real numbers $s_1,s_2,...,s_n$ arranged so the equation is satisfied when the values $x_1=s_1,x_2=s_2,...,x_n=s_n$ are substituted into the equation
- the set of all solutions of a linear equation is called its **solution set**
    - the equation is **solved** when this set is found
- instead of a sequence of $n$ real numbers, a solution can be represented using parameters, which is caled **parametric representation** <br/>
    - _example: solve the linear equation_ $x_1+2x_2=4$ 
    > to find the solution set of an equation involving 2 variables, solve for one of the variables in terms of the other variable. If you solve for $x_1$ in terms of $x_2$, you obtain $x_1 = 4-x_2$ <br/>
    - here, $x_2$ is **free** (it can take on any real value)
    - the variable $x_1$ is not free because its value depends on the value assigned to $x_2$. To represent the infinite number of solutions of this equations, we introduce a third variable %t% called a **paramater**. By letting $x_2=t$, you represent the solution set as: <br/>
      $x_1=4-2t, x_2=t, t$ is any real number

## SYSTEMS OF LINEAR EQUATIONS
- a **system of $m$ linear equations in $n$ variables** is a set of $m$ equations, each of which is linear in the same $n$ variables
- a **solution of a system of linear equations** is a sequence of numbers that is the solution of each of the linear equations in the system

## SOLVING A SYSTEM OF LINEAR EQUATIONS 

- 2 systems of linear equations are called **equivalent** if they have the same solution set
- **operations that lead to equivalent systems of equations**
1. interchange 2 equations
2. multiply an equation by a non zero constant
3. add a multiple of an equation to another equation 
- to solve a system of linear equations, we perform these operations on the system to turn it into a form called **row echelon form**
``` math
\begin{matrix} x-2y+3z&=&9 \\ y+3z&=&5 \\ z&=&2 \end{matrix}
```
- after that, you can use **back-substitution** to solve the system
```math
\begin{matrix}
x-2(-2) &=& 5 \\
x&=&1
\end{matrix}
```
- the process above is called **Gaussian elimination**: rewriting a system of linear equations in row-echolon form using one of the 3 basics operations (product a chain of equivalent systems)
- a few tips
    - *work from the upper left corner of the system, saving the first variable, then work your way down from there*
    - *since the process comprises of many calculations, you should check the solution by substituting it into each equation in the original system to check the equation holds*
- types of system of linear equations
  - **inconsistent system**
    - has a false statement (example: $2=0$)
    - the planes do not have a point in common 
  - **systems withan infinite number of solutions**
    - the solution can be written using a parametric representation
   
## MATRIX 
- *[matrix syntax](https://www.math-linux.com/latex/faq/latex-faq/article/how-to-write-matrices-in-latex-matrix-pmatrix-bmatrix-vmatrix-vmatrix)*
- a $m \times n$ matrix is a rectangular array ($m, n$ are positive integers)
```math
\begin{bmatrix}
    a_{11} & a_{12} & a_{13} & \dots  & a_{1n} \\
    a_{21} & a_{22} & a_{23} & \dots  & a_{2n} \\
    \vdots & \vdots & \vdots & \ddots & \vdots \\
    a_{m1} & a_{m2} & a_{m3} & \dots  & a_{mn}
\end{bmatrix}
```
- syntax of a matrix
  - $m$ rows (horizontal lines)
  - $n$ columns (vertical lines)
  - **entry** $a_{i,j}$ is a number
  - $i$ is called the **row subscript**
  - $j$ is called the **column subscript**
  - if $m=n$, the matrix is called a **square matrix of order** $n$
  - for a square matrix, the entries $a_{11}, a_{22},...,a_{nn}$ form the **main diagonal**
- we can use matrices to represent systems of linear equations
- *system of linear equations*
```math
\begin{matrix}
&x&-&4y&+&3z&&=&5 \\
&-x&+&3y&-&z&&=&-3 \\
&2x& &&- &4z& &=& 6
\end{matrix}
```
  - *augmented matrix*
```math
\begin{equation*}
\begin{bmatrix}
1 & -4 & 3 & 5\\
-1 & 3 & -1 & -3\\
2 & 0 & -4 & 6
\end{bmatrix}
\end{equation*}
```
  - *coefficient matrix*
  ```math
\begin{equation*}
\begin{bmatrix}
1 & -4 & 3 \\
-1 & 3 & -1 \\
2 & 0 & -4 
\end{bmatrix}
\end{equation*}
```
- **elementary row operations** are operations that can be performed on a system of linear equations to produce
1. interchange rows
2. multiply a row by a real number
3. add a multiplication of one row to another row
- 2 matrices are said to be **row-equivalent** if one can be obtained from the other by performing a finite sequence of elementary row operations
- a matrix in **row-echelon form** has the following properties
1. all rows consisting entirely of zeros occur at the bottom of the matrix
2. for each row that does not consist entirely of zeros, the first nonzero entry is 1, called **leading 1**
3. for 2 successive (non zero) rows, the leading 1 in the higher row is farther to the left than the leading 1 in the lower row
- **reduced row-echelon form**: every column that has a leading 1 has zeros in every position above and below its leading 1
```math
\begin{bmatrix}
1 & 0 & 0 & a \\
0 & 1 & 0 & b \\
0 & 0 & 1 & c
\end{bmatrix}
```
- steps to solve a system of linear equations using matrix notation and **Gaussian elimination with back-substitution**
1. write the augmented matrix of the system of linear equations
2. use elementary row operations to rewrite the augmented matrix in row-echelon form
3. write the system of linear equations corresponding to the matrix in row-echelon form, and use back substitution to find the solution
- the **Gauss-Jordan elimination** adds another final step: continues the reduction process until a reduced-row-echelon form is obtained
- **Homogenous system of linear equations** is a type of system in which each of the constant term is $0$
  - the system must have at least one solution, called the **trivial** or **obvious** solution
  - every homogenous system of linear equations is consistent
  - moreover, if a homogenous system has fewer equations than variables, then it must have an infinite number of solutions
```math
\begin{aligned}
x - 2y + 3z &= 0 \\
2x + y - z &= 0 \\
-x + 4y + 2z &= 0
\end{aligned}
```



