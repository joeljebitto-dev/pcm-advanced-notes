# Week 2 — Day 1
## Linear Algebra, Gravitation as an Inverse-Square Field, and Chemical Equilibrium

## 0. Plan Row and Completion Status

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Linear algebra: matrices, systems, basis | Complete |
| Physics | Gravitation as inverse-square field | Complete |
| Chemistry | Chemical equilibrium: \(K,Q\), activities preview | Complete |
| Required output | Field analogy sheet | Complete |

---

# 1. Day Purpose

This day connects three major languages used later in advanced PCM:

- **Linear algebra**: systems, constraints, span, independence, basis, and rank.
- **Gravitation**: inverse-square fields, superposition, scalar potential, potential energy, and orbital energy.
- **Chemical equilibrium**: equilibrium constants, reaction quotients, direction of shift, thermodynamic driving force, and activities.

The unifying idea:

> Linear algebra explains how components combine. Gravitation explains how sources create fields and potentials. Chemical equilibrium explains how a current state compares with a balanced thermodynamic state.

---

# 2. Mathematics Detailed Reading
## Linear Algebra: Matrices, Systems, Basis

## 2.1 Matrix as a System Tool

A matrix packages many linear equations into one object.

The central form is:

$$
A\vec{x}=\vec{b}
$$

where:

| Symbol | Meaning |
|---|---|
| \(A\) | coefficient matrix or linear transformation |
| \(\vec{x}\) | unknown vector |
| \(\vec{b}\) | output / target vector |

This appears in mechanics, reaction balancing, electric circuits, coordinate transformations, data fitting, and quantum mechanics.

---

## 2.2 Matrix-Vector Multiplication

Let:

$$
A=
\begin{pmatrix}
1 & 2\\
3 & 4
\end{pmatrix},
\qquad
\vec{x}=
\begin{pmatrix}
x\\
y
\end{pmatrix}
$$

Then:

$$
A\vec{x}
=
\begin{pmatrix}
x+2y\\
3x+4y
\end{pmatrix}
$$

Column view:

$$
A\vec{x}
=
x
\begin{pmatrix}
1\\
3
\end{pmatrix}
+
y
\begin{pmatrix}
2\\
4
\end{pmatrix}
$$

So matrix-vector multiplication is a **linear combination of columns**.

This is the most important interpretation for span and consistency.

---

## 2.3 Systems as Matrix Equations

The system:

$$
x+2y=5
$$

$$
3x+4y=11
$$

becomes:

$$
\begin{pmatrix}
1 & 2\\
3 & 4
\end{pmatrix}
\begin{pmatrix}
x\\
y
\end{pmatrix}
=
\begin{pmatrix}
5\\
11
\end{pmatrix}
$$

This asks:

> Can \(\vec b\) be produced from the columns of \(A\)?

If yes, the system is consistent. If no, the system is inconsistent.

---

## 2.4 Row Operations

Allowed operations:

| Operation | Meaning |
|---|---|
| \(R_i\leftrightarrow R_j\) | swap rows |
| \(R_i\to kR_i,\ k\ne0\) | scale a row |
| \(R_i\to R_i+kR_j\) | add multiple of one row to another |

These preserve the solution set.

A contradiction such as:

$$
0=5
$$

means no solution.

---

## 2.5 Span

The span of vectors is all possible linear combinations:

$$
\text{span}(\vec v_1,\ldots,\vec v_n)
=
\{c_1\vec v_1+\cdots+c_n\vec v_n\}
$$

Short meaning:

> Span = what the vectors can build.

Example:

$$
\vec e_1=
\begin{pmatrix}
1\\0
\end{pmatrix},
\quad
\vec e_2=
\begin{pmatrix}
0\\1
\end{pmatrix}
$$

These span \(\mathbb R^2\), because every vector \((x,y)\) equals:

$$
x\vec e_1+y\vec e_2
$$

---

## 2.6 Linear Independence

Vectors are linearly independent if:

$$
c_1\vec v_1+\cdots+c_n\vec v_n=\vec0
$$

has only the trivial solution:

$$
c_1=\cdots=c_n=0
$$

If one vector can be built from the others, the set is dependent.

Example:

$$
\begin{pmatrix}
2\\4
\end{pmatrix}
=
2
\begin{pmatrix}
1\\2
\end{pmatrix}
$$

So these two vectors are dependent.

---

## 2.7 Basis

A basis is a set that is both:

1. linearly independent
2. spanning

Thus:

$$
\boxed{\text{basis}=\text{independent spanning set}}
$$

A basis gives coordinates.

In standard \(\mathbb R^2\):

$$
\vec v=
\begin{pmatrix}
3\\5
\end{pmatrix}
=
3
\begin{pmatrix}
1\\0
\end{pmatrix}
+
5
\begin{pmatrix}
0\\1
\end{pmatrix}
$$

So coordinates are coefficients in a basis expansion.

---

## 2.8 Rank and Consistency

Rank is the number of independent directions in a matrix.

For a system with \(n\) unknowns:

| Condition | Result |
|---|---|
| inconsistent row \(0=c,\ c\ne0\) | no solution |
| rank = number of unknowns | unique solution |
| rank < number of unknowns and consistent | infinitely many solutions |

Column-space interpretation:

$$
A\vec{x}=\vec{b}
$$

is solvable exactly when \(\vec b\) lies in the column space of \(A\).

---

## 2.9 Math Drill Record

### M1 — Matrix System
**Difficulty: JEE Adv L2**

System:

$$
x+2y-z=3
$$

$$
2x-y+3z=9
$$

$$
3x+y+2z=10
$$

From the first equation:

$$
x=3-2y+z
$$

Substitute into equation 2:

$$
6-5y+5z=9
$$

$$
z-y=\frac35
$$

Substitute into equation 3:

$$
9-5y+5z=10
$$

$$
z-y=\frac15
$$

Contradiction:

$$
\frac35\ne\frac15
$$

Therefore:

$$
\boxed{\text{No solution; inconsistent system}}
$$

User answer: correct.

---

### M2 — Basis Test
**Difficulty: JEE Adv L3**

Vectors:

$$
\vec v_1=
\begin{pmatrix}
1\\1\\0
\end{pmatrix},
\quad
\vec v_2=
\begin{pmatrix}
2\\0\\1
\end{pmatrix},
\quad
\vec v_3=
\begin{pmatrix}
3\\1\\1
\end{pmatrix}
$$

Since:

$$
\vec v_1+\vec v_2=\vec v_3
$$

the vectors are linearly dependent.

Therefore:

$$
\boxed{\text{They do not form a basis of }\mathbb R^3}
$$

User answer: correct.

---

### M3 — Parameter Dependence
**Difficulty: Olympiad L1**

Vectors:

$$
\begin{pmatrix}
1\\2
\end{pmatrix},
\quad
\begin{pmatrix}
a\\4
\end{pmatrix}
$$

They are dependent when:

$$
\begin{vmatrix}
1 & a\\
2 & 4
\end{vmatrix}
=0
$$

$$
4-2a=0
$$

$$
\boxed{a=2}
$$

User answer: correct.

---

# 3. Physics Detailed Reading
## Gravitation as an Inverse-Square Field

## 3.1 Field View of Gravity

Newton's law:

$$
F=\frac{GMm}{r^2}
$$

Field view:

> Source mass \(M\) creates a gravitational field in space. Test mass \(m\) experiences force in that field.

Gravitational field intensity:

$$
\boxed{\vec g=\frac{\vec F}{m}}
$$

For point mass \(M\):

$$
\boxed{\vec g=-\frac{GM}{r^2}\hat r}
$$

Magnitude:

$$
\boxed{g=\frac{GM}{r^2}}
$$

