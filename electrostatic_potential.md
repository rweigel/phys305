= Electric Potential \(V\) =

* http://web.mit.edu/viz/EM/visualizations/coursenotes/modules/guide03.pdf

=== Computing Work ===

A point charge \(+q\) is at the origin.  

1. Compute how much work it would take to move a \(+Q\) charge from (x,y,z) = (0,0,a) to (0,b,0) along an arbitrary path. <span style="background-color:yellow">+2 for correct work.</span> 
2. Justify any equations that you use. <span style="background-color:yellow">+2 for correct justification.</span>

<div style="background-color:#E8E8E8">
1. The work required to move a charge \(Q\) in the field created by a charge \(q\) is \(W = Q(V_f-V_i) = kQq(1/r_f - 1/r_i)\), where \(r_f\) and \(r_i\) are the final and initialy distances between the charges.  So \(W = kQq(1/b - 1/a)\).  If \(b<a\), \(W > 0\) as would be expected (positive work is required to move \(Q\) closer to \(q\)).
2. I was looking for anything indicating that you understood that the change in energy of a charge due to a change in its position in the field of another charge was independent of path. (The problem statement notes that you need to compute the work along an arbitrary path). I also accepted: \(\nabla \times \mathbf{E} = 0\), \(\oint \mathbf{E}\cdot d\mathbf{l}=0\), or \(\mathbf{E}=\nabla V\) as a justification, but really additional explanation is needed to justify why these equations imply path independence.  For more rigor, see 2.2.4 and 2.3.1 of Griffiths.
</div>

=== Computing Electric Potential ===

A point charge \(+q\) is at the origin.  Compute how much work it would take to move a \(+Q\) charge from (x,y,z) = (0,0,10) to (0,5,0) by explicitly computing the integral

$$W = \int \mathbf{F}\cdot d\mathbf{l}$$

where \(\mathbf{F}\) is the electrostatic force of \(+q\) on \(+Q\) and \(d\mathbf{l}\) is a differential vector that always points tangent to the path of movement.  See also Example 1.6 of Griffiths.

<span style="background-color:yellow">Note that there is an easy way of computing the answer using a method used in PHYS 260.  You should use this method to check your answer if you did this the formal way.  If you use the easy way, make sure that you justify why it is valid.</span>

# TODO

1. Change from, e.g., 3 C to 3 10^{-9} C so forces and energy consistent with a person can provide.

2. A, B, C on plot to a, b, c (C is used for Coulomb)

3. The intro talks about the work of an external agent and how it changes U: W^{external} = \Delta U. The book talks about the work of a conservative force. Need to modify for consistency. Technically W^{external} = \Delta U is only correct when movement is arbitrarily slow from initial to final.

# Introduction

# Electric Potential Energy Differences ($\Delta U$)

Recall from mechanics that the symbol $U$ was used to represent potential energy. The potential energy of an object increases when you do a positive amount of work on it. For example, if you lift a mass from the floor, you increase its potential energy. In addition, recall that work done on an object _changes_ its potential energy, and this change is represented by $\Delta U$.

Mathematically, the work done by a force $\mathbf{F}$ in moving an object from position $a$ to position $b$ is

$$
W_{a\rightarrow b}=\int_a^b \mathbf{F}\cdot d\mathbf{l}
$$
\label{eqn:work}

and this work changes the potential energy of an object according to 

%\begin{equation}
$$
W_{a\rightarrow b} = U_b-U_a \equiv \Delta U
$$
%\end{equation}

where the symbol $\equiv$ is used to indicate that $\Delta U$ is defined to be the final potential at $b$ minus the initial potential at $a$.

If a force is always perpendicular to the direction of movement, the work due to that force is zero. 

When the force on an object does not change when it is moved a distance $L$ from $a$ to $b$ along a straight line, and the force vector is aligned with the path of movement, then

$$W_{a\rightarrow b}=\int_a^b \mathbf{F}\cdot d\mathbf{l}=(\pm)|\mathbf{F}|L$$

where $L$ is positive; the $+$ sign is used for a force that is in the direction of movement and the $-$ sign is used for a force that is in the opposite direction of movement. (You should know how to derive this.) For example, if you lift a mass $m$ upwards by a distance $L$, the force you exert is in the same direction of movement, so you do a work of $mgL$. The gravitational force on the mass is in the opposite direction of movement, so the work done by the gravitational force is $-mgL$.

