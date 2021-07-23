# Field Lines

https://tutorial.math.lamar.edu/classes/calciii/VectorFields.aspx

\subsection{Electric Field Lines}

In the examples in the previous section, the electric field at only one was point was computed. Suppose that we want to know about the electric field everywhere. One option is to draw many electric field vectors. At the page \url{https://www.geogebra.org/m/KMVuhygy}, the electric field vector is shown at many locations for four point charges and you can see that the vectors appear to form lines. These vectors were drawn so that they all have the same length even though the magnitude of the electric field is not the same at all locations. The reason for this is that electric field lines are determined by considering the direction of the electric field only. (If you select the ``Show Electric Field Magnitude and Direction" checkbox, you will see that the diagram becomes more difficult to understand because the lengths of the vectors vary so much.)

In this course, we will not compute exact field lines. Instead, we will use basic reasoning to determine the general trend of field lines using only knowledge of the general direction of the electric field at a given location. As a result, {\bf you do not need to calculate the exact magnitude of the electric field} as was done in the previous section. Instead, you will need to only determine the general direction within approximately $45^{\circ}$.

Because we do not consider the magnitude of the electric field when computing electric field lines, it may appear that information about the magnitude of the electric field is lost in a field line diagram. As you will see, it turns out that the {\it relative} strength of the electric field is reflected by how closely spaced the lines are.

% For solution, discuss this app:
% https://academo.org/demos/electric-field-line-simulator/

Electric field lines are computed with the following algorithm:

\begin{enumerate}
    \item Pick a starting point \((x,y)\) in space. Estimate the electric field vector direction there (ignore the magnitude).
    \item Take a small step along this vector to another point. Estimate the electric field direction at this point. Pay particular attention to how the direction changes relative to the previous direction. Connect this point to the previous point with a straight line.
    \item Repeat 2. until you step off the page, step into a charge, or reach a location where the electric field is zero.
    \item Repeat 1.-3. until you have as many electric field lines as desired.
\end{enumerate}

\clearpage

\begin{tcolorbox}[parbox=false,,colback=white,colframe=blue,title=Example 2.1,height fill]
Draw a field line starting at $(x,y)=(1,1)$ due to positive point charge $q$ at $(x,y)=(2,0)$.

Because there is only one charge, we know that the electric field will point along a line connecting the point $(x,y)=(1,1)$ with $(x,y)=(2,0)$. We know that the direction of the electric field at $(x,y)=(1,1)$ will be as shown by vector 1. because by convention, the electric field points in the direction that a positive charge would be pushed if placed there and we are given that $q$ is positive. If we take a step along vector 1., we arrive at point 2., which is located at $(x,y)=(0,2)$. The direction of the electric field will be the same. In the figure on the right, the vectors have been removed and replaced with a line.

\input{figures/Example_2.1.tex}

It is important to note that vectors 1, 2, and 3 are not the correct lengths. If we drew vectors with lengths that were consistent with the magnitude of the electric field, vector 1 would be much longer than vector 2, which would be much longer than vector 3.

In addition, keep in mind that the electric field line tells you the direction of force a test charge would feel if placed on the line. As noted in the textbook, a common misconception is that the field line is the path along which a charge will move if released at any point on the line. This is not true in general.
\end{tcolorbox}

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white!100!white,title=Problem 2.1,height fill]
\\[1em]
\begin{enumerate}
    \item In Example 2.1, how much larger is the magnitude of electric field vector 1 than electric field vector 2? (State the ratio of their magnitudes.)
    \ifsolutions
        \\\\
        {\bf Answer}
        $E_1=kq/2$, $E_2=kq/4$ $\Rightarrow$ $E_1/E_2=2$
    \fi
    \\[1cm]
    \item Draw a field line starting at (a.) $(x,y)=(2,1)$ and (b.) $(x,y)=(3,1)$ on the diagram in Example 2.1.
    \ifsolutions
        \\\\
        {\bf Answer}. Dotted lines were drawn to show that field lines for a single charge are straight lines that pass through the charge and the starting point. The vectors drawn on the left to help draw the field lines on the right are not the correct relative lengths for the reasons discussed earlier.
        \input{Field_Lines/figures/Problem_2.1_Solution}
    \fi
    \\[1cm]
    \item If the point charge in Example 2.1 was replaced with a charge of magnitude $10q$, how would field lines that you drew change?
    \ifsolutions
        \\\\
        {\bf Answer}: No change. You did not account for the magnitude of the charge when you drew the field lines. As a result, for this case, the field lines would not change. If, however, there were multiple charges and only one of the charges changed magnitudes, the field lines would change.
    \fi
    \\[1cm]
