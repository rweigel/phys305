= Discrete Charge Distributions =

# Problem Point Charge Electric Field Calculation

In the left part of the previous diagram, the 9 positive charges are uniformly spaced. If the distance between $q_1$ and $q_9$ is $6a$ and the open circle is a perpendicular distance $2a$ above the horizontal line, what is

\begin{itemize}
    \item $\mathbf{r}_1$? Write your answer in the form $\mathbf{r}_1 = r_x\ihat+r_y\jhat$ and find $r_x$ and $r_y$ in terms of $a$ and/or numbers.
    \ifsolutions
    \\
    \\
    {\bf Answer}: $\mathbf{r}_1=3a\ihat + 2a\jhat$
    \else
    \\[2cm]
    \fi
    \item $\hat{\mathbf{r}}_1$? Write your answer in the form $\hat{\mathbf{r}}_1 = \hat{r}_x\ihat+\hat{r}_y\jhat$ and find $\hat{r}_x$ and $\hat{r}_y$ in terms of $a$ and/or numbers.
    \ifsolutions
    \\
    \\
    {\bf Answer}: $\hat{\mathbf{r}}_1=\frac{3}{\sqrt{13}}\ihat + \frac{2}{\sqrt{13}}\jhat$. Unit vectors are dimensionless, so $a$ is not part of solution.
    \else
    \\[2cm]
    \fi
    \item $\mathbf{E}_1$, the electric field at the open circle due to $q_1$? Write your answer in the form $\mathbf{E}_1 = E_x\ihat+E_y\jhat$ and find $E_x$ and $E_y$ in terms of one or more of $k$, $a$, $q_1$, and numbers.
    \ifsolutions
    \\
    \\
    {\bf Answer}: $\mathbf{r}_1=\frac{kq_1}{a^2(13)^{3/2}}(3\ihat + 2\jhat)$
    \else
    \\[3cm]
    \begin{tikzpicture}
    \draw[step=1,black,thin] (0,0) grid (8,8)
    \end{tikzpicture}
    \fi
    \end{itemize}
\end{tcolorbox}

== Basic Calculation ==

\(q\) is located at \((x,y,z) = (0,0,1)\); \(Q\) is located \((x,y,z) = (0,1,0)\).  The force of \(q\) on \(Q\) is \(\mathbf{F}_{qQ} = \frac{qQ}{4\pi\epsilon_0}(a\hat{\mathbf{x}} + b\hat{\mathbf{y}} + c\hat{\mathbf{z}})\).  What are \(a\), \(b\), and \(c\)?  What is \(F\) (or \(|\mathbf{F}|\))?

Use the formula \(F = kqQ/d^2\) to check your answer and signs.

== Basic Calculation ==

Charge \(2q\) is located at \((x,y,z)\)=\((0,2d,2d)\). Charge \(3q\) is located at \((x,y,z)\)=\((0,-3d,-3d)\). Compute the electric field due to these charges at \((d,0,0)\).

== Charge on Points of Triangle ==

An equilateral triangle with sides of length \(d\) has charges of \(+q\) on each of its corners. Compute (or state answer with justification and no calculation) the electric field at the center of the triangle.

== Charges on Points of Square ==

A square with sides of length \(d\) has charges of \(+q\) on each of its corners. Compute (or state answer with justification and no calculation) the electric field at
* the center of the square and
* along the center of its sides.

== One charge ==

Charge \(+q\) is located at \((x,y,z)=(0,0,d)\).

# Sketch the electric field lines in the \(y,z\) plane.
# What is the direction of the total electric field, \(\mathbf{E}\), along the \(y\)-axis?
# What is the total electric potential, \(V\), on the \(y\)-axis? (This was supposed to be an easier version of the next question, but it caused confusion. To answer this question, use the equation for \(V\) you get from the next question and set \(z=0\).
# What is \(V\) as a function of \((y,z)\)?
# What is \(\mathbf{E}\) as a function of \((y,z)\)?
# When \(z=0\) and \(y>>d\), the point charge at the origin "looks" like it is at the origin and so the expected \(V\) is that of a charge \(q\) at the origin: \(V=kq/|y|\). Show that your equation for \(V\) is consistent with this expectation.
# When \(y=0\) and \(z>>d\), the point charge at the origin "looks" like it is at the origin and so the expected \(V\) is that of a charge \(q\) at the origin: \(V=kq/|z|\). Show that your equation for \(V\) is consistent with this expectation.
# A large distances relative to \(d\) in the \((y,z)\) plane, corresponding to \(y^2+z^2>>d^2\), the point charge "looks" like it is at the origin and so the expected \(V\) is that of a charge of \(q\) at the origin: \(V=kq/\sqrt{y^2+z^2}\). Show that your equation for \(V\) is consistent with this expectation.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Hint on last question
|-
|
To simplify notation, define \(\epsilon^2 \equiv d^2/(y^2+z^2)\) and \(r^2\equiv y^2+z^2\) and then show \(V(y,z)\) can be written as