The second form of the integral that is used is for the case when the force on an object changes as it is moved. This is covered on pages 749-750 in the textbook.

One of the most common difficulties in calculating work and energy is getting the correct sign for the answer. The following two problems have questions that ensure that you are able to predict the correct sign of work and changes in potential energy.

\newpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 1.1,height fill]
## Problem: Uniform Field

The following diagram shows a region of space where the electric field is constant and has a value of $3$~N/C.

<img src="figures/Uniform_Field.svg"/>

1\. You place a charge of $+3$~C at point $A$. What happens to that charge when it is released?
\ifsolutions
\\
\\
{\bf Answer}: Moves to right. By convention field lines point in direction of force on positive charge.
\else
\vspace{2.7cm}
\fi

2\. You move charge of $+3$~C from $A$ to $B$. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the charge changed?
\ifsolutions
\\
\\
{\bf Answer}: The charge naturally wants to move from A to B since it is a positive charge moving with the field lines. Since the work is done by the field not by you, your force must be in the opposite direction of movement so your work is negative. The force the field exerts on the charge is $\mathbf{F}=Q\mathbf{E}=(3\mbox{ C})(3\mbox { N/C})\ihat = (9\mbox{ N})\ihat$, where $\ihat$ points to the right. Your force is equal and opposite. The work done by you is the force over the path parallel to the field: 

$$W_{a\rightarrow b}=\int_a^b \mathbf{F}\cdot d\mathbf{l}=(\pm)|\mathbf{F}|L$$ 

So your work is $(-9\mbox{ N})(2 m) = -18 \mbox{ J}$. (a) $(-9 \mbox{ N})(2\mbox {m})=-18\mbox{ J}$ (b) $(+9 \mbox{ N})(2\mbox {m})=+18\mbox{ J}$ (c) $\Delta U = -18\mbox{ J}$ The change in PE is equal and opposite to the work done by the field. See derivation of equation 23.2 in the textbook.
\else 
\vspace{2.7cm}
\fi
\item You place a charge of $-3$~C at point $A$. What happens to that charge when it is released?
\ifsolutions
\\
\\
{\bf Answer}: Moves to left.
\else
\vspace{2.7cm}
\fi

3\. A charge of $-3$~C is moved from $A$ to $B$. How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the charge changed?
\ifsolutions
{\bf Answer}: (a) $+18\mbox{ J}$ (b) $-18\mbox{ J}$ (c) $\Delta U = +18\mbox{ J}$ The change in PE is equal and opposite to the work done by the field. See derivation of equation 23.2 in the textbook.
\else 
\vspace{4cm}
\fi

4\. You move a charge of $+3$\~C straight downward from $A$ to $C$. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the charge changed?
\ifsolutions
{\bf Answer}: Your force and the force due to the field are both perpendicular to the direction of movement. So the work done by both forces is zero. (a) $0\mbox{ J}$ (b) $0\mbox{ J}$ (c) $0 \mbox{ J}$
\else 
\vspace{2.7cm}
\fi

5\. If you move a charge of $-3$~C from $A$ to $C$ but deviate from a straight line, will your answers to the previous problem change? If no, explain why. If yes, provide new answers.
\ifsolutions
{\bf Answer}: No, they won't change. Think of movement along a smooth and curved line as being made of a series of tiny equal-sized steps in the vertical and horizontal directions. There is no work associated with the vertical steps. There is positive work associated with steps to the right and negative work associated with steps to the left. To get from $A$ to $C$ along an arbitrary path, you must take an equal number of steps to the left as you do to the right. See also Figure 23.1 and 23.2 which show how the work done by a conservative force does not depend on path.
\else 
\fi

\clearpage

## Problem: Radial Field

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 1.2,height fill]

In the previous problem, a charge was moved in a region of space where the electric field was constant and so the calculation of work did not require integration. In this problem, the electric field is not constant and so the calculation of work requires integration. The type of integration that must be performed to compute work in this case is given by Equation 23.8 in the textbook.

<img src="figures/Radial_Field.svg"/>

