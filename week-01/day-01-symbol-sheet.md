# Week 1 — Day 1
## Sets/Functions as Maps, Measurements/Errors, Mole Concept

## 0. Plan Row

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Sets and functions as maps | Complete |
| Physics | Measurement, dimensions, and error propagation | Complete |
| Chemistry | Moles, stoichiometry, and concentration | Complete |
| Required output | Symbol sheet | Complete |

---

# 1. Mathematics Detailed Reading
## Sets and Functions as Maps

A **set** is a well-defined collection of objects. The objects are called elements. Examples:

$$
A=\{1,2,3,4\},\qquad B=\{x:x\in\mathbb R, x>0\}
$$

A function is a map from one set to another:

$$
f:A\to B
$$

This notation is more precise than just writing a formula. A complete function has three parts:

$$
\boxed{\text{function} = \text{domain} + \text{rule} + \text{codomain}}
$$

For example, the formula $f(x)=x^2$ behaves differently depending on the domain. If

$$
f:\mathbb R\to\mathbb R,\quad f(x)=x^2,
$$

then the range is $[0,\infty)$. The function is not one-one because $f(2)=f(-2)=4$, and it is not onto $\mathbb R$ because negative outputs are not produced. But if

$$
f:[0,\infty)\to[0,\infty),\quad f(x)=x^2,
$$

then it is both one-one and onto, so it has an inverse.

## 1.1 Domain, Codomain, Range

| Word | Meaning |
|---|---|
| Domain | allowed inputs |
| Codomain | declared target set |
| Range | actual outputs produced |

Always remember:

$$
\text{Range}(f)\subseteq \text{Codomain}(f)
$$

This distinction is important in inverse functions, graphs, transformations, and calculus.

## 1.2 One-One, Onto, Bijective

A function is **one-one/injective** if different inputs give different outputs:

$$
f(a)=f(b)\Rightarrow a=b
$$

A function is **onto/surjective** if every element of the codomain is hit:

$$
\text{Range}(f)=\text{Codomain}(f)
$$

A function is **bijective** if it is both one-one and onto. Only bijective functions have genuine inverse functions from codomain back to domain.

## 1.3 Composition

If

$$
f:A\to B,\qquad g:B\to C,
$$

then

$$
(g\circ f)(x)=g(f(x))
$$

Composition is usually not commutative:

$$
g\circ f\ne f\circ g
$$

Example:

$$
f(x)=x+1,\quad g(x)=x^2
$$

$$
(g\circ f)(x)=(x+1)^2,
\qquad
(f\circ g)(x)=x^2+1
$$

These are different.

## 1.4 Inverse Functions

To find an inverse, set $y=f(x)$, solve for $x$, and then swap notation.

Example:

$$
f(x)=5x+7
$$

$$
y=5x+7\Rightarrow x=\frac{y-7}{5}
$$

$$
\boxed{f^{-1}(x)=\frac{x-7}{5}}
$$

Session examples:

$$
f(x)=2x-3\Rightarrow \boxed{f^{-1}(x)=\frac{x+3}{2}}
$$

Important correction: $(x+3)/2$ is not the same as $x+3/2$. Use brackets.

$$
f(x)=\frac{x-4}{3}\Rightarrow \boxed{f^{-1}(x)=3x+4}
$$

For $x^2$, domain restriction matters:

$$
x^2:[0,\infty)\to[0,\infty)\Rightarrow f^{-1}(x)=\sqrt x
$$

$$
x^2:(-\infty,0]\to[0,\infty)\Rightarrow f^{-1}(x)=-\sqrt x
$$

---

# 2. Physics Detailed Reading
## Measurement, Dimensions, and Error Propagation

Physics begins with measurement. A physical quantity is not just a number. It has magnitude, unit, and dimension.

Example:

$$
5\text{ m}
$$

means magnitude $5$, unit metre, dimension length.

## 2.1 Fundamental Dimensions

The main mechanical dimensions are:

| Quantity | Dimension |
|---|---|
| Mass | $M$ |
| Length | $L$ |
| Time | $T$ |

