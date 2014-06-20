.. title: Integration of quadratic algebraic functions
.. slug: integration-of-quadratic-functions
.. date: 2014-06-12 14:06:06 UTC+03:00
.. tags: mathjax
.. link: 
.. description: Reduction of quadratic integrals
.. type: text

Integration of quadratic algebraic functions
============================================

Algebraic function fields
-------------------------

In algebraic geometry, an *algebraic function field* (of one variable)
over a field $K$
is a finite algebraic extension of the field $K(X)$ of rational
fractions with coefficients in $K$.

If $K$ is a subfield of $\\mathbf{C}$, elements of $K(X)$ may be
regarded as meromorphic functions in the extended complex plane
(*Riemann sphere*). These are called $K$-*rational functions*, or
*rational functions* if the role of $K$ is not important.

An element $f$ of an algebraic function field does not, in general,
correspond to a function in the complex plane even if $K$ is
a subfield of $\\mathbf{C}$. However, it satisfies an algebraic
equation
$$ f^n + g_1f^{n-1} + \\cdots + g_n = 0, $$ 
where the coefficients $g_i$ are in $K(X)$. Hence it can be
regarded as a "multi-valued function" whose values $y=f(x)$ are the
roots of the equation
$$ y^n + g_1(x)y^{n-1} + \\cdots + g_n(x) = 0 $$
at each point $x$ that is not a pole of any $g_i$.

In more exact terms, the elements of an algebraic function field over
a subfield of $\\mathbf{C}$ correspond to (single-valued) meromorphic
functions on a multi-leaved *Riemann surface* over Riemann sphere.

If $K$ is not a subfield of $\\mathbf{C}$, elements of an
algebraic function field may be regarded as functions on an
*algebraic curve*. (Not a surface; even a Riemann surface has
complex dimension one.)

Quadratic function fields
-------------------------
Assume now that $K$ is $\\mathbf{C}$ or one of its subfields, typically
finitely generated over $\\mathbf{Q}$. The field $K(X)$ will be
identified with the field of $K$-rational functions, denoted by
$K(x)$ where $x$ is the identity mapping of Riemann sphere.

Let $F$ be an algebraic extension of degree two of $K(x)$ and let $y$
be one of its elements not in $K(x)$. It then satisfies a quadratic
equation
$$ y^2 + f(x)y + g(x) = 0 \\quad(f,g\\in K(X)) $$
and generates the whole extension: $F=K(x,y)$.

If $f$ and $g$ are constants, $K'=K(y)$ is a quadratic extension of $K$
that can be embedded into $\\mathbf{C}$. The field $F$ then becomes
$K'(x)$, the field of $K'$-rational functions obtained from $K(X)$
by extension of the constant subfield.
We shall assume that $f$ and $g$ are not both constants. Then $F$ is 
a proper *quadratic function field*.

Solving the equation we obtain the formula
$$ y = -f(x)/2 + \\sqrt{d(x)}, $$
where $d = f^2/4 - g$, so $y$ can be replaced with $\\sqrt{d(x)}$ as
a generator: $F=K(x,\\sqrt{d(x)})$.

This may be further simplified. After writing
$$ d(x) = c\\prod_i (x - a_i)^{n_i}, $$
where the $a_i$ are complex numbers, the $n_i$ are integers, positive or
negative, and $c$ is a constant, we can omit $c$ and remove all even
powers of the factors $x - a_i$ leaving only a single factor of each of those
with odd exponent $n_i$. (The ground field $K$ may have to be extended.)

Hence we obtain a representation of the form $F = K(x,y)$, where
$ y = \\sqrt{p(x)}$ and
$$ p(x) = \\prod_{i=1}^n (x - a_i) $$
with distinct complex numbers $a_i$.

Reduction of integrals
----------------------

Consider now integrals of the form $\\int R(x,y)\\,dx$ where $R$ is
a rational fraction of two variables and $y^2 = p(x) = \\prod_i (x - a_i)$
as above. 
Since $(1,y)$ is a basis of $F$ over $K(x)$, we have a unique representation
$$ R(x,y) = f(x) + g(x)y\\quad (f,g \\in K(X)). $$
As is well known, this can be obtained explicitly as follows. First,
substituting $p(x)$ for $y^2$ in the numerator and denominator of $R(x,y)$,
we get
$$ R(x,y) = \\frac{P(x,y)}{Q(x,y)} = \\frac{P_0(x) + P_1(x)y}{Q_0(x) + 
Q_1(x)y}. $$ 
Then, after multiplying both the numerator and the denominator by
$Q_0(x) - Q_1(x)y$ the latter becomes $Q_0(x)^2 - Q_1(x)^2p(x)$,
independent of $y$ as desired.

As rational functions $f(x)$ can be integrated by elementary means we
are left with the integrand $g(x)y$. It is advantageous to write this
in the form $g(x)y^2/y = g(x)p(x)/y = f(x)/y$, because $y\\,dx$ is
always singular at infinity while $dx/y$ is regular if $\\deg(p) > 2$.

The integral $\\int dx/y$ is well defined even at the zeroes
$a_i$ of $p$. In fact, $dx/y$ is regular at these points.
This may be seen by differentiating $y^2 = p(x)$.
From $2y\\,dy = p'(x)\\,dx$ we obtain
$$ \\frac{dx}{y} = -\\frac{2\\,dy}{p'(x)}, $$
where $p'(a_i) = \\prod_{j\\ne i}(a_i - a_j) \\ne 0$ in the denominator.

One may also investigate the behavior of $dx/y$ by means of local
parameters. The square root of $\\prod_{j\\ne i} (x - a_j)$ has two
well-defined holomorphic branches in a neighborhood of $a_i$; let $h(x)$
be one of them. In terms of the parameter $t = \\sqrt{x-a_i}$ we then
have $x = t^2 + a_i$, and therefore
$$ \\frac{dx}{y} = \\frac{2t\\,dt}{y} = \\frac{2\\,dt}{h(t^2 + a_i)} $$
is regular at $t=0$.

If $n = \\deg(p)$ is even, the local nature of $dx/y$ at infinity may
be studied with the parameter substitution $x = 1/t$. Then
$$ \\frac{dx}{y} = \\frac{-t^{-2}dt}{t^{-n/2}\\sqrt{\\prod_i (1 - a_i t)}}, $$
whose both branches are regular at $t=0$ if $n/2 \\ge 2$. If $n$ is odd
one has to set $x = 1/t^2$. The result
$$ \\frac{dx}{y} = \\frac{-2t^{-3}dt}{t^{-n}\\sqrt{\\prod_i (1 - a_i t^2)}} $$
is regular provided $n \\ge 3$.

Basic forms of integrals
------------------------

To reduce the integral $\\int f(x)\\,dx/y$ further we split $f(x)$ into
rational fractions. The integral then becomes a linear combination of
integrals of the type
$$ I_k = \\int \\frac{x^kdx}{y} $$
and
$$ J_k(c) = \\int \\frac{dx}{(x-c)^ky} $$
for integral exponents $k$ and complex constants $c$. (For this it is
necessary to extend the ground field $K$ to include the $c$'s.)

To find relations among the $I_k$ we write $p(x)$ in the form $\\sum_{i=0}^n
b_i x^i$, where $b_n = 1$. It then follows from
$$ 2y\\,dy = d(y^2) = p'(x)\\,dx = \\sum_{i=0}^n ib_i x^{i-1}dx $$
that for each integer $m$
\\begin{align*} d(x^m y) & = mx^{m-1}p(x)\\,dx/y + x^m p'(x)\\,dx/2y \\\\
& = \\sum_{i=0}^n (m + i/2)b_i x^{m+i-1}dx/y.
\\end{align*}
Hence $$\\sum_{i=0}^n (m + i/2)b_i I_{m+i-1} = x^my$$ (up to a constant
of integration).

Setting $m = k - n + 1$ we see that $I_k$ can be reduced to the integrals
$I_i$ for $k-n \\le i < k$, and therefore each $I_k$ 
$(k \\ge n)$ is a linear combination of $I_0, I_1, \\ldots, I_{n-1}$ and
an element of the function field. Taking $m=0$ we see that even
$I_{n-1}$ can be expressed in terms of the remaing ones, since $mb_0=0$.

Turning to the integrals $J_k(c)$ we notice that the relations above
also apply to the case $c=0$ as $J_k(0) = I_{-k}$. If $b_0 \\ne 0$
and $k>1$, $I_{-k}$ reduces to the integrals $I_{-i}$ where $k-n \\le i
< k$. In particular, they all can be expressed in terms of $J_1(0) =
I_{-1}$ and $I_0, I_1, \\ldots, I_{n-2}$.
Further reduction of $J_1(0)$ is not possible as the coefficient
$mb_0$ of $I_{m-1}$ vanishes for $m=0$.

If $b_0=0$, $p$ has $0$ as a root, but $b_1\\ne 0$, since all roots are
simple by assumption. In addition, $m + 1/2\\ne 0$ for all integers $m$.
The integrals $I_{-k}$ can then be reduced as above along with $I_{-1}$
so that no $J_k(0)$ remains.

As to the integrals $J_k(c)$, the above reductions still apply after a
change of the coefficients. In fact,
expanding the powers in $p((x-c)+c)$ we obtain $p(x) = \\sum_{i=0}^n
c_i(x-c)^i$. It then follows that
$$ d((x-c)^m y) = \\sum_{i=0}^n (m + i/2)c_i (x-c)^{m+i-1}dx/y, $$
and therefore
$$ \\sum_{i=0}^n (m + i/2)c_i J_{-m-i+1}(c) = (x-c)^m y $$
(with a suitable choice of the constants of integration).
The integrals $J_k(c)$ $(k>1)$ can then be reduced to $J_1(c)$ and
the integrals
$$ J_{-i}(c) = \\int \\frac{(x-c)^i dx}{y} $$
for $0\\le i \\le n-2$.  
But these are obviously linear combinations of the integrals
$I_i$ for $0\\le i \\le n-2$. Moreover, if $p(c)=0$, even $J_1(c)$
can be expressed in terms of the latter integrals.

Summing up, the integrals $\\int f(x)\\,dx/y$ are linear combinations of
three types of terms.

1. $\\displaystyle I_k = \\int \\frac{x^k dx}{y}\\qquad (0\\le k \\le n-2)$

2. $\\displaystyle J_1(c) = \\int \\frac{dx}{(x-c)y}\\qquad
   (c\\ne a_1,\\ldots,a_n)$

3. Elements of the function field.

The three kinds of non-elementary integrals
-------------------------------------------

Consider now the singularities of the integrals $I_k$ $(0\\le k \\le n-2)$.
As was seen above, the only singularities of $x^k dx/y$ lie at infinity.
Assume, for the moment, that $n$ is even, and set $x = 1/t$. Then
$$\\frac{x^k dx}{y} = \\frac{-t^{-k-2}dt}{t^{-n/2}\\sqrt{\\prod_i(1-a_it)}},$$
which is regular at $t=0$ whenever $0 \\le k \\le n/2-2$.
Such everywhere regular integrals are called *integrals of the first kind*.

To understand the singularities of the integrals $I_k$ for $k > n/2-2$
one should note the two branches of the square root in
the denominator above. One of them has the value $1$ and the other one
the value $-1$ at $t=0$ corresponding to the two branches of $y$
at infinity asymptotically equal to $x^{n/2}$ and $-x^{n/2}$ respectively.

The integrand of $I_{n/2-1}$ has two simple poles at infinity, one at
each branch, with the residues $1$ and $-1$. Hence the integral has
singularities of logarithmic type. The integrands of $J_1(c)$ also have
simple poles with non-zero residues at $x=c$
and therefore logarithmic singularities.
These integrals are called *integrals of the third kind*.

Finally, there remain the integrals $I_k$ for $n/2 \\le k \\le n-2$.
Their integrands have poles of order $k - n/2 + 2$ at infinity.
They also have non-zero residues, in general. The values of these
residues at the two branches are opposite to each other, since they
come from the two opposite branches of the square root above.
(Besides, the sum of the residues is always zero quite generally.)
Hence there exist constants $c_k$ (the residue at one branch) such
that the integrands of $I_k - c_k I_{n/2-1}$ have no residues.
Therefore the singularities of these integrals are of polar type
with no logarithmic part. Such integrals are *integrals of the second kind*.

If $n$ is odd, there is only one branch of order two at infinity.
Setting $x = 1/t^2$, we obtain the local representation
$$ \\frac{x^kdx}{y} = \\frac{-2t^{-2k-3}dt}{t^{-n}
\\sqrt{\\prod_i (1-a_it^2)}}, $$
which has order $n-2k-3$ at $t=0$.

Hence $I_k$ is of the first kind for $0\\le k \\le (n-3)/2$. Moreover,
the Laurent series expansion of the integrand only has terms of even
exponent. Therefore all the integrals $I_k$ $((n-1)/2 \\le k \\le n-2)$ are
of the second kind, with no residues. The remaining integrals $J_1(c)$
are again of the third kind.

Genus
-----

The number of linearly independent integrals of the first kind is
$n/2 - 1$ if $n$ is even, and $(n-1)/2$ if $n$ is odd. It is remarkable
that the number of linearly independent integrals of the second kind
is the same. This number is known as the *genus* of the function field
and denoted customarily by $g$. Hence the degree of the polynomial $p$ 
defining the quadratic function field of genus $g$ is either
$2g + 2$ or $2g + 1$.

The difference between the even and odd cases is not essential. They
can readily be transformed into each other by a change of the
independent variable $x$. The genus is also preserved when the change of
variable is invertible (a fractional linear transformation).

Assume, for example, that $n$ is odd, and that  
$p(x) = \\prod_{i=0}^n (x - a_i)$
has non-zero constant term $c = -\\prod_i a_i$. If $z = 1/x$, then 
$w = yz^{(n+1)/2}/\\sqrt{c}$ satisfies the equation
$$ w^2 = q(z) = z\\prod_{i=1}^n (z - a_i^{-1}), $$
where the polynomial $q$ has even degree $n+1$. If $p(0)=0$, then the
same effect is achieved by the transformation $z = 1/(x-a)$ whenever
$p(a) \\ne 0$.

Conversely, if $n$ is even, then the transformation $z = 1/(x - a_i)$
takes the zero $a_i$ of $p$ to infinity leaving a polynomial of
odd degree $n-1$.

Fields of genus 0 are are called *rational*, since they can be reduced
to a field of rational fractions. In fact, if $n=2$, then
$$ y = \\sqrt{(x-a_1)(x-a_2)} = (x-a_2)\\sqrt{\\frac{x-a_1}{x-a_2}}. $$
Hence both $x$ and $y$ can be written as rational expressions of
a single variable $t = \\sqrt{(x-a_1)/(x-a_2)}$. 
($x$ is a fractional linear expression of $t^2$.)
In particular, all integrals are elementary.

Fields of genus 1 are *elliptic* function fields. Their integrals have been
studied extensively for over three hundred years. The name derives
from the integral giving the arc length of an ellipse. There is a
large body of literature on the subject including various standard forms.

Quadratic function fields of genus $g \\ge 2$ are called *hyperelliptic*.
Their theory is well developed but not standardized in the way of
the elliptic integrals.

Relations between integrals of the third kind
---------------------------------------------

We have seen that integrals of quadratic algebraic functions can be
expressed as linear combinations of three kinds of non-elementary integrals
together with algebraic functions and integrals of rational functions.
The latter include logarithms of pure rational functions; the logarithms of
algebraic functions appear to be missing.

That is not the case, however. Such logarithms can be expressed by means
of integrals of the third kind. Consider, for example, the function
$$ f = \\frac{y - d}{y + d}, $$
where $d$ is a constant. Its logarithmic differential may be written
$$ d\\log f = \\frac{dy}{y-d} - \\frac{dy}{y+d}
= \\frac{2d\\,dy}{y^2 - d^2} = \\frac{p'(x)\\,dx}{(p(x) - d^2)y} $$
using $2ydy = p'(x)dx$. Assuming that the roots $c_1,\\ldots,c_n$ of
$p - d^2$ are simple, we have the rational fraction expansion
$$ \\frac{p'(x)}{p(x) - d^2} = \\sum_{i=1}^n \\frac{e_i}{x - c_i} $$
for some constants $e_i$, since $\\deg(p') = n-1 < \\deg(p - d^2)$.
Hence we obtain the expression
$$ \\log f = \\sum_{i=1}^n e_i J_1(c_i). $$

The logarithms of other quadratic functions have similar expansions
possibly including logarithms of purely rational functions $f(x)$.
The existence of such representations implies that the integrals of
the third kind are not independent of each other. In particular,
it is hard to device a unique standard form for integrals
involving such components.

Elementary integrals
--------------------

We can make use of these results to study the possibility
of elementary integration of functions $f = R(x,y)$ in the quadratic
function field $F$, such as the combinations of integrals of the third
kind above, for example. These considerations are not specific to
quadratic fields, however. For the most part they apply to all
algebraic function fields.

First recall some definitions and notations.

Let $f$ be a function in $F$. It is defined and meromorphic
on a Riemann surface $S$ over the Riemann sphere (with two leaves
in the quadratic case).

If $t$ is a local parameter at a point $P$ of $S$, then $f$
has a unique Laurent expansion
$$ f = \\sum_{k\\ge n} a_k t^k $$
where $a_n\\ne 0$ at $P$. 

The integer $n$ is the *order* $\\mathrm{ord}_P(f)$ of $f$ at $P$.
If $n>0$, $P$ is a *zero* of $f$; if $n<0$, $P$ is a *pole* of
order $-n$ of $f$.

The *residue* $\\mathrm{res}_P f\\,dt$ of the differential $f\\,dt$
at $P$ is the coefficient $a_{-1}$ of the term of degree $-1$. It is
independent of the choice of the local parameter $t$.

The differential of $f$ has the expansion
$$ df = \\sum_{k\\ge n} ka_k t^{k-1}dt $$
with residue
$$ \\mathrm{res}_P\\,{df} = 0a_0 = 0 $$
The expansion of the logarithmic differential of $f$ begins with
$$ \\frac{df}{f} = \\frac{na_nt^{n-1}(1+\\ldots)}{a_nt^n(1+\\ldots)} 
= \\frac{n}{t} + \\ldots, $$
so it has a simple pole with residue
$$ \\mathrm{res}_P \\frac{df}{f} = n = \\mathrm{ord}_P(f). $$

Let us write $\\omega = R(x,y)\\,dx$ for brevity.
By `Liouville's theorem <http://en.wikipedia.org/wiki/
Liouville%27s_theorem_%28differential_algebra%29>`_,
if $\\int\\omega$ is elementary, there are
constants $c_1,\\ldots,c_r$ and functions $u_1,\\ldots,u_r,v$ in $F$
such that
$$ \\omega = \\sum_{k=1}^r c_k \\frac{du_k}{u_k} + dv. $$

This gives a necessary condition for elementary integration.
There remains the problem, how to recognize the possibility
of such a representation.

Assume first that $r$ is $1$, and set $u = u_1$, $c = c_1$.
The residues can then be computed:
$$ \\mathrm{res}_P\\,\\omega = c\\,\\mathrm{ord}_P(u). $$
They are all integral multiples of the single coefficient $c$.
In particular, the additive group $L$ generated by the residues of
$\\omega$ is 
a subgroup of $\\mathbf{Z}c$, the group of all integral multiples of $c$.

Hence $L$ is generated by $jc$ for some integer $j\\ge 1$ (the gcd of the
orders $\\mathrm{ord}_P(u)$ of $u$).
For each point $P$ there is then an integer $n_P$ such that
$n_P jc = c\\,\\mathrm{ord}_P(u)$, or simply
$$ \\mathrm{ord}_P(u) = jn_P. $$

This result is usually expressed more conveniently as follows.
The group of *divisors* of $S$ is the free abelian group generated
by the points of $S$. Its elements are (formal) sums $\\sum_{P\\in S}
n_P P$, where the $n_P$:s are integers of which only a finite number
are different from zero. In particular, the integers $n_P$ above are
the coefficients of a divisor $D$.

The divisor of a function $u$ is defined as
$$ \\mathrm{div}(u) = \\sum_P \\mathrm{ord}_P(u) P. $$
With this notation the above condition becomes
$$ \\mathrm{div}(u) = jD. $$
In other words, a multiple of $D$ is a *principal divisor*, i.e., the
divisor of a function.

Consider next the general case. Let again $L$ be the additive group
of complex numbers generated by the residues of $\\omega$. As it is
finitely generated and torsion free, it is a free abelian group with
a finite basis $(b_1,\\ldots,b_l)$. 

The additive group $M$ generated by the coefficients $c_k$ is also free
with a finite basis $(a_1,\\ldots,a_m)$.
Using the representation of Liouville's theorem,
we see that all the residues
$$ 
\\mathrm{res}_P\\,\\omega = \\sum_{k=1}^r c_k\\,\\mathrm{ord}_P(u_k)
$$
are in $M$.
Hence $L$ is a subgroup of $M$.
In particular, there exist integers $n_{ij}$ such that
$$ b_i = \\sum_{j=1}^m n_{ij}a_j\\qquad (1\\le i\\le l). $$

Putting the matrix $(n_{ij})$ in `Smith normal form <http://en.wikipedia.org/
wiki/Smith_normal_form>`_ we can find new bases $(a'_1,\\ldots,a'_m)$ and
$(b'_1,\\ldots,b'_l)$ such that $b'_i = j_ia'_i$ for some integers $j_i\\ge 1$
$(1\\le i\\le l)$.

Now, each $c_k$ is a linear combination of the basis elements $a'_i$
with integer coefficients
$$
c_k = \\sum_{i=1}^m e_{ki}a'_i\\qquad (1\\le k\\le r).
$$
Hence the residues of $\\omega$ may be expressed in the form
$$
\\mathrm{res}_P\\,\\omega = \\sum_{k=1}^r \\sum_{i=1}^m e_{ki}a'_i
\\mathrm{ord}_P(u_k) = \\sum_{i=1}^m a'_i\\mathrm{ord}_P(v'_i),
$$
where $v'_i = \\prod_{k=1}^r u_k^{e_{ki}}$ $(1\\le i\\le m)$.

On the other hand,
for each $P$ in $S$ there are unique
integers $n'_{i,P}$ $(1\\le i \\le l)$ such that
$$
\\mathrm{res}_P\\,\\omega = \\sum_{i=1}^l n'_{i,P} b'_i.
$$
Only a finite number of the $n'_{i,P}$ are non-zero, so
$$ D'_i = \\sum_P n'_{i,P} P $$
is a divisor for each $i$.
Using the equalities $b'_i = j_ia'_i$ we now see that for each $P$ and $i$
$$ \\mathrm{ord}_P(v'_i) = j_i n'_{i,P}, $$
since $(a'_i)$ is a basis. In terms of divisors this
may be written
$$ \\mathrm{div}(v'_i) = j_i\\,D'_i. $$
Hence, again, a multiple of each divisor $D'_i$ is a principal divisor.

These results on the divisors $D'_i$ are of limited use as such, because
they depend on the previous knowledge of the coefficients $c_k$.
However, it is not hard to see that the divisors derived from an
arbitrary basis of $L$, such as $(b_i)$ above, must have the same
properties.

To begin with, for each $P$ in $S$ there exist unique integers
$n_{i,P}$ $(1\\le i\\le l)$ such that
$$
\\mathrm{res}_P\\,\\omega = \\sum_{i=1}^l n_{i,P} b_i,
$$
and they define the divisors
$$ D_i = \\sum_P n_{i,P} P. $$

Expressing the basis $(b'_i)$ in terms of $(b_i)$ as
$$ b'_i = \\sum_{j=1}^l m_{ji} b_j $$
with integer coefficients $m_{ji}$, we find
$$
\\mathrm{res}_P\\,\\omega = \\sum_{i=1}^l \\sum_{j=1}^l n'_{i,P} m_{ji} b_j,
$$
and so
$$ n_{j,P} = \\sum_{i=1}^l m_{ji} n'_{i,P}\\quad (1\\le j\\le l). $$
This means that the divisors $D_i$ are linear combinations of the $D'_i$'s
$$ D_i = \\sum_{j=1}^l m_{ij} D'_j. $$

We have seen that a multiple $j_i D'_i$ of each divisor $D'_i$ is principal.
Since a multiple of a principal divisor is again principal
($n\\mathrm{div}(u) = \\mathrm{div}(u^n)$), 
we may replace each $j_i$ with their lcm $j$. Hence each $jD_i$ is a
linear combination of the principal divisors $jD'_i$.
But linear combinations of principal divisors are also principal
($n\\mathrm{div}(u) + m\\mathrm{div}(v) = \\mathrm{div}(u^n v^m)$).
Therefore we arrive at the following conclusion.

    A necessary condition for the integral $\\int \\omega$ to be
    elementary is that some multiples of the divisors $D_i$ derived
    from the residues as shown above are principal. 

This criterion appears to depend on an infinite number of tests, one
for each multiple $D_i, 2D_i, 3D_i,\\ldots$. This is where the
finite generation of the ground field $K$ comes to use. As indicated by
Risch (The solution of the problem of integration in finite terms,
Bull. Amer. Math. Soc. 76, 1970, 605-608) the ground field may be
replaced with a finite field for the tests, and then there are
only a finite number of multiples to be examined. (Of course, this
is purely algebraic, involving no analysis.) Hence
the criterion can be made effective, at least in theory.

Assume now that the conditions are fulfilled with the divisors $D_i$
associated to the basis $(b_i)$ satisfying $j_iD_i = \\mathrm{div}(v_i)$
for some functions $v_i$ and integers $j_i$. Then the differential
$$ \\omega' = \\sum_{i=1}^l \\frac{b_i}{j_i}\\frac{dv_i}{v_i} $$
of logarithmic type has the same residues as $\\omega$. Hence the difference
$\\omega - \\omega'$ has no residues.

Expressing it as a linear combination of the three kinds of integrals
and a function (as above in the quadratic case) we get no integrals
of the third kind. (They have been absorbed into $\\int\\omega'$.)
If no integrals of the first or second kind are left,
the integral $\\int \\omega$ is elementary; otherwise it is non-elementary.
