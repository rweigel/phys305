Due on Thursday, September 2nd at 3:00 pm.

Send your solutions to the email address rweigel+phys305@gmu.edu as a scanned PDF. If you do not have a scanner, use a smartphone PDF scanning app such as Genius Scan or Adobe Scan. **Do not send photos of your assignment.** If you have difficulty with this, feel free to contact me for help.

You are welcome to ask questions about homework problems on Discord. I will not give direct answers, but I will give hints. I will also first ask you for your solution to a related problem that was covered in class or in the notes. You are welcome to answer questions from other students on Discord, but please only give suggestions and hints.

This homework involves topics covered in [Vectors](vectors.html), [Vector Fields](vector_fields.html), [Field Lines](field_lines.html), and  [Equipotentials](equipotentials.html). 
 
# Vector Notation

Given $\mathbf{r}$ is a vector from the origin to the point $(x,y,z)$ and $\mathbf{r}'$ is a vector from the origin to the point $(x',y',z')$ and a scalar function $f$ defined according to

$$f = \frac{1}{|\mathbf{r}-\mathbf{r}'|^2}$$

1. Write $f$ in cartesian coordinates.

2. Show that $|\mathbf{r}-\mathbf{r}'|^2$ can be written as $r^2+r'^2-2\mathbf{r}\dot\mathbf{r}'$

3. Compute $\boldsymbol{\nabla}\left(\frac{1}{|\mathbf{r}-\mathbf{r}'|}\right)$, where $\boldsymbol{\nabla}f(x,y,z)=\frac{\partial f}{\partial x}\xhat+\frac{\partial f}{\partial y}\yhat+\frac{\partial f}{\partial z}\zhat$

4. If $\textbf{\char"0509} \equiv \mathbf{r}-\mathbf{r}'$

    a. Show that

    $$\frac{\hat{\textbf{\char"0509}}\phantom{^2}}{\char"0509^2}=\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}$$

    b. Write $\hat{\textbf{\char"0509}}/{\char"0509^2}$ in cartesian coordinates with cartesian unit vectors.

# Tangent Vectors

An object is moved along the path $y=x^2$ from $x=0$ to $x=x_o$ when there is an external force of $\mathbf{F}=-mg\yhat$.

1\. Compute the force tangent to the path at $x_o/2$ and $x_o$.

2\. Compute the force perpendicular to the path at $x_o/2$ and $x_o$.

3\. (Extra credit) Compute $\int_{\mathcal{L}}\mathbf{F}\dot d\mathbf{l}$ where $\mathcal{L}$ is the path along $y=x^2$ from $x=0$ to $x=x_o$.

# Normal Vectors

A plane has corners at $(x,y,z)=(0,0,0)$, $(x,y,z)=(1,0,0)$, $(x,y,z)=(0,1,1)$, and $(x,y,z)=(1,1,1)$. 

1\. Sketch the plane with a 3--dimensional diagram.

2\. Sketch the plane in the $y$--$z$ plane. (That is, what you would see if you looked toward the origin from a point with large $x$.)

3\. Find a vector normal to the plane that has a positive $z$--component.

4\. There is a force acting on the plane of $\mathbf{F}=F_x\xhat+F_y\yhat+F_z\zhat$. Find the component of force perpendicular to the plane.

# Notation and Vector Fields

A positive charge $q$ is placed at $(x,y)=(x_o,0)$ and a negative charge $-q$ at $(x,y)=(-x_o,0)$.

The force on a charge $Q$ due to $q$ and $-q$ is

$$\mathbf{F}=kqQ\frac{\hat{\textbf{\char"0509}}\_+}{\char"0509^2\_+}-kqQ\frac{\hat{\textbf{\char"0509}}\_{-}}{\char"0509^2\_{-}}$$

where $\textbf{\char"0509}\_+=\mathbf{r}-\mathbf{r\_+}$, $\textbf{\char"0509}\_-=\mathbf{r}-\mathbf{r\_-}$, $\mathbf{r}=x\xhat + y\yhat$, $\mathbf{r\_+}$ is the vector from the origin to the positive charge, and $\mathbf{r\_-}$ is the vector from the origin to the negative charge.

Find $\mathbf{F}$ in cartesian coordinates with cartesian unit vectors in terms of the constants given at

1\. $(x,y)=(2,0)$

2\. $(x,y)=(0,2)$

It may help to solve this by using the techniques from Physics 260 first. This is a straightforward problem that his written in the notation used by Griffiths.

# Field Lines and Equipotentials

1\. Draw field lines associated with the two starting points shown in the diagram for $\mathbf{A}=-\sin\phi\xhat + \cos\phi\yhat$. Draw the field lines until they encounter the $-x$--axis.

2\. Sketch four equipotential lines.

<img src="figures/Field_Lines_3.svg" width=100%/>


