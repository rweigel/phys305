The spheres are conductors, so the charges that appear on them will distribute uniformly on the surfaces and the distribution will be independent of $\theta$ and $\phi$. As a result, the potential will not depend on $\theta$ and $\phi$. In spherical coordinates, the Laplacian is 

$$\nabla^2V={ {1 \over r^{2}}{\partial  \over \partial r}\!\left(r^{2}{\partial V \over \partial r}\right)\!+\!{1 \over r^{2}\!\sin \theta }{\partial  \over \partial \theta }\!\left(\sin \theta {\partial V \over \partial \theta }\right)\!+\!{1 \over r^{2}\!\sin ^{2}\theta }{\partial ^{2}V \over \partial \varphi ^{2}}}$$

and the second two terms are zero. We need to solve

$$\nabla^2V={1 \over r^{2}}{\partial \over \partial r}\!\left(r^{2}{\partial V \over \partial r}\right)=0$$

Becuase $V$ depends only on $r$, we can replace the partial derivative with the total derivative

$$\nabla^2V={1 \over r^{2}}{d \over d r}\!\left(r^{2}{d V \over d r}\right)=0$$

subject to the boundary conditions

$$V(a)=V_o$$

$$V(b)=0$$

To solve the ODE, note that the following must hold

$$r^2{dV\over dr} = C_1$$

where $C_1$ is a constant.  Direct integration gives

$$V(r) = {C_1 \over r} + C_2$$

The two unknowns are solved for by using the boundary conditions

$$V(a) = V_o = {C_1 \over a} + C_2$$

$$V(b) = 0 = {C_1 \over b} + C_2$$

Solving for $C_1$ and $C_2$ gives

$$C_1 = {V_o \over \left({1\over a}-{1\over b}\right)}$$
$$C_2 = -{{V_o/b}\over{\left({1\over a}-{1\over b}\right)}}$$

and subsitution of these constants into $V(r) = {C_1 \over r} + C_2$ gives

$$V(r) = {V_o \over \left({1\over a}-{1\over b}\right)}{\left({1\over r}-{1\over b}\right)}$$

as a check of the algebraic steps, plug in $r=a$ and $r=b$ into this equation and verify that the boundary conditions used,

$$V(a)=V_o$$

$$V(b)=0$$

are satisfied.

Next, find the electric field using $\mathbf{E}=-\nabla V$. In spherical coordinates when $V$ depends only on $r$,

$$\nabla V={\partial V \over \partial r} \hat{\mathbf{r}}$$

giving

$$\mathbf{E}={V_o \over \left({1\over a}-{1\over b}\right)}{1\over r^2}\hat{\mathbf{r}}$$

This field points outward radially as expected given the potential on the inner surface is higher than that on the outer surface.

# 2-D


Try these problems before continuing to read.

----

### Laplace's Equation

1. Show that $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$.
2. Does $m$ need to be constrained in order for $\nabla^2 V=0$?

### Equivalence of forms (I) and (III)

Show that 

$ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $

can be written as 

$ V(x,y) = \big(A'e^{mx}+B'e^{-mx})(C\cos\,my+D\sin\,my\big) $

where $A'$ and $B'$ are constants that depend on $A$ and $B$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Starting with

$ f(x) = A\cosh\,mx+B\sinh\,mx $

replace the hyperbolic forms with their corresponding exponential forms, e.g.,

$\cosh\,mx=(1/2)(e^{mx}+e^{-mx})$ and $\sinh\,mx=(1/2)(e^{mx}-e^{-mx})$

giving

$ f(x) = (A/2)(e^{mx}+e^{-mx})+(B/2)(e^{mx}-e^{-mx})

or, after rearrangment,

$ f(x) = ((A+B)/2)e^{mx}+((A-B)/2)e^{-mx}$

or

$ f(x) = A'e^{mx}+B'e^{-mx}$ where $A'\equiv(A+B)/2$ and $B'\equiv(A-B)/2$.
|}

### Equivalence of forms (I) and (II)

Suppose that it is found that $m$ is imaginary, so that it can be written as $im'$, where $m'$ is a real constant and $i=\sqrt{-1}$. Show that forms (I) and (II) are equivalent.

----


In examples 3.3 and 3.4 of Griffiths, which are 2-D cartesian problems, he comes up with an equation for $V(x,y)$ that satisfies three of the four boundary conditions and has one unknown constant:

Example 3.3: 

$$V(x,y) = Ce^{-n\pi x/a}\sin(n\pi y/a)\,\,\mbox{with}\,\, n=1,2,...$$

Example 3.4:

$$V(x,y) = C\cosh(n\pi x/a)\sin(n\pi y/a)\,\,\mbox{with}\,\, n=1,2,...$$

