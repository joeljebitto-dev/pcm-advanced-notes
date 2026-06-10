# Week 1 — Day 7
## Integrated Revision and 2-Hour Diagnostic

## 0. Plan Row and Completion Status

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Integrated revision: functions, vectors, calculus, ODEs | Complete |
| Physics | Mechanics diagnostic: motion, forces, energy, rotation | Complete |
| Chemistry | Diagnostic: mole concept, atomic structure, bonding, thermodynamics | Complete |
| Required output | 2-hour diagnostic + error log | Complete |

---

# 1. Purpose of Day 7

Day 7 was a diagnostic checkpoint for all major Week 1 concepts. The goal was to test method selection, sign conventions, domain restrictions, accumulation vs rate reasoning, and repair of errors.

---

# 2. Diagnostic Overview

| Section | Target | Result |
|---|---|---|
| Mathematics | functions, vectors, calculus, ODEs | Completed |
| Physics | kinematics, friction, work-energy, angular momentum | Completed |
| Chemistry | mole concept, Bohr model, bonding, thermodynamics | Completed |
| Error log | record and repair mistakes | Completed |

---

# 3. Mathematics Diagnostic

## M1 — Function Invertibility
**Difficulty: JEE Adv L2**

Given:

$$
f:\mathbb{R}\to\mathbb{R},\qquad f(x)=x^2-4x+7
$$

Complete the square:

$$
f(x)=(x-2)^2+3
$$

The function is not one-one over all real numbers because it is symmetric about:

$$
x=2
$$

For example:

$$
f(1)=4,\qquad f(3)=4
$$

but:

$$
1\ne3
$$

So:

$$
\boxed{\text{not one-one on }\mathbb{R}}
$$

A valid restriction is:

$$
\boxed{x\in[2,\infty)}
$$

On this interval, the function is increasing and invertible.

Let:

$$
y=(x-2)^2+3
$$

Then:

$$
y-3=(x-2)^2
$$

Since \(x\ge2\), take the positive root:

$$
x=2+\sqrt{y-3}
$$

Therefore:

$$
\boxed{f^{-1}(x)=2+\sqrt{x-3}},\qquad x\ge3
$$

**User result:** all parts correct.

---

## M2 — Vector + Calculus Link
**Difficulty: JEE Adv L3**

Given:

$$
\vec r(t)=t^3\hat i+(2t^2-1)\hat j
$$

Velocity:

$$
\vec v(t)=\frac{d\vec r}{dt}=3t^2\hat i+4t\hat j
$$

Acceleration:

$$
\vec a(t)=\frac{d\vec v}{dt}=6t\hat i+4\hat j
$$

At \(t=1\):

$$
\vec v(1)=3\hat i+4\hat j
$$

$$
\vec a(1)=6\hat i+4\hat j
$$

Dot product:

$$
\vec v(1)\cdot\vec a(1)=3(6)+4(4)=34
$$

Use:

$$
\frac{d}{dt}\left(\frac12v^2\right)=\vec v\cdot\vec a
$$

Since:

$$
\vec v(1)\cdot\vec a(1)=34>0
$$

the speed is increasing at \(t=1\).

$$
\boxed{\text{speed is increasing}}
$$

**User result:** fully correct.

---

## M3 — Integral as Accumulation
**Difficulty: JEE Adv L3**

Evaluate:

$$
\int_0^2 |x^2-3x+2|\,dx
$$

Factor:

$$
x^2-3x+2=(x-1)(x-2)
$$

Zeros:

$$
x=1,\quad x=2
$$

Sign:

| Interval | Sign |
|---|---|
| \(0\le x<1\) | positive |
| \(1<x\le2\) | negative |

Therefore:

$$
\int_0^2 |x^2-3x+2|\,dx
=
\int_0^1(x^2-3x+2)\,dx
-
\int_1^2(x^2-3x+2)\,dx
$$

Antiderivative:

$$
\frac{x^3}{3}-\frac{3x^2}{2}+2x
$$

First area:

$$
\int_0^1(x^2-3x+2)\,dx=\frac56
$$

Second signed integral:

