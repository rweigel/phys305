= Electric Field \(\mathbf{E}\) =

* http://web.mit.edu/viz/EM/visualizations/coursenotes/modules/guide02.pdf

The electric field at a point in space is a quantity used to determine the force that an infinitesimal "test" charge, \(q_0\), would feel if placed there.

Given the electric field at a location \(x,y,z\) in space and an amount of charge, \(q_0\), placed there, one can use

$$\mathbf{F}(x,y,z)=\mathbf{E}(x,y,z){q_0}$$

to compute the force on \(q_0\).

Technically, the electric field is defined as 

$$\mathbf{E}(x,y,z)=\lim_{q_0\to 0} \frac{\mathbf{F}(x,y,z)}{q_0}$$

The amount of charge \(q_0\) must be infinitesimal so that its presence does not change the electric field. To see how a charge could alter an existing electric field, consider two positively charged beads that can move freely on a rod. The beads will repel each other and move to the ends of the rod. The electric field at a distance \(d\) above the center of the rod depends on the distance of the two beads to this point. Now, if we place a large charge, \(-Q\) a distance \(d\) above the center of the rod, the beads will move towards the center of the rod until the system is in force balance. A much smaller charge \(-q_0\) placed in the same position \(d\) above the rod will cause the beads to move a much smaller amount. The electric field due to the two beads computed at \(d\) when \(-Q\) is placed there much different than the electric field computed \(d\) when \(-q_0\) is placed.

We do something similar in circuits. We define a hypothetical voltmeter that is able to tell us the potential difference between two points. In reality, when we use a real voltmeter, we'll always get a different value than the hypothetical voltmeter, because the real voltmeter affects the current flow in the circuit.

\section{Introduction}

Prior to starting this tutorial, review Chapters 21.4-21.6 of your textbook.

There are two abstract concepts that are used in electricity and magnetism: A \textbf{field} and a \textbf{field line}.

Fields and field lines are two of the most fundamental concepts in electricity and magnetism. Later on in the semester, you will encounter a quantity called ``electric potential'' and lines of constant electric potential (equipotentials), which are found by first finding electric field lines. In addition, you will encounter ``electric flux''. This quantity is related to the number of electric field lines that pass through a surface.

In this tutorial, electric fields and field lines associated with static (not moving) charges are considered. Magnetic fields and field lines associated with steady currents are considered later in the semester.

\subsection{Electric Fields}

A {\bf field} is a quantity that is used with additional information to compute something concrete, usually a force. You've already dealt with fields in mechanics - the gravitational field near Earth's surface has a magnitude of 9.8 m/s$^2$. If you multiply this by your mass, you'll get the force that your feel due to (primarily) Earth's mass. To determine the gravitational field at a given point in space, we place a small test mass $m_o$ there and measure the force $\mathbf{F}_m$ on it due to all other masses in the universe. The gravitational field $\mathbf{g}$ is then

\begin{equation}
\mathbf{g} = \frac{\mathbf{F}_m}{m_o}
\end{equation}

where the subscript ``m'' is added to $\mathbf{F}$ to indicate that it is a force due to masses. Fields are useful because if I want to compute the force on an object at a given point, I simply need to multiply $\mathbf{g}$ by the mass.

The electric field at a given point is defined as the ratio of the force a test charge $q_o$ would feel if placed at that point by the value of the charge $q_o$:
\begin{equation}
\mathbf{E} = \frac{\mathbf{F}_e}{q_o}
\end{equation}

where the subscript ``e'' indicates that it is a force due to charges. The force in this equation is the force on the charge $q_o$ due to all other charges in the universe. By convention, we always assume the test charge $q_o$ is positive. The SI units for electric field are Newtons/Coulomb.

The electric field vector at any point is found by first computing the force a positive test charge \(q_o\) would experience when placed there due to all other charges. The electric field vector at that point is simply this force vector divided by \(q_o\).

In the above, the term ``test charge'' was used. A test charge has three properties: it is positive, infinitesimally small in size, and has an infinitesimal total charge. The reason that we require small size and total charge is we don't want the introduction of the test charge to modify the electric field. If, for example, the test charge had a very large charge, it could cause other charges in the system to move, and this would result in a change in the electric field.

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=blue!100!blue,title=Example 1.1,height fill]
Compute the electric field at $(x,y) = (a,a)$ due to a positive charge $q$ at the origin.