\end{enumerate}

Earlier it was stated that the closeness of the field lines tells you something about the relative magnitude of the electric field. You should be able to see this in your diagram - the three field lines drawn should be more closely spaced near $q$, which corresponds to where the the electric field magnitude is large.
\end{tcolorbox}

\clearpage

\begin{tcolorbox}[parbox=false,,colback=white,colframe=blue,title=Example 2.2,height fill]
Positive point charges of $+q$ are at $(x,y) = (-1m,0m)$ and $(x,y) = (+1m,0m)$. In the diagram below, the plot on the left shows the vectors (black arrows) that were drawn to help determine field lines which are shown in the plot on the right. Calculating each of the vectors is described below.

\begin{enumerate}
    \item $(x,y) = (-1.25,0)$ The force on a charge $q_o$ placed here due to the two charges will be directly to the left. The force due to the green charge will be smaller than the force due to the purple charge because the green charge is farther away. If you take a small step in along the direction of the resultant force vector to, say, $(x,y) = (-2,0)$, the force due to the two charges is still directly to the left. So the field line for this starting point should be a line going from $(x,y) = (-1.25,0)$ to negative infinity.
    \item $(x,y) = (+1.25,0)$ Similar to the previous, but the force and thus field is to the right.
    \item $(x,y) = (-0.5,0)$ the force due to the green charge is to the left and the force due to the purple charge is to the right. The net force (and thus field) is to the right because the force due to the purple charge is larger than the force due to the green charge. As one steps closer to the origin, the forces due to the two charges become nearly equal. At the origin, the force is zero and so the field line stops.
    \item $(x,y) = (+0.5,0)$ Similar to the previous but the net force and thus field is to the left.
    \item $(x,y) = (0,+0.5)$ The horizontal components of the force due to each charge are equal in magnitude but opposite in direction so they cancel leaving a net vertical force. A step upwards, the net force is still vertical so the field line continues upwards to infinity.
    \item $(x,y) = (1,1)$ The electric field vector at $(x,y) = (1,1)$ associated with each charge is shown. The exact magnitude has not been calculated - we only want to get an approximation of the field line. We know that the field due to the purple charge must be smaller than that of the green charge, which is reflected by the length of the green vector. The direction of the purple vector was determined by drawing a straight line from the purple charge to $(x,y) = (1,1)$, and a similar process was used for the green vector. The vector sum of the purple and green vectors will be closer to the green vector because it is larger. Computing the vector the same way a step along the black vector, the electric field is in approximately the same direction, but is tilted slightly to the right relative to the previous vector. (Challenge question: Can you explain why there is a slight tilt to the right without making any calculations?)
\end{enumerate}

\input{figures/Example_2.2.tex}

\end{tcolorbox}

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white,title=Problem 2.2]
On the same graph above, draw field lines for starting points of 
\\
\begin{enumerate}
\item $(x,y) = (-0.5,0.5)$
\item $(x,y) = (-0.5,-0.5)$
\item $(x,y) = (0.5,-0.5)$
\end{enumerate}

\ifsolutions
    {\bf Answer:} A test charge placed at point 1. will feel a force due to both charges, but the force due to the blue charge will be larger. The sum of the two forces will be approximately in the direction shown by the black vector. If one takes a small step along the black vector, the horizontal components of the electric field due to both charges becomes more equal. As a result, the field line becomes more vertical. Because field lines do not cross, the field line that starts at 1. will eventually become parallel to the vertical field line on the $y$-axis computed earlier.

    \input{Field_Lines/figures/Problem_2.2_Solution_Part_1}
        
    The field lines for 2. and 3. will have the same shape as that for 1. - the force magnitudes will be the same, but the direction will be different.
    
    
    \input{Field_Lines/figures/Problem_2.2_Solution_Part_2}
\fi