There is a charge of $-6$\~C at the origin. Some electric field lines for this charge are shown. To simplify the math, use $k=9\cdot 10^9$~N$\cdot$m$^2$/C$^2$.

1\. You move a charge of $+3$\~C from $A$ to $B$. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the moved charge changed?

\ifsolutions {\bf Answer}: According to equation 23.8, the work done by the field, labeled $W^E$ here, when a charge $q_0$ is moved from a distance $r_a$ from a charge $q$ to a distance $r_b$ is
$$
W^{E}\_{a\rightarrow b} = kqq_o\left(\frac{1}{r_a}-\frac{1}{r_b}\right)
$$
For this problem, $q=-6$\~C, $q_0=3$\~C, $r_a=3$\~m, and $r_b=2$\~m.
$$
W^{E}\_{a\rightarrow b} = (9\cdot 10^9)(-6)(+3)\left(\frac{1}{3}-\frac{1}{2}\right)\mbox{ J} = 27\cdot 10^9\mbox{ J}
$$

This is the answer for (b). The work that you do is equal and opposite to the work that the field does. The change in potential is equal and opposite to the work done by the field. In summary, (a) $-27\cdot 10^9\mbox{ J}$, (b) $+27\cdot 10^9\mbox{ J}$, (c) $-27\cdot 10^9\mbox{ J}$. (Use the techniques given in the previous problem to make sure that the signs of these answers are correct.)

\else
\vspace{2cm}
\fi

2\. You move a charge of $-3$~C from $A$ to $B$. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the moved charge changed?
\ifsolutions
\\
\\
{\bf Answer}: (a) $+27\cdot 10^9\mbox{ J}$, (b) $-27\cdot 10^9\mbox{ J}$, (c) $+27\cdot 10^9\mbox{ J}$. 
\else
\vspace{2cm}
\fi

3\. You move a charge of $-3$\~C from $B$ to $C$ along the dotted line. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the moved charge changed?
\ifsolutions
\\
\\
{\bf Answer}: (a) 0\~J, (b) 0\~J, (c) 0\~J
\else
\vspace{2cm}
\fi

4\. You move a charge of $-3$\~C from $C$ to $B$ but deviate from the dotted line. (a) How much work did you do? (b) How much work was done by the electric field? (c) By how much has the potential energy of the moved charge changed?
\ifsolutions
\\
\\
{\bf Answer}: (a) 0\~J, (b) 0\~J, (c) 0\~J
\else
\vspace{2cm}
\fi

\clearpage

# Electric potential difference $\Delta V$

In the previous section, we considered moving an arbitrary amount of charge (either positive or negative) from point $a$ to point $b$ and computed its change in potential energy $\Delta U$. 

An electric potential difference $\Delta V$ is defined to be the change in electric potential energy of a (positive by convention) test charge when it is moved from point $a$ to point $b$ divided by the magnitude of the test charge.

As a result, the only difference between the $\Delta U$ calculations performed previously and $\Delta V$ calculations is that we first compute $\Delta U$ for a $+1$\~C charge. To get $\Delta V$, we simply divide by $\Delta U$ by $+1$\~C.

The definition of electric potential is similar to the definition of electric field in that they both involve consideration of a test charge. That is, the electric field is the force on a test charge divided by the magnitude of the test charge:

$$\mathbf{E} = \frac{\mathbf{F}}{q_o}$$

A change in potential is the change in potential of a  test charge divided by the magnitude of the test charge's charge:

$$\Delta V = \frac{\Delta U}{q_o}$$

The advantage of using changes in electric potential ($\Delta V$) as opposed to changes in electric potential energy ($\Delta U$) of a specific amount of charge is that once the electric potential difference $\Delta V$ is known for a test charge, the change in potential energy for an arbitrary amount of charge $Q$ can be computed by simply multiplying $\Delta V$ and $Q$. This is similar to the advantage of the electric field. If we know the electric field at a given point, we can find the force on an arbitrary charge $Q$ by multiplying $\mathbf{E}$ and $Q$.

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.1,height fill]

The following diagram shows a region of space where the electric field is constant and has a value of $3$~N/C. 

\input{Electrostatic_Potential/figures/Uniform_Field2}