$$
\int_1^2(x^2-3x+2)\,dx=-\frac16
$$

Absolute contribution:

$$
\frac16
$$

Total:

$$
\boxed{1}
$$

### Error

The user differentiated instead of integrating.

```text
M3 error:
Differentiated instead of integrating.

Correction:
For definite integral / area / accumulation questions, integrate.
With absolute value, split at roots/sign-change points first.
```

---

## M3 Repair Problem
**Difficulty: JEE Adv L3**

Evaluate:

$$
\int_0^3 |x^2-4x+3|\,dx
$$

Factor:

$$
x^2-4x+3=(x-1)(x-3)
$$

Zeros:

$$
x=1,\quad x=3
$$

Sign:

| Interval | Sign |
|---|---|
| \(0\le x\le1\) | positive |
| \(1\le x\le3\) | negative |

Total area:

$$
\frac43+\frac43=\boxed{\frac83}
$$

**User answer:** correct.

---

## M4 — Linear ODE Review
**Difficulty: Olympiad L1**

Solve:

$$
\frac{dy}{dx}+2xy=2x,\qquad y(0)=3
$$

This is linear with:

$$
P(x)=2x,\qquad Q(x)=2x
$$

Integrating factor:

$$
\mu=e^{\int2x\,dx}=e^{x^2}
$$

Multiply by \(e^{x^2}\):

$$
e^{x^2}\frac{dy}{dx}+2xe^{x^2}y=2xe^{x^2}
$$

Left side:

$$
\frac{d}{dx}(e^{x^2}y)
$$

Therefore:

$$
\frac{d}{dx}(e^{x^2}y)=2xe^{x^2}
$$

Integrate:

$$
e^{x^2}y=e^{x^2}+C
$$

$$
y=1+Ce^{-x^2}
$$

Use \(y(0)=3\):

$$
3=1+C
$$

$$
C=2
$$

Final:

$$
\boxed{y=1+2e^{-x^2}}
$$

Equivalent:

$$
\boxed{y=\frac{e^{x^2}+2}{e^{x^2}}}
$$

**User answer:** correct.

---

# 4. Physics Diagnostic

## P1 — Kinematics + Calculus
**Difficulty: JEE Adv L2**

Given:

$$
v(t)=3t^2-12t+9,\qquad0\le t\le5
$$

Factor:

$$
v(t)=3(t-1)(t-3)
$$

Zeros:

$$
t=1,\quad t=3
$$

Sign:

| Interval | Sign |
|---|---|
| \(0<t<1\) | positive |
| \(1<t<3\) | negative |
| \(3<t<5\) | positive |

Net displacement:

$$
\int_0^5(3t^2-12t+9)\,dt
$$

Antiderivative:

$$
t^3-6t^2+9t
$$

Evaluate:

$$
125-150+45=\boxed{20}
$$

Total distance:

$$
\int_0^5|v(t)|\,dt
$$

Areas:

$$
0\to1:4,\qquad1\to3:4,\qquad3\to5:20
$$

Total:

$$
\boxed{28}
$$

Positive direction:

$$
\boxed{0\le t<1\quad\text{and}\quad3<t\le5}
$$

**User net displacement and total distance:** correct.

---

## P2 — Newton's Laws + Friction
**Difficulty: JEE Adv L3**

Given:

$$
m=5\,\text{kg},\quad F=40\,\text{N},\quad \theta=37^\circ
$$

$$
\mu_k=0.2,\quad g=10\,\text{m s}^{-2}
$$

$$
\sin37^\circ=\frac35,\qquad\cos37^\circ=\frac45
$$

Resolve the force:

$$
F_x=40\cdot\frac45=32\,\text{N}
$$

$$
F_y=40\cdot\frac35=24\,\text{N}
$$

Since the force is upward, it reduces the normal reaction.

Vertical balance:

$$
N+F_y=mg
$$

$$
N+24=50
$$

$$
\boxed{N=26\,\text{N}}
$$

Friction:

$$
f_k=\mu_kN=0.2(26)=\boxed{5.2\,\text{N}}
$$

Horizontal equation:

$$
F_x-f_k=ma
$$

