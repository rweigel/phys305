## Problem

Plot field lines associated with the two starting points shown in the diagram for $\mathbf{A}=-\sin\phi\xhat + \cos\phi\yhat$. Draw the field lines until they encounter the $y$--axis.

## Example

Draw a field line starting at $(x,y)=(1,1)$ for the vector field $\mathbf{A}\equiv\mathbf{E}(r)/kQ = \boldsymbol{\hat{r}}/r^2$.

<img src="figures/Field_Lines_1a.svg"/>

It is important to note that vectors 1, 2, and 3 are not the correct lengths. If we drew vectors with lengths that were consistent with the magnitude of the electric field, vector 1 would be much longer than vector 2, which would be much longer than vector 3.

In the following figure, two additional field lines were drawn by following the same algorithm. In addition, dotted lines are shown -- if we had drawn lines by following the algorithm except stepping in the opposite direction, these field lines result.

<img src="figures/Field_Lines_1b.svg"/>

## Problem


## Problem

* In Example 2.1, how much larger is the magnitude of electric field vector 1 than electric field vector 2? (State the ratio of their magnitudes.)

    **Answer**: $E_1=kq/2$, $E_2=kq/4$ $\Rightarrow$ $E_1/E_2=2$

* Draw a field line starting at (a.) $(x,y)=(2,1)$ and (b.) $(x,y)=(3,1)$ on the diagram in Example 2.1.

    **Answer**: Dotted lines were drawn to show that field lines for a single charge are straight lines that pass through the charge and the starting point. The vectors drawn on the left to help draw the field lines on the right are not the correct relative lengths for the reasons discussed earlier.

    \input{Field_Lines/figures/Problem_2.1_Solution}

* If the point charge in Example 2.1 was replaced with a charge of magnitude $10q$, how would field lines that you drew change?

    **Answer**: No change. You did not account for the magnitude of the charge when you drew the field lines. As a result, for this case, the field lines would not change. If, however, there were multiple charges and only one of the charges changed magnitudes, the field lines would change.

Earlier it was stated that the closeness of the field lines tells you something about the relative magnitude of the electric field. You should be able to see this in your diagram - the three field lines drawn should be more closely spaced near $q$, which corresponds to where the the electric field magnitude is large.

## Example

Positive point charges of $+q$ are at $(x,y) = (-1m,0m)$ and $(x,y) = (+1m,0m)$. In the diagram below, the plot on the left shows the vectors (black arrows) that were drawn to help determine field lines which are shown in the plot on the right. Calculating each of the vectors is described below.

* $(x,y) = (-1.25,0)$ The force on a charge $q_o$ placed here due to the two charges will be directly to the left. The force due to the green charge will be smaller than the force due to the purple charge because the green charge is farther away. If you take a small step in along the direction of the resultant force vector to, say, $(x,y) = (-2,0)$, the force due to the two charges is still directly to the left. So the field line for this starting point should be a line going from $(x,y) = (-1.25,0)$ to negative infinity.

* $(x,y) = (+1.25,0)$ Similar to the previous, but the force and thus field is to the right.

* $(x,y) = (-0.5,0)$ the force due to the green charge is to the left and the force due to the purple charge is to the right. The net force (and thus field) is to the right because the force due to the purple charge is larger than the force due to the green charge. As one steps closer to the origin, the forces due to the two charges become nearly equal. At the origin, the force is zero and so the field line stops.

* $(x,y) = (+0.5,0)$ Similar to the previous but the net force and thus field is to the left.

* $(x,y) = (0,+0.5)$ The horizontal components of the force due to each charge are equal in magnitude but opposite in direction so they cancel leaving a net vertical force. A step upwards, the net force is still vertical so the field line continues upwards to infinity.

* $(x,y) = (1,1)$ The electric field vector at $(x,y) = (1,1)$ associated with each charge is shown. The exact magnitude has not been calculated - we only want to get an approximation of the field line. We know that the field due to the purple charge must be smaller than that of the green charge, which is reflected by the length of the green vector. The direction of the purple vector was determined by drawing a straight line from the purple charge to $(x,y) = (1,1)$, and a similar process was used for the green vector. The vector sum of the purple and green vectors will be closer to the green vector because it is larger. Computing the vector the same way a step along the black vector, the electric field is in approximately the same direction, but is tilted slightly to the right relative to the previous vector. (Challenge question: Can you explain why there is a slight tilt to the right without making any calculations?)

