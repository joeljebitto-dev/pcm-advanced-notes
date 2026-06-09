# Week 1 — Day 4
## Limits/Derivatives, Newton's Laws/FBD, Periodicity/Effective Nuclear Charge

## 0. Plan Row

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Limits, derivatives, and chain rule | Complete |
| Physics | Newton's laws, force models, and free-body systems | Complete |
| Chemistry | Periodicity, effective nuclear charge, and trends | Complete |
| Required output | Concept maps | Complete |

---

# 1. Mathematics Detailed Reading
## Limits, Derivatives, and Chain Rule

A limit describes what value a function approaches:

\[
\lim_{x\to a}f(x)=L
\]

Example:

\[
\lim_{x\to3}(x^2+2x)=3^2+2(3)=\boxed{15}
\]

Limits are the basis of derivatives and integrals.

## 1.1 Derivative Definition

\[
\boxed{f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}}
\]

The derivative is instantaneous rate of change and tangent slope.

Physics meaning:

\[
v=\frac{dx}{dt},\qquad a=\frac{dv}{dt}
\]

## 1.2 Power Rule

\[
\frac{d}{dx}x^n=nx^{n-1}
\]

Examples:

\[
\frac{d}{dx}x^4=4x^3
\]

\[
\frac{d}{dx}(5x^3-2x+7)=15x^2-2
\]

## 1.3 Chain Rule

If

\[
y=f(g(x)),
\]

then

\[
\boxed{\frac{dy}{dx}=f'(g(x))g'(x)}
\]

Short way: derivative of outside, keep inside, multiply by derivative of inside.

Examples corrected:

\[
\frac{d}{dx}(2x+5)^4=\boxed{8(2x+5)^3}
\]

not \(8(2x+5)^4\).

\[
\frac{d}{dx}(x^2+1)^3=\boxed{6x(x^2+1)^2}
\]

not \(6x(x^2+1)\).

Repair examples:

\[
\frac{d}{dx}(3x-1)^5=15(3x-1)^4
\]

\[
\frac{d}{dx}(x^2+4)^6=12x(x^2+4)^5
\]

---

# 2. Physics Detailed Reading
## Newton's Laws, Force Models, Free-Body Systems

Newton's laws connect forces to motion.

## 2.1 First Law

If net external force is zero:

\[
\sum\vec F=0
\]

then velocity is constant. Rest is a special case of constant velocity.

## 2.2 Second Law

\[
\boxed{\sum\vec F=m\vec a}
\]

Component form:

\[
\sum F_x=ma_x,
\qquad
\sum F_y=ma_y
\]

Example:

\[
m=5kg,\quad F=20N
\]

\[
a=\frac Fm=\boxed{4m/s^2}
\]

## 2.3 Third Law

Forces occur in pairs:

\[
\vec F_{AB}=-\vec F_{BA}
\]

They act on different bodies and should not both be placed on the same free-body diagram.

## 2.4 Force Models

| Force | Expression/Direction |
|---|---|
| Weight | \(mg\), downward |
| Normal | perpendicular to surface |
| Tension | along string |
| Kinetic friction | \(f_k=\mu_kN\) |
| Static friction | \(f_s\le\mu_sN\) |
| Spring | \(F=-kx\) |

## 2.5 Free-Body Diagram Method

1. Select object.
2. Draw all external forces acting on it.
3. Choose axes.
4. Resolve forces.
5. Apply \(\sum F=ma\).

Examples:

A \(10kg\) block on a horizontal table with \(g=10m/s^2\):

\[
W=100N,
\qquad N=100N
\]

A \(4kg\) block with \(30N\) applied and \(10N\) friction:

\[
F_{net}=20N
\]

\[
a=\frac{20}{4}=\boxed{5m/s^2}
\]

---

# 3. Chemistry Detailed Reading
## Periodicity, Effective Nuclear Charge, Trends

The periodic table is arranged by atomic number:

\[
Z=\text{number of protons}
\]

Chemical behavior is largely controlled by valence electrons.

## 3.1 Effective Nuclear Charge

Outer electrons do not feel the full nuclear charge because inner electrons shield them.

\[
\boxed{Z_{eff}=Z-S}
\]

where \(S\) is shielding.

Across a period:

- protons increase,
- electrons enter same shell,
- shielding does not increase enough,
- \(Z_{eff}\) increases.

Down a group:

- new shells are added,
- shielding increases,
- valence electrons are farther from nucleus.

## 3.2 Atomic Radius

Across a period:

\[
\boxed{\text{atomic radius decreases}}
\]

Down a group:

\[
\boxed{\text{atomic radius increases}}
\]

Important correction from session:

\[
\boxed{r_{Na}>r_{Cl}}
\]

because Na and Cl are in the same period and Cl has greater effective nuclear charge.

Repair example:

\[
\boxed{r_{Mg}>r_S}
\]

## 3.3 Ionization Energy

Ionization energy is energy needed to remove an electron from a gaseous atom.

Across a period:

\[
\boxed{IE\text{ generally increases}}
\]

Down a group:

\[
\boxed{IE\text{ generally decreases}}
\]

Reason: down a group, electrons are farther away and more shielded.

Exceptions occur due to subshell stability and pairing effects, e.g. Be/B and N/O anomalies.

---

# 4. Formula Sheet

## Mathematics

\[
\lim_{x\to a}f(x)
\]

\[
f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}
\]

\[
\frac{d}{dx}x^n=nx^{n-1}
\]

\[
\frac{d}{dx}f(g(x))=f'(g(x))g'(x)
\]

## Physics

\[
\sum\vec F=m\vec a
\]

\[
W=mg
\]

\[
f_k=\mu_kN
\]

\[
f_s\le\mu_sN
\]

\[
F_{spring}=-kx
\]

## Chemistry

\[
Z_{eff}=Z-S
\]

Across period:

\[
Z_{eff}\uparrow,
\quad r\downarrow,
\quad IE\uparrow
\]

Down group:

\[
\text{shells}\uparrow,
\quad r\uparrow,
\quad IE\downarrow
\]

---

# 5. Important Derivations

## 5.1 Chain Rule Idea

Let:

\[
y=f(u),\quad u=g(x)
\]

Then:

\[
\frac{dy}{dx}=\frac{dy}{du}\frac{du}{dx}
\]

\[
\boxed{\frac{d}{dx}f(g(x))=f'(g(x))g'(x)}
\]

## 5.2 Effective Nuclear Charge Trend

Across a period, \(Z\) increases but electrons are added to the same shell. Same-shell shielding is weak, so \(Z_{eff}\) increases. The nucleus pulls valence electrons closer, so atomic radius decreases.

---

# 6. Solved Examples and Corrections

| Area | Problem | Correct answer | Note |
|---|---|---|---|
| Math | \(\lim_{x\to3}(x^2+2x)\) | 15 | direct substitution |
| Math | \(d(x^4)/dx\) | \(4x^3\) | power rule |
| Math | \(d(2x+5)^4/dx\) | \(8(2x+5)^3\) | chain rule |
| Math | \(d(x^2+1)^3/dx\) | \(6x(x^2+1)^2\) | chain rule |
| Physics | \(m=5,F=20\) | \(a=4\) | \(F=ma\) |
| Physics | \(10kg\) on table | \(W=N=100N\) | no vertical acceleration |
| Physics | \(m=4,F=30,f=10\) | \(a=5\) | net force 20N |
| Chemistry | larger radius Na/Cl | Na | period trend |
| Chemistry | larger radius Mg/S | Mg | period trend |

---

# 7. Required Output — Concept Maps

## Mathematics

```text
Limit
  -> derivative definition
  -> instantaneous rate/tangent slope
  -> differentiation rules
  -> chain rule for composite functions
```

## Physics

```text
Choose object
  -> draw free-body diagram
  -> resolve forces
  -> apply Sigma F = ma
  -> solve acceleration/normal/tension/friction
```

## Chemistry

```text
Atomic number Z
  -> nuclear attraction + shielding
  -> effective nuclear charge Zeff
  -> atomic radius / ionization energy / electronegativity
  -> periodic trends
```

---

# 8. Short Ways and Traps

## Short Ways

- Limit = value approached.
- Derivative = instant slope.
- Chain rule = outside derivative × inside derivative.
- FBD first, equations second.
- Across period, electrons are pulled tighter.
- Down group, new shell dominates.

## Traps

| Trap | Fix |
|---|---|
| Forgetting chain multiplier | multiply by derivative of inside |
| Not reducing power | \(n(g)^{n-1}g'\) |
| Putting action-reaction pair on same FBD | they act on different objects |
| Assuming \(N=mg\) always | check vertical acceleration/geometry |
| Saying radius increases across period | it decreases |
| Ignoring shielding | use \(Z_{eff}\) |

---

# 9. Completion Checklist

| Item | Status |
|---|---|
| Limits | Complete |
| Derivative definition | Complete |
| Power rule | Complete |
| Chain rule | Complete |
| Newton's laws | Complete |
| Force models | Complete |
| Free-body diagrams | Complete |
| Effective nuclear charge | Complete |
| Periodic trends | Complete |
| Concept maps | Complete |

\[
\boxed{\text{Week 1 Day 4 Complete}}
\]