$$
32-5.2=5a
$$

$$
a=\boxed{\frac{134}{25}\,\text{m s}^{-2}=5.36\,\text{m s}^{-2}}
$$

### Error

```text
P2 error:
Used incorrect vertical component or normal reaction.

Correction:
For a pull above the horizontal:
N = mg - F sin(theta)
not mg - F cos(theta).
Then fk = μN and a = (F cos(theta) - fk)/m.
```

---

## P2 Repair Problem
**Difficulty: JEE Adv L3**

Given:

$$
m=10\,\text{kg},\quad F=50\,\text{N},\quad \theta=53^\circ
$$

$$
\mu_k=0.25,\quad g=10
$$

$$
\sin53^\circ=\frac45,\qquad\cos53^\circ=\frac35
$$

Resolve:

$$
F_x=30\,\text{N},\qquad F_y=40\,\text{N}
$$

Normal:

$$
N=100-40=\boxed{60\,\text{N}}
$$

Friction:

$$
f_k=0.25(60)=\boxed{15\,\text{N}}
$$

Acceleration:

$$
30-15=10a
$$

$$
\boxed{a=1.5\,\text{m s}^{-2}}
$$

The user got \(N\) and \(f_k\) correct, but acceleration incorrect.

---

## P3 — Work-Energy with Variable Force
**Difficulty: JEE Adv L3**

Given:

$$
F(x)=kx-\lambda x^3
$$

Find speed at:

$$
x=\sqrt{\frac{k}{\lambda}}
$$

Use:

$$
W=\Delta K
$$

Since initial speed is zero:

$$
\int_0^{\sqrt{k/\lambda}}(kx-\lambda x^3)\,dx=\frac12mv^2
$$

Antiderivative:

$$
\frac{kx^2}{2}-\frac{\lambda x^4}{4}
$$

At:

$$
x^2=\frac{k}{\lambda},\qquad x^4=\frac{k^2}{\lambda^2}
$$

Work:

$$
W=\frac{k^2}{2\lambda}-\frac{k^2}{4\lambda}
$$

$$
\boxed{W=\frac{k^2}{4\lambda}}
$$

Then:

$$
\frac12mv^2=\frac{k^2}{4\lambda}
$$

$$
\boxed{v=\frac{k}{\sqrt{2m\lambda}}}
$$

### Error

```text
P3 error:
Integrated -λx^3 incorrectly.

Correction:
∫x^3 dx = x^4/4.
So ∫(kx - λx^3) dx = kx²/2 - λx⁴/4.
```

---

## P3 Repair Problem
**Difficulty: JEE Adv L3**

Given:

$$
F(x)=ax-bx^3
$$

Find speed at:

$$
x=\sqrt{\frac{a}{2b}}
$$

Work:

$$
W=\int_0^{\sqrt{a/(2b)}}(ax-bx^3)\,dx
$$

$$
W=\left[\frac{ax^2}{2}-\frac{bx^4}{4}\right]_0^{\sqrt{a/(2b)}}
$$

At:

$$
x^2=\frac{a}{2b},\qquad x^4=\frac{a^2}{4b^2}
$$

Therefore:

$$
W=\frac{a^2}{4b}-\frac{a^2}{16b}=\frac{3a^2}{16b}
$$

Use:

$$
W=\frac12mv^2
$$

$$
\boxed{v=\sqrt{\frac{3a^2}{8bm}}}
$$

**User answer:** correct.

---

## P4 — Rotation + Angular Momentum
**Difficulty: Olympiad L1**

Disk moment of inertia:

$$
I_{\text{disk}}=\frac12MR^2
$$

Clay at rim:

$$
I_{\text{clay}}=mR^2
$$

No external torque acts, so angular momentum is conserved:

$$
L_i=L_f
$$

Initial angular momentum:

$$
L_i=\frac12MR^2\omega_0
$$

Final moment of inertia:

$$
I_f=\frac12MR^2+mR^2
$$

Conservation:

$$
\frac12MR^2\omega_0=
\left(\frac12MR^2+mR^2\right)\omega_f
$$

Cancel \(R^2\):