\begin{enumerate}
\item What is difference in potential $\Delta V = V_B-V_A$.
\ifsolutions
\\
\\
{\bf Answer}: As discussed in the introduction to this section, the difference in potential can be determined by first computing $\Delta U$ for a $+1$\~C charge. Then $\Delta V = \Delta U/(1\mbox{ C})$. The steps for computing $\Delta V$ for a $+1\$~C charge will be identical to those in problem 1.1.2 of this tutorial. The result is $\Delta U=-6\mbox{ J}$. Thus

$$\Delta V = \frac{-6\mbox{ J}}{+1\mbox{ C}}= -6\mbox{ Volt}$$

A faster way of solving this is to simply compute $\Delta V$ by using $\Delta U$ for the $3$\~C charge and dividing by $3$\~C. This is also valid and makes sense -- a difference in potential from point $A$ to point $B$ corresponds to the change in potential energy associated with moving a positive unit of charge from point $A$ to point $B$. If you computed the change in energy associated with moving with 3 units of charge, then you divide this energy by 3 to get the difference in potential.
\else
\vspace{2cm}
\fi

\item What is the difference in potential $\Delta V = V_B-V_C$.
\ifsolutions
\\
\\
{\bf Answer}: $-6\mbox{ Volts}$. This is the same as (V$_B$ - V$_A$) + (V$_A$ - V$_C$) = -6 + 0 = -6 Volts
\else
\vspace{2cm}
\fi

\item You move a charge of $+3$~C from $A$ to $B$. By how much has the electric potential energy of the moved charge changed?

\ifsolutions
\\
\\
{\bf Answer}: This question was already answered in problem 1.1.2. But given $\Delta V$, we can compute $\Delta U$:

$$\Delta U = Q\Delta V=(3\mbox{ C})(-6\mbox{ Volt})=
(3\mbox{ C})\left(-6\frac{\mbox{ J}}{ \mbox{ C}}\right)=-18\mbox{ J}$$
\else
\vspace{2cm}
\fi
\item You move a charge of $-3$~C from $A$ to $B$. By how much has the electric potential energy of the moved charge changed?
\ifsolutions
\\
\\
{\bf Answer}: This question was already answered in problem 1.1.2. But given $\Delta V$, we can compute $\Delta U$:

$$\Delta U = Q\Delta V=(-3\mbox{ C})(-6\mbox{ Volt})=
(-3\mbox{ C})\left(-6\frac{\mbox{ J}}{ \mbox{ C}}\right)=+18\mbox{ J}$$
\else
\vspace{2cm}
\fi

\item You move a charge of $-3$~C from $B$ to $C$. By how much has the electric potential energy of the moved charge changed?
\ifsolutions
\\
\\
{\bf Answer}: The move from $B$ to $C$ can be made by a move from $B$ to $A$ then a move from $A$ to $C$. The change in potential in going from $B$ to $A$ is opposite the change in potential in going from $A$ to $B$, which was found to be $-6\mbox{ Volt}$. The change in potential in going from $A$ to $C$. Thus

$$\Delta U = Q\Delta V=(-3\mbox{ C})(+6\mbox{ Volt})=-18\mbox{ J}$$

\else
\vspace{2cm}
\fi

\end{enumerate}

\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.2,height fill]

\input{Electrostatic_Potential/figures/Negative_Charge_Field_Lines2}

There is a charge of $-6$\~C at the origin. Some electric field lines for this charge are shown. To simplify the math, use $k=9\cdot 10^9$~N$\cdot$m$^2$/C$^2$.

\begin{enumerate}
\item What is difference in potential $\Delta V = V_B-V_A$.
\ifsolutions
In general, the potential at a point in space due to a point charge a distance $r$ from that point is $V=\frac{kq}{r}$.

$$V_A=\frac{k(-6\mbox{ C})}{3\mbox { m}}=-18\cdot 10^9\mbox{ Volt}$$

$$V_B=\frac{k(-6\mbox{ C})}{2\mbox { m}}=-27\cdot 10^9\mbox{ Volt}$$

$$V_B-V_A=-6\cdot 10^9\mbox{ Volt}$$

A negative value is expected because a positive charge placed at $A$ will tend to move towards $B$, which has a lower potential.

\else
\vspace{3cm}
\fi

\item What is difference in potential $\Delta V = V_C-V_A$.