Derived examples:

$$
[v]=LT^{-1}
$$

$$
[a]=LT^{-2}
$$

Since

$$
F=ma,
$$

$$
\boxed{[F]=MLT^{-2}}
$$

Energy/work:

$$
W=Fs\Rightarrow [W]=ML^2T^{-2}
$$

Power:

$$
P=\frac Wt\Rightarrow [P]=ML^2T^{-3}
$$

## 2.2 Dimension of Gravitational Constant

Newton's law:

$$
F=\frac{Gm_1m_2}{r^2}
$$

Solving for $G$:

$$
G=\frac{Fr^2}{m_1m_2}
$$

$$
[G]=\frac{(MLT^{-2})(L^2)}{M^2}
$$

$$
\boxed{[G]=M^{-1}L^3T^{-2}}
$$

## 2.3 Dimensional Homogeneity

Every physically valid equation must have the same dimensions on both sides. For example:

$$
s=ut+\frac12at^2
$$

$$
[ut]=(LT^{-1})(T)=L
$$

$$
[at^2]=(LT^{-2})(T^2)=L
$$

Both terms are lengths. Dimensional analysis catches structural errors but cannot find dimensionless constants like $2,\pi,1/2$.

## 2.4 Errors

If a measured value is:

$$
x=x_0\pm \Delta x,
$$

then:

$$
\text{relative error}=\frac{\Delta x}{x}
$$

$$
\text{percentage error}=\frac{\Delta x}{x}\times100\%
$$

For products, quotients, and powers:

$$
Q=x^ay^bz^c
$$

maximum relative error is:

$$
\boxed{\frac{\Delta Q}{Q}=|a|\frac{\Delta x}{x}+|b|\frac{\Delta y}{y}+|c|\frac{\Delta z}{z}}
$$

Examples covered:

$$
A=xy^3,\\ x=2\%,\ y=4\%
$$

$$
\frac{\Delta A}{A}=2\%+3(4\%)=\boxed{14\%}
$$

$$
Q=\frac{a^2b}{c^3},\quad a=1\%,\ b=2\%,\ c=3\%
$$

$$
\frac{\Delta Q}{Q}=2(1\%)+2\%+3(3\%)=\boxed{13\%}
$$

---

# 3. Chemistry Detailed Reading
## Mole Concept, Stoichiometry, Concentration

A mole is a counting unit:

$$
1\text{ mol}=6.022\times10^{23}\text{ entities}
$$

The entity may be atoms, molecules, ions, electrons, or formula units.

## 3.1 Moles from Mass

$$
\boxed{n=\frac mM}
$$

where $m$ is given mass and $M$ is molar mass.

Example:

$$
44\text{ g CO}_2
$$

Molar mass:

$$
12+2(16)=44\text{ g mol}^{-1}
$$

$$
n=\frac{44}{44}=\boxed{1\text{ mol}}
$$

## 3.2 Stoichiometry

A balanced chemical equation gives mole ratios.

$$
N_2+3H_2\to2NH_3
$$

This means:

$$
1\text{ mol }N_2:3\text{ mol }H_2:2\text{ mol }NH_3
$$

For $2$ mol $N_2$, required $H_2$ is $6$ mol. If only $3$ mol $H_2$ is present, then:

$$
\boxed{H_2\text{ is limiting reagent}}
$$

## 3.3 Concentration

Molarity:

$$
\boxed{C=\frac nV}
$$

where $V$ must be in litres.

Example:

$$
0.5\text{ mol in }250\text{ mL}=0.250\text{ L}
$$

$$
C=\frac{0.5}{0.250}=\boxed{2\text{ M}}
$$

---

# 4. Formula Sheet

## Mathematics

$$
f:A\to B
$$

$$
(g\circ f)(x)=g(f(x))
$$

$$
f^{-1}(f(x))=x
$$

$$
f(a)=f(b)\Rightarrow a=b\quad\text{for one-one functions}
$$

## Physics

$$
[F]=MLT^{-2}
$$