\input{figures/Example_2.2.tex}


## Problem

On the same graph above, draw field lines for starting points of 

1. $(x,y) = (-0.5,0.5)$
2. $(x,y) = (-0.5,-0.5)$
3. $(x,y) = (0.5,-0.5)$

**Hints**: The field lines will not be straight lines and will not cross other field lines. You need to reason out how the direction of the force on a charge at $q_o$ will change as you make small steps to determine how the lines curve.

**Answer**: A test charge placed at point 1. will feel a force due to both charges, but the force due to the blue charge will be larger. The sum of the two forces will be approximately in the direction shown by the black vector. If one takes a small step along the black vector, the horizontal components of the electric field due to both charges becomes more equal. As a result, the field line becomes more vertical. Because field lines do not cross, the field line that starts at 1. will eventually become parallel to the vertical field line on the $y$-axis computed earlier.

\input{Field_Lines/figures/Problem_2.2_Solution_Part_1}
        
The field lines for 2. and 3. will have the same shape as that for 1. - the force magnitudes will be the same, but the direction will be different.

\input{Field_Lines/figures/Problem_2.2_Solution_Part_2}


## Problem

A negative point charge $-q$ is at $(x,y) = (-1,0)$ and a positive point charge $+q$ is at $(x,y) = (+1,0)$ meters. Draw an electric field line for the following starting points.


* $(x,y) = (-1.25,0)$ 
* $(x,y) = (+1.25,0)$ 
* $(x,y) = (-0.5,0)$ 
* $(x,y) = (1,1)$

\input{figures/Problem_2.3.tex}

**Answer**: The force on a test charge placed at point 1. due to the blue charge will be to the right. The force on it due to the green charge will be to the left. The force due to the blue charge will be larger because point 1. is closer to it. Field lines stop when they hit a charge, a location where the field is zero, or go off the page. In this case, field line 1. runs into the blue charge. 

Similar arguments can be made to justify field lines that start on point 2. and 3.

A test charge placed at point 4. will experience a force in the direction shown by the black arrow. The electric field due to the negative charge points along the line connecting the negative charge to point 4. The electric field due to the positive charge will be upwards. The vector sum of these two fields will be in the direction shown by the black arrow, which is the vector sum of the blue and green arrows. When you take a small step along the black arrow, the line will bend to become more horizontal because the force due to the green charge will have a component to the left. When the field line passes $x=0$, the vertical electric field due to the two charges cancels; the electric field vectors for both charges is drawn at the point where the field line crosses the $y$-axis.

\input{Field_Lines/figures/Problem_2.3_Solution}

## Problem

Later in the semester, you will encounter a line of charge, which is created by placing many closely spaced charges along a line. Suppose 17 positive charges are placed along the line connecting $(x,y) = (-3.5, 0)$ and $(x,y) = (3.5, 0)$.


For starting points that are not on the line that connects $(x,y) = (-3.5, 0)$ and $(x,y) = (3.5, 0)$, identify all starting points where drawing the electric field line will be a straight line and draw the lines with an arrow to indicate the electric field direction.

\input{figures/Problem_2.4.tex}
    
**Answer**: As shown in the following figure, at any point on the $y$-axis, one can find a charge on the left half ($x<0$) of the line that has an equal an opposite horizontal electric field to a charge on the right half of the line ($x>0$). Because there are an equal number of charges to the left and to the right of the $y$-axis, the net electric field will be vertical. This argument can be repeated by considering the electric field due to the blue and green charges shown at a point on the $-y$-axis.

\input{figures/Problem_2.4_Solution_a.tex}
    
A test charge placed on the $x$-axis and to the left of the charges will have a net force to the left because the force on it from each charge on the line will be to the left. (Recall that by convention, a test charge is always positive). A test charge placed on the $x$-axis and to the right of the charges will have a net force to the right because the force from each charge on the line will be to the right.
    