{\bf Method 1}

For this method, assume that there is a charge $q_o$ at $(x,y) = (a,a)$.

The magnitude of the force is
\begin{equation}
|\mathbf{F}| = F = \frac{k|qq_o|}{d^2}
\end{equation}
where $d$ is the separation distance and the direction is along the line that connects the two charges. Because both charges are positive, the force on $q_o$ will be in the direction shown. In the equation above, both ways of representing the magnitude of a vector ($|\mathbf{F}|$ and $F$) were used as a reminder of their equivalence.

\input{figures/Example_1.1a.tex}

The separation distance between the two charges is $d=\sqrt{a^2+a^2}=a\sqrt{2}$ and so 

\begin{equation}
|\mathbf{F}| = F = \frac{k|qq_o|}{a^2\sqrt{2}^2}= \frac{k|qq_o|}{2a^2}
\end{equation}

Using the equations in the diagram that show the calculation of $F_x$ and $F_y$,

\begin{equation}
\mathbf{F} = F_x\hat{\mathbf{x}}+F_y\hat{\mathbf{y}}=\frac{F}{\sqrt{2}}\hat{\mathbf{x}}+\frac{F}{\sqrt{2}}\hat{\mathbf{y}}
\end{equation}

Using the value of $F$ found earlier in this equation gives the final answer:
\begin{equation}
\mathbf{F} =\frac{k|qq_o|/2a^2}{\sqrt{2}}\hat{\mathbf{x}}+\frac{k|qq_o|/2a^2}{\sqrt{2}}\hat{\mathbf{y}} = kqq_o\frac{\hat{\mathbf{x}}+\hat{\mathbf{y}}}{a^22\sqrt{2}}
\end{equation}

The electric field is found by dividing both sides of this equation by $q_o$

\begin{equation}
\mathbf{E} = \frac{\mathbf{F}}{q_o} = kq\frac{\hat{\mathbf{x}}+\hat{\mathbf{y}}}{a^22\sqrt{2}}
\end{equation}

To get the direction of the field as the angle from the positive $x$-axis we use trigonometry:

\begin{equation}
    \tan(\theta) = \frac{1a}{1a}\;\Rightarrow\;\theta = 45^{\circ}
\end{equation}

{\bf Method 2}

Instead of assuming a point charge $q_o$ at $(x,y) = (a,a)$, we begin by computing the electric field using

\begin{equation}
E=|\mathbf{E}|=\frac{|\mathbf{F}|}{q_o} = \frac{k|q|}{d^2} = \frac{k|q|}{2a^2}
\end{equation}

It should be clear that we can follow the steps used in Method 1 to arrive at the same answer for $\mathbf{E}$

{\bf Method 3}

This method often leads to an answer more quickly than Method 1. Equation 21.7 of your textbook is

\begin{equation}
\mathbf{E}= kq\frac{\hat{\mathbf{r}}}{r^2}
\end{equation}

(The textbook uses a somewhat unconventional notation for a vector -- boldface font and an arrow - $\overrightarrow{\mathbf{E}}$. Usually $\mathbf{E}$ is used for type-written equations and $\overrightarrow{E}$ for hand-written equations; using both is redundant. In this tutorial, the conventional bold-face-only notation is used.)

The textbook does not note this, but you'll be able to solve problems even faster if you re-write this equation using the definition of a unit vector as a vector divided by its magnitude. Using $\hat{\mathbf{r}}=\mathbf{r}/r$ in the previous equation gives

\begin{equation}
\mathbf{E}= kq\frac{\hat{\mathbf{r}}}{r^2} = kq\frac{\mathbf{r}/r}{r^2} = kq\frac{\mathbf{r}}{r^3}
\end{equation}

To compute $\mathbf{E}$, we need only to draw the vector $\mathbf{r}$ that goes from $q$ to the point where we are computing the electric field. Based on the following diagram, it is $\mathbf{r}=a\hat{\mathbf{x}}+a\hat{\mathbf{y}}$. The magnitude of this vector is $|\mathbf{r}|=r=\sqrt{a^2+a^2}=\sqrt{2}a$. 

\input{figures/Example_1.1b.tex}

Plugging in the values of $r$ and $\mathbf{r}$ found earlier gives the same answer as before:

\begin{equation}
\mathbf{E}= kq\frac{\mathbf{r}}{r^3} = kq\frac{a\hat{\mathbf{x}}+a\hat{\mathbf{y}}}{a^3\sqrt{2}^3} = kq\frac{\hat{\mathbf{x}}+\hat{\mathbf{y}}}{a^22\sqrt{2}}
\end{equation}

To get the magnitude of the field, combine the vector components and can see that you get the same answer that you got for Method 2:

$
    |\mathbf{E}| = E = \sqrt{E_x^2 + E_y^2} = \sqrt{\left( \frac{kq}{a^22\sqrt{2}} \right)^2 + \left( \frac{kq}{a^22\sqrt{2}} \right)^2} = \sqrt{\frac{k^2q^2}{4a^4}} = \frac{k|q|}{2a^2}
$

\end{tcolorbox}
\clearpage

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white,title=Problem 1.1,breakable,height fill]
Compute the electric field at $(x,y) = (a,2a)$ due to a positive charge $q$ at the origin. Do this using both Method 2 (computing both magnitude and direction for the field) and Method 3 (computing the vector field and then showing it is the same as what you got for Method 2) in the example. Provide the same types of diagrams shown in the example.
\ifsolutions

{\bf Solution}

\begin{wrapfigure}{r}{0.35\textwidth}
  \begin{center}
    \input{Field_Lines/figures/Problem_1.1_Method_2}
  \end{center}
   \caption{Method 2 diagram}
\end{wrapfigure}
Method 2

The electric field magnitude is
$|\mathbf{E}| = E = \frac{k|q|}{d^2}$,
where $d$ is the separation distance and the direction is along the line that connects the two charges. $d=\sqrt{a^2+(2a)^2}=a\sqrt{5}$ and $q$ is positive so 

$|\mathbf{E}| = E = \frac{kq}{a\sqrt{5}^2}= \frac{kq}{5a^2}$

The $x$- and $y$- components of $\mathbf{E}$ are computed on the diagram. The result is
$\mathbf{E} = E_x\hat{\mathbf{x}}+E_y\hat{\mathbf{y}}={E}\cos\theta\hat{\mathbf{x}}+{E}\sin\theta\hat{\mathbf{y}}$

(A common question is if the $x$-component will always have $\cos$ and the $y$-component $\sin$. The answer is that it depends on how you define the angle. If we had defined $\theta$ to be the angle of $E$ with respect to the $y$-axis, the $x$-component would have a $\sin$ and the $y$-component a $\cos$.)

From the diagram, $\cos\theta = \frac{a}{d};\quad \sin\theta = \frac{2a}{d}$

After some algebra, $\mathbf{E}=\frac{kq}{a^25^{3/2}}(\xhat + 2\yhat)$

\vspace{-2\parskip}
\begin{center}\rule{10cm}{0.4pt}\end{center}

\begin{wrapfigure}{r}{0.35\textwidth}
    %\begin{center}
    \input{Field_Lines/figures/Problem_1.1_Method_3}
  %\end{center}
    \caption{Method 3 diagram}
\end{wrapfigure}

Method 3

$\mathbf{r}=a\xhat + 2a\yhat\qquad r=\sqrt{a^2+(2a)^2}=a\sqrt{5}\qquad\mathbf{E}=kq\frac{\mathbf{r}}{r^3}$

Plugging $\mathbf{r}$ and $r$ above into the equation for $\mathbf{E}$ gives

$\mathbf{E}=kq\frac{a\xhat + 2a\yhat}{[a\sqrt{5}]^3}$, which simplifies to $\mathbf{E}=\frac{kq}{a^25^{3/2}}(\xhat + 2\yhat)$. The magnitude is

$|\mathbf{E}|=E=\left|\frac{kq}{a^25^{3/2}}\right|\sqrt{1^2+2^2}=\frac{kq}{5a^2}$

