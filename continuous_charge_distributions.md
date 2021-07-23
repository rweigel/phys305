\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage[letter, margin=1in]{geometry}

\usepackage{amssymb}

\usepackage{hyperref}
\hypersetup{
    colorlinks,
    urlbordercolor=blue,
    urlcolor=blue,
    pdfborderstyle={/S/U/W 1}
}

\usepackage[colorinlistoftodos]{todonotes}

% Header
\usepackage{fancyhdr}
\pagestyle{fancy}
\fancyhf{}
\lhead{Continuous Charge Distributions Tutorial}
\rhead{\thepage}
%\rhead{\leftmark}
%\renewcommand{\footrulewidth}{1pt}

% Paragraphs
% Don't indent paragraphs
\setlength{\parindent}{0ex}
% Space after paragraph
\setlength{\parskip}{1em}

% Colored boxes
\usepackage[most]{tcolorbox}

\usepackage{amsmath}
\newcommand{\ihat}{\boldsymbol {\hat \imath}}
\newcommand{\jhat}{\boldsymbol {\hat \jmath}}
\newcommand{\khat}{\boldsymbol {\hat \kmath}}
\newcommand{\xhat}{\mathbf {\hat x}}
\newcommand{\yhat}{\mathbf {\hat y}}

\newif\ifsolutions
\solutionstrue % Show solutions
%\solutionsfalse % Hide solutions

\newif\ifsolutions
\notestrue
%\notesfalse

\begin{document}
\section{Learning Objectives}

\subsection{Concepts}
At the end of this tutorial, you should be familiar with and understand:
\begin{itemize}
\item Unit vector notation
\item Lines of charge
\item Differential charge
\item Differential length
\item Electric field due to a differential charge
\end{itemize}
\subsection{Skills}
At the end of this tutorial, you should be able to:
\begin{itemize}
\item Use your understanding of electric field lines to explain the \textbf{relationship} between the magnitude of two charges
%\item Find the \textbf{position} at a point due to a line of charges
\item Find the \textbf{electric field} at a point due to a line of charges
\item Find the \textbf{linear charge density} due to a line of charges
\item Find the \textbf{total charge} from a given linear charge density
\item Find the differential \textbf{electric field}, $d\mathbf{E}$, due to a differential charge at an arbitrary location on a line
\item Integrate $d\mathbf{E}$ to find the \textbf{electric field}
\end{itemize}


\ifnotes
\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=red!100!blue,title=Instructor's note]
This tutorial was last edited on \today.

For the most up-to-date version of this tutorial, send Bob Weigel your OverLeaf username. The tutorial will then be accessible at \href{https://www.overleaf.com/project/5f2ca52a2b4ee3000122c48e}{OverLeaf}.

To hide the solutions and instructor's notes, comment out the line \texttt{solutionstrue} and \texttt{notestrue} at the start of this document.
\end{tcolorbox}
\else
\fi

\ifnotes
\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=red!100!blue,title=Instructor's note]
The following is a list of notes based on experience with this tutorial.

\begin{itemize}
    \item 
\end{itemize}


\end{tcolorbox}
\else
\fi

\clearpage


\section{Lines of Charge}

Previously, you have calculated the electric field due to a collection of point charges. The electric field at any point in space is the sum of the electric field due to all point charges.

Suppose that you wanted to know the electric field created by a plastic rod that was positively charged by rubbing it against fabric. The number of charges that you would need to account for is on the order of $\sim 10^{20}$. If you could do one calculation per second, computing the electric field due to each of the charges would take longer than the time since the Big Bang.

To allow for an answer in a finite amount of time, the approximation that charge is uniformly distributed along a line can be made. Consider 9 charges placed on a line as shown on the left-hand-side of the diagram below. To compute the electric field at the open circle, we would need to compute the electric field due to each of the 9 charges there. Graphically, we will make the approximation shown in the diagram. The 9 charges on the left are smeared out onto the line to form a continuous charge density.

\begin{center}
\input{Continuous_Charge_Distributions/figures/Figure_2_1}
\end{center}

Mathematically, the we are converting a sum to an integral. The electric field at the open circle is

$$
\mathbf{E}=k\frac{q_1}{r_1^2}\hat{\mathbf{r}}_1+k\frac{q_2}{r_2^2}\hat{\mathbf{r}}_2+...+k\frac{q_9}{r_9^2}\hat{\mathbf{r}}_9=\sum_{i=1}^Nk\frac{q_i}{r_i^2}\hat{\mathbf{r}}_i\simeq \int_{L} k\frac{dq}{r^2}\hat{\mathbf{r}}
$$

where the integral is over the line \(L\) occupied by the smeared charges. The advantage of using the integral approximation is that to get an answer, we only need to solve an integral - we do not need to compute electric field contribution for each point charge and then do a vector sum.

The integral equation 

$$\mathbf{E}=\int_{L} k\frac{dq}{r^2}\hat{\mathbf{r}}$$
\noindent
is not yet useful for solving problems because the line is not specified and neither is how $dq$ varies over the line. 

Before actually solving a problem using integration, we first need to introduce linear charge densities and how to re-write $dq$ in terms of it.

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.1.1 - Point Charge Electric Field Calculation,height fill]
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

