___
**Review: Solve By Elimination**
$$
\begin{cases}
x + y = 4 \\
x - 2y = 8
\end{cases}
$$
**Lets Eliminate $y$ so**
$$2(x+y) =2(4)$$
$$2x + 2y = 8$$
**Lets add $R_{1}$ to $R_{2}$ 
$$3x+0=16$$
Solve For $x$**
$$x=\frac{16}{3}$$
**Now Solve For Y**
$$-1(x+y) = -1(4)$$
$$-x-y=-4$$

$$-3y=4$$
$$y=-\frac{4}{3}$$
___
**N-Variables & N-Coefficients Of A Linear System**
$$a_{1}x_{1}+a_{2}x_{2}+a_{\dots}x_{\dots}+a_{n}x_{n} = b$$
This is a linear coefficient (equation) of variables
$$x_{1},x_{2},\dots x_{n} = \text{Variables}$$
$$a_{1},a_{2},\dots a_{n}= \text{Coefficients}$$
$$b = \text{Constant Term}$$
A sequence of numbers $S_{1},S_{2},S_{\dots},S_{n}$ is a solution to a linear equation if $a_{1}S_{1}+a_{2}S_{2}+a_{\dots}S_{\dots}+a_{n}S_{n}=b$ is a true statement.
___
**Example: Show The For Arbitrary Values of $S$ & $t$
$$\begin{cases}  x_{1}=t-S+1 \\
x_{2}=t+S+2 \\
x_{3}=S \\
x_{4}=t
\end{cases}$$
Is a solution to
$$x_{1}-2x_{2}+3x_{3}+x_{4}=-3$$
$$2x_{1}-x_{2}+3x_{3}-x_{4}=0$$
Solve By Setting All Parameters To Zero
Let
$$S=0$$
$$t=0$$
The system is now
$$\begin{cases}
x_{1}=1\\
x_{2}=2 \\
x_{3}=0 \\
x_{4}=0
\end{cases}$$
We can then verify
$$1-2(2)+3(0)+0=-3$$
$$2(1)-2+0-0=0$$
Since these statement are true $S=0$ & $t=0$ has to be one of the solutions
___
There are three cases 
1. There is only one solution
2. There is no solution
3. There is infinitely many solutions
___
**Describe All Solutions (Choose And Pick Parameters/Parametric Form)**
$$3x-y+2z=6$$
Let
$$x=S, z=t$$
Plug it in
$$3S-y+2t=6$$
Solve for $y$
$$-y=6-2t-3S$$
$$y=2t+3S-6$$
NOTE: Usually don't pick the leading value
___
**The Relationship Between Linear System Of Equations & Augmented Matrixes**
People Representation
$$\begin{cases}
x+2y=-2 \\
2x+y=7
\end{cases}$$
Matrix Representation
$$\begin{array}{cc|c}
1&2&-2 \\
2&1&7
\end{array}$$
Elementary Operations
1. Interchange two equations (rows)
2. Multiple one equation by a (Scalar = Constant $\neq$ 0)
3. Adding one equation to another
Example: Solve the given matrix

$R_{1}(-2)+R_{2}$
$$\begin{array}{cc|c}
1&2&-2 \\
0&1&-\frac{11}{3}
\end{array}$$
$R_{2}(-2)+R_{1}$
$$\begin{array}{cc|c}
1&0& \frac{16}{3} \\
0&1& -\frac{11}{3}
\end{array}$$
Thus
$$x_{1}=\frac{16}{3},x_{2} =-\frac{11}{3}$$