Note that in computing $|\mathbf{E}|$, I used a short-cut. Instead of computing the magnitude of
$\frac{kq}{a^25^{3/2}}\xhat + \frac{2kq}{a^25^{3/2}}\yhat$ using $\sqrt{(\frac{kq}{a^25^{3/2}})^2 + (\frac{2kq}{a^25^{3/2}})^2}$, I factored out the common terms and computed the magnitude of $\frac{kq}{a^25^{3/2}}(\xhat + 2\yhat)$ using $|\frac{kq}{a^25^{3/2}}|\sqrt{1^2 + 2^2}$. The reason is that for any vector in the form, $\mathbf{A}=d(b\xhat+c\yhat)$, $|\mathbf{A}|=|d|\sqrt{b^2+c^2}$ (you should be able to show this; recall that $\sqrt{d^2}=|d|$). So, if you have a vector where there are common terms in the $\xhat$ and $\yhat$ components, factor the common terms out to save some writing.
\else
\\\\
\\[1cm]
\begin{tikzpicture}
\draw[step=1cm,black,thin] (0,0) grid (6,6);
\end{tikzpicture}
\\[4cm]
\begin{tikzpicture}
\draw[step=1cm,black,thin] (0,0) grid (6,6);
\end{tikzpicture}
\fi
\end{tcolorbox}

\clearpage

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white!100!white,title=Problem 1.2,height fill]
Compute the electric field at $(x,y) = (-a,2a)$ due to a negative charge $-q$ at the origin. Do this using both Method 2 and Method 3 in the example. Provide the same types of diagrams shown in the example.

\ifsolutions
{\bf Solution}

\begin{wrapfigure}{r}{0.35\textwidth}
  \begin{center}
    \input{Field_Lines/figures/Problem_1.2_Method_2}
  \end{center}
   \caption{Method 2 diagram}
\end{wrapfigure}
Method 2

The electric field magnitude is
$|\mathbf{E}| = E = \frac{k|q|}{d^2}$,
where $d$ is the separation distance and the direction is along the line that connects the two charges. $d=\sqrt{a^2+(2a)^2}=a\sqrt{5}$ 

$|\mathbf{E}| = E = \frac{k|-q|}{a\sqrt{5}^2}= \frac{kq}{5a^2}$

The magnitude is the same as the previous problem because the separation distance is the same.

The $x$- and $y$- components of $\mathbf{E}$ are computed on the diagram. The angle $\theta$ was chosen in such a way that $\sin$ appears in the $x$-component and $\cos$ appears in the $y$-component (see discussion in previous solution). The result is
$\mathbf{E} = E_x\hat{\mathbf{x}}+E_y\hat{\mathbf{y}}={E}\sin\theta\hat{\mathbf{x}}+{E}\cos\theta\hat{\mathbf{y}}$

From the diagram, $\cos\theta = \frac{2a}{d};\quad \sin\theta = \frac{a}{d}$

After some algebra, $\mathbf{E}=\frac{kq}{a^25^{3/2}}(\xhat - 2\yhat)$.

Compare this solution to the previous solution. The only change is the sign of the $\yhat$ component, which is consistent with the diagram. 

\begin{wrapfigure}{r}{0.35\textwidth}
  \begin{center}
    \input{Field_Lines/figures/Problem_1.2_Method_3}
  \end{center}
   \caption{Method 2 diagram}
\end{wrapfigure}
Method 3

$\mathbf{r}=-a\xhat + 2a\yhat\qquad r=\sqrt{a^2+(2a)^2}=a\sqrt{5}\qquad\mathbf{E}=kq\frac{\mathbf{r}}{r^3}$

Recall that $\mathbf{r}$ is the vector that goes from the charge causing the field to the point where we want to know the field. One does not account for the sign of the charge when determining this vector. Plugging $\mathbf{r}$ and $r$ above into the equation for $\mathbf{E}$ gives

$\mathbf{E}=k(-q)\frac{-a\xhat + 2a\yhat}{[a\sqrt{5}]^3}$

In the above, $-q$ was used because the $q$ and not $|q|$ is in the equation $\mathbf{E}=kq{\mathbf{r}}/{r^3}$. If you are ever in doubt about signs, use the diagram as a guide to check your answer. The last equation simplifies to

$\mathbf{E}=\frac{kq}{a^25^{3/2}}(\xhat - 2\yhat)$ 

The magnitude can be computed using the short-cut described in the previous problem:

$|\mathbf{E}|=E=\left|\frac{kq}{a^25^{3/2}}\right|\sqrt{1^2+2^2}=\frac{kq}{5a^2}$

\else
\\\\
\\[1cm]
\begin{tikzpicture}
\draw[step=1cm,black,thin] (0,0) grid (6,6);
\end{tikzpicture}
\\[4cm]
\begin{tikzpicture}
\draw[step=1cm,black,thin] (0,0) grid (6,6);
\end{tikzpicture}
\fi

\end{tcolorbox}