The capital letter used for the leading constant can be $A,B,C,$ or $D$ or a combination of them (the product of constants is a constant); in the derivation of the above two equations, Griffiths notes that the $C$ in the final equations is not the same as the $C$ in the original equations (one of form (I)-(IV)). Technically it would be better to use something like $C'$ in the final equation to emphasize this point, but to keep the notation simple, he redefines $C$.

In examples 3.3 and 3.4, Griffiths happens to choose

1. The best form (I)-(IV) to start with
2. The best order of boundary conditions to address

The problem students have with solving other problems is when they don't happen to choose the "best" way to get to the answer. In the following, I go through examples 3.3 and 3.4 by addressing the boundary conditions in a different order than Griffiths did. The examples highlight many of the actual complications one will encounter if the "best" order of addressing the boundary conditions is not selected.

### Example 3.3

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = 0$ - Griffiths starts by supposing $V_o(y)$ but then assumes $V_o$
4. $V\rightarrow 0$ as $x\rightarrow\infty$

Griffiths starts with form (III)

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

and boundary condition 4. Here I am going to start with form (III) but boundary condition 1.


'''BC 1.''': $V = 0$ when $y = 0$

Plugging $V = 0$ and $y = 0$ into

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

gives

$$0 = \big(Ae^{mx}+Be^{-mx})(C\cos\,m0+D\sin\,m0\big)$$

or

$$0 = \big(Ae^{mx}+Be^{-mx}\big)C$$

There are two ways for this equation to be true for any $x \ge 0$

1. Both $A$ and $B$ are zero. We reject this option because then form (III) reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $C=0$ is the remaining option.

This leaves

$$V(x,y) = \big(Ae^{mx}+Be^{-mx}\big)D\sin\,my$$

or, defining $A'=AD$ and $B'=BD$,

$$V(x,y) = \big(A'e^{mx}+B'e^{-mx}\big)\sin\,my$$


'''BC 2.''': $V = 0$ when $y = a$

Plugging these values into the equation we left off with after addressing boundary condition 1. gives

$$0 = \big(A'e^{mx}+B'e^{-mx}\big)\sin\,ma$$

There are two ways for this equation to be true for any $x \ge 0$:

1. Both $A'$ and $B'$ are zero. We reject this option because then form (III) reduces to $V(x,y)=0$, which satisfies Laplace's equation, but can't satisfy all of the boundary conditions.
2. $\sin\,ma=0$ is only the remaining option.

The only way for $\sin\,ma=0$ to be true generally is if $ma=0,\pm \pi,\pm 2\pi,...$. 

From this we conclude

$m=\frac{n\pi}{a}$ with $n$ constrained to be $0, \pm 1, \pm 2, ...$

This leaves

$$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin\,n\pi y/a$$

Inspection of this equation allows us to reject the possibility that $n=0$ - if $n=0$, this equation reduces to $V(x,y)=0$, which cannot satisfy all of the boundary conditions.

'''BC 3.''': $V = V_o$ when $x = 0$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi 0/a}+B'e^{-n\pi 0/a}\big)\sin\,n\pi y/a$$

or, because $e^0=1$,

$$V_o = \big(A'+B'\big)\sin\,n\pi y/a$$

There is only one way for this equation to be true for any $0\le y\le a$: 

$$A'+B'=V_o$$

This equation is true but is not immediately useful for simplifying our equation for $V(x,y)$. So we move on to the next boundary condition.


'''BC 4.''': $V = 0$ when $x \rightarrow \infty$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi \infty/a}+B'e^{-n\pi \infty/a}\big)\sin\,n\pi y/a$$

or, because $e^{-\infty}=0$,

$$V_o = \big(A'e^{n\pi \infty/a}\big)\sin\,n\pi y/a$$

There is only one way for this equation to be true: $A'=0$. (There is technically a mathematical issue that I am ignoring because zero times infinity is indeterminate; there is a way around this issue, but for now, it is not important and I'll use this dubious notation.)

Recall that the result from addressing boundary condition 3. was

$$A'+B'=V_o$$

Given that $A'=0$ is required to satisfy boundary condition 4., we conclude

$$B'=V_o$$

This leaves

$$V(x,y) = B'e^{-n\pi x/a}\sin\,n\pi y/a$$

which the same as equations 3.28 and 3.29 with one exception. In the above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $B'$ is computed.

The final step is determining $B'$. This would seem to be impossible because boundary condition 3., $V = V_o$ when $x = 0$, gives

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(n\pi y/a)$$

and this equation needs to hold true for any $0\le y \le a$. To see that finding a $B'$ that satisfies this is impossible, suppose $y=a/2$ and $n=1$, then we have

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(\pi/2)$$