The final result:

\input{figures/Problem_2.4_Solution_b.tex}

## Example

In the previous section, an algorithm was given for starting electric field lines. There are three additional facts that can be used to complete an electric field line diagram.


1. Near a point charge, the electric field lines are radial. (Radial lines are made by drawing a straight line that passes through the point charge.) The reason for this is that when you are very close to a point charge, the electric field is dominated by that point charge - the electric field due to all other point charges is small in comparison.
2. If you are far away enough from a collection of point charges, where the total charge is not zero, the electric field is approximately the same as if all of the charges were located at a single point.
3. Electric field line do not cross.

For the charge configuration in Example 2.2, we can use the above facts to extend the field lines drawn previously and sketch new field lines. Below, the electric field vectors used as a guide for drawing the field lines in Example 2.2 are shown on the left. On the right, dashed or dotted lines have been added to the previously drawn field lines based on the following arguments.

1. The gap between the horizontal lines and charges were filled in by using the fact that in this gap region, the electric field must still be horizontal.
2. The dashed line a. was drawn based on the fact that it far away from the two point charges. This line was drawn as if the two positive point charges are at the origin. If you trace this line backwards along a straight line, the line will pass through the origin.
3. The dashed line b. is points radially outward from the green point charge.
4. The dotted line c. was drawn to connect lines a. and b.
5. The dotted line d. was drawn by asking how the line it connects to must look as it approaches the green charge. As this line is traced backwards, it must become more and more radial, and when it reaches the green charge, it must be exactly radially outward from the green charge.
6. The dotted line e. was drawn by using the fact that there must be a field line that traces outwards and lies between the other two lines that were already drawn.

\input{figures/Example_2.3.tex}

## Problem

* Use the facts mentioned in Example 2.3 to fill out the electric field diagram that you started in Problem 2.3. Your diagram should have at least 10 lines with arrows that start near the line of charge and continue outwards.
* Where are the field lines the straightest?
* If many, and an equal number of, charges were added to both ends of the existing charges (with the same spacing) how would the field lines in the region between $-3.5\le x\le 3.5$ change?

\input{figures/Problem_2.4.tex}

**Answer**
    
1\. 

\input{Field_Lines/figures/Problem_2.5_Solution}
    
To see why the lines bend as shown, consider a point just above the charges and to the right of the $y$-axis as shown with an open circle. The charges with a blue line over them will produce a field that points in the $+y$ direction (there are an equal number of blue charges to the left of the open circle as to the right). The charges with a red line over them will produce a field having a smaller magnitude (because of their distance) and a component in the $+x$ direction. The net field is shown with a black arrow.
    
2\. The field lines will be the straightest near the center.
    
3\. As more charges are added to left and right, the curved field lines shown become straighter.

## Problem

\includegraphics[scale=0.15]{figures/field-lines2.png}

1. In the above electric field line diagram, $q_L$ is the charge on the left and $q_R$ is the charge on the right. What are the signs of these two charges? Circle one of the following answers.

   a. $q_L > 0$, $q_R > 0$

   b. $q_L > 0$, $q_R < 0$

   c. $q_L < 0$, $q_R < 0$

   d. $q_L < 0$, $q_R > 0$

   e. Not enough information to determine.

**Answer**: b.

2. What is the relationship between the magnitude of these two charges? Circle one of the following answers.

    a. $|q_L| > |q_R|$ 

    b. $|q_L| < |q_R|$

    c. $|q_L| = |q_R|$

    d. Not enough information to determine.

    **Answer**: If charge magnitudes were equal the total field at the open dot, which is on the line half-way between the charges, would be in the +x-direction (as it is for a dipole, where charges are equal and opposite). For $|q_L|$ larger than $|q_R|$, the total field is rotated in the +y-direction. Make sure you can use drawing and vector addition to explain this.

3. Briefly describe what these lines represent.

    **Answer**: The lines represent the direction of the force on a positive charge if placed at a point on the line. The lines do not generally represent the path that a charge will follow if released.

    \includegraphics[scale=0.35]{figures/field-lines.png}
