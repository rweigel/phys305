# Introduction

The Binomial Theorem is

$$(x+y)^m = \sum_{k=0}^m {m \choose k}x^{m-k}y^k$$

When $x=1$, it simplifies to

$$(1+y)^m = \sum_{k=0}^m {m \choose k}y^k$$

Written as a power series, it is

$$(1+y)^m = 1 + my + \frac{m(m-1)}{2}y^2 + ...$$

From this, it follows that

$$\frac{1}{(1+y)^n} = 1 - ny + \frac{n(n+1)}{2}y^2 + ...$$

(This equation can also be derived using the Taylor series expansion around $y=0$.)

In this course, we are going to use this expansion many times when $y$ is small. To emphasize this, $\delta$ will be used instead of $y$ as the variable. 

$$\frac{1}{(1+\delta)^n} = 1 - n\delta + \frac{n(n+1)}{2!}\delta^2- \frac{n(n+1)(n+2)}{3!}\delta^3...$$

The actual equation that you will most often use and should memorize is the truncated expansion to first order in $\delta$:

$$\boxed{\frac{1}{(1+\delta)^n} \simeq 1 - n\delta}$$

> "First--order in $\delta$" means that the highest power in the approximate answer is $\delta$, so only the $n\delta$ terms is kept as in the boxed equation above. "Second--order in $\delta$" means that the $n(n-1)\delta^2$ term is kept.

This equation becomes more and more accurate as $\delta \rightarrow 0$.

We will use this equation repeatedly to check our answers -- typically, we will be able to say, "For large $\delta$, I expect the answer to approach the answer to a similar to the answer for a simpler problem for which I know the answer". For example, if the problem is to compute the electric field for two positive charges $q$ at $x=\pm 1$, we expect the electric field to approach that for a charge of $2q$ at the origin, which is simply $2kq\hat{\mathbf{r}}/r^2$. This statement allows you to check your equation for the electric field -- if for large $r$ your equation matches the equation at the origin, you will be more confident that you solved the problem correctly.

To use this equation, you will typically need to rewrite an equation so that a term of this form appears. This is demonstrated in the following examples.

## Example -- ${1}/{12}$

Approximate $\frac{1}{12}$ using ${1}/{(1+\delta)^n} \simeq 1 - n\delta$.

**Answer**

$\displaystyle\frac{1}{12}=\frac{1}{10}\frac{1}{1+\frac{2}{10}}$

In this equation, we identify $n=1$ and $\delta = 2/10$, so

$\displaystyle\frac{1}{12}\simeq\frac{1}{10}\left(1-\frac{2}{10}\right)=\frac{1}{10}\frac{8}{10}=\frac{8}{100}=0.08$

This is close to the exact answer of $1/12=0.08\overline{3}$.

## Example -- $\{1}/{(3 + x)^2}$

Approximate $\{1}/{(3 + x)^2}$ using the binomial expansion to first order in $x$. Check your answer by using $x=0.1$ in the given equation and your approximation.

**Answer**:

Here $n=2$ and we can rewrite the equation by factoring out the $3$ from the term in the denominator to obtaiin a term of the form ${1}/{(1+\delta)^n}$

$\displaystyle\frac{1}{(3 + x)^2}=\frac{1}{3^2}\frac{1}{(1 + \frac{x}{3})^2}$

In the above, we identify $\delta=x/3$ and so

$\displaystyle\frac{1}{3^2}\frac{1}{(1 + \frac{x}{3})^2}\simeq\frac{1}{3^2}\left[1-2\left(\frac{x}{3}\right)\right]=\frac{1}{3^2}\left(1-\frac{2}{3}x\right)$

When $x=0.1$, the exact answer to four decimal places is $1/(3.1)^2=0.1041$. The approximate answer is $0.1037$

# Problems

## ${1}/{\sqrt{a + x}}$

Approximate ${1}/{\sqrt{a + x}}$ using the binomial expansion to first order in $x$. Check your answer by using plugging $a=1$ and $x=0.1$ into the given equation and your approximation. They should be close.

**Answer**:

To do the expansion, we need to write the equation in the form $1/(1+\delta)^n$, where $\delta \ll 1$.

$\displaystyle \frac{1}{\sqrt{a+x}}=\frac{1}{\sqrt{a(1+\frac{x}{a})}} = \frac{1}{a^{1/2}}\frac{1}{\left(1+\frac{x}{a}\right)^{1/2}}$

From this, we identify $\delta=x/a$ and $n=1/2$, so using $1/(1+\delta)^n\simeq 1-n\delta$ gives

$\displaystyle \frac{1}{\sqrt{a+x}}\simeq \frac{1}{\sqrt{a}}\left(1 - \frac{1}{2}\frac{x}{a}\right)$

## Approximating $\mathbf{E}$ Due to $q$ at $\pm b$

Find the equation for the electric field for two positive charges $q$ at $x=\pm b$. Verify that for large $r/b$, this equation approaches the equation for the electric field for $2q$ at the origin.