\ifsolutions
{\bf Answer}: The potential at $B$ is the same as the potential at $C$. This can be seen mathematically from the equation $V=\frac{kq}{r}$ -- at $A$ and $B$, $r$ is the same. Physically, in moving from $A$ to $B$ along the dotted line, no work is required because the electric field is perpendicular to this path. The problem statement did not require moving from $A$ to $C$ along the dotted line, but was established earlier, the changes in potential energy are independent of path for a conservative force, so we are free to choose a convenient path. Based on this, $V_C-V_A=V_B-VA$ and so the answer is the same as the previous problem.
\else
\vspace{3cm}
\fi

\item You move a charge of $-3$~C from $A$ to $B$. By how much has the potential energy of the moved charge changed?
\ifsolutions
This is most easily found using

$$\Delta U = U_{final}-U_{initial}= Q{\Delta V}=Q(V_{final}-V_{initial})$$

Earlier it was found $V_B-V_A=-6\cdot 10^9\mbox{ Volt}$. As a result, 

$$U_B-U_A= (-3\mbox{ C})(V_B-V_A)=-27\cdot 10^9$$

This answer matches the answer for an identical question in problem 2.1.2 of this tutorial.

\else
\vspace{3cm}
\fi

\item You move a charge of $-3$~C from $B$ to $C$. By how much has the potential energy of the moved charge changed?

\ifsolutions
{\bf Answer}: 0~J. See answer to question 1. for the justification.
\else
\vspace{3cm}
\fi
\end{enumerate}
\end{tcolorbox}

# $\mathbf{E} = -\boldsymbol{\nabla}V$

Recall that the gradient of a scalar field $f$ gives a vector field. That is, we can associate a vector field $\mathbf{U}$ with a scalar field by performing the operation

$$\mathbf{U}=\boldsymbol{\nabla}f$$

For $f$ in cartesian coordinates, we would compute $\mathbf{U}$ using

$$\mathbf{U}= \boldsymbol{\nabla}f(x,y,z)=\frac{\partial f}{\partial x}\xhat+\frac{\partial f}{\partial y}\yhat+\frac{\partial f}{\partial z}\zhat$$

and for $f$ in cylindrical or spherical coordinates, the equations are given on the second--to last page of Griffiths. 

