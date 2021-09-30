# Satisfying 3 of the 4 BCs

Consider the boundary condition for an infinite conducting tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$
5. Find an equation that satisfies three of the four boundary conditions and has two unknown constants, one of them being $m$.
6. What is the constraint on the values of $m$ for this problem?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$$V(x,y)=C\sin\,mx\,\sinh\,my$$
or
$$V(x,y)=C\sin\,mx\,\left(e^{my}-e^{-my}\right)$$
where $C$ is a constant and $m = n\pi /w$ and $n$ is a positive integer.
|}

# Satisfying 2 of the 4 BCs

Consider the boundary condition for an infinite conducting tube of

1. $V(x=0,y) = V_o$ for $0\le y\le h$
2. $V(x=w,y) = V_o$  for $0\le y\le h$
3. $V(x,y=0) = 0$  for $0\le x\le w$
4. $V(x,y=h) = 0$  for $0\le x\le w$

This problem is similar to Example 3.4, with the difference being the location of the origin.

1. Find an equation that satisfies two of the four boundary conditions and has two unknown constants, one of them being $m$.
2. What is the constraint on the values of $m$ for this problem?

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
$(Ae^{mx} + Be^{-mx})\sin\,my$

satisfies the last two boundary conditions provided that $m=n\pi/h$, where $n$ is a positive integer.

----

As a prelude to future problems, note that you can relate $A$ and $B$ by using the first two boundary conditions

$V(x=0,y) = V_o = (Ae^{m0} + Be^{-m0})\sin\,my = (A + B)\sin\,my$

and

$V(x=w,y) = V_o = (Ae^{mw} + Be^{-mw})\sin\,my$

Combining these two equations gives $A=B(e^{-mw}-1)/(1-e^{mw})$

so that

$V(x,y) = (Ae^{mx} + Be^{-mx})(\sin\,my) = B(e^{mx}(e^{-mw}-1)/(1-e^{mw}) + e^{-mx})\sin\,my$

Although we have only satisfied two of the four boundary conditions, the equation 

(A) $V(x,y) = B(e^{mx}(e^{-mw}-1)/(1-e^{mw}) + e^{-mx})\sin\,my$

gives the same equation for the first two boundaries at $x=0$ and $x=w$ of 

$V(x=0,y) = V(x=w,y) = B\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my$, 

which can be shown by subtitution of $x=0$ and $x=w$ into (A) and simplifying.

When doing Fourier's trick, $x$ is replaced with its boundary value. So doing the Fourier Trick for the first boundary condition at $x=0$ using (A) would start with

$V(x=0,y) = V_o = B_1\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my + B_2\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my +...$

which is the same as the equation one would start with for the second boundary condition at $x=w$ using (A):

$V(x=w,y) = V_o = B_1\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my + B_2\left[(e^{-mw}-e^{mw})/(1-e^{mw})\right]\sin\,my+...$

Therefore, even though only the second two boundaries have been matched, the Fourier analysis needed to make the first two match will be identical. So Fourier's trick only needs to be applied once.  (The Fourier analysis involves finding values for $B_1,B_2,...$ such that the equality holds.)
|}


# Computing C's

Show that if the last boundary condition in Example 3.3 was $V(x=0,0\le y\le a)=V_o\,\sin(3\pi y/a)$ instead of $V(x=0,0\le y\le a)=V_o$, Fourier's Trick is not needed in order to find an equation that satisfies all four boundary conditions. (Could this last boundary be a conducting plate in this case?)

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
The equation that satisfied three of the boundary conditions in Example 3.3 was

$$V(x,y) = Ce^{-n\pi x/a}\sin\,n\pi y/a$$

To satisfy the last boundary condition, we would need values of $C$ and $n$ such that the following equality held true:

$$V(x=0,y)=V_o\,\sin(3\pi y/a) = Ce^{-n\pi 0/a}\sin\,n\pi y/a = C\sin\,n\pi y/a$$

for $0\le y\le a$. This equation is true if we select $C=V_o$ and $n=3$. One can then verify that

$$V(x,y) = V_oe^{-n\pi x/a}\sin\,3\pi y/a$$

satisfies all of the boundary conditions of Example 3.3 and Laplace's Equation. It does, and therefore we have a unique solution for the electric potential for the problem.
|}

# Computing C's


# Computing C's

Apply the three steps of Fourier's Trick to the equation you found for the problem in which the the boundary conditions were

1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$

to the point that you have an equation similar to the last equation in the Fourier's Trick description above (which was for the problem of Example 3.3<sup>*</sup>)