\subsection{$\lambda$, $dq$, and $dl$}

Before doing integration, we need to write the differential charge $dq$ in terms of a differential length. The relationship is
$$
dq = \lambda(l) dl
$$

where $dl$ is a {\it generic} differential length and $l$ is a position on the line. Integration of $\lambda(l)\,dl$ over the length of the line gives the total charge on a line.

\begin{center}
\input{Continuous_Charge_Distributions/figures/Line_Differentials}
\end{center}

Most often, $\lambda(l)$ will be given as  constant and written as $\lambda$. In this case, the relationship between between the total charge $Q$ on a line of length $L$ and $\lambda$ is $Q=\lambda L$.

It was noted that $dl$ is a generic differential length. In order to do an integration, this generic length must be written in terms of a coordinate system (e.g., Cartesian, cylindrical, spherical). If the line of charge is along the $x$-axis, then $dl=dx$. If the line of charge is along the $y$-axis, then $dl=dy$ (see Example 21.10 of the textbook). If the line of charge is a circle of radius $b$ in the $x$-$y$ plane centered on the origin, then $dl=ds$, where $ds$ is a differential length along a circle (see Example 21.9 of the textbook).

For a circle, we could write $dl$ in terms of $dx$ and $dy$, but this leads to a more complicated integral. Recall from integration problems in calculus that one usually uses a coordinate system that makes the integration easy.

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.1.1 - Computing $\lambda$]

If the uniformly spaced point charges each with charge $q$ and shown by dots are smeared onto the line they are on, what is $\lambda$? 
Write your answer on the diagrams.

\begin{center}
\input{Continuous_Charge_Distributions/figures/charge_densities}
\end{center}
\ifsolutions
\\
{\bf Answer}: $9q/L$ (line) and 5$q/\pi a$ (arc)
\else
\fi
\end{tcolorbox}

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.1.2 - Computing Total Charge]

Along a line from $x=0$ to $x=a$, a total charge $Q$ is distributed non-uniformly such that $\lambda(x) = Cx^2$. What is the constant $C$ in terms of $Q$ and $a$?
\ifsolutions
\\
\\
{\bf Answer}: $dq = \lambda(x)dx\Rightarrow Q = \int_L \lambda(x)dx\Rightarrow Q = \int_0^a Cx^2dx\Rightarrow C=3Q/a^3$
\else
\\[2cm]
\fi
\end{tcolorbox}

\clearpage

\subsection{Computing d\mathbf{E}}

Prior to doing the integration

$$\mathbf{E}=\int_{L} k\frac{dq}{r^2}\hat{\mathbf{r}}$$

we first consider the electric field created by a single $dq$ at an arbitrary location on the line. The electric field due to this differential (infinitesimally small) charge is referred to as $d\mathbf{E}$:

$$
d\mathbf{E} =k\frac{dq}{r^2}\hat{\mathbf{r}}\quad\text{which has magnitude}\quad dE = k\frac{dq}{r^2}
$$

In principle, finding $d\mathbf{E}$ due to a $dq$ is as straightforward as finding $\mathbf{E}$ due to a $q$. However, in practice, it is often more challenging because we do not plug in numbers for the positions - we need to use variables because the equation will be integrated. 

\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=blue!100!blue,title=Example 2.2.1 - Computing $d\mathbf{E}$]

A total charge $Q$ is uniformly distributed along the line $-a\le x\le a$.

Find the electric field $d\mathbf{E}$ at a point $y_o$ on the positive \(y\)-axis due to a differential charge $dq$ at an arbitrary location $x$ on the line. Write your answer in terms of $x$, $dx$, $k$, and $\lambda$. Check that your equation for $d\mathbf{E}$ makes sense.

{\bf Answer}: This problem is similar to finding the electric field of a point charge at a given location. The primary difference is that instead of a point charge, we have a differential charge $dq$. In addition, we must find an equation that is valid when $dq$ is anywhere along the line $-a\le x\le a$.