$$
\frac12M\omega_0=\left(\frac M2+m\right)\omega_f
$$

Therefore:

$$
\boxed{\omega_f=\frac{M}{M+2m}\omega_0}
$$

---

# 5. Chemistry Diagnostic

## C1 — Mole + Limiting Reagent
**Difficulty: JEE Adv L2**

Reaction:

$$
2Al+3Cl_2\to2AlCl_3
$$

Given:

$$
5.4\,g\,Al,\qquad7.1\,g\,Cl_2
$$

Moles of aluminum:

$$
n_{Al}=\frac{5.4}{27}=\boxed{0.20\,\text{mol}}
$$

Moles of chlorine:

$$
n_{Cl_2}=\frac{7.1}{71}=\boxed{0.10\,\text{mol}}
$$

Limiting reagent comparison:

$$
\frac{n_{Al}}{2}=\frac{0.20}{2}=0.10
$$

$$
\frac{n_{Cl_2}}{3}=\frac{0.10}{3}=0.0333
$$

So:

$$
\boxed{Cl_2\text{ is limiting}}
$$

Product moles:

$$
n_{AlCl_3}=\frac23(0.10)=\boxed{0.0667\,\text{mol}}
$$

User answer \(0.06\) was close but should be \(0.0667\).

---

## C2 — Bohr Model
**Difficulty: JEE Adv L2**

For hydrogen:

$$
E_n=-\frac{13.6}{n^2}\text{ eV}
$$

For \(n=2\):

$$
E_2=-\frac{13.6}{4}=-3.4\,\text{eV}
$$

For \(n=4\):

$$
E_4=-\frac{13.6}{16}=-0.85\,\text{eV}
$$

Energy absorbed:

$$
\Delta E=E_4-E_2
$$

$$
\Delta E=-0.85-(-3.4)
$$

$$
\boxed{\Delta E=2.55\,\text{eV}}
$$

**User answer:** correct.

---

## C3 — Bonding + VSEPR
**Difficulty: JEE Adv L3**

For nitrate:

$$
NO_3^-
$$

Nitrate has three equivalent resonance structures because the double bond can be placed with any one of the three oxygen atoms.

$$
\boxed{3\text{ resonance structures}}
$$

Nitrogen has three electron domains and zero lone pairs.

Steric number:

$$
3
$$

Electron-domain geometry:

$$
\boxed{\text{trigonal planar}}
$$

Hybridization:

$$
\boxed{sp^2}
$$

Molecular shape:

$$
\boxed{\text{trigonal planar}}
$$

Average bond order:

$$
\frac{2+1+1}{3}=\boxed{\frac43}
$$

Because the resonance structures are equivalent:

$$
\boxed{\text{all }N-O\text{ bond lengths are equal}}
$$

User made one error: resonance structures should be 3, not 2.

---

## C4 — Thermodynamics
**Difficulty: Olympiad L1**

Given:

$$
\Delta H=-60\,\text{kJ mol}^{-1}
$$

$$
\Delta S=-150\,\text{J mol}^{-1}\text{K}^{-1}
$$

Convert entropy:

$$
-150\,\text{J mol}^{-1}\text{K}^{-1}
=
-0.150\,\text{kJ mol}^{-1}\text{K}^{-1}
$$

Use:

$$
\Delta G=\Delta H-T\Delta S
$$

Substitute:

$$
\Delta G=-60-T(-0.150)
$$

$$
\Delta G=-60+0.150T
$$

For spontaneity:

$$
\Delta G<0
$$

$$
-60+0.150T<0
$$

$$
0.150T<60
$$

$$
\boxed{T<400\,K}
$$

**User answer:** correct.

---

# 6. Formula Sheet — Day 7

## Mathematics

$$
f^{-1}(x)=2+\sqrt{x-3}
$$

$$
\vec v(t)=\frac{d\vec r}{dt}
$$

$$
\vec a(t)=\frac{d\vec v}{dt}
$$

$$
\frac{d}{dt}\left(\frac12v^2\right)=\vec v\cdot\vec a
$$

$$
\int |f(x)|\,dx=\text{split at sign-change points}
$$

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