To this equation,
1. Evaluate the first integral on the right-hand side and choose the integration variable and integration limits so that the result of the integration is only non-zero if $l=1$;
2. Evaluate the second and third integrals on the right-hand-side using the same integration variable and limits and $l=1$;
3. Evaluate the integral on the left-hand side using the same integration variable and limits and $l=1$; and
4. Write down the value for $C_1$ that follows from this procedure.

Note that you can find the values for $C_2$ using the same procedure but using $l=2$ instead of $l=1$, but I am only asking for $C_1$.

<sup>*</sup> The equation for Example 3.3 was

$$\int_0^a V_o\,dy\,\sin\,l\pi y/a = C_1\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,\pi y/a \:+\: C_2\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,2\pi y/a \:+\: C_3\int_0^a dy\,\sin\,l\pi y/a\,e^{0}\sin\,3\pi y/a \:+\: ...$$
 
#### 2-D Cartesian

Consider the boundary conditions for an infinite conducting rectangular tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_0$ for $0\le x\le w$

1. Find an equation that satisfies three of the four boundary conditions and has two unknown constants, one of them being $m$. Justify your steps and indicate why some options for satisfying certain boundary conditions are rejected.
2. What is the constraint on the values of $m$?

For reference, $V(x,y) = \big(A\cos\,mx+B\sin\,mx\big)\big(Ce^{my}+De^{-my}\big)$ satisfies Laplace's Equation.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|

For the most part, students were able to get the correct answer. In many cases, it was not clear that there was an understanding for the motivation for each of the steps, which I gave in detail in a previous lecture. This is important - in more complex problems, one has to consider all possibilities when building a solution. I have given a full justification in this solution. I didn't expect this level of detail at this point from you, and in general, I only took off is something was wrong or not-quite-correct.

Procedure: Find values of constants $A,B,C,D,m$ in 

$V(x,y) = \big(A\cos\,mx+B\sin\,mx\big)\big(Ce^{my}+De^{-my}\big)$

so that three of the four boundary conditions are matched.

BC #1: 

$V(x=0,y) = 0 = \big(A\cos\,m0+B\sin\,m0\big)\big(Ce^{my}+De^{-my}\big) = A\big(Ce^{my}+De^{-my}\big)$

This can be satisfied in two ways: (1) if $A=0$ and (2) if $C=D=0$. If we accept (2), then our answer is $V(x,y)=0$ but then we have no hope of matching the last boundary condition. So $A=0$.

BC #2 (using $A=0$):

$V(x=w,y) = 0 = \big(B\sin\,mw\big)\big(Ce^{my}+De^{-my}\big) = B\sin\,mw\,\big(Ce^{my}+De^{-my}\big)$

This BC equation can be satisfied in three ways: if (1) $B=0$, (2) $\sin\,mw=0$, (3) $C=D=0$, and (4) $m=0$. If we accept (1), (3), or (4) then our answer is $V(x,y)=0$ but then we have no hope of matching the last boundary condition. So choose $\sin\,mw=0$, which is satisfied if $mw=n\pi$, where $n=...-2,-1,0,1,2,...$. If $n=0$, then solution is $V(x,y)=0$, so we need to omit it. The negative values are not needed (can't see that here, but would see it when doing Fourier's Trick).

BC #3 (using $A=0$ but not replacing $m$ with $n\pi/w$ so equation is shorter):

$V(x,y=0) = 0 = B\sin\,mx,\big(Ce^{m0}+De^{-m0}\big) = B\sin\,mx\,(C+D)$

$\sin\,mx$ is not zero for all $0\le x\le w$. So this BC equation can be satisfied only if (1) if $B=0$ or (2) $C=-D$. Reject (1) because solution would be $V(x,y)=0$.

In summary,

$V(x,y) = BC\sin(n\pi x/w)\big(e^{n\pi y/w} - e^{-n\pi y/w}\big)$, where $n=1,2,3,...$

or

$V(x,y) = 2BC\sin(n\pi x/w)\,\sinh{n\pi y/w}$, where $n=1,2,3,...$
|}

==== Tube with Variable Potential ====

Consider the boundary condition for an infinite conducting tube of
1. $V(x=0,y) = 0$ for $0\le y\le h$
2. $V(x=w,y) = 0$ for $0\le y\le h$
3. $V(x,y=0) = 0$ for $0\le x\le w$
4. $V(x,y=h) = V_o\sin(3\pi x/w)$ for $0\le x\le w$

1. Find an equation that satisfies the first three boundary conditions and has two unknown constants, one of them being $m$. Justify your steps and indicate why some options for satisfying certain boundary conditions are rejected.
2. What is the constraint on the values of $m$ for this problem?
3. Using the last boundary condition, find the two unknown constants.
4. The boundary with potential that varies as $V_o\sin(3\pi x/w)$ cannot be a conductor. Why?