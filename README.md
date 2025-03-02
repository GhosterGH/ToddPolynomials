# ToddPolynomials
Data for Todd polynomials up to degree 40

The 'data' directory contains 40 files named T1.txt through T40.txt,
each containing data for one Todd polynomial.

Each file consists simply of integers with spaces and newlines as separators.

The first line is the denominator of the polynomial.

The remaining lines encode the numerator of the polynomial, one term per line.

The first integer on a line is the coefficient of the term.

The remaining integers on a line are pairs (i, p) specifying c_i^p factors in the term.

Example:

T5.txt is

```
720
-1 1 4
4 1 2 2 1
3 2 2
1 1 1 3 1
-1 4 1
```

This encodes the polynomial

```
1/720 ( -c_1^4 + 4 c_1^2 c_2 + 3 c_2^2 + c_1 c_3 - c_4 )
```

The minimalist formatting is intentional in order to be CAS-agnostic.

The polynomials were computed in *Mathematica* using an algorithm suggested by Richard Stanley in [this MathOverflow question](https://mathoverflow.net/questions/488555/reference-request-a-list-of-todd-polynomials). The computation took about 10 minutes.