## Approximating $\mathbf{E}$ Due to $\pm q$ at $z=\pm x$

Two point charges $q$ are located at $x=\pm b$.

1. Find $\mathbf{E}$ on the $x$--axis in terms of $k$, $q$, $b$, and cartesian coordinates and unit vectors.
2. For $x\gg b$, write an equation for $\mathbf{E}$ in the form

   $\displaystyle \mathbf{E}=\left[B_o+\frac{B_1}{x} + \frac{B_2}{x^2} + \frac{B_3}{x^3}\right]\xhat$
   
   by using the binomial expansion formula with your answer from 1. The values for $B_0, ..., B_3$, if non--zero, should be written in terms of $k$, $q$, and $b$. The binomial expansion formula to first order in $\delta$ is $1/(1+\delta)^n\simeq 1-n\delta$, which applies for $\delta \ll 1$.
3. State at least one check that you made of your answer to 2.

**Answer**

1. Two ways of getting the answer are
   1. Write the field due to each charge in the regions $x\lt -b$, $-b\lt x\lt b$, and $x>b$ and manually insert the correct sign. For example, in the region $-b\lt x\lt b$, the charge at $+b$ has a field that points to the left, so $\mathbf{E}\_{+b}=-kq\xhat/(b-x)^2$; the charge at $-b$ has a field that points to the right, so $\mathbf{E}\_{-b}=+kq\xhat/(b-x)^2$. Many students only wrote the equation for $\mathbf{E}$ in one region, but the problem asked for $\mathbf{E}(x)$, which implies for all $x$.

   2. Use $\displaystyle kq\frac{\hat{\textbf{\char"0509}}}{\char"0509^2}=kq\frac{\mathbf{r}-\mathbf{r}'}{|\mathbf{r}-\mathbf{r}'|^3}$ with $\mathbf{r}'=\pm b\xhat$ and $\mathbf{r}=b\xhat$.

      $\displaystyle\mathbf{E}=\mathbf{E}\_{+b}+\mathbf{E}\_{-b}=kq\frac{x\xhat-b\xhat}{|x\xhat-b\xhat|^3}+kq\frac{x\xhat+b\xhat}{|x\xhat+b\xhat|^3}$

      This simplifies to

      $\displaystyle\mathbf{E}=\mathbf{E}\_{+b}+\mathbf{E}\_{-b}=kq\frac{(x-b)\xhat}{|x-b|^3}+kq\frac{(x+b)\xhat}{|x+b|^3}$

      where now the $|\cdot|$ operator corresponds to the abslute value. This equation gives the correct sign for the fields due to each charges in all three regions mentioned above.

2. For $x\gt b$, the absolute value signs can be dropped and cancellation gives 

  $\displaystyle\mathbf{E}=\mathbf{E}\_{+b}+\mathbf{E}\_{-b}=kq\xhat\left(\frac{1}{(x-b)^2}+\frac{1}{(x+b)^2}\right)$
      
  Factoring out $x$ gives

  $\displaystyle\mathbf{E}=\frac{kq}{x^2}\xhat\left(\frac{1}{(1-b/x)^2}+\frac{1}{(1+b/x)^2}\right)$
   
   Using $1/(1+\delta)^n\simeq 1-n\delta$ with $n=2$ and $\delta=-b/x$ and $\delta=b/x$ gives
   
   $\displaystyle\mathbf{E}\simeq\frac{kq}{x^2}\xhat\left[1+\frac{2b}{x}+\left(1-\frac{2b}{x}\right)\right]=\frac{2kq}{x^2}\xhat$

   From this, we conclude $B_0=B_1=B_3=0$ and $B_2=2kq$. (To verify that $B_3$ is zero, one could keep an additional term in the binomial expansion. In this case, $B_3$ is still zero because there is no $1/x^3$ term that results; there will be a postive $B_4$ term, which means that the approximation of $2q/x^2$ is an underestimate -- do you see why this would be?)

3. The answer to 2. corresponds to the field due to $2q$ at the origin, which is expected for $x\gg b$. In addition the direction is in the $+\xhat$ direction, which is expected if $q$ is positive.

## Approximating Line of Charge $\mathbf{E}$ I.

The electric field on the $z$--axis due to a line of charge $\lambda$ between $\pm L$ is

$$\mathbf{E}=\frac{2k\lambda L}{z}\left[\frac{1}{\sqrt{z^2+L^2}}\right]\zhat$$

Expand the term in square braces to first order in $z$. Note that $\sqrt{z^2}=|z|$.

## Approximating Line of Charge $\mathbf{E}$ II.

The exact answer for the electric field in the $y=0$ plane due to a line of charge with charge density $\lambda$ between $0$ and $L$ on the $x$--axis is

$$\mathbf{E} = \frac{k\lambda}{z}\left[\left(-1+\frac{z}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{x}} + \left(\frac{L}{\sqrt{z^2+L^2}}\right)\hat{\mathbf{z}}\right]$$

Expand the term in square braces to first order in $z$. Note that $\sqrt{z^2}=|z|$.
