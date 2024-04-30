# Lecture VII. Taylor polynomial and Taylor series. Newton's method of solving nonlinear equations

## Abstract  

In this lecture we will introduce the **Taylor's formula** and **the Taylor polynomial** and we will give examples of their application for computation of approximate values of a function. We will also define a **MacLaurin series**, a **Taylor series** and find **MacLaurin's expansion** of some functions. Finally we will describe **Newton's method of approximate solving nonlinear equations**.

# 1. Taylor's formula, MacLaurin's formula

**Definition**  

A polynomial  
![](https://gakko.pjwstk.edu.pl/materialy/259/lec/an7/Image2847.gif)  

is called a **Taylor polynomial** of order k of a function f at a point x0, provided the function f has at x0 the derivative of order k.

In the case when x<sub>0</sub> = 0 a polynomial

![](https://gakko.pjwstk.edu.pl/materialy/259/lec/an7/Image2848.gif))

is called MacLaurin polynomial of order k of a function f.

Remarks

• The definition of a Taylor polynomial of order k of a function f at a point xo implies that the degree of this polynomial is at most k, but it can be smaller than k (if f (k)(x0) = 0).

• It is plain to see that a Taylor polynomial of order k of a function f at xo, is the only polynomial of order not greater than k such that



It means that if f is a polynomial of order n ≤ k then a Taylor polynomial of the function f at x0 is the function f itself (if n > k then f is not its own Taylor polynomial of order k).

It appears that for values of x close to x0 a number  is a good approximation of a number f (x). More accurate estimation of an error Rn(x) of this approximation is possible owing to the following theorem:

Theorem (Taylor's formula with the remainder of the Lagrange's form)

If a function f

(1) has the continuous derivative of order n -1 in an interval [x0, x],

(2) has the derivative of order n in an open interval (x0, x),

then there exists a point c ∈ (x0, x) such that





and Tx0(x) is a Taylor polynomial of order n -1.

The formula (*) is called a Taylor's formula with the nth remainder of the Lagrange's form, and the expression



the nth remainder of the Lagrange's form.

Remarks

• The Taylor's formula remains valid for an interval [x, x0] (then x0 ∈ (x, x0)).

In both cases: x0 > x and x0 < x can be described by a single formula



• For x0=0 the Taylor's formula takes on the form



and it is called a MacLaurin's formula with the nth reminder.

• Neglecting the remainder Rn(x) in the Taylor's formula, we obtain an approximation of a function f in a neighbourhood x0 by a polynomial of order (at most) n -1:



that is



Let us notice that the nth remainder in the Taylor's formula is simply a number



i.e., an error of the approximation of f (x) by 

By estimation of an error of such approximation, we understand a determination of a number a such that │Rn (x)│ ≤ a.

Examples

• We will write down a MacLaurin's formula with the 4th remainder R4 (x) for the function f (x)=cosx. We will also evaluate an error of the approximation of the function f by a MacLaurin polynomial of order 3 for ⎪x⎪ ≤ 0,3.

Since f (x)=cosx, f ' (x)=-sinx, f '' (x)=-cosx, f (3)(x)=sinx, f (4)(x)=cosx,

f (0)=1, f ' (0)=0, f '' (0)=-1, f (3) (0)=0, the MacLaurin's formula with R 4(x) for the function cosx is of the form



for some c lying between 0 and x. Thus the MacLaurin polynomial of order 3 for the function f (x)=cosx is of the form

.

In this case the degree of MacLaurin polynomial is smaller than its degree. What remains to be done is to evaluate an error of the approximation of cosx by



for ⎪ x⎪≤ 0,3. We have



The second last inequality corresponds to the fact that ⎪ cosc⎪≤ 1.

•  We will write down a Taylor's formula with the 4th remainder for the function f (x)=x /(x-3) at the point x0 = -2. We will find an approximated formula for a value of this function, which is obtained after neglecting the remainder R4 (x). We will also evaluate the error we make by application of this formula at the point -1,95 i.e., approximating the number f (-1,95) by T-2 (-1,95), where T-2 (x) is Taylor polynomial of the function f of order 3.





This implies that the Taylor's formula with the remainder R4 (x) for the function f at the point x0 is of the form





for some c lying between -2 and x.

The Taylor polynomial of order 3 of the function f at the point -2 is given by the formula

,

and thus the approximate formula for values of the function f for x close to -2 is given by



In particular:



An error of this approximation can be evaluated in the following way:



Since for c such that -2 < c < -1,95 we have | c - 3| ∈ (4,95, 5). Thus 4 < | c - 3|, and finally | c - 3| - 5 ≤ 1/45.

•  We will write down a Taylor's formula with the 3rd remainder for the function f (x) = x1/3 at the point x0=125. Then we will apply this formula for an approximation of the number 1241/3. We will also evaluate an error of this approximation.





Thus the Taylor's formula with R3 (x) for the function f at the point x0=125 is of the form



for some c lying between 125 and x.

The Taylor polynomial of order 2 of the function f at the point 125 is given by the formula



and thus the approximate formula for values of the function f for x close to 125 is given by



In particular for x = 124 we obtain:



An error of this approximation can be evaluated in the following way:



The last inequality follows from the fact that 124<c<125. Hence 4<1241/3<c1/3 which implies that

c-8/3<4-8.

•  We will find MacLaurin polynomials of order 3 and 4 as well as Taylor's formula with R5 (x) at the point -1 for the function f (x)=x4-x3+3x2+1.

We have f ' (x)=4x3-3x2+6x, f '' (x)=12x2-6x+6, f(3)(x)=24x-6, f(4)(x)=24, f(5)(x)=0, hence f (0)=1, f ' (0)=0, f'' (0)=6, f(3)(0)=-6, f(4)(0)=24. The MacLaurin polynomial of order 3 is of the form:



an of order 4:



The last identity illustrates the aforementioned fact that if a function f is a polynomial of degree n then every corresponding Taylor polynomial of order k ≥ n is the function f itself.

In order to determine the Taylor's formula with R5 (x) for the function f (x) at the point x0=1 we compute:

f (1)=4, f ' (1)=7, f '' (1)=12, f(3)(1)=18, f(4)(1)=24, which gives



since R5(x)=0 (by one of the remarks) (f (5)(x)=0). This means that we represented the function f as a linear combination of powers of the monomial x - 1.

Remark

Similarly, writing down a Taylor's formula with Rk(x) for any polynomial f of degree n ≤ k, at any point x0, we simply express this polynomial in terms of a linear combination of powers of the monomial x-x0.

•  We will write down a MacLaurin's formula with the nth remainder for the function f (x) = ex. We will evaluate an error of the approximation of the number e = f (1) by T0(1), where T0(x) is a Taylor polynomial of order n-1 of the function ex.

We have: f(x) = ex, f ' (x) = ex, f ' ' (x) = ex, ..., f(n-1) (x) = ex, f(n) (x) = ex, that is

f (0) = 1, f ' (0) = 1, f '' (0) = 1, ..., f(n-1) (0) = 1. Thus MacLaurins formula with the nth remainder of the function ex is of the form:



Let us evaluate an error of the approximation of the number e by the number

: .

In particular, for n = 5 the error does not exceed 1/40, whereas for n = 7 it is smaller than or equal to 1/1680.

Remark

• There are also another formulae describing the nth remainder Rn (x). For instance, if the assumptions of the theorem on Taylor polynomial with the remainder of the Lagrange's form are satisfied, then for every x∈ (a, b), there exists l ∈ (0,1) such that



The last expression is called an nth reminder of the Cauchy's form. The remainder of the Lagrange's form and the remainder of the Cauchy's form are different formulas denoting one number



Lagrange's form allows for much simpler (but often much weaker) estimation of an error of an approximation Rn (x) then the Cauchy's form does. According to this, we used here only the Lagrange's form of the remainder.