{\bf Method 2}

\input{Continuous_Charge_Distributions/figures/Example_2_1_1}

With $\theta$ as defined in the diagram {\color{red} In original tutorial, $\sin$ and $\cos$ were swapped in the following equation, which is inconsistent with the equations on the diagram. Correct version below.}

$$d\mathbf{E}=-dE\sin\theta\ihat + dE\cos\theta\jhat$$

Also from the diagram,

$$\cos\theta=\frac{y_o}{r}=\frac{y_o}{\sqrt{x^2+y_o^2}}\qquad\sin\theta=\frac{x}{r}=\frac{x}{\sqrt{x^2+y_o^2}}$$

The magnitude of the field is

$$dE=k\frac{dq}{r^2}=k\frac{dq}{x^2+y_o^2}$$

Substitution of $dE$, $\cos\theta$, and $\sin\theta$ found above in

$$d\mathbf{E}=-dE\sin\theta\ihat + dE\cos\theta\jhat$$

gives

$$
\boxed{d\mathbf{E} = k\frac{dq}{\sqrt{x^2 + y_o^2}^3}(-x\ihat + y_o\jhat)
}$$

{\bf Method 3}

In this answer, Method 3 described on the Field Lines tutorial will be used. Methods 2 and 3 are equally valid, but Method 3 will work for more general problems than the problems given as examples in the textbook. (As a working engineer, mathematician, or scientist, you'll find that you nearly always solve problems in two different ways and compare answers; without a solution to check, this is one way that you can build confidence in your answer before you build something based on your answer.)

As in the previous tutorial, solving the problem will be easier if we use the definition of a unit vector as a vector divided by its magnitude. Using $\hat{\mathbf{r}}=\mathbf{r}/r$, we can write

$$
d\mathbf{E} = k\frac{dq}{r^2}\hat{\mathbf{r}}=k\frac{dq}{r^3}\mathbf{r}
$$

First, we need to find $\mathbf{r}$ and $r$ for a charge $dq$ at an arbitrary location on the line. In Method 3, we only need to know the vector $\mathbf{r}$ that is drawn from the charge to the point where we want to compute the electric field. This vector is shown on the following diagram.

\begin{center}
\input{Continuous_Charge_Distributions/figures/Line_of_charge}
\end{center}

Make sure that you understand why there is a negative sign in the $x$ component. The vector $\mathbf{r}$ drawn in the diagram above has a negative $x$ component. If $x$ is a positive number, say $x=1.5$, plugging it into the equation for $\mathbf{r}=-x\ihat+y_o\jhat$ gives a negative $x$ component for $\mathbf{r}$, which is consistent with vector drawn on the diagram below on the left. As a second check, suppose the $dq$ was chosen to be at a location $x < 0$, say $x=-1.5$. In this case, plugging $x=-1.5$ into $\mathbf{r}=-x\ihat+y_o\jhat$ gives a vector $\mathbf{r}$ that is consistent with the vector drawn on the diagram below on the right.

\begin{center}
\input{Continuous_Charge_Distributions/figures/Line_of_charge2}
\end{center}

We now have all of the information needed to find the electric field using

$$
d\mathbf{E} = k\frac{dq}{r^3}\mathbf{r}
$$

As found above, $\mathbf{r}=-x\ihat + y_o\jhat$ and its magnitude is $r=|\mathbf{r}|=\sqrt{(-x)^2 + y_o^2}=\sqrt{x^2 + y_o^2}$ and so

$$
\boxed{d\mathbf{E} = k\frac{dq}{\sqrt{x^2 + y_o^2}^3}(-x\ihat + y_o\jhat)
}$$

{\bf Checking the answer}

We can check this solution in by noting that if $x=0$ (for a $dq$ at the origin), we expect the electric field to be in the $+y$-direction. Plugging in $x=0$ gives 

$$
d\mathbf{E} = k\frac{dq}{\sqrt{y_o^2}^3}(y_o\jhat)
$$

which has only a positive vertical component. Another check that we can make is to confirm that the electric field is in $+y$-direction for all $x$ values. The $y$-component of the boxed solution for $d\mathbf{E}$ is

$$
dE_{y} = k\frac{dq}{\sqrt{x^2+y_o^2}^3}(y_o)
$$

which is positive for all values of $x$.


\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.2.1 - Computing d$\mathbf{E}$,height fill]
A total charge $Q$ is uniformly distributed along the line $-a\le x\le a$.