{\bf Hints:} The field lines will not be straight lines and will not cross other field lines. You need to reason out how the direction of the force on a charge at $q_o$ will change as you make small steps to determine how the lines curve.
\end{tcolorbox}

\clearpage

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white,title=Problem 2.3,height fill]
A negative point charge $-q$ is at $(x,y) = (-1,0)$ and a positive point charge $+q$ is at $(x,y) = (+1,0)$ meters. Draw an electric field line for the following starting points.
\\
\begin{enumerate}
    \item $(x,y) = (-1.25,0)$ 
    \item $(x,y) = (+1.25,0)$ 
    \item $(x,y) = (-0.5,0)$ 
    \item $(x,y) = (1,1)$
\end{enumerate}

\ifsolutions
{\bf Answer}: The force on a test charge placed at point 1. due to the blue charge will be to the right. The force on it due to the green charge will be to the left. The force due to the blue charge will be larger because point 1. is closer to it. Field lines stop when they hit a charge, a location where the field is zero, or go off the page. In this case, field line 1. runs into the blue charge. 

Similar arguments can be made to justify field lines that start on point 2. and 3.

A test charge placed at point 4. will experience a force in the direction shown by the black arrow. The electric field due to the negative charge points along the line connecting the negative charge to point 4. The electric field due to the positive charge will be upwards. The vector sum of these two fields will be in the direction shown by the black arrow, which is the vector sum of the blue and green arrows. When you take a small step along the black arrow, the line will bend to become more horizontal because the force due to the green charge will have a component to the left. When the field line passes $x=0$, the vertical electric field due to the two charges cancels; the electric field vectors for both charges is drawn at the point where the field line crosses the $y$-axis.
\input{Field_Lines/figures/Problem_2.3_Solution}
\else
\input{figures/Problem_2.3.tex}
\fi

\end{tcolorbox}

\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white,title=Problem 2.4,height fill]
Later in the semester, you will encounter a line of charge, which is created by placing many closely spaced charges along a line. Suppose 17 positive charges are placed along the line connecting $(x,y) = (-3.5, 0)$ and $(x,y) = (3.5, 0)$.

\begin{enumerate}
    \item For starting points that are not on the line that connects $(x,y) = (-3.5, 0)$ and $(x,y) = (3.5, 0)$, identify all starting points where drawing the electric field line will be a straight line and draw the lines with an arrow to indicate the electric field direction.
\end{enumerate}
\vspace{1cm}

\ifsolutions
    {\bf Answer}:
    As shown in the following figure, at any point on the $y$-axis, one can find a charge on the left half ($x<0$) of the line that has an equal an opposite horizontal electric field to a charge on the right half of the line ($x>0$). Because there are an equal number of charges to the left and to the right of the $y$-axis, the net electric field will be vertical. This argument can be repeated by considering the electric field due to the blue and green charges shown at a point on the $-y$-axis.

    \input{figures/Problem_2.4_Solution_a.tex}
    
    A test charge placed on the $x$-axis and to the left of the charges will have a net force to the left because the force on it from each charge on the line will be to the left. (Recall that by convention, a test charge is always positive). A test charge placed on the $x$-axis and to the right of the charges will have a net force to the right because the force from each charge on the line will be to the right.
    
    The final result:
    \input{figures/Problem_2.4_Solution_b.tex}
\else
    \input{figures/Problem_2.4.tex}
\fi

\end{tcolorbox}

\clearpage

\begin{tcolorbox}[parbox=false,,colback=white,colframe=blue,title=Example 2.3,height fill]
In the previous section, an algorithm was given for starting electric field lines. There are three additional facts that can be used to complete an electric field line diagram.

\begin{enumerate}
    \item Near a point charge, the electric field lines are radial. (Radial lines are made by drawing a straight line that passes through the point charge.) The reason for this is that when you are very close to a point charge, the electric field is dominated by that point charge - the electric field due to all other point charges is small in comparison.
    \item If you are far away enough from a collection of point charges, where the total charge is not zero, the electric field is approximately the same as if all of the charges were located at a single point.
    \item Electric field line do not cross.
\end{enumerate}

For the charge configuration in Example 2.2, we can use the above facts to extend the field lines drawn previously and sketch new field lines. Below, the electric field vectors used as a guide for drawing the field lines in Example 2.2 are shown on the left. On the right, dashed or dotted lines have been added to the previously drawn field lines based on the following arguments.