The negative sign means the field points inward, toward the mass.

---

## 3.2 Inverse-Square Behavior

Because:

$$
g\propto\frac{1}{r^2}
$$

doubling distance makes field one-fourth:

$$
r\to2r\Rightarrow g\to\frac{g}{4}
$$

tripling distance makes field one-ninth:

$$
r\to3r\Rightarrow g\to\frac{g}{9}
$$

Geometric reason: influence spreads across a spherical area:

$$
A=4\pi r^2
$$

---

## 3.3 Superposition

Fields add as vectors:

$$
\boxed{\vec g_{\text{net}}=\vec g_1+\vec g_2+\cdots}
$$

Do not add magnitudes blindly.

For equal masses at \(x=-a\) and \(x=+a\), the net field at origin is zero because the two fields are equal and opposite.

---

## 3.4 Gravitational Potential Energy

For two masses:

$$
\boxed{U=-\frac{GMm}{r}}
$$

The zero is chosen at infinity:

$$
U(\infty)=0
$$

At finite \(r\), \(U<0\), because gravity is attractive and the system is bound.

---

## 3.5 Gravitational Potential

Potential is potential energy per unit test mass:

$$
\boxed{V=\frac{U}{m}}
$$

For a point mass:

$$
\boxed{V=-\frac{GM}{r}}
$$

Important distinction:

| Quantity | Type | Dependence |
|---|---|---|
| field \(\vec g\) | vector | \(1/r^2\) |
| potential \(V\) | scalar | \(1/r\) |

Thus, zero field does not imply zero potential.

---

## 3.6 Field-Potential Relation

In one dimension:

$$
\boxed{g=-\frac{dV}{dr}}
$$

For:

$$
V=-\frac{GM}{r}
$$

$$
\frac{dV}{dr}=\frac{GM}{r^2}
$$

so:

$$
g=-\frac{GM}{r^2}
$$

Field points downhill in potential.

---

## 3.7 Escape Speed

For just escape from surface radius \(R\):

$$
\frac12mv_e^2-\frac{GMm}{R}=0
$$

So:

$$
\boxed{v_e=\sqrt{\frac{2GM}{R}}}
$$

The test mass cancels.

---

## 3.8 Circular Orbit

Gravity supplies centripetal force:

$$
\frac{GMm}{r^2}=\frac{mv^2}{r}
$$

Thus:

$$
\boxed{v=\sqrt{\frac{GM}{r}}}
$$

Kinetic energy:

$$
\boxed{K=\frac{GMm}{2r}}
$$

Potential energy:

$$
\boxed{U=-\frac{GMm}{r}}
$$

Total energy:

$$
\boxed{E=-\frac{GMm}{2r}}
$$

High-yield relations:

$$
K=-\frac{U}{2}
$$

$$
E=\frac{U}{2}=-K
$$

---

## 3.9 Shell Theorem Preview

Outside spherical body:

$$
g=\frac{GM}{r^2}
$$

Inside thin spherical shell:

$$
g=0
$$

Inside uniform solid sphere:

$$
g(r)=\frac{GMr}{R^3}
$$

so:

$$
g\propto r
$$

---

## 3.10 Physics Drill Record

### P1 — Field Superposition on a Line
**Difficulty: JEE Adv L2**

Mass \(M\) at \(x=0\), mass \(4M\) at \(x=3a\).

Let zero-field point be at \(x\) from \(M\).

$$
\frac{GM}{x^2}=\frac{4GM}{(3a-x)^2}
$$

$$
3a-x=2x
$$

$$
\boxed{x=a}
$$

User answer: correct.

---

### P2 — Potential vs Field
**Difficulty: JEE Adv L3**

Equal masses at \(x=-a\) and \(x=+a\).

At origin:

$$
\boxed{\vec g_{\text{net}}=0}
$$

Potential:

$$
V=-\frac{GM}{a}-\frac{GM}{a}
$$

$$
\boxed{V=-\frac{2GM}{a}}
$$

User error: wrote \(-2GM/a^2\). That is field-style denominator. Potential varies as \(1/r\), not \(1/r^2\).

---

### P3 — Circular Orbit Energy
**Difficulty: JEE Adv L3**

Correct results:

$$
\boxed{v=\sqrt{\frac{GM}{r}}}
$$

$$
\boxed{K=\frac{GMm}{2r}}
$$

$$
\boxed{U=-\frac{GMm}{r}}
$$

$$
\boxed{E=-\frac{GMm}{2r}}
$$

User answer: correct.

---

### P4 — Escape Speed
**Difficulty: Olympiad L1**

Correct:

$$
\boxed{v_e=\sqrt{\frac{2GM}{R}}}
$$

User answer: correct.

---

# 4. Chemistry Detailed Reading
## Chemical Equilibrium: \(K,Q\), Activities Preview

## 4.1 Dynamic Equilibrium

For:

$$
aA+bB\rightleftharpoons cC+dD
$$

equilibrium means:

$$
\text{forward rate}=\text{reverse rate}
$$

It is dynamic, not static. The forward and reverse reactions continue, but concentrations remain constant.

---

## 4.2 Equilibrium Constant \(K_c\)

For:

$$
aA+bB\rightleftharpoons cC+dD
$$

$$
\boxed{K_c=\frac{[C]^c[D]^d}{[A]^a[B]^b}}
$$

Coefficients become powers.

Pure solids and pure liquids are omitted because their activities are constant.

Example:

$$
N_2+3H_2\rightleftharpoons2NH_3
$$

$$
K_c=\frac{[NH_3]^2}{[N_2][H_2]^3}
$$

---

## 4.3 Reaction Quotient \(Q\)

\(Q\) has the same form as \(K\), but uses current concentrations.

| Quantity | Uses |
|---|---|
| \(K\) | equilibrium concentrations |
| \(Q\) | current concentrations |

Direction rule:

$$
Q<K\Rightarrow\text{forward}
$$

$$
Q=K\Rightarrow\text{equilibrium}
$$

$$
Q>K\Rightarrow\text{reverse}
$$

---

## 4.4 \(K_p\) and \(K_c\)

For gases:

$$
\boxed{K_p=K_c(RT)^{\Delta n_g}}
$$

where:

$$
\Delta n_g=\text{gaseous product moles}-\text{gaseous reactant moles}
$$

For:

$$
N_2+3H_2\rightleftharpoons2NH_3
$$

$$
\Delta n_g=2-4=-2
$$

Thus:

$$
K_p=K_c(RT)^{-2}
$$

---

## 4.5 Le Chatelier's Principle

When disturbed, an equilibrium shifts to oppose the disturbance.

| Disturbance | Shift |
|---|---|
| add reactant | forward |
| add product | reverse |
| decrease volume for gases | side with fewer gas moles |
| increase volume for gases | side with more gas moles |
| raise temperature for endothermic reaction | forward |
| raise temperature for exothermic reaction | reverse |

Only temperature changes \(K\). Concentration and pressure changes alter position but not \(K\) at fixed \(T\).

---

## 4.6 Gibbs Free Energy Link

$$
\Delta G=\Delta G^\circ+RT\ln Q
$$

At equilibrium:

$$
\Delta G=0,\quad Q=K
$$

Therefore:

$$
\boxed{\Delta G^\circ=-RT\ln K}
$$

If:

$$
K>1
$$

then:

$$
\Delta G^\circ<0
$$

Products are favored.

---

## 4.7 Activities Preview

The rigorous expression uses activities:

$$
\boxed{
K=\frac{a_C^c a_D^d}{a_A^a a_B^b}
}
$$

For dilute solutions:

$$
a_i\approx[i]
$$

For ideal gases:

$$
a_i\approx\frac{P_i}{P^\circ}
$$

For pure solids and liquids:

$$
\boxed{a=1}
$$

This is why pure solids and liquids do not appear in equilibrium constant expressions.

---

## 4.8 Chemistry Drill Record

### C1 — Write \(K_c\)
**Difficulty: JEE Adv L2**

For:

$$
2SO_2(g)+O_2(g)\rightleftharpoons2SO_3(g)
$$

$$
\boxed{K_c=\frac{[SO_3]^2}{[SO_2]^2[O_2]}}
$$

---

### C2 — Reaction Quotient Direction
**Difficulty: JEE Adv L3**

For:

$$
H_2+I_2\rightleftharpoons2HI
$$

given:

$$
K_c=64,\quad [H_2]=2,\quad[I_2]=2,\quad[HI]=8
$$

$$
Q_c=\frac{[HI]^2}{[H_2][I_2]}
$$

$$
Q_c=\frac{8^2}{2\cdot2}=16
$$

Since:

$$
Q<K
$$

the reaction shifts forward.

$$
\boxed{\text{more }HI\text{ forms}}
$$

---

### C3 — \(K_p\) and \(K_c\)
**Difficulty: JEE Adv L3**

For:

$$
N_2+3H_2\rightleftharpoons2NH_3
$$

$$
\Delta n_g=2-4=-2
$$

$$
\boxed{K_p=K_c(RT)^{-2}=\frac{K_c}{(RT)^2}}
$$

---

### C4 — Activities Preview
**Difficulty: Olympiad L1**

For:

$$
CaCO_3(s)\rightleftharpoons CaO(s)+CO_2(g)
$$

Activity form:

$$
K=\frac{a_{CaO}a_{CO_2}}{a_{CaCO_3}}
$$

Pure solids have activity \(1\):

$$
a_{CaO}=1,\quad a_{CaCO_3}=1
$$

So:

$$
\boxed{K=a_{CO_2}}
$$

For ideal gas:

$$
\boxed{K\approx\frac{P_{CO_2}}{P^\circ}}
$$

Basic shorthand:

$$
K_p=P_{CO_2}
$$

---

# 5. Required Output — Field Analogy Sheet

## 5.1 Core Analogy Table

| Idea | Gravitation | Electrostatics | Chemical equilibrium |
|---|---|---|---|
| Source | mass \(M\) | charge \(q\) | reactants/products |
| Test object | mass \(m\) | test charge \(q_0\) | reaction mixture |
| Field-like quantity | \(\vec g\) | \(\vec E\) | driving force via \(\Delta G\) |
| Force law | \(\vec F=m\vec g\) | \(\vec F=q_0\vec E\) | shift from \(Q\) vs \(K\) |
| Potential | \(V=-GM/r\) | \(V=kq/r\) | \(\Delta G=\Delta G^\circ+RT\ln Q\) |
| Equilibrium condition | net field/force zero | net field/force zero | \(Q=K,\ \Delta G=0\) |
| Superposition | vector addition | vector addition | thermodynamic contributions combine |

---

## 5.2 Field vs Potential

| Quantity | Formula | Type | Meaning |
|---|---|---|---|
| gravitational field | \(\vec g=-GM\hat r/r^2\) | vector | force per unit mass |
| gravitational potential | \(V=-GM/r\) | scalar | energy per unit mass |
| gravitational potential energy | \(U=-GMm/r\) | scalar | stored interaction energy |

Key distinction:

$$
\boxed{\text{field}\sim\frac{1}{r^2}}
$$

$$
\boxed{\text{potential}\sim\frac{1}{r}}
$$

---

## 5.3 Superposition

Gravitational field:

$$
\vec g_{\text{net}}=\sum_i \vec g_i
$$

Gravitational potential:

$$
V_{\text{net}}=\sum_i V_i
$$

Fields add as vectors. Potentials add as scalars.