$$
[G]=M^{-1}L^3T^{-2}
$$

$$
\frac{\Delta Q}{Q}=\sum |p_i|\frac{\Delta x_i}{x_i}
$$

## Chemistry

$$
n=\frac mM
$$

$$
N=nN_A
$$

$$
C=\frac nV
$$

---

# 5. Important Derivations

## 5.1 Inverse of a Linear Function

$$
f(x)=ax+b
$$

$$
y=ax+b\Rightarrow x=\frac{y-b}{a}
$$

$$
\boxed{f^{-1}(x)=\frac{x-b}{a}}
$$

## 5.2 Dimension of $G$

$$
F=\frac{Gm_1m_2}{r^2}\Rightarrow G=\frac{Fr^2}{m_1m_2}
$$

$$
\boxed{[G]=M^{-1}L^3T^{-2}}
$$

## 5.3 Error Propagation

Taking logarithms of $Q=x^ay^b$:

$$
\ln Q=a\ln x+b\ln y
$$

Differentiating approximately:

$$
\frac{\Delta Q}{Q}=a\frac{\Delta x}{x}+b\frac{\Delta y}{y}
$$

For maximum error, use absolute values.

---

# 6. Solved Examples and Corrections

| Area | Problem | Correct result | Correction note |
|---|---|---|---|
| Math | $f(x)=2x-3$ | $(x+3)/2$ | bracket the numerator |
| Math | restricted $x^2$ | $\sqrt x$ or $-\sqrt x$ | depends on domain |
| Physics | $[G]$ | $M^{-1}L^3T^{-2}$ | solve from gravitation law |
| Physics | $A=xy^3$ errors | $14\%$ | exponent multiplies error |
| Chemistry | $44g\ CO_2$ | 1 mol | use molar mass |
| Chemistry | $N_2+3H_2$ | $H_2$ limiting | compare mole ratios |
| Chemistry | 0.5 mol/250 mL | 2 M | convert mL to L |

---

# 7. Short Ways and Memory Hooks

- Function = domain + rule + codomain.
- Range is actual output; codomain is declared output set.
- True inverse needs one-one behavior.
- Dimensions track structure, not numerical constants.
- In percentage error, powers become multipliers.
- Mole is the bridge between particles and grams.
- Limiting reagent is the reagent that runs out first.

---

# 8. Common Traps

| Trap | Fix |
|---|---|
| Confusing range and codomain | range is actual output |
| Writing $(x+3)/2$ as $x+3/2$ | use brackets |
| Forgetting domain restrictions | restrict to make inverse possible |
| Using mass ratios in stoichiometry | use mole ratios |
| Forgetting litre conversion | mL must become L |
| Ignoring powers in error propagation | multiply by exponent |

---

# 9. Required Output — Symbol Sheet

## Mathematics

| Symbol | Meaning |
|---|---|
| $A,B$ | sets |
| $f:A\to B$ | map from $A$ to $B$ |
| $D_f$ | domain |
| $\text{Range}(f)$ | range |
| $g\circ f$ | composition |
| $f^{-1}$ | inverse |

## Physics

| Symbol | Meaning |
|---|---|
| $M,L,T$ | mass, length, time dimensions |
| $\Delta x$ | absolute error |
| $\Delta x/x$ | relative error |
| $G$ | gravitational constant |

## Chemistry

| Symbol | Meaning |
|---|---|
| $n$ | moles |
| $m$ | mass |
| $M$ | molar mass |
| $N_A$ | Avogadro constant |
| $C$ | molarity |
| $V$ | volume in litres |

---

# 10. Completion Checklist

| Item | Status |
|---|---|
| Sets | Complete |
| Functions as maps | Complete |
| Domain/codomain/range | Complete |
| Inverse functions | Complete |
| Measurements and dimensions | Complete |
| Error propagation | Complete |
| Mole concept | Complete |
| Stoichiometry | Complete |
| Concentration | Complete |
| Symbol sheet | Complete |

$$
\boxed{\text{Week 1 Day 1 Complete}}
$$

