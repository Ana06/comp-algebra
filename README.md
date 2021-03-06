# Computational Algebra

Fundamental Computer Algebra algorithms implemented in Maple


## euclides.mws


**Euclides algorithm for Z, Zp, Z[i], Q[X], Fp[X] and Fq[X] with q=p^n.**


 Euclides algorithm calculates the gcd of two elements using the subtraction operation.
 
 
(*) For example, gcd(126,35):
126 = 3*35 + 21;
35   = 1*21 + 14;
21   = 1*14 + 7;
14   = 2*7 ;


Execution of examples that use mcd in euclides.mws:

![alt Euclides examples](https://github.com/Ana06/comp-algebra/blob/master/images/euclides.PNG "Euclides examples")


Execution of examples that use mcdq in euclides.mws (case Fq[X]). For example, we work in F16[X]:

![alt Euclides examples in Fq[X]](https://github.com/vicgalle/comp-algebra/blob/master/images/euclidesFq.PNG "Euclides examples in Fq[X]")


## extendedEuclides.mws

**Extended euclidean algorithm**

It computes the gcd of the given inputs and represents it as a linear combination, following the equalities (*) in the previous section in ascending order.

Some examples that use this function:

![alt Extended Euclides examples](https://github.com/vicgalle/comp-algebra/blob/master/images/extendedEuclides.PNG "Extended Euclides examples")


## additionProduct64.mws


**Addition and product in base 64.**

Numbers are unsigned and represented as integer lists. Take into consideration that the most significant position is the first in the right.

Execution of examples that use functions in additionProduct64.mws:

![alt Addition and product in base 64 examples](https://github.com/Ana06/comp-algebra/blob/master/images/additionProduct64.PNG "Addition and product in base 64 examples")
 
 
## chineseRemainder.mws

**Algorithm to compute the Chinese Remainder Theorem**

Given m0, ... , mr-1 integers and pairwise coprime, and v0, ... , vr-1 arbitrary integers, the algorithm obtains the unique f such that f = vi mod mi for all i.

Example that use the cr function. We want to find the unique two digit natural number which is 2 mod 11 and 7 mod 13. This can be possible due to the fact that the map X(f) = (f mod 11, f mod 13) = (2 mod 11, 7 mod 13) in Z_11 x Z_13 is surjective. In addition, Z_m is isomorph to Z_m0 x ... x Z_mr-1 where m = m0...mr_1 and its factors and pairwise coprime.

![alt Chinese remainder examples](https://github.com/vicgalle/comp-algebra/blob/master/images/chineseRemainder.PNG "Chinese remainder example")



## modularEuclides.mws

**Modular Euclides algorithm (big prime version)**

Input: polinomios primitivos f,g en Z[x] con deg(f)=n>=deg(g)>=1 y maxnorm(f), maxnorm(g) <= A.
Este algoritmo elige un primo grande p, calcula el mcd mod p y recupera el mcd en Z[X] desde el mcd en Fp[X]. Si falla, se repite con otro primo p.

Input: primitive polynomials f,g in Z[x] with deg(f)=n>=deg(g)>=1 and maxnorm(f), maxnorm(g) <= A.
This algorithm chooses a big prime p, computes the gcd mod p and then it obtains the gcd in Z[x]. If it fails, then it repeats using another prime p.

Examples that use the modeuc function.

![alt Modular euclides examples](https://github.com/vicgalle/comp-algebra/blob/master/images/modularEuclides.PNG "Modular euclides examples")
 

## inverseFq.mws

Inverse of an element in a finite field.

Given a, the algorithm computes b so that a*b = 1 in Fq. We apply the extended euclidean algorithm, using the property that
gcd(a,p) = 1 = s*a + t*p = s*a mod p

![alt Inverse examples](https://github.com/vicgalle/comp-algebra/blob/master/images/inverse.PNG "Inverse examples")


## polynomialIrreducibilityTest.mws

Finite field polynomial test of irreducibility.


We use that a polynomial f is irreducible if and only if:

(i) f divide x^(q^n)-x, y

(ii) gcd(x^(q^n/t)-x,f) = 1 fot all prime divisor t of n


Execution of examples that use functions in polynomialIrreducibilityTest.mws:

![alt Finite field polynomial test of irreducibility - repsquaring](https://github.com/Ana06/comp-algebra/blob/master/images/polynomialIrreducibilityTest-repsquaring.PNG "Finite field polynomial test of irreducibility examples - repsquaring")

![alt Finite field polynomial test of irreducibility - comp_modular](https://github.com/Ana06/comp-algebra/blob/master/images/polynomialIrreducibilityTest-comp_modular.PNG "Finite field polynomial test of irreducibility examples - comp_modular")

![alt Finite field polynomial test of irreducibility examples](https://github.com/Ana06/comp-algebra/blob/master/images/polynomialIrreducibilityTest.PNG "Finite field polynomial test of irreducibility examples")


## finiteFieldFactor.mws

Finite field factorization.

This algorithm computes the factors (with multiplicities) of a polynomial over Fp.

An example:

![alt Finite field factorization](https://github.com/vicgalle/comp-algebra/blob/master/images/finiteFieldFactorization.PNG "Finite field factorization")


## berlekamp.mws

Berlekamp's factorization algorithm.

Its input is a monic and square-free polynomial f in Fq[x] with q an odd power of a prime number.

An example:

![alt Berlekamp](https://github.com/vicgalle/comp-algebra/blob/master/images/berlekamp.PNG "Berlekamp")


## zassenhaus.mws

Zassenhaus factorization algorithm using the Hensel lifting.

Returns the factors of a polynomial f in Z[X] and with lc(f) > 0.

An example:

![alt Zassenhaus](https://github.com/vicgalle/comp-algebra/blob/master/images/zassenhaus.PNG "Zassenhaus")


## pollard.mws

This algorithm returns a proper factor of n (or "failure"). It uses the cycle detection trick by Floyd.
n must not be a composite number nor perfect power.

Some examples:

![alt Pollard](https://github.com/vicgalle/comp-algebra/blob/master/images/pollard.PNG "Pollard")



 
## Authors

This project has been developed by Ana María Martínez Gómez and Víctor Adolfo Gallego Alcalá.



## Licence

Code published under MIT License (see [LICENSE](LICENSE)).