Example at origin for equal masses at \(-a\) and \(+a\):

$$
\boxed{\vec g_{\text{net}}=0}
$$

but:

$$
\boxed{V_{\text{net}}=-\frac{2GM}{a}}
$$

Zero field does not imply zero potential.

---

## 5.4 Linear Algebra Link

Matrix equation:

$$
A\vec x=\vec b
$$

means:

> Is \(\vec b\) in the span of the columns of \(A\)?

Field superposition similarly asks:

> What vector results from adding all source contributions?

Both are structured combinations:

$$
A\vec x=x_1\vec a_1+x_2\vec a_2+\cdots
$$

$$
\vec g_{\text{net}}=\vec g_1+\vec g_2+\cdots
$$

Linear algebra is the language of structured addition.

---

## 5.5 Equilibrium Analogy

| System | Equilibrium condition |
|---|---|
| Mechanical force balance | \(\sum\vec F=0\) |
| Gravitational field cancellation | \(\vec g_{\text{net}}=0\) |
| Chemical equilibrium | \(Q=K\) |
| Thermodynamic equilibrium | \(\Delta G=0\) |
| Linear system consistency | \(\vec b\) lies in column space of \(A\) |

Equilibrium always means a balance condition, but the mathematical form changes by subject.

---

## 5.6 Direction Rules

Gravity:

$$
\vec F=m\vec g
$$

Potential-field relation:

$$
\vec g=-\nabla V
$$

Chemical reaction direction:

$$
Q<K\Rightarrow\text{forward}
$$

$$
Q>K\Rightarrow\text{reverse}
$$

$$
Q=K\Rightarrow\text{equilibrium}
$$

---

## 5.7 One-Line Summary

```text
Linear algebra tells how components combine.
Gravitation tells how masses create vector fields and scalar potentials.
Equilibrium tells how the current composition compares with the balanced thermodynamic state.
```

---

# 6. Formula Sheet — Day 8

## Linear Algebra

$$
A\vec x=\vec b
$$

$$
A\vec x=x_1\vec a_1+x_2\vec a_2+\cdots+x_n\vec a_n
$$

$$
\text{span}(\vec v_1,\ldots,\vec v_n)
=
\{c_1\vec v_1+\cdots+c_n\vec v_n\}
$$

$$
\text{basis}=\text{independent spanning set}
$$

For dependence in \(\mathbb R^2\):

$$
\begin{vmatrix}
a & b\\
c & d
\end{vmatrix}=0
$$

---

## Gravitation

$$
F=\frac{GMm}{r^2}
$$

$$
\vec g=-\frac{GM}{r^2}\hat r
$$

$$
U=-\frac{GMm}{r}
$$

$$
V=-\frac{GM}{r}
$$

$$
\vec g=-\nabla V
$$

$$
v_{\text{orb}}=\sqrt{\frac{GM}{r}}
$$

$$
v_e=\sqrt{\frac{2GM}{R}}
$$

$$
K=\frac{GMm}{2r}
$$

$$
E=-\frac{GMm}{2r}
$$

---

## Equilibrium

$$
K_c=\frac{[C]^c[D]^d}{[A]^a[B]^b}
$$

$$
Q_c=\frac{[C]^c[D]^d}{[A]^a[B]^b}
$$

$$
Q<K\Rightarrow\text{forward}
$$

$$
Q=K\Rightarrow\text{equilibrium}
$$

$$
Q>K\Rightarrow\text{reverse}
$$

$$
K_p=K_c(RT)^{\Delta n_g}
$$

$$
\Delta G=\Delta G^\circ+RT\ln Q
$$

$$
\Delta G^\circ=-RT\ln K
$$

$$
K=\frac{a_C^c a_D^d}{a_A^a a_B^b}
$$

---

# 7. Important Derivations

## 7.1 Circular Orbit Energy

Gravity provides centripetal force:

$$
\frac{GMm}{r^2}=\frac{mv^2}{r}
$$

So:

$$
v^2=\frac{GM}{r}
$$

Kinetic energy:

$$
K=\frac12mv^2=\frac{GMm}{2r}
$$

Potential energy:

$$
U=-\frac{GMm}{r}
$$

Total energy:

$$
E=K+U
$$

$$
E=\frac{GMm}{2r}-\frac{GMm}{r}
$$

$$
\boxed{E=-\frac{GMm}{2r}}
$$

---

## 7.2 Escape Speed

At minimum escape:

$$
E_i=E_f=0
$$

At surface:

$$
\frac12mv_e^2-\frac{GMm}{R}=0
$$

Therefore:

$$
\boxed{v_e=\sqrt{\frac{2GM}{R}}}
$$

---

## 7.3 Gibbs and Equilibrium Constant

$$
\Delta G=\Delta G^\circ+RT\ln Q
$$

At equilibrium:

$$
\Delta G=0,\quad Q=K
$$

Therefore:

$$
0=\Delta G^\circ+RT\ln K
$$

$$
\boxed{\Delta G^\circ=-RT\ln K}
$$

---

# 8. Error Log

| Code | Topic | Error | Correction |
|---|---|---|---|
| P2 | Gravitational potential | Used \(a^2\) in denominator | Potential varies as \(1/r\), so \(V=-2GM/a\) |
| Math | Linear algebra drill | No errors | Maintain contradiction/basis checks |
| Chemistry | Equilibrium drill | Answered directly by assistant | Review \(Q\), \(K\), and activities |

---

# 9. Short Ways and Memory Hooks

## Linear Algebra

- Span = what you can build.
- Independence = no redundancy.
- Basis = minimum toolkit for a space.
- Rank = independent directions.
- \(A\vec x\) = linear combination of columns.

## Gravitation

- Field = force per unit mass.
- Potential = energy per unit mass.
- Field is vector; potential is scalar.
- Field falls as \(1/r^2\); potential falls as \(1/r\).
- Escape speed comes from total energy reaching zero.
- Circular orbit total energy is negative.

## Chemical Equilibrium

- \(K\): equilibrium ratio.
- \(Q\): current ratio.
- \(Q<K\): forward.
- \(Q>K\): reverse.
- Pure solids/liquids have activity 1.
- Only temperature changes \(K\).

---

# 10. Common Traps

| Topic | Trap | Correction |
|---|---|---|
| Matrix systems | declaring inconsistency without contradiction | find conflicting equations or \(0=c\) |
| Basis | checking only number of vectors | also check independence |
| Gravitation | adding field magnitudes | add field vectors |
| Gravitation | confusing field and potential | field \(1/r^2\), potential \(1/r\) |
| Gravitation | saying zero field means zero potential | false |
| Orbit | saying total energy is zero in circular orbit | \(E=-GMm/(2r)\) |
| Equilibrium | including solids in \(K\) | pure solids have activity 1 |
| Equilibrium | confusing \(Q\) and \(K\) | \(Q\) current, \(K\) equilibrium |
| Equilibrium | saying catalyst changes \(K\) | catalyst changes rate, not \(K\) |

---

# 11. Completion Checklist

| Item | Status |
|---|---|
| Matrices | Complete |
| Systems | Complete |
| Basis | Complete |
| Span | Complete |
| Linear independence | Complete |
| Rank and consistency | Complete |
| Gravitation inverse-square law | Complete |
| Gravitational field | Complete |
| Superposition | Complete |
| Potential and potential energy | Complete |
| Escape speed | Complete |
| Circular orbital energy | Complete |
| Chemical equilibrium | Complete |
| \(K,Q\) | Complete |
| \(K_p,K_c\) | Complete |
| Activities preview | Complete |
| Field analogy sheet | Complete |

$$
\boxed{\text{Week 2 Day 1 Complete}}
$$