\begin{itemize}
    \item The gap between the horizontal lines and charges were filled in by using the fact that in this gap region, the electric field must still be horizontal.
    \item The dashed line a. was drawn based on the fact that it far away from the two point charges. This line was drawn as if the two positive point charges are at the origin. If you trace this line backwards along a straight line, the line will pass through the origin.
    \item The dashed line b. is points radially outward from the green point charge.
    \item The dotted line c. was drawn to connect lines a. and b.
    \item The dotted line d. was drawn by asking how the line it connects to must look as it approaches the green charge. As this line is traced backwards, it must become more and more radial, and when it reaches the green charge, it must be exactly radially outward from the green charge.
    \item The dotted line e. was drawn by using the fact that there must be a field line that traces outwards and lies between the other two lines that were already drawn.
\end{itemize}

\input{figures/Example_2.3.tex}

\end{tcolorbox}

\clearpage
 
\begin{tcolorbox}[parbox=false,colframe=black!50!black,colback=white,title=Problem 2.5 - Extra Credit,height fill]
\begin{enumerate}
    \item Use the facts mentioned in Example 2.3 to fill out the electric field diagram that you started in Problem 2.3. Your diagram should have at least 10 lines with arrows that start near the line of charge and continue outwards.
    \item Where are the field lines the straightest?
    \item If many, and an equal number of, charges were added to both ends of the existing charges (with the same spacing) how would the field lines in the region between $-3.5\le x\le 3.5$ change?
\end{enumerate}
\input{figures/Problem_2.4.tex}
\ifsolutions

    {\bf Answer}
    
    1. 

    \input{Field_Lines/figures/Problem_2.5_Solution}
    
    To see why the lines bend as shown, consider a point just above the charges and to the right of the $y$-axis as shown with an open circle. The charges with a blue line over them will produce a field that points in the $+y$ direction (there are an equal number of blue charges to the left of the open circle as to the right). The charges with a red line over them will produce a field having a smaller magnitude (because of their distance) and a component in the $+x$ direction. The net field is shown with a black arrow.
    
    2. The field lines will be the straightest near the center.
    
    3. As more charges are added to left and right, the curved field lines shown become straighter.
\fi
\end{tcolorbox}

\section{Review Problem}

\begin{tcolorbox}[enhanced,breakable,parbox=false,colframe=black!50!black,colback=white,title=Review Problem: Electric Field Lines,height fill]

\ifsolutions
\includegraphics[scale=0.15]{figures/field-lines2.png}
\else
\includegraphics[scale=0.35]{figures/field-lines.png}
\fi

1. In the above electric field line diagram, $q_L$ is the charge on the left and $q_R$ is the charge on the right. What are the signs of these two charges? Circle one of the following answers.
\begin{itemize}
    \item[a.] $q_L > 0$, $q_R > 0$
    \item[b.] $q_L > 0$, $q_R < 0$ \ifsolutions {\bf Answer} \fi
    \item[c.] $q_L < 0$, $q_R < 0$
    \item[d.] $q_L < 0$, $q_R > 0$
    \item[e.] Not enough information to determine.
\end{itemize}

2. What is the relationship between the magnitude of these two charges? Circle one of the following answers.
\begin{itemize}
    \item[a.] $|q_L| > |q_R|$ \ifsolutions {\bf Answer}. Explanation: If charge magnitudes were equal the total field at the open dot, which is on the line half-way between the charges, would be in the +x-direction (as it is for a dipole, where charges are equal and opposite). For $|q_L|$ larger than $|q_R|$, the total field is rotated in the +y-direction. Make sure you can use drawing and vector addition to explain this.\fi
    \item[b.] $|q_L| < |q_R|$
    \item[c.] $|q_L| = |q_R|$
    \item[d.] Not enough information to determine.
\end{itemize}

3. Briefly describe what these lines represent.
\ifsolutions
\\
\\
{\bf Answer}: The lines represent the direction of the force on a positive charge if placed at a point on the line. The lines do not generally represent the path that a charge will follow if released.
\else
\\[2cm]
\fi

\end{tcolorbox}

\end{document}