Giving $B'=V_o$. Now suppose $y=a/4$ and $n=1$, then

$$V_o = B'e^{-n\pi 0/a}\sin\,n\pi y/a=B'\sin(\pi/4)$$

Giving $B'=\sqrt{2}V_o$. One can repeat this for all allowed values and $n$ and you will come to the conclusion that there is no value of $B'$ that can satisfy this equation for any $0\le y \le a$.

To satisfy this last boundary condition, superposition and "Fourier's Trick" is needed.

### Example 3.4

The boundary conditions are

1. $V = 0$ when $y = 0$
2. $V = 0$ when $y = a$
3. $V = V_o$ when $x = b$
4. $V = V_o$ when $x = -b$

Griffiths starts with form (III)

$$V(x,y) = \big(Ae^{mx}+Be^{-mx})(C\cos\,my+D\sin\,my\big)$$

and a symmetry argument to conclude $A=B$. Here I am going to start with form (III) but boundary condition 1. In addition, I won't make use of the symmetry argument as it does not apply generally.


'''BC 1.''': $V = 0$ when $y = 0$

'''BC 2.''': $V = 0$ when $y = 0$

The starting form (III) and boundary conditions 1. and 2. are identical to that from example 3.3, so we can re-use the result concluded from addressing them:

$$V(x,y) = \big(A'e^{n\pi x/a}+B'e^{-n\pi x/a}\big)\sin\,n\pi y/a$$

with $n$ constrained to be $0, \pm 1, \pm 2, ...$.

'''BC 3.''': $V = V_o$ when $x = b$

Plugging these values into the equation we left off with after addressing boundary condition 2. gives

$$V_o = \big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin\,n\pi y/a$$

Now we seem stuck. How does one constrain $A'$ and $B') for this equation to hold? We have one other boundary condition to address, so hopefully it provides some insight.

'''BC 4.''': $V = V_o$ when $x = -b$

$$V_o = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

Here we would seem to be stuck again. However, notice that the equation here can be combined with that from BC 4:

$$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)\sin\,n\pi y/a=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

the $\sin\,n\pi y/a$ term appears on both sides and can be dropped, leaving

$$\big(A'e^{n\pi b/a}+B'e^{-n\pi b/a}\big)=\big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)$$

which simplifies to

$$A'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)=B'\big(e^{n\pi b/a}-e^{-n\pi b/a}\big)$$

The terms in parentheses are identical, so we conclude

$$A'=B'$$

Therefore, the equation we ended with when addressing boundary condition 2.,

$$V(x,y) = \big(A'e^{-n\pi b/a}+B'e^{n\pi b/a}\big)\sin\,n\pi y/a$$

simplifies to

$$V(x,y) = A'\big(e^{-n\pi x/a}+e^{n\pi x/a}\big)\sin\,n\pi y/a$$

This can be futher simplified using the definition $\cosh\,z=(e^z+e^{-z})/2$

$$V(x,y) = 2A'\cosh(n\pi x/a)\sin(n\pi y/a)$$

As with example 3.3, we ended up with one constant that is still unknown. This equation is equivalent to Griffiths' 3.41 if $2A'$ is replaced with a constant labeled $C$.

As was the case in my solution to example 3.3, above I concluded $n$ could be $\pm 1, \pm 2, ...$ where Griffiths concludes $n=1, 2, 3, ...$. The equivalence of these two conclusions will be shown when $A'$ is computed.

### Problems

#### Laplace's Equation

1. Show that $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$.
2. Does $m$ need to be constrained in order for $\nabla^2 V=0$?
3. Where does the equation $\nabla^2V = 0$ come from?
4. Why don't we use the equation $V(x,y)=\int kdq/|\mathbf{r}-\mathbf{r}'|$ to solve for the potential as we did for some problems in chapter 2 and for the image problems in chapter 3.2?
5. $ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $ satisfies $\nabla^2V = \partial^2 V/\partial x^2 + \partial^2 V/\partial y^2 = 0$. Does $m$ need to be constrained in order for $\nabla^2 V=0$?

#### Equivalence of forms (I) and (III)

Show that 

$ V(x,y) = \big(A\cosh\,mx+B\sinh\,mx\big)\big(C\cos\,my+D\sin\,my\big) $

can be written as 

$ V(x,y) = \big(A'e^{mx}+B'e^{-mx})(C\cos\,my+D\sin\,my\big) $

where $A'$ and $B'$ are constants that depend on $A$ and $B$.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
Starting with

$ V(x,y) = A\cosh\,mx+B\sinh\,mx $

replace the hyperbolic forms with their corresponding exponential forms, e.g.,