$$
\mu=e^{\int P(x)\,dx}
$$

---

## Physics

$$
\text{net displacement}=\int v(t)\,dt
$$

$$
\text{total distance}=\int |v(t)|\,dt
$$

$$
F_x=F\cos\theta
$$

$$
F_y=F\sin\theta
$$

For upward pulling force:

$$
N=mg-F\sin\theta
$$

$$
f_k=\mu_kN
$$

$$
F_x-f_k=ma
$$

$$
W=\int F(x)\,dx
$$

$$
W=\frac12mv^2
$$

$$
L_i=L_f
$$

$$
I_{\text{disk}}=\frac12MR^2
$$

$$
I_{\text{rim particle}}=mR^2
$$

---

## Chemistry

$$
n=\frac{m}{M}
$$

$$
\text{limiting reagent: compare }\frac{n}{\text{coefficient}}
$$

$$
E_n=-\frac{13.6}{n^2}\text{ eV}
$$

$$
\Delta E=E_f-E_i
$$

$$
\text{average bond order}=\frac{\text{total bond order}}{\text{number of bonds}}
$$

$$
\Delta G=\Delta H-T\Delta S
$$

Spontaneous:

$$
\Delta G<0
$$

---

# 7. Error Log

| Code | Topic | Error | Correct repair |
|---|---|---|---|
| M3 | Integral as accumulation | Differentiated instead of integrating | Definite integral means accumulation; split absolute value at roots |
| P2 | Friction with angled pull | Normal reaction calculated incorrectly | For upward pull, \(N=mg-F\sin\theta\) |
| P2 Repair | Friction acceleration | Horizontal net force computed incorrectly | \(F_{net}=F_x-f_k\) |
| P3 | Variable force work | Integrated \(x^3\) incorrectly | \(\int x^3dx=x^4/4\) |
| C1 | Stoichiometry | Product amount rounded too low | \(0.10\times2/3=0.0667\) |
| C3 | Resonance | Nitrate resonance structures counted as 2 | \(NO_3^-\) has 3 equivalent resonance structures |

---

# 8. Short Ways and Memory Hooks

## Mathematics

- Inverse function: restrict the domain where the graph is monotonic.
- If the problem asks for area or accumulation, integrate.
- If absolute value appears inside an integral, split where the inside expression is zero.
- For speed increasing/decreasing, use \(ec v\cdot\vec a\).
- Linear ODE = integrating factor.

## Physics

- Net displacement uses signed velocity.
- Total distance uses absolute velocity.
- Pulling upward reduces normal force.
- Friction depends on normal reaction, not directly on weight.
- Variable force work is area under the \(F-x\) graph.
- Angular momentum conservation requires zero external torque.

## Chemistry

- Limiting reagent: compare moles divided by stoichiometric coefficient.
- Bohr absorption: final energy minus initial energy.
- Equivalent resonance means equal bond lengths.
- Convert entropy units before using \(\Delta G=\Delta H-T\Delta S\).

---

# 9. Common Traps

| Topic | Trap | Correction |
|---|---|---|
| Functions | finding inverse without restricting domain | restrict to one monotonic branch |
| Integrals | differentiating in accumulation problem | integrate |
| Absolute value integrals | not splitting at roots | split at sign changes |
| Kinematics | confusing displacement and distance | distance uses \(|v|\) |
| Friction | using \(mg\) for \(N\) despite angled force | vertical force changes \(N\) |
| Work-energy | integrating \(x^3\) as \(x^3/3\) | integral is \(x^4/4\) |
| Rotation | using energy for sticking collision | angular momentum is conserved, KE usually not |
| Stoichiometry | using mass ratio | use mole ratio |
| Thermodynamics | mixing J and kJ | convert units first |

---

# 10. Final Diagnostic Status

| Section | Status |
|---|---|
| Math diagnostic | Complete |
| Math repair | Complete |
| Physics diagnostic | Complete |
| Physics repairs | Complete |
| Chemistry diagnostic | Complete |
| Error log | Complete |
| 2-hour diagnostic output | Complete |

$$
\boxed{\text{Week 1 Day 7 Complete}}
$$