For example, in [HW #1](hw1.html), you showed that 
$\boldsymbol{\nabla}\left(\frac{1}{|\mathbf{r}-\mathbf{r}'|}\right)=\displaystyle -\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}$ by first writing $f=1/|\mathbf{r}-\mathbf{r}'|$ in cartesian coordinates.

The operation $\boldsymbol{\nabla}f$ results in a vector and involves an operation on a scalar function $f$; the equation is read as "the gradient of $f$". In contrast, the operation $\boldsymbol{\nabla}\bfcdot \mathbf{U}$ results in a scalar function and involves an operation on a vector function $\mathbf{U}$. See also the [caution in the notes on divergence]( http://localhost:9000/divergence.html#-boldsymbol-nabla-bfcdot-mathbf-u).

**Question**: It is simple to compute a vector function $\mathbf{U}$ given a scalar function $f$ using $\boldsymbol{\nabla}f$. Can we reverse this process -- that is, given a vector function $\mathbf{U}$, can we find a scalar function $f$?

The answer is yes, provided that $\boldsymbol{\nabla} \times \mathbf{U} = 0$. The proof of this is given in ... of Griffiths; it requires the Fundamental Theorem of Gradients and Stoke's theorem, both of which will be covered later in the semester. At this point, we will only cover the result, which is

$$f(\mathbf{r}) = f(\mathbf{a}) + \int_\mathbf{a}^\mathbf{\mathbf{r}}\mathbf{U}\bfcdot d\mathbf{l}$$

where the line integral can be taken over any path from $\mathbf{a}$ to $\mathbf{r}$.

The statement $f(\mathbf{r})$ is short--hand for $f(x,y,z)$; the justification is that the vector $\mathbf{r}=x\xhat + y\yhat +z\zhat$ ends at the point in space $(x,y,z)$. Vectors in limits of integration are not common -- in the integral above, the upper limit of $\mathbf{r}$ means that the line integrated over ends at $(x,y,z)$ and the lower limit $\mathbf{a}$ means the line integrated over starts at the point $(a_x,a_y,a_z)$.

In E&M, we use $\mathbf{E}=-\mathbf{U}$ and $V$ for $f$.

In this notation, given $V$, we can compute $\mathbf{E}$ using

$$\mathbf{E}=-\boldsymbol{\nabla}V$$

and given $\mathbf{E}$, we can compute $V$ using

$$V(\mathbf{r}) = V(\mathbf{a}) - \int_\mathbf{a}^\mathbf{\mathbf{r}}\mathbf{E}\bfcdot d\mathbf{l}$$

## Example

Suppose $V=kq/r$.

1. Compute $\mathbf{E}$.
2. Use this computed $\mathbf{E}$ and $\displaystyle V(\mathbf{r}) = V(\mathbf{a}) - \int_\mathbf{a}^\mathbf{\mathbf{r}}\mathbf{E}\bfcdot d\mathbf{l}$ to compute $V$.

For the path, use a straight line between $\mathbf{a}=(R\xhat + R\yhat)/\sqrt{2}$ to $\mathbf{r}=2(R\xhat + R\yhat)/\sqrt{2}$ 

**Answer**:

1\.

From Griffiths, for $f$ in cartesian coordinates,

$$\boldsymbol{\nabla}f(x,y,z)=\frac{\partial f}{\partial x}\xhat+\frac{\partial f}{\partial y}\yhat+\frac{\partial f}{\partial z}\zhat$$

We could use this equation by re-writing $V$ as $kq/\sqrt{x^2+y^2+z^2}$. Alternatively, we can use

$$\boldsymbol{\nabla} f(r,\theta,\phi) = {\partial f \over \partial r}\hat{\mathbf r}+ {1 \over r}{\partial f \over \partial \theta}\hat{\boldsymbol \theta}+ {1 \over r\sin\theta}{\partial f \over \partial \phi}\hat{\boldsymbol \phi}$$

$$\mathbf{E}=-\boldsymbol{\nabla} V=-\left({\partial V \over \partial r}\hat{\mathbf r}+ {1 \over r}{\partial V \over \partial \theta}\hat{\boldsymbol \theta}+ {1 \over r\sin\theta}{\partial V \over \partial \phi}\hat{\boldsymbol \phi}\right)$$

The last two terms are zero because $V$ does not depend on $\theta$ or $\phi$. This leaves

$$\mathbf{E}=-{\partial (\frac{kq}{r}) \over \partial r}\hat{\mathbf r} = \frac{kq}{r^2}\hat{\mathbf r}$$

2\.

We need to evaluate 
$\displaystyle V(\mathbf{r}) = V(\mathbf{a}) - \int_\mathbf{a}^{\mathbf{r}}\mathbf{E}\bfcdot d\mathbf{l}$

The integral will be straight--forward to compute if we write $d\mathbf{l}$ in spherical coordinates, which is $d\mathbf{l}=dr\hat{\mathbf r}$ along a radial line.

$\displaystyle V(\mathbf{r})=V(\mathbf{a})- \int_a^{r}\frac{kq}{r^2}\hat{\mathbf r}\bfcdot dr\hat{\mathbf r}=V(\mathbf{a})-\int_a^{r}\frac{kq}{r^2}dr=V(\mathbf{a})-\left[-\frac{kq}{r}\right]_a^r=V(\mathbf{a})+\frac{kq}{r}-\frac{kq}{a}$

In summary,

$\displaystyle V(\mathbf{r})=V(\mathbf{a})+\frac{kq}{r}-\frac{kq}{a}$

The first and last terms on the right--hand side are constants. As a result, we have found

$\displaystyle V(\mathbf{r})=const + \frac{kq}{r}$

which is equal to the $V$ that we started with only if $const=0$. This constant cannot be determined unless we are told the functional form of $V$ and also $V$ at some reference point. That is, given $\mathbf{E}$, we cannot uniquely compute $V$ unless we are also told $V$ at some position in space.

For example, if the problem statement was $V=kq/r$ and $V(\infty)=0$, then we can conclude $const=0$. We also could have been told that $V(a)=0$, in which case $const=-kq/a$.

Physically, the reason is that a value of potential at a point is not useful -- we must know the potential at a reference point in order to determine how much work is required to move an object from the reference point to a given point.

Another way explaining this is to consider a similar problem: if $F=df/dx$, show that $\int_a^x F(x')dx'$ gives $f$. If $f=x^2$, then $F=2x$ and $\int_a^x F(x') dx'= x^2 - f(a)$. We can't show that $\int Fdx$ gives $f$ unless we are told that $f(a)$ is zero.

Although it does not make sense to say $V=kq/r$ without also giving the potential at a reference point, we do it anyway. The convention is that if a potential at a reference point is not given, then the reference point is infinity and the reference potential is zero. That is, instead of stating "$V=kq/r$ with $V(\infty)=0$", we simply state "$V=kq/r$".

## Example

Compute $V(\mathbf{b})-V(\mathbf{a})$ using $V(\mathbf{b}) = V(\mathbf{a}) - \int_\mathbf{a}^\mathbf{\mathbf{b}}\mathbf{E}\bfcdot d\mathbf{l}$ and

1. Path 1
2. Path 2

Show and justify all steps in your calculation.

**Answer**:

We expect the answers to be the same because the line integral of $\mathbf{E}$ applies to arbitrary paths.


# $V$ for a point charge

For a point charge at the origin, $\mathbf{E}=kq/r^2$ and the calculation of 

$$V(\mathbf{r}) = V(\mathbf{a}) - \int_\mathbf{a}^\mathbf{\mathbf{r}}\mathbf{E}\bfcdot d\mathbf{l}$$

was given in an example in the previous section and the result was

$$V(\mathbf{r}) = const + \frac{kq}{r}$$

By convention, for point charges at any location, we always assume that $V(\infty)=0$, so $const=0$ and

$$V(r) = \frac{kq}{r}$$

For a point charge not at the origin, the potential depends on the radial distance $\char"0509$ from the point charge to the point of interest: 

$$V(\textbf{\char"0509}) = \frac{kq}{\char"0509}$$

where $\textbf{\char"0509}=\mathbf{r}-\mathbf{r}'$, $\mathbf{r}$ is a vector from the origin to the point of interest and $\mathbf{r}'$ is a vector from the origin to the point charge. By convention, we usually omit the functional dependence in $V$. Or, we write the functional dependence as $V(\mathbf{r})$ because $\mathbf{r}'$ is usually fixed or given and we care about how $V$ varies relative to the origin as opposed to the location of the charge. Thus, we usually write

$$\boxed{V(\mathbf{r}) = \frac{kq}{|\mathbf{r}-\mathbf{r}'|}}$$

Recall that the electric field due to a point charge at $\mathbf{r}'$ is

$$\mathbf{E}(\mathbf{r})=kq\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}$$

You have already shown that these two equations satisfy $\mathbf{E}=-\boldsymbol{\nabla}V$ in [HW #1](hw1.html), where you showed that 
$\boldsymbol{\nabla}\left(\frac{1}{|\mathbf{r}-\mathbf{r}'|}\right)=\displaystyle -\frac{\phantom{|}\mathbf{r}-\mathbf{r}'\phantom{|^3}}{|\mathbf{r}-\mathbf{r}'|^3}$.

## Example

A point $q$ is at $(x,y,z)=(R,R,R)/\sqrt{3}$. Compute $V(x,y,z)$.

**Answer**

$\mathbf{r}=x\xhat + y\yhat + z\zhat$

$\mathbf{r}'=R\xhat + R\yhat + R\zhat$

$\displaystyle V(\mathbf{r}) = \frac{kq}{\char"0509}= \frac{kq}{|\mathbf{r}-\mathbf{r}'|}=kq\frac{1}{\sqrt{(x-R)^2+(y-R)^2+(z-R)^2}}$

## Problem

A point $q$ charge is at $(x,y,z)=(b,0,0)$. A point charge $q$ is at $(x,y,z)=(-b,0,0)$. Compute $V$ and then use $\mathbf{E}=-\boldsymbol{\nabla}V$ to compute $\mathbf{E}$.


# $U$ and $V$ for  of a Group of Charges

Previously, differences in electric potential energy, $\Delta U$, and electric potential, $\Delta V$, were considered. Only differences in $U$ and $V$ are meaningful. However, in E&M, we often discuss $U$ and $V$; in this case, these quantities are relative to the respective quantities for a charge at infinity, in which case $U$ and $V$ are zero. That is, instead of discussing $\Delta U$ in the equation $\Delta U = U(x) - U_{\infty}$, we discuss $U(x)$, which is equal to $\Delta U$ because $U_{\infty}$ is zero.

The electric potential energy of a charge $q_0$ that is a distance of $r_1$ from a charge $q_1$ is defined to be 

$$U=k\frac{q_0q_1}{r_1}$$

In this formula, if the charges have opposite signs then $U$ is negative; if they have the same sign then $U$  is positive. Note that there is a sign associated with the potential energy but the direction of the vector that connects the charges does not matter; the equation for $U$ only involves the values of the charges and the magnitude of the separation distance between them.

Consider next the potential energy of charge $q_0$ when it is a distance $r_1$ from charge $q_1$ and a distance $r_2$ from charge $q_2$. Because potential energy is a scalar and not a vector, the potential energy of $q_0$ is the {\bf algebraic} sum, rather than the vector sum, of the potential energies due to $q_1$ and $q_2$

$$U=k\frac{q_0q_1}{r_1}+k\frac{q_0q_2}{r_2}$$

More generally, if there is a group of $N$ charges, the potential energy of charge $q_0$ is

$$U=k q_0 \sum_{i=1}^N {\frac{q_i}{r_i}}$$

Similarly, the electric potential at a point in space due to a group of $N$ charges is the {\bf algebraic} sum of the potentials due to each of the charges at that point in space

$$V=k \sum_{i=1}^N {\frac{q_i}{r_i}}$$

\newpage

## Example

## Problem

%We examine the potential energy and potential for an group of 4 charges, $q_0$, $q_1$, $q_2$, and $q_3$ separated by distances $r_1$, $r_2$, $r_3$ from $q_0$. 

<img src="figures/Assembly_of_Charges.svg"/>

\begin{enumerate}
\item What is the potential energy of the charge $q_0$ in the diagram shown? 

\ifsolutions
{\bf Answer}
$$U = \frac{kq_oq_1}{r_1}+\frac{kq_oq_2}{r_2}+\frac{kq_oq_3}{r_3}$$
\else
\vspace{2cm}
\fi

This represents that amount of energy it would take to move charge $q_o$ from infinity to its position on the diagram.

\item What is the potential at the position of $q_0$ if that charge were to be removed (i.e., the potential due to charges $q_1$, $q_2$, and $q_3$)? 

\ifsolutions
{\bf Answer}
From $U=QV$, where here $Q=q_o$, $V=U/q_o$ 

$$V = \frac{kq_1}{r_1}+\frac{kq_2}{r_2}+\frac{kq_3}{r_3}$$

That is, the potential at a given location is found from potential energy of a charge at that location by dividing by the charge's potential energy by the value of the charge. 
\else
\vspace{2cm}
\fi

\item Can you find the potential energy at the position of $q_0$ if that charge were to be removed? Why or why not? 

\ifsolutions
{\bf Answer}: No. It does not make sense to ask what the potential energy is at a point in space. Only physical objects (e.g., masses, charges) have potential energy.
\else
\vspace{2cm}
\fi

\item Explain the difference between potential and potential energy. 

\ifsolutions
{\bf Answer}: A potential is a value associated with a location in space and an electric potential is created by charges at all locations in space.

Potential energy is the energy associated with an object at a given location in space. The electric potential energy of a charge is the energy required to move it from a large distance away from all other charges to a given location in space. The electric potential energy of a charge $Q$ at a point in space is related to the electric potential at that point in space by $U=QV$.
\else
\vspace{2cm}
\fi

\end{enumerate}
\end{tcolorbox}

# Total $U$ and $V$ for a Group of Charges

In the previous section, the potential energy associated with a charge $q_0$ was considered. This is the energy required to move $q_0$ into place with the other charges fixed. Another consideration is the energy required to put all of the charges in place. Suppose there are no charges and $q_3$ in moved into position. Because there is no electric field, this requires no energy. To move $q_2$ into position, work must be done due to the force from $q_3$. To move $q_1$ into position, work must be done due to the force from $q_3$ and $q_2$. To move $q_0$ into position, work must be done due to the force from $q_3$, $q_2$, and $q_1$.

## Example


## Problem



