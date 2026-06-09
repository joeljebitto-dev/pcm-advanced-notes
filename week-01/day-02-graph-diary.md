# Week 1 — Day 2
## Logs/Exponentials, Kinematics as Differential Equations, Bohr Model to Orbitals

## 0. Plan Row

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Logs, exponentials, and scaling laws | Complete |
| Physics | Kinematics as differential equations | Complete |
| Chemistry | Bohr model to orbitals | Complete |
| Required output | Graph diary | Complete |

---

# 1. Mathematics Detailed Reading
## Logs, Exponentials, and Scaling Laws

An exponential function has the variable in the exponent:

\[
y=a^x,\qquad a>0,\ a\ne1
\]

The most important exponential is \(e^x\), because it is its own derivative:

\[
\frac{d}{dx}e^x=e^x
\]

A logarithm is the inverse of an exponential:

\[
a^x=y\Longleftrightarrow \log_a y=x
\]

Examples covered:

\[
\log_2 32=5
\]

\[
\ln(e^7)=7
\]

\[
e^{\ln 12}=12
\]

The inverse relation works with domain restrictions:

\[
e^{\ln x}=x\quad (x>0)
\]

\[
\ln(e^x)=x\quad (x\in\mathbb R)
\]

## 1.1 Laws of Logs

\[
\log_a(xy)=\log_a x+\log_a y
\]

\[
\log_a\left(\frac xy\right)=\log_a x-\log_a y
\]

\[
\log_a(x^n)=n\log_a x
\]

\[
\log_a x=\frac{\ln x}{\ln a}
\]

All log arguments must be positive.

## 1.2 Scaling Laws

If

\[
y=kx^n,
\]

then multiplying \(x\) by \(a\) multiplies \(y\) by \(a^n\):

\[
x\to ax\Rightarrow y\to a^ny
\]

Examples:

\[
y=x^3,\\ x\to2x\Rightarrow y\to8y
\]

\[
A\propto r^2,\\ r\to3r\Rightarrow A\to9A
\]

This is crucial in dimensional reasoning, physics laws, geometric scaling, reaction rates, and data analysis.

## 1.3 Log-Log Plots

For a power law:

\[
y=kx^n
\]

Taking logs:

\[
\ln y=\ln k+n\ln x
\]

A graph of \(\ln y\) vs \(\ln x\) is a line with slope \(n\). This is used experimentally to identify power laws.

---

# 2. Physics Detailed Reading
## Kinematics as Differential Equations

Kinematics studies motion without asking what force caused it.

Position:

\[
x(t)
\]

Velocity:

\[
\boxed{v(t)=\frac{dx}{dt}}
\]

Acceleration:

\[
\boxed{a(t)=\frac{dv}{dt}=\frac{d^2x}{dt^2}}
\]

Thus:

\[
x(t)\xrightarrow{d/dt}v(t)\xrightarrow{d/dt}a(t)
\]

and reverse direction uses integration:

\[
a(t)\xrightarrow{\int}v(t)\xrightarrow{\int}x(t)
\]

## 2.1 Differentiation Example

\[
x(t)=3t^2+2t+1
\]

\[
v(t)=6t+2
\]

\[
a(t)=6
\]

## 2.2 Integration Example

If:

\[
a=6,
\]

then:

\[
v=\int6dt=6t+C
\]

Using \(v(0)=2\):

\[
v=6t+2
\]

Then:

\[
x=\int(6t+2)dt=3t^2+2t+C_2
\]

Using \(x(0)=1\):

\[
\boxed{x=3t^2+2t+1}
\]

## 2.3 Kinematics as ODEs

A differential equation connects a quantity to its derivatives:

\[
\frac{d^2x}{dt^2}=a(t,x,v)
\]

Examples:

| System | ODE |
|---|---|
| constant acceleration | \(x''=a\) |
| spring motion | \(x''=-\omega^2x\) |
| velocity drag | \(v'=-kv\) |
| free fall | \(y''=-g\) |

This prepares Day 6 ODEs.

## 2.4 Derivation of \(v^2=u^2+2as\)

\[
a=\frac{dv}{dt}=\frac{dv}{dx}\frac{dx}{dt}=v\frac{dv}{dx}
\]

\[
v\,dv=a\,dx
\]

Integrate:

\[
\int_u^v v\,dv=\int_0^s a\,dx
\]

\[
\frac{v^2-u^2}{2}=as
\]

\[
\boxed{v^2=u^2+2as}
\]

---

# 3. Chemistry Detailed Reading
## Bohr Model to Orbitals

The Bohr model introduced quantized energy levels. For hydrogen-like species:

\[
\boxed{E_n=-\frac{13.6Z^2}{n^2}\text{ eV}}
\]

For hydrogen, \(Z=1\):

\[
\boxed{E_n=-\frac{13.6}{n^2}\text{ eV}}
\]

Examples:

\[
E_1=-13.6\text{ eV}
\]

\[
E_2=-3.4\text{ eV}
\]

\[
E_3=-1.51\text{ eV}
\]

The negative sign means the electron is bound. Zero energy corresponds to a free electron infinitely far from the nucleus.

## 3.1 Transition Energy

\[
\Delta E=E_f-E_i
\]

For \(1\to2\):

\[
\Delta E=-3.4-(-13.6)=\boxed{10.2\text{ eV}}
\]

For \(2\to3\):

\[
\Delta E=-1.51-(-3.4)=\boxed{1.89\text{ eV}}
\]

Absorption corresponds to upward transitions. Emission corresponds to downward transitions.

## 3.2 From Orbits to Orbitals

Bohr used fixed circular orbits. Quantum mechanics uses orbitals: probability distributions for electron location.

| Bohr model | Quantum model |
|---|---|
| orbit | orbital |
| fixed path | probability cloud |
| exact radius | probability density |
| mostly hydrogen | general atomic structure |

Subshells:

| Subshell | \(l\) | Max electrons |
|---|---:|---:|
| s | 0 | 2 |
| p | 1 | 6 |
| d | 2 | 10 |
| f | 3 | 14 |

This leads directly into Day 3 electronic configuration and quantum numbers.

---

# 4. Formula Sheet

## Mathematics

\[
a^x=y\Longleftrightarrow \log_a y=x
\]

\[
\ln(e^x)=x
\]

\[
e^{\ln x}=x,\quad x>0
\]

\[
y=kx^n\Rightarrow x\to ax,\ y\to a^ny
\]

## Physics

\[
v=\frac{dx}{dt}
\]

\[
a=\frac{dv}{dt}=\frac{d^2x}{dt^2}
\]

\[
v=u+at
\]

\[
s=ut+\frac12at^2
\]

\[
v^2=u^2+2as
\]

## Chemistry

\[
E_n=-\frac{13.6Z^2}{n^2}\text{ eV}
\]

\[
\Delta E=E_f-E_i
\]

\[
E=\frac{hc}{\lambda}
\]

---

# 5. Solved Examples and Corrections

| Area | Problem | Correct answer |
|---|---|---|
| Math | \(\log_2 32\) | 5 |
| Math | \(\ln(e^7)\) | 7 |
| Math | \(e^{\ln 12}\) | 12 |
| Math | \(x^3\), double \(x\) | factor 8 |
| Math | area \(\propto r^2\), triple \(r\) | factor 9 |
| Physics | \(x=3t^2+2t+1\) | \(v=6t+2, a=6\) |
| Physics | \(v=4t^3-2t\) | \(a=12t^2-2\) |
| Chemistry | \(E_1\) H | \(-13.6\) eV |
| Chemistry | \(E_2\) H | \(-3.4\) eV |
| Chemistry | \(1\to2\) | 10.2 eV |

---

# 6. Required Output — Graph Diary

## Mathematics Graph Diary

### \(y=e^x\)
- domain: \(\mathbb R\)
- range: \((0,\infty)\)
- passes through \((0,1)\)
- increasing everywhere
- horizontal asymptote \(y=0\)

### \(y=\ln x\)
- domain: \((0,\infty)\)
- range: \(\mathbb R\)
- passes through \((1,0)\)
- vertical asymptote \(x=0\)
- inverse of \(e^x\)

### \(y=x^n\)
- exponent \(n\) controls scaling
- doubling input multiplies output by \(2^n\)

## Physics Graph Diary

For:

\[
x=3t^2+2t+1,
\]

\[
v=6t+2,
\]

\[
a=6.
\]

- \(x-t\): parabola
- \(v-t\): straight line
- \(a-t\): horizontal line

## Chemistry Graph Diary

Hydrogen energy levels:

\[
E_1=-13.6,
\quad E_2=-3.4,
\quad E_3=-1.51
\]

Levels become closer as \(n\) increases and approach zero from below.

---

# 7. Short Ways and Traps

## Short Ways

- Log asks: what exponent?
- Exponential undoes logarithm.
- Power scaling: input factor \(a\) gives output factor \(a^n\).
- Differentiate position to get velocity, velocity to get acceleration.
- Integrate acceleration to get velocity, velocity to get position.
- Bohr energies are negative because the electron is bound.

## Traps

| Trap | Fix |
|---|---|
| Taking log of negative real numbers | log argument must be positive |
| Forgetting base of log | \(\log_2\) and \(\ln\) differ |
| Treating \(v=x/t\) as instantaneous velocity | use \(v=dx/dt\) |
| Forgetting integration constants | apply initial conditions |
| Using Bohr model exactly for all atoms | exact only for hydrogen-like systems |

---

# 8. Completion Checklist

| Item | Status |
|---|---|
| Logs | Complete |
| Exponentials | Complete |
| Scaling laws | Complete |
| Kinematics by differentiation | Complete |
| Kinematics by integration | Complete |
| ODE interpretation of motion | Complete |
| Bohr energy levels | Complete |
| Transition energies | Complete |
| Orbitals introduction | Complete |
| Graph diary | Complete |

\[
\boxed{\text{Week 1 Day 2 Complete}}
\]