Find the electric field $d\mathbf{E}$ at a point $-y_o$ (where $y_o$ is a positive number) on the negative \(y\)-axis due to a differential charge $dq$ at an arbitrary location $x$ on the line. Write your answer in terms of $x$, $dx$, $y_o$, $k$, and $\lambda$. Check that your equation for $d\mathbf{E}$ makes sense.
\ifsolutions
\\
\\
{\bf Answer}:
$$
d\mathbf{E}=k\frac{\lambda dx}{\sqrt{x^2+y_o^2}^3}(-x\ihat-y_o\jhat)
$$
From a diagram similar to that used in the examples (not shown) when $x< 0$, expect $d\mathbf{E}$ to point South East. When $x> 0$ expect $d\mathbf{E}$ to point South West. When $x=0$, expect $d\mathbf{E}$ to point due South.
\fi
\end{tcolorbox}

\clearpage

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Problem 2.2.2 - Computing $d\mathbf{E}$,height fill]
A total charge $Q$ is uniformly distributed along the line $0\le y\le a$.

Find the electric field $d\mathbf{E}$ at a point $x_o$ on the positive $x$ axis. Write your answer in terms of $y$, $x_o$, $dy$, $k$, and $\lambda$. Check that your equation for $d\mathbf{E}$ makes sense.

\ifsolutions
\\
\\
{\bf Answer}:
$$
d\mathbf{E}=k\frac{\lambda dy}{\sqrt{x^2+y_o^2}^3}(x_o\ihat-y\jhat)
$$
From a diagram similar to that used in the examples (not shown) when $y> 0$, expect $d\mathbf{E}$ to point South East. When $x=0$ expect $d\mathbf{E}$ to point due East.
\fi

\end{tcolorbox}

\subsection{Integrating $\mathbf{dE}$}

\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=blue!100!blue,title=Example 2.3.1 - Integrating $d\mathbf{E}$]

Integrate $d\mathbf{E}$ found in Example 2.2.1.

First, we need to write $dq$ in terms of a differential length element. In general, $dq=\lambda dl$. In this problem, the differential length is the width of $dq$, which is along the $x$ direction, so $dl=dx$ and $dq = \lambda dx$. The equation of the electric field created by a single differential charge at an arbitrary location on the $x$-axis found previously was

$$
d\mathbf{E} = k\frac{\lambda dx}{(x^2 + y_o^2)^{3/2}}(-x\ihat + y_o\jhat)
$$

$$
\mathbf{E} = \int_{-a}^{a}k\lambda\frac{ -x\,dx}{(x^2 + y_o^2)^{3/2}}\ihat + \int_{-a}^{a}k\lambda\frac{ y_o\,dx}{(x^2 + y_o^2)^{3/2}}\jhat
$$

Before you attempt to do an integration, you should find ways to avoid doing integration. Based on the diagram, for every charge with $x<0$, there is a charge with $x>0$ that cancels its horizontal electric field. (Look back at the previous tutorial where this fact was also used.)

As a result, we know that the answer cannot have a $x$ component and the first integral must evaluate to zero. Mathematically, another way to show this is to use the fact that the integrand of the first integral, $-x/(x^2+y_o^2)^{3/2}$ is an odd function on the interval $x=[-a,a]$.

To get the final answer, we only need to do one integral:

$$
\mathbf{E} = \int_{-a}^{a}k\lambda\frac{ y_o\,dx}{(x^2 + y_o^2)^{3/2}}\jhat
$$

On exams, you will only be asked to set up the integral and it will be assumed that you can either do the integral or look it up. For the curious, the integration is given here.

The integral part of the right-hand-side is $E_y$

$$
E_y = \int_{-a}^{a}k\lambda\frac{y_o\,dx}{(x^2 + y_o^2)^{3/2}}
$$

This integral was given in Example 21.10 of the textbook (but with different variables). Using it gives

$$
E_y = k\frac{2a\lambda}{y_o\sqrt{a^2 + y_o^2}}
$$

Note that $2a\lamba$ is the total charge on the line. The answer in terms of the parameters given and $\mathbf{E}$ is

$$
\mathbf{E} = k\frac{Q}{y_o\sqrt{a^2 + y_o^2}}\jhat
$$

\end{tcolorbox}

\clearpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=black!100!black,title=Problem 2.3.1 - Checking Answer,height fill]
%\end{tcolorbox}

\clearpage

%\begin{tcolorbox}[enhanced,breakable,parbox=false,colback=white!0!white,colframe=black!100!black,title=Problem 2.3.2,height fill]

%Compute $\mathbf{E}$ at the center of quarter circle? Probably tutorial is long enough already.
%\end{tcolorbox}


\end{document}
