= Binomial and Taylor Series =

== Problems ==

=== Binomial Expansion ===
Your calculator does not have a square root button and you need to approximately calculate

\(1/(z^2+L^2)^{1/2}\)

for \(z=3\) and \(L=1\) and \(z=1\) and \(L=10\).  Write down an approximate values as a fraction (e.g., 99/44). <span style='background-color:yellow'>++1 if ''both'' correct.</span>

<div style="background-color:#E8E8E8">
In this problem, I expected you to know that \(\frac{1}{(1+\epsilon)^n}\simeq 1-n\epsilon\) for \(|\epsilon| << 1\); it is one of the formulas that you should just know.
Can re-write in two ways:
# \(\frac{1}{(z^2+L^2)^{1/2}} = \frac{1}{z}\frac{1}{(1+L^2/z^2)^{1/2}}\simeq \frac{1}{z}\left(1-\frac{L^2}{2z^2}\right)\) (approximation acceptable if \(L/z << 1\))
# \(\frac{1}{(z^2+L^2)^{1/2}} = \frac{1}{L}\frac{1}{(1+z^2/L^2)^{1/2}}\simeq \frac{1}{L}\left(1-\frac{z^2}{2L^2}\right)\) (approximation acceptable if \(z/L << 1\))

# \(z=3\) and \(L=1\): \(17/54\)
# \(z=1\) and \(L=10\): \(199/2000\)

Some students got an answer that was a negative number, was greater than one, or was close to one.  When you get an answer, always do a "sanity check".  For example, in the first problem, you are estimating \(1/\sqrt{10}\), which should be close to \(1/\sqrt{9}=1/3\).  If you answer is not close, something went wrong, and you should let me know that you noticed!
</div>

=== Binomial Expansion ===

Write down, from memory, the first two terms in the Taylor Series expansion of <math>1/(1+\epsilon)^n</math>.  

Describe the constraints, if any, on <math>\epsilon</math> for the two-term approximation give above to be accurate.

Answer:

<math>\frac{1}{(1+\epsilon)^n} \simeq 1 - n\epsilon</math>

<div style="background-color:yellow">Note: in an earlier version, I had a "+" sign instead of a "-" sign.  By inspection, I know this is incorrect - think about <math>1/(1+10)^1=0.1/(1+0.1)^1</math>.  The exact answer, <math>1/11</math>, should be less than 0.1 and not greater than 0.1.  The full Taylor Series expansion of [https://www.wolframalpha.com/input/?i=1%2F(1%2Bx)%5En+taylor+series this equation] can be found at [https://www.wolframalpha.com/ WolframAlpha].</div>

<math>\frac{}{}|\epsilon| << 1</math>

=== Binomail Expansion ===

Your calculator does not have a square root button and you need to approximately calculate

<math>1/(z^2+L^2)^{1/2}</math>

for <math>z=5</math> and <math>L=1</math>.  Write down an approximate value as a fraction (e.g., 99/44).

=== Binomail Expansion ===

For <math>z<<L</math>, write down the first two terms in the Taylor Series expansion approximation of

<math>1/(z^2+L^2)^{3/2}</math>

(To check your answer, pick values of <math>z</math> and <math>L</math> and use the original formula to compute the answer and compare it with the answer given by the first two terms of the Taylor Series expansion and verify that the Taylor Series expansion formula gets closer to the answer for the original formula as you increase <math>L</math> relative to <math>z</math>.)

----

For <math>z>>L</math>, write down the first two terms in the Taylor Series expansion approximation of

<math>1/(z^2+L^2)^{3/2}</math>

(To check your answer, follow a similar procedure as given above.)