$\cosh\,mx=(1/2)(e^{mx}+e^{-mx})$ and $\sinh\,mx=(1/2)(e^{mx}-e^{-mx})$

giving

$ V(x,y) = (A/2)(e^{mx}+e^{-mx})+(B/2)(e^{mx}-e^{-mx})

or, after rearrangment,

$ V(x,y) = ((A+B)/2)e^{mx}+((A-B)/2)e^{-mx}$

or

$ V(x,y) = A'e^{mx}+B'e^{-mx}$ where $A'\equiv(A+B)/2$ and $B'\equiv(A-B)/2$.
|}

==== Satisfying 3 of the 4 BCs ====

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

#### Satisfying 2 of the 4 BCs

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

==== Series sum ====

Show that

$V(x,y) = C_1e^{-\pi x/a}\sin\,\pi y/a + C_2e^{-2\pi x/a}\sin\,2\pi y/a + C_3e^{-3\pi x/a}\sin\,3\pi y/a + ... $

satisfies Laplace's equation and the boundary conditions of Example 3.3.

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
From a previous problem, we know that equations of the form (I)-(IV) satisfy Laplace's Equation, but explicitly,

$$\nabla^2 \big(C_ne^{-n\pi x/a}\sin\,n\pi y/a\big) = $$

$$C_n\sin\,n\pi y/a\frac{\partial^2 e^{-n\pi x/a}}{\partial x^2} + C_ne^{-n\pi x/a}\frac{\partial^2 \sin\,n\pi y/a}{\partial y^2} = $$

$$C_n \sin\,n\pi y/a\,(-n\pi x/a)(-n\pi x/a)e^{-n\pi x/a} + C_n e^{-n\pi x/a}(n\pi x/a)(-n\pi x/a)\sin\,n\pi y/a = 0$$

|}

==== Integrals ====

1. Show that $\int_0^\pi \sin\,2x\,\sin\,x\,dx$ = 0. Note that you can solve this without doing any calculations.  Just plot $\sin\,x$ and $\sin\,2x$ and think about the area under the curve for their product.
2. Show that $\int_0^\pi \sin\,nx\,\sin\,lx\,dx$ = 0 if $l\ne n$ by explicitly evaluating the integral.
3. Compute $\int_0^\pi \sin\,nx\,\sin\,nx\,dx$

{| class="wikitable collapsible collapsed"
! align="left" |&nbsp;Answer
|-
|
The motivation for giving you these problems is to help you remember that

$\int_0^\pi \sin\,nx\,\sin\,lx\,dx = 0$ if $l\ne n$

which is important for Fourier sum problems.

A way to reason this out without doing a calculation is by considering a plot of the integrand $\sin\,nx\,\sin\,lx$ over the interval $0\le x\le \pi$ by plotting two $\sin$ curves for $l\ne m$ and thinking about what the product of the curves looks like; over half interval the product will be positive and over the other half of the interval it will be negative, so the integral will be zero.

When $l=m$, the integrand is $\sin^2\,mx$, which is always positive, so its integral is not zero over any interval of $x$.
|}

#### Computing C's

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

#### Computing C's

The three steps of Fourier's Trick given above applied to the equation from Example 3.3:

$V_o = C_1e^{-\pi x/a}\sin\,\pi y/a + C_2e^{-2\pi x/a}\sin\,2\pi y/a + C_3e^{-3\pi x/a}\sin\,3\pi y/a + ... $

gives

(A) $$\int_0^a V_ody\,\sin\,l\pi y/a = C_1\int_0^a dy\,\sin\,l\pi y/a\,e^{-\pi x/a}\sin\,\pi y/a \:+\: C_2\int_0^a dy\,\sin\,l\pi y/a\,e^{-2\pi x/a}\sin\,2\pi y/a \:+\: C_3\int_0^a dy\,\sin\,l\pi y/a\,e^{-3\pi x/a}\sin\,3\pi y/a \:+\: ...$$

Show the details of the steps needed to get the same values of $C_1, C_2,$ and $C_3$ as Griffiths, which are

*$C_1=\frac{4V_o}{1\pi}$
*$C_2=0$
*$C_3=\frac{4V_o}{3\pi}$

To do this, set $l=1$ in (A) and evaluate all of the integrals. This will give you $C_1$. Next, set $l=2$ in (A) and evaluate all of the integrals.  This will give you $C_2$.
Finally, set $l=3$ in (A) and evaluate all of the integrals to get $C_3$.

Do you see why the limits of integration were chosen to be $[0,a]$? If not, try finding $C_1,C_2,C_3$ using integration limits of $[0,a/3]$.

==== Computing C's ====

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