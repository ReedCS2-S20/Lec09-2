# Lecture 09-2: INTRO TO OO IN C++ (CONT'D)

This lecture folder continues the complex number work in Lecture 09-1,
giving more details about the code's features. It only includes the
PDF of my lecture slides `slides.pdf`. Take a look at the `samples`
folder from the last lecture.

I also offer an (optional) exercise for Friday:

## Exercise

Devise a `Rational` class that represents a rational number, one that
is a quotient of two integers. Each `Rational` object should have two
attributes, both of type `int`, its `nunerator` and its
`denominator`. It should have several constructors:

• `Rational()`: constructs a rational number with numerator
`0` and denominator `1`.  

• `Rational(int n)`: constructs a rational number with numerator
`n` and denominator `1`.  

• `Rational(int n, int d)`: constructs a rational number with numerator
`n` and denominator `d`.  You can assume that `d` is a positive integer.

In addition, it should support the following methods:

• `Rational plus(Rational that)`: returns the sum of `this` and
`that`. Recall that the sum of two fractions is given by:

     n1     n2    n1*d2 + n2*d1
    ---- + ---- = -------------
     d1     d2        d1*d2

• `Rational minus()`: returns the negation of `this`, i.e. the
  additive inverse.

        n    -n
     - --- = ---
        d     d

• `Rational minus(Rational that)`: returns the difference between
`this` and `that`.  Use the `plus` and `minus` methods just described
to write this one.

• `Rational times(Rational that)`: returns the product of `this` and
  `that`.  Recall that

     n1     n2    n1*n2
    ---- * ---- = -----
     d1     d2    d1*d2


• `std::string to_string()`: return a string representing the `Rational`.
Some example rational strings include:

    -2
    2/3
    0
    -2/3
    42
    137/17

### BONUS:

• `Rational reciprocal()`: returns a `Rational` that is the
multiplicative inverse of `this`. Write it so that the new `Rational`
instance has a positive denominator. This means that you should flip
the signs of both the numerator and the denominator, if the numerator
of `this` was negative. You can assume that the numerator of `this` is
not 0.

         n     d
    1 / --- = ---
         d     n

• `Rational div(Rational that)`: division of this `this` by `that`.
Use the `times` and `reciprocal` methods just described to write this
one.

• **compute the GCD**  
This class works more cleanly if you reduce the numerator and
denominator so that they have no common divisor. You could write a
helper function that computes the greatest common divisor of two
integers and use it in the general constructor, dividing the suggested
numerator and denominator each by their greatest common divisor.
