# Week 1 — Day 5
## Integrals as Accumulation, Work-Energy, Conservative Fields, Chemical Bonding

## 0. Plan Row

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Integrals as accumulation | Complete |
| Physics | Work-energy theorem and conservative fields | Complete |
| Chemistry | Chemical bonding: VSEPR, hybridization, and MO introduction | Complete |
| Required output | Derivation notes | Complete |

---

# 1. Mathematics Detailed Reading
## Integrals as Accumulation

An integral measures accumulation. If a rate is known, integration gives total change.

\[
\boxed{\text{accumulated quantity}=\int \text{rate}\,d(\text{input})}
\]

Examples:

| Rate | Integral gives |
|---|---|
| velocity | displacement |
| acceleration | change in velocity |
| force | work |
| current | charge |
| reaction rate | concentration change |

## 1.1 Indefinite and Definite Integrals

Indefinite integral:

\[
\int f(x)dx=F(x)+C
\]

Definite integral:

\[
\int_a^b f(x)dx=F(b)-F(a)
\]

A definite integral gives signed accumulation. If the graph is below the axis, contribution is negative.

## 1.2 Fundamental Theorem of Calculus

If:

\[
F(x)=\int_a^x f(t)dt,
\]

then:

\[
\boxed{F'(x)=f(x)}
\]

If:

\[
F(x)=\int_a^{g(x)}f(t)dt,
\]

then:

\[
\boxed{F'(x)=f(g(x))g'(x)}
\]

If both limits vary:

\[
F(x)=\int_{u(x)}^{v(x)} f(t)dt,
\]

then:

\[
\boxed{F'(x)=f(v(x))v'(x)-f(u(x))u'(x)}
\]

## 1.3 Session FTC Problems

Problem:

\[
F(x)=\int_0^{x^2}\frac{\sin t}{1+t^2}dt
\]

\[
\boxed{F'(x)=\frac{2x\sin(x^2)}{1+x^4}}
\]

Correction: do not forget the chain factor \(2x\).

Repair:

\[
F(x)=\int_{\cos x}^{x^2}\frac{e^t}{1+t^2}dt
\]

\[
\boxed{F'(x)=\frac{2xe^{x^2}}{1+x^4}+\frac{\sin x\ e^{\cos x}}{1+\cos^2x}}
\]

## 1.4 Net Displacement vs Total Distance

For velocity \(v(t)\):

\[
\text{net displacement}=\int_a^b v(t)dt
\]

\[
\text{total distance}=\int_a^b |v(t)|dt
\]

Example:

\[
v(t)=t^2-4t+3=(t-1)(t-3),\quad0\le t\le4
\]

Net displacement:

\[
\boxed{\frac43}
\]

Total distance:

\[
\boxed{4}
\]

Correction: total distance is not the same as net displacement when velocity changes sign.

## 1.5 Rational Integral Example

\[
\int_0^1\frac{x^3}{1+x^2}dx
\]

Rewrite:

\[
\frac{x^3}{1+x^2}=x-\frac{x}{1+x^2}
\]

Then:

\[
\int_0^1x dx-\int_0^1\frac{x}{1+x^2}dx
\]

\[
=\frac12-\frac12\ln2
\]

\[
\boxed{\frac{1-\ln2}{2}}
\]

---

# 2. Physics Detailed Reading
## Work-Energy Theorem and Conservative Fields

## 2.1 Work

For constant force:

\[
\boxed{W=\vec F\cdot\vec s=Fs\cos\theta}
\]

For variable force:

\[
\boxed{W=\int_{x_i}^{x_f}F(x)dx}
\]

Vector line integral:

\[
\boxed{W=\int_C\vec F\cdot d\vec r}
\]

Work measures energy transferred by force along displacement.

## 2.2 Work-Energy Theorem

\[
\boxed{W_{net}=\Delta K}
\]

\[
W_{net}=\frac12mv_f^2-\frac12mv_i^2
\]

Derivation:

\[
F=ma,
\qquad a=v\frac{dv}{dx}
\]

\[
Fdx=mvdv
\]

Integrate:

\[
\int Fdx=\int mvdv
\]

\[
\boxed{W=\frac12mv_f^2-\frac12mv_i^2}
\]

## 2.3 Conservative Forces

A force is conservative if work is path independent. Equivalent signs:

\[
\oint \vec F\cdot d\vec r=0
\]

and potential exists:

\[
\boxed{\vec F=-\nabla U}
\]

In one dimension:

\[
\boxed{F=-\frac{dU}{dx}}
\]

For conservative forces:

\[
W_{cons}=-\Delta U
\]

If only conservative forces act:

\[
\boxed{K+U=\text{constant}}
\]

## 2.4 Spring Potential

\[
F=-kx
\]

Since:

\[
F=-\frac{dU}{dx},
\]

\[
\frac{dU}{dx}=kx
\]

\[
\boxed{U=\frac12kx^2}
\]

## 2.5 Variable Force Problem

\[
F(x)=ax-bx^3
\]

from \(0\) to \(\sqrt{a/b}\):

\[
W=\int_0^{\sqrt{a/b}}(ax-bx^3)dx
\]

\[
=\left[\frac{ax^2}{2}-\frac{bx^4}{4}\right]_0^{\sqrt{a/b}}
\]

\[
\boxed{W=\frac{a^2}{4b}}
\]

Using \(W=\frac12mv^2\):

\[
\boxed{v=\frac{a}{\sqrt{2mb}}}
\]

Correction: mass enters after calculating work, not inside the work integral.

## 2.6 Stability from Potential

Equilibrium:

\[
F=0\quad\Longleftrightarrow\quad \frac{dU}{dx}=0
\]

Stable equilibrium corresponds to a local minimum of potential; unstable corresponds to local maximum.

For:

\[
U=\alpha x^4-\beta x^2
\]

\[
F=-\frac{dU}{dx}=2\beta x-4\alpha x^3
\]

Equilibria:

\[
\boxed{x=0,\quad x=\pm\sqrt{\frac{\beta}{2\alpha}}}
\]

Classification:

\[
x=0\text{ unstable},
\qquad x=\pm\sqrt{\frac{\beta}{2\alpha}}\text{ stable}
\]

---

# 3. Chemistry Detailed Reading
## Chemical Bonding: VSEPR, Hybridization, MO Introduction

Chemical bonding explains molecular shape, polarity, bond length, bond strength, magnetism, and reactivity.

## 3.1 Lewis Structures and Formal Charge

Formal charge:

\[
\boxed{FC=V-N-\frac B2}
\]

where:

- \(V\) = valence electrons of free atom,
- \(N\) = nonbonding electrons,
- \(B\) = bonding electrons.

Stable Lewis structures usually minimize formal charge and place negative charge on more electronegative atoms.

## 3.2 Resonance

Resonance occurs when multiple Lewis structures contribute to the real structure.

For \(NO_2^-\), there are two equivalent resonance structures. Therefore the two \(N-O\) bond lengths are equal and average bond order is:

\[
\boxed{1.5}
\]

Correction: the bonds are equal due to resonance, not unequal.

## 3.3 VSEPR

VSEPR = Valence Shell Electron Pair Repulsion.

Electron domains repel and arrange to minimize repulsion.

Repulsion order:

\[
LP-LP>LP-BP>BP-BP
\]

Steric number:

\[
\boxed{SN=\sigma\text{ bonds}+\text{lone pairs on central atom}}
\]

Common geometries:

| SN | Electron geometry | Example |
|---:|---|---|
| 2 | linear | \(CO_2\) |
| 3 | trigonal planar | \(BF_3\) |
| 4 | tetrahedral | \(CH_4\) |
| 5 | trigonal bipyramidal | \(PCl_5\) |
| 6 | octahedral | \(SF_6\) |

## 3.4 Hybridization

| Steric number | Hybridization |
|---:|---|
| 2 | \(sp\) |
| 3 | \(sp^2\) |
| 4 | \(sp^3\) |
| 5 | \(sp^3d\) |
| 6 | \(sp^3d^2\) |

Examples:

| Molecule | Hybridization | Shape | Angle |
|---|---|---|---|
| \(NH_3\) | \(sp^3\) | trigonal pyramidal | \(\approx107^\circ\) |
| \(H_2O\) | \(sp^3\) | bent | \(\approx104.5^\circ\) |
| \(BF_3\) | \(sp^2\) | trigonal planar | \(120^\circ\) |
| \(CO_2\) | \(sp\) | linear | \(180^\circ\) |

Angle order:

\[
\boxed{H_2O<NH_3<BF_3<CO_2}
\]

Correction: \(NH_3\) and \(H_2O\) are both \(sp^3\), even though their molecular shapes differ from tetrahedral because lone pairs affect geometry.

## 3.5 Molecular Orbital Introduction

Atomic orbitals combine to form molecular orbitals. There are bonding and antibonding orbitals.

Bond order:

\[
\boxed{BO=\frac{N_b-N_a}{2}}
\]

Higher bond order means shorter, stronger bond.

For oxygen species:

| Species | Bond order | Magnetism | Bond length |
|---|---:|---|---|
| \(O_2^+\) | 2.5 | paramagnetic | shortest |
| \(O_2\) | 2 | paramagnetic | intermediate |
| \(O_2^-\) | 1.5 | paramagnetic | longest |

---

# 4. Formula Sheet

## Mathematics

\[
\int f(x)dx=F(x)+C
\]

\[
\int_a^b f(x)dx=F(b)-F(a)
\]

\[
\frac{d}{dx}\int_a^{g(x)}f(t)dt=f(g(x))g'(x)
\]

\[
\frac{d}{dx}\int_{u(x)}^{v(x)}f(t)dt=f(v)v'-f(u)u'
\]

\[
\text{distance}=\int |v(t)|dt
\]

## Physics

\[
W=\vec F\cdot\vec s
\]

\[
W=\int F(x)dx
\]

\[
W_{net}=\Delta K
\]

\[
F=-\frac{dU}{dx}
\]

\[
K+U=\text{constant}
\]

\[
U_{spring}=\frac12kx^2
\]

## Chemistry

\[
FC=V-N-\frac B2
\]

\[
SN=\sigma\text{ bonds}+\text{lone pairs}
\]

\[
BO=\frac{N_b-N_a}{2}
\]

---

# 5. Advanced Practice Record

## Mathematics

| Problem | Difficulty | Correct answer | Mistake/correction |
|---|---|---|---|
| \(F(x)=\int_0^{x^2}\frac{\sin t}{1+t^2}dt\) | JEE Adv L2 | \(\frac{2x\sin(x^2)}{1+x^4}\) | include chain factor |
| \(\int_0^1\frac{x^3}{1+x^2}dx\) | JEE Adv L2 | \(\frac{1-\ln2}{2}\) | rewrite integrand |
| \(v=t^2-4t+3\), \([0,4]\) | JEE Adv L3 | net \(4/3\), distance 4 | distance uses absolute value |
| variable limits \(\cos x\) to \(x^2\) | JEE Adv L3 | see detailed expression above | lower limit gives minus sign |

## Physics

| Problem | Difficulty | Correct answer | Mistake/correction |
|---|---|---|---|
| \(F=ax-bx^3\) | JEE Adv L3 | \(W=a^2/(4b), v=a/\sqrt{2mb}\) | mass enters after work |
| \(U=\alpha x^4-\beta x^2\) | JEE Adv L3 | \(0\) unstable, \(\pm\sqrt{\beta/(2\alpha)}\) stable | classify using potential |
| \(F=y^2i+2xyj\) closed path | JEE Adv L3 | work 0 | conservative field |
| \(F=kx-\lambda x^3\) | JEE Adv L3 | \(v=\sqrt{3k^2/(8m\lambda)}\) | integrate force |
| potential barrier threshold | JEE Adv L3 | \(\sqrt{2U_0/m}\) | equality reaches barrier only |

## Chemistry

| Problem | Difficulty | Correct answer | Mistake/correction |
|---|---|---|---|
| \(NO_2^-\) | JEE Adv L2 | bent, resonance, equal bonds, BO 1.5 | resonance equalizes bonds |
| \(NH_3,H_2O,BF_3,CO_2\) | JEE Adv L2 | \(sp^3,sp^3,sp^2,sp\) | lone pairs change shape, not SN |
| \(O_2,O_2^+,O_2^-\) | JEE Adv L3 | BO 2,2.5,1.5 | antibonding electrons control BO |

---

# 6. Required Output — Derivation Notes

Included derivations:

1. Integral as accumulation.
2. Fundamental theorem of calculus with variable limits.
3. Work-energy theorem.
4. Conservative force-potential relation.
5. Spring potential energy.
6. Bond order from MO theory.

---

# 7. Short Ways and Traps

## Short Ways

- Integral = accumulated rate.
- Definite integral = signed accumulation.
- Total distance = integrate absolute velocity.
- Work = area under force-displacement graph.
- Conservative force = no path memory.
- Stable equilibrium = potential minimum.
- VSEPR = electron domains repel.
- Hybridization follows steric number.
- Bond order rises when antibonding electrons are removed.

## Traps

| Trap | Fix |
|---|---|
| Forgetting chain factor in FTC | multiply by limit derivative |
| Confusing displacement and distance | use \(|v|\) for distance |
| Putting mass inside work integral | integrate force first |
| Calling every equilibrium stable | inspect potential/force direction |
| Assuming closed-loop work is always zero | only conservative fields |
| Saying resonance structures switch | real molecule is resonance hybrid |
| Ignoring lone pairs in VSEPR | lone pairs compress angles |
| Treating hybridization as exact truth | it is a model |
| Ignoring antibonding orbitals | they reduce bond order |

---

# 8. Completion Checklist

| Item | Status |
|---|---|
| Integrals as accumulation | Complete |
| Definite/indefinite integrals | Complete |
| FTC and variable limits | Complete |
| Net displacement vs distance | Complete |
| Work-energy theorem | Complete |
| Conservative forces | Complete |
| Potential energy and stability | Complete |
| Lewis structures/formal charge | Complete |
| VSEPR | Complete |
| Hybridization | Complete |
| MO theory intro | Complete |
| Derivation notes | Complete |

\[
\boxed{\text{Week 1 Day 5 Complete}}
\]