$$V(y,z) = \frac{kq}{\sqrt{y^2+(z-d)^2}} = \frac{kq}{\sqrt{y^2+z^2}}\cdot\frac{1}{\sqrt{1-2(z/r)\epsilon + \epsilon^2}}$$

Note that the maximum value of \(|z/r|\) is 1, so \(2(z/r)\epsilon\) is small because \(\epsilon << 1\).

|}

== Two charges ==

Charge \(+q\) is located at \((x,y,z)=(0,0,d)\). Charge \(-q\) is located at \((x,y,z)=(0,0,-d)\).

# Sketch the electric field lines in the \(y,z\) plane.
# What is the direction of the total electric field, \(\mathbf{E}\), along the \(y\)-axis?
# What is the total electric potential, \(V\), on the \(y\)-axis?
# What is \(V\) as a function of \((y,z)\)?
# What is \(\mathbf{E}\) as a function of \((y,z)\)?
# When \(z=0\) and \(y>>d\), the two point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.
# When \(y=0\) and \(z>>d\), the two point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.
# A large distances relative to \(d\) in the \((y,z)\) plane, corresponding to \(y^2+z^2>>d^2\), the two point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.

== Two charges ==

Charge \(+q\) is located at \((x,y,z)=(0,0,d)\). Charge \(+q\) is located at \((x,y,z)=(0,0,-d)\).

# Sketch the electric field lines in the \(y,z\) plane.
# What is the direction of the total electric field, \(\mathbf{E}\), along the \(y\)-axis?
# What is the total electric potential, \(V\), along the \(y\)-axis?
# What is \(\mathbf{E}\) as a function of \((y,z)\)?
# What is \(V\) as a function of \((y,z)\)?
# When \(z=0\) and \(y>>d\), the two-point charges "look" like they overlap and so the expected \(V\) is that of a charge of \(2q\) at the origin: \(V=2kq/|y|\). Show that your equation for \(V\) is consistent with this expectation.
#When \(y=0\) and \(z>>d\), the two-point charges "look" like they overlap and so the expected \(V\) is that of a charge of \(2q\) at the origin: \(V=2kq/|z|\). Show that your equation for \(V\) is consistent with this expectation.
# A large distances relative to \(d\) in the \((y,z)\) plane, corresponding to \(y^2+z^2>>d^2\), the two-point charges "look" like they overlap and so the expected \(V\) is that of a charge of \(2q\) at the origin: \(V=2kq/\sqrt{y^2+z^2}\). Show that your equation for \(V\) is consistent with this expectation.

== Three charges ==

Charge \(+q\) is located at \((x,y,z)=(0,0,d)\). Charge \(+q\) is located at \((x,y,z)=(0,0,-d)\). Charge \(-2q\) is located at \((x,y,z)=(0,0,0)\).

# What is the direction of the electric field, \(\mathbf{E}\), on the \(x\)-axis? (Both positive and negative \(x\).)
# What is the direction of the electric field, \(\mathbf{E}\), on the \(y\)-axis? (Both positive and negative \(x\).)
# What is the direction of the electric field, \(\mathbf{E}\), on the \(z\)-axis? (Both positive and negative \(x\).)
# What is the total electric potential, \(V\), as a function of \((y,z)\)?
# What is \(\mathbf{E}\) as a function of \((y,z)\)?
# When \(y=0\) and \(z>>d\), the three point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.
# When \(z=0\) and \(y>>d\), the three point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.
# A large distances relative to \(d\) in the \((y,z)\) plane, corresponding to \(y^2+z^2>>d^2\), the three-point charges "look" like they overlap and \(V\) is expected to be approximately zero. Show that your equation for \(V\) is consistent with this expectation.
