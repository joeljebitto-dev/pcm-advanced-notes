# Week 1 — Day 6  
## First-Order ODEs, Rotation, and Thermodynamics

## 0. Plan Row and Completion Status

| Block | Required topic | Status |
|---|---|---|
| Mathematics | First-order ODEs; separable and linear equations | Complete |
| Physics | Rotation: torque, angular momentum, rigid-body energy | Complete |
| Chemistry | Thermodynamics: \(U,H,S,G\) | Complete |
| Required output | ODE model sheet | Complete |

---

# 1. Mathematics Detailed Reading  
## First-Order ODEs: Separable, Linear, and Autonomous Models

## 1.1 What an ODE Is

An ordinary differential equation relates an unknown function to its derivatives with respect to one independent variable.

A first-order ODE has the general form:

$$
\frac{dy}{dx}=f(x,y)
$$

The highest derivative is first derivative.

Examples:

$$
\frac{dy}{dx}=xy
$$

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

$$
\frac{dy}{dt}=y(1-y)
$$

ODEs convert local rate laws into global behavior. This is why they appear in mechanics, reaction kinetics, thermodynamics, electronics, population models, and cooling laws.

---

## 1.2 General Solution and Particular Solution

A first-order ODE usually gives a family of curves containing one arbitrary constant.

Example:

$$
\frac{dy}{dx}=2x
$$

Integrating:

$$
y=x^2+C
$$

This is the general solution.

If:

$$
y(0)=3
$$

then:

$$
3=0+C
$$

so:

$$
C=3
$$

The particular solution is:

$$
y=x^2+3
$$

Initial conditions select one member from the family of solution curves.

---

## 1.3 Separable ODEs

A separable ODE can be written as:

$$
\frac{dy}{dx}=g(x)h(y)
$$

Then:

$$
\frac{dy}{h(y)}=g(x)\,dx
$$

and both sides can be integrated.

### Example: Exponential Growth and Decay

$$
\frac{dy}{dt}=ky
$$

Separate:

$$
\frac{dy}{y}=k\,dt
$$

Integrate:

$$
\ln|y|=kt+C
$$

Exponentiate:

$$
y=Ce^{kt}
$$

Using \(y(0)=y_0\):

$$
\boxed{y=y_0e^{kt}}
$$

If \(k>0\), the model grows.  
If \(k<0\), the model decays.

---

## 1.4 First-Order Chemical Decay Model

For a first-order reaction:

$$
A\to \text{products}
$$

the rate law is:

$$
-\frac{d[A]}{dt}=k[A]
$$

so:

$$
\frac{d[A]}{dt}=-k[A]
$$

Separate:

$$
\frac{d[A]}{[A]}=-k\,dt
$$

Integrate:

$$
\ln[A]=-kt+C
$$

Using:

$$
[A](0)=[A]_0
$$

we get:

$$
\boxed{[A]=[A]_0e^{-kt}}
$$

Half-life occurs when:

$$
[A]=\frac{[A]_0}{2}
$$

Thus:

$$
\frac12=e^{-kt_{1/2}}
$$

$$
\ln2=kt_{1/2}
$$

$$
\boxed{t_{1/2}=\frac{\ln2}{k}}
$$

This is a direct bridge between Day 2 exponentials, Day 5 integrals, and Day 6 ODEs.

---

## 1.5 Linear First-Order ODEs

A first-order linear ODE has form:

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

The integrating factor is:

$$
\boxed{\mu(x)=e^{\int P(x)\,dx}}
$$

Multiplying the ODE by \(\mu(x)\):

$$
\mu\frac{dy}{dx}+\mu P(x)y=\mu Q(x)
$$

The left side becomes:

$$
\frac{d}{dx}[\mu(x)y]
$$

Thus:

$$
\frac{d}{dx}[\mu y]=\mu Q
$$

Integrate:

$$
\mu y=\int \mu Q\,dx+C
$$

So:

$$
\boxed{
y=\frac{1}{\mu(x)}
\left[
\int \mu(x)Q(x)\,dx+C
\right]
}
$$

---

## 1.6 Why the Integrating Factor Works

We want:

$$
\mu\frac{dy}{dx}+\mu P y
$$

to become:

$$
\frac{d}{dx}(\mu y)
$$

But by product rule:

$$
\frac{d}{dx}(\mu y)=\mu\frac{dy}{dx}+y\frac{d\mu}{dx}
$$

So we need:

$$
\frac{d\mu}{dx}=\mu P
$$

Separate:

$$
\frac{d\mu}{\mu}=P\,dx
$$

Integrate:

$$
\ln\mu=\int P\,dx
$$

Therefore:

$$
\boxed{\mu=e^{\int P\,dx}}
$$

The integrating factor is the multiplier that forces the product rule to appear.

---

## 1.7 Autonomous ODEs and Stability

An autonomous equation has form:

$$
\frac{dy}{dt}=f(y)
$$

Equilibria occur when:

$$
f(y)=0
$$

If the system starts at an equilibrium point, it stays there.

Classification:

| Phase-line behavior | Type |
|---|---|
| arrows point toward equilibrium | stable |
| arrows point away | unstable |
| arrows pass same direction through point | semistable |

Example from the session:

$$
\frac{dy}{dt}=y(y-1)^2(y-3)
$$

Equilibria:

$$
y=0,\quad y=1,\quad y=3
$$

Sign intervals:

```text
(-∞,0): positive
(0,1): negative
(1,3): negative
(3,∞): positive
```

Classification:

$$
\boxed{y=0\text{ stable}}
$$

$$
\boxed{y=1\text{ semistable}}
$$

$$
\boxed{y=3\text{ unstable}}
$$

---

## 1.8 Very Hard Nonlinear ODE Example

Problem:

$$
\frac{dy}{dx}=y^2-x^2,\qquad y(0)=0
$$

This is nonlinear and does not have a simple elementary solution, but it can be studied using symmetry and power series.

### Oddness

Define:

$$
u(x)=-y(-x)
$$

Then:

$$
u'(x)=y'(-x)
$$

Using the ODE:

$$
y'(-x)=y(-x)^2-x^2
$$

Since:

$$
u(x)^2=y(-x)^2
$$

we get:

$$
u'=u^2-x^2
$$

and:

$$
u(0)=0
$$

By uniqueness:

$$
u(x)=y(x)
$$

Therefore:

$$
\boxed{y(-x)=-y(x)}
$$

so the solution is odd.

### Power Series

The first five nonzero terms are:

$$
\boxed{
y(x)
=
-\frac{x^3}{3}
+
\frac{x^7}{63}
-
\frac{2x^{11}}{2079}
+
\frac{13x^{15}}{218295}
-
\frac{46x^{19}}{12442815}
+\cdots
}
$$

For small positive \(x\):

$$
y(x)\approx -\frac{x^3}{3}
$$

so:

$$
\boxed{y(x)<x\text{ for small }x>0}
$$

Substitution:

$$
z=y+x
$$

gives:

$$
\boxed{z'=1+z^2-2xz}
$$

This exposes Riccati-type structure.

---

# 2. Physics Detailed Reading  
## Rotation: Torque, Angular Momentum, and Rigid-Body Energy

## 2.1 Big Picture

Rotation is translational mechanics around an axis.

| Translation | Rotation |
|---|---|
| Position \(x\) | Angle \(\theta\) |
| Velocity \(v\) | Angular velocity \(\omega\) |
| Acceleration \(a\) | Angular acceleration \(\alpha\) |
| Mass \(m\) | Moment of inertia \(I\) |
| Force \(F\) | Torque \(\tau\) |
| Momentum \(p=mv\) | Angular momentum \(L=I\omega\) |
| Kinetic energy \(\frac12mv^2\) | Rotational kinetic energy \(\frac12I\omega^2\) |

The analogy is useful, but rotation has extra geometry: axis choice, lever arm, cross product, and mass distribution.

---

## 2.2 Angular Variables

Angular displacement:

$$
\theta=\frac{s}{r}
$$

Angular velocity:

$$
\omega=\frac{d\theta}{dt}
$$

Angular acceleration:

$$
\alpha=\frac{d\omega}{dt}
$$

For a point at distance \(r\):

$$
s=r\theta
$$

$$
v=r\omega
$$

$$
a_t=r\alpha
$$

$$
a_c=r\omega^2
$$

Tangential acceleration changes speed.  
Centripetal acceleration changes direction.

---

## 2.3 Constant Angular Acceleration

If \(\alpha\) is constant:

$$
\omega=\omega_0+\alpha t
$$

$$
\theta=\theta_0+\omega_0t+\frac12\alpha t^2
$$

$$
\omega^2=\omega_0^2+2\alpha(\theta-\theta_0)
$$

Use these only when angular acceleration is constant. If torque depends on angle or time, energy or differential equations are usually safer.

---

## 2.4 Torque

Torque measures the turning effect of a force.

Vector definition:

$$
\boxed{\vec\tau=\vec r\times\vec F}
$$

Magnitude:

$$
\boxed{\tau=rF\sin\phi}
$$

where \(\phi\) is the angle between \(\vec r\) and \(\vec F\).

Lever-arm form:

$$
\boxed{\tau=F r_\perp}
$$

where \(r_\perp\) is the perpendicular distance from the axis to the line of action of the force.

A force creates more torque when it is larger, farther from the axis, and more perpendicular to the radius vector.

---

## 2.5 Rotational Newton's Law

For fixed-axis rotation with constant \(I\):

$$
\boxed{\sum\tau=I\alpha}
$$

The deeper general law is:

$$
\boxed{\sum\vec\tau_{\text{ext}}=\frac{d\vec L}{dt}}
$$

If \(I\) is constant and \(L=I\omega\):

$$
\tau=I\frac{d\omega}{dt}=I\alpha
$$

If \(I\) changes:

$$
\tau=\frac{d}{dt}(I\omega)=I\alpha+\omega\frac{dI}{dt}
$$

This is why a skater spins faster when pulling arms inward.

---

## 2.6 Moment of Inertia

For point masses:

$$
\boxed{I=\sum m_ir_i^2}
$$

For continuous bodies:

$$
\boxed{I=\int r^2\,dm}
$$

Moment of inertia is rotational mass. More mass farther from the axis means larger \(I\).

Standard results:

| Body | Axis | Moment of inertia |
|---|---|---|
| Ring | central axis | \(MR^2\) |
| Solid disk | central axis | \(\frac12MR^2\) |
| Solid sphere | diameter | \(\frac25MR^2\) |
| Hollow sphere | diameter | \(\frac23MR^2\) |
| Rod | center, perpendicular to length | \(\frac{1}{12}ML^2\) |
| Rod | end, perpendicular to length | \(\frac13ML^2\) |

---

## 2.7 Parallel Axis Theorem

If \(I_{\text{cm}}\) is known about an axis through the center of mass, then about a parallel axis distance \(d\) away:

$$
\boxed{I=I_{\text{cm}}+Md^2}
$$

Example: rod about one end.

$$
I_{\text{cm}}=\frac{1}{12}ML^2
$$

$$
d=\frac L2
$$

$$
I_{\text{end}}=\frac{1}{12}ML^2+M\left(\frac L2\right)^2
$$

$$
\boxed{I_{\text{end}}=\frac13ML^2}
$$

---

## 2.8 Angular Momentum

For a particle:

$$
\boxed{\vec L=\vec r\times\vec p}
$$

Since:

$$
\vec p=m\vec v
$$

$$
\boxed{\vec L=\vec r\times m\vec v}
$$

Magnitude:

$$
\boxed{L=rmv\sin\phi}
$$

If \(b\) is the perpendicular distance from origin to the line of motion:

$$
\boxed{L=mvb}
$$

For a rigid body rotating about a fixed symmetry axis:

$$
\boxed{L=I\omega}
$$

---

## 2.9 Conservation of Angular Momentum

If external torque is zero:

$$
\sum\vec\tau_{\text{ext}}=0
$$

then:

$$
\frac{d\vec L}{dt}=0
$$

so:

$$
\boxed{\vec L=\text{constant}}
$$

Angular momentum is conserved when net external torque about the chosen point is zero.

---

## 2.10 Rotational Kinetic Energy

For a rigid body rotating about a fixed axis:

$$
\boxed{K_{\text{rot}}=\frac12I\omega^2}
$$

Derivation:

Each mass element has speed:

$$
v_i=r_i\omega
$$

Total kinetic energy:

$$
K=\sum \frac12m_iv_i^2
$$

$$
K=\sum\frac12m_i(r_i\omega)^2
$$

$$
K=\frac12\omega^2\sum m_ir_i^2
$$

Since:

$$
I=\sum m_ir_i^2
$$

we get:

$$
\boxed{K=\frac12I\omega^2}
$$

---

## 2.11 Rotational Work-Energy

Rotational work:

$$
dW=\tau\,d\theta
$$

So:

$$
\boxed{W=\int_{\theta_i}^{\theta_f}\tau(\theta)\,d\theta}
$$

Rotational work-energy theorem:

$$
\boxed{W_{\text{rot}}=\Delta K_{\text{rot}}}
$$

If torque depends on angular position, use:

$$
W=\int \tau(\theta)\,d\theta
$$

not constant-acceleration formulas.

Session problem:

$$
\tau(\theta)=\tau_0\cos\theta
$$

from:

$$
0\to\frac{\pi}{3}
$$

Work:

$$
W=\int_0^{\pi/3}\tau_0\cos\theta\,d\theta
$$

$$
W=\tau_0\sin\frac{\pi}{3}
$$

$$
W=\frac{\sqrt3}{2}\tau_0
$$

Starting from rest:

$$
\frac12I\omega^2=\frac{\sqrt3}{2}\tau_0
$$

$$
\boxed{\omega=\sqrt{\frac{\sqrt3\tau_0}{I}}}
$$

---

## 2.12 Rolling Without Slipping

Rolling condition:

$$
\boxed{v_{\text{cm}}=R\omega}
$$

Total kinetic energy:

$$
\boxed{K=\frac12Mv_{\text{cm}}^2+\frac12I_{\text{cm}}\omega^2}
$$

For rolling down height \(h\):

$$
Mgh=\frac12Mv^2+\frac12I\omega^2
$$

For a solid sphere:

$$
I=\frac25MR^2
$$

and:

$$
\omega=\frac vR
$$

Thus:

$$
Mgh=\frac12Mv^2+\frac12\left(\frac25MR^2\right)\left(\frac vR\right)^2
$$

$$
Mgh=\frac12Mv^2+\frac15Mv^2
$$

$$
Mgh=\frac{7}{10}Mv^2
$$

$$
\boxed{v=\sqrt{\frac{10gh}{7}}}
$$

---

# 3. Chemistry Detailed Reading  
## Thermodynamics: \(U,H,S,G\)

## 3.1 Big Picture

Thermodynamics studies energy transfer and the direction of natural processes.

| Symbol | Name | Meaning |
|---|---|---|
| \(U\) | internal energy | microscopic stored energy |
| \(H\) | enthalpy | heat content at constant pressure |
| \(S\) | entropy | energy dispersal / microstates |
| \(G\) | Gibbs free energy | spontaneity criterion at constant \(T,P\) |

Short memory:

```text
U = stored energy
H = heat at constant pressure
S = dispersal
G = useful driving energy
```

---

## 3.2 System, Surroundings, Universe

$$
\text{Universe}=\text{System}+\text{Surroundings}
$$

| Type | Matter exchange | Energy exchange |
|---|---|---|
| Open | yes | yes |
| Closed | no | yes |
| Isolated | no | no |

---

## 3.3 State Functions and Path Functions

State functions depend only on initial and final states.

Path functions depend on the path taken.

| State functions | Path functions |
|---|---|
| \(U\) | \(q\) |
| \(H\) | \(w\) |
| \(S\) |  |
| \(G\) |  |
| \(P,V,T\) |  |

Thus:

$$
\Delta U,\Delta H,\Delta S,\Delta G
$$

are state-function changes, but \(q\) and \(w\) are path-dependent.

---

## 3.4 Internal Energy \(U\)

Internal energy includes microscopic translational, rotational, vibrational, electronic, intermolecular, and bond energies.

Change in internal energy:

$$
\Delta U=U_f-U_i
$$

First law:

$$
\boxed{\Delta U=q+w}
$$

Chemistry sign convention:

| Quantity | Positive when |
|---|---|
| \(q\) | heat enters system |
| \(w\) | work is done on system |

Pressure-volume work:

$$
\boxed{w=-P_{\text{ext}}\Delta V}
$$

Expansion:

$$
\Delta V>0\Rightarrow w<0
$$

Compression:

$$
\Delta V<0\Rightarrow w>0
$$

---

## 3.5 Enthalpy \(H\)

Definition:

$$
\boxed{H=U+PV}
$$

At constant pressure:

$$
\boxed{\Delta H=q_p}
$$

At constant volume:

$$
\boxed{\Delta U=q_v}
$$

For ideal gases:

$$
\boxed{\Delta H=\Delta U+\Delta n_gRT}
$$

where:

$$
\Delta n_g=
\text{gaseous product moles}
-
\text{gaseous reactant moles}
$$

Session drill:

$$
2CO(g)+O_2(g)\to2CO_2(g)
$$

$$
\Delta n_g=2-3=-1
$$

Therefore:

$$
\boxed{\Delta H=\Delta U-RT}
$$

---

## 3.6 Entropy \(S\)

Entropy measures energy dispersal and number of microstates.

Boltzmann relation:

$$
\boxed{S=k\ln W}
$$

For reversible heat transfer:

$$
\boxed{\Delta S=\frac{q_{\text{rev}}}{T}}
$$

More generally:

$$
\boxed{\Delta S=\int\frac{\delta q_{\text{rev}}}{T}}
$$

Second law:

$$
\boxed{\Delta S_{\text{universe}}>0\text{ for spontaneous processes}}
$$

At equilibrium:

$$
\boxed{\Delta S_{\text{universe}}=0}
$$

Entropy increases for:

- solid to liquid
- liquid to gas
- increase in gas moles
- mixing
- temperature increase

---

## 3.7 Gibbs Free Energy \(G\)

Definition:

$$
\boxed{G=H-TS}
$$

At constant temperature:

$$
\boxed{\Delta G=\Delta H-T\Delta S}
$$

At constant temperature and pressure:

| Condition | Meaning |
|---|---|
| \(\Delta G<0\) | spontaneous |
| \(\Delta G=0\) | equilibrium |
| \(\Delta G>0\) | non-spontaneous forward |

Temperature dependence:

| \(\Delta H\) | \(\Delta S\) | Spontaneity |
|---:|---:|---|
| negative | positive | all \(T\) |
| positive | negative | no \(T\) |
| positive | positive | high \(T\) |
| negative | negative | low \(T\) |

---

## 3.8 Gibbs Free Energy and Equilibrium

For a reaction:

$$
\boxed{\Delta G=\Delta G^\circ+RT\ln Q}
$$

At equilibrium:

$$
\Delta G=0
$$

and:

$$
Q=K
$$

So:

$$
0=\Delta G^\circ+RT\ln K
$$

Therefore:

$$
\boxed{\Delta G^\circ=-RT\ln K}
$$

If \(\Delta G^\circ<0\), then \(K>1\). Products are favored.

If \(\Delta G^\circ>0\), then \(K<1\). Reactants are favored.

---

# 4. Required Output — ODE Model Sheet

## 4.1 Core ODE Models

### Exponential Model

$$
\frac{dy}{dt}=ky
$$

$$
y=y_0e^{kt}
$$

For decay:

$$
\frac{dy}{dt}=-ky
$$

$$
y=y_0e^{-kt}
$$

Half-life:

$$
t_{1/2}=\frac{\ln2}{k}
$$

---

### Separable Model

$$
\frac{dy}{dx}=g(x)h(y)
$$

$$
\frac{dy}{h(y)}=g(x)\,dx
$$

$$
\int\frac{dy}{h(y)}=\int g(x)\,dx
$$

---

### Linear Model

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

$$
\mu=e^{\int P(x)\,dx}
$$

$$
\frac{d}{dx}(\mu y)=\mu Q
$$

---

### Autonomous Model

$$
\frac{dy}{dt}=f(y)
$$

Equilibrium:

$$
f(y)=0
$$

Stability from phase-line arrows.

---

## 4.2 Cross-Subject Models

### First-order chemical reaction

$$
\frac{d[A]}{dt}=-k[A]
$$

$$
[A]=[A]_0e^{-kt}
$$

### Kinematics

$$
\frac{dx}{dt}=v
$$

$$
\frac{dv}{dt}=a
$$

### Rotation

$$
\frac{d\theta}{dt}=\omega
$$

$$
I\frac{d\omega}{dt}=\tau
$$

If torque depends on angle:

$$
I\omega\frac{d\omega}{d\theta}=\tau(\theta)
$$

### Cooling

$$
\frac{dT}{dt}=-k(T-T_s)
$$

$$
T=T_s+(T_0-T_s)e^{-kt}
$$

---

# 5. Formula Sheet

## Mathematics

$$
\frac{dy}{dx}=g(x)h(y)
$$

$$
\frac{dy}{h(y)}=g(x)\,dx
$$

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

$$
\mu=e^{\int P(x)\,dx}
$$

$$
y=\frac{1}{\mu}\left[\int \mu Q\,dx+C\right]
$$

$$
\frac{dy}{dt}=f(y)
$$

---

## Physics

$$
\omega=\frac{d\theta}{dt}
$$

$$
\alpha=\frac{d\omega}{dt}
$$

$$
\vec\tau=\vec r\times\vec F
$$

$$
\tau=rF\sin\phi
$$

$$
\sum\tau=I\alpha
$$

$$
I=\sum m_ir_i^2
$$

$$
I=I_{\text{cm}}+Md^2
$$

$$
\vec L=\vec r\times\vec p
$$

$$
L=I\omega
$$

$$
K_{\text{rot}}=\frac12I\omega^2
$$

$$
W=\int\tau\,d\theta
$$

$$
v_{\text{cm}}=R\omega
$$

---

## Chemistry

$$
\Delta U=q+w
$$

$$
w=-P_{\text{ext}}\Delta V
$$

$$
H=U+PV
$$

$$
\Delta H=\Delta U+\Delta n_gRT
$$

$$
S=k\ln W
$$

$$
\Delta S=\frac{q_{\text{rev}}}{T}
$$

$$
G=H-TS
$$

$$
\Delta G=\Delta H-T\Delta S
$$

$$
\Delta G^\circ=-RT\ln K
$$

---

# 6. Important Derivations

## 6.1 Integrating Factor

Starting from:

$$
\frac{dy}{dx}+P(x)y=Q(x)
$$

We want:

$$
\mu\frac{dy}{dx}+\mu Py=\frac{d}{dx}(\mu y)
$$

By product rule:

$$
\frac{d}{dx}(\mu y)=\mu\frac{dy}{dx}+y\frac{d\mu}{dx}
$$

So:

$$
\frac{d\mu}{dx}=\mu P
$$

$$
\frac{d\mu}{\mu}=P\,dx
$$

$$
\boxed{\mu=e^{\int P\,dx}}
$$

---

## 6.2 Rotational Kinetic Energy

Each mass element:

$$
v_i=r_i\omega
$$

Total kinetic energy:

$$
K=\sum\frac12m_iv_i^2
$$

$$
K=\sum\frac12m_i(r_i\omega)^2
$$

$$
K=\frac12\omega^2\sum m_ir_i^2
$$

Since:

$$
I=\sum m_ir_i^2
$$

$$
\boxed{K=\frac12I\omega^2}
$$

---

## 6.3 Rolling Sphere Speed

$$
Mgh=\frac12Mv^2+\frac12I\omega^2
$$

For solid sphere:

$$
I=\frac25MR^2
$$

and:

$$
\omega=\frac vR
$$

Therefore:

$$
Mgh=\frac12Mv^2+\frac15Mv^2
$$

$$
Mgh=\frac{7}{10}Mv^2
$$

$$
\boxed{v=\sqrt{\frac{10gh}{7}}}
$$

---

## 6.4 Gibbs-Equilibrium Relation

$$
\Delta G=\Delta G^\circ+RT\ln Q
$$

At equilibrium:

$$
\Delta G=0,\quad Q=K
$$

So:

$$
0=\Delta G^\circ+RT\ln K
$$

$$
\boxed{\Delta G^\circ=-RT\ln K}
$$

---

# 7. Solved Examples and Corrections

## Mathematics

| Problem | Correct answer | Note |
|---|---|---|
| \(\frac{dy}{dx}=y^2,\ y(0)=1\) | \(y=\frac{1}{1-x}\) | separable |
| validity interval | \((-\infty,1)\) | blow-up at \(x=1\) |
| \(x\frac{dy}{dx}+2y=x^2,\ y(1)=0\) | \(\frac{x^4-1}{4x^2}\) | integrating factor |
| \(y(y-1)^2(y-3)\) equilibria | \(0,1,3\) | autonomous |
| classification | stable, semistable, unstable | phase line |

## Physics

| Problem | Correct answer | Note |
|---|---|---|
| \(\tau=\tau_0\cos\theta\), \(0\to\pi/3\) | \(\omega=\sqrt{\frac{\sqrt3\tau_0}{I}}\) | use work-energy |
| rolling solid sphere | \(v=\sqrt{\frac{10gh}{7}}\) | include rotational KE |
| particle angular momentum | \(L=mvb\) | impact parameter |

## Chemistry

| Problem | Correct answer | Note |
|---|---|---|
| absorbs \(800J\), does \(300J\) work | \(\Delta U=500J\) | work by system is negative |
| \(2CO+O_2\to2CO_2\) | \(\Delta H=\Delta U-RT\) | \(\Delta n_g=-1\) |
| \(\Delta H=40kJ,\Delta S=100J/K\) | \(T>400K\) | convert units |
| \(\Delta G^\circ=-5.708kJ\) at \(298K\) | \(K\approx10\) | use \(-RT\ln K\) |

---

# 8. Advanced Practice Record

## Mathematics

### Problem 1 — Finite-time blow-up  
**Difficulty: JEE Adv L3**

$$
\frac{dy}{dx}=y^2,\quad y(0)=1
$$

Correct:

$$
\boxed{y=\frac{1}{1-x}}
$$

Largest interval containing \(0\):

$$
\boxed{(-\infty,1)}
$$

---

### Problem 2 — Linear ODE  
**Difficulty: JEE Adv L3**

$$
x\frac{dy}{dx}+2y=x^2,\quad y(1)=0
$$

Correct:

$$
\boxed{y=\frac{x^4-1}{4x^2}}
$$

---

### Problem 3 — Stability  
**Difficulty: Olympiad L1**

$$
\frac{dy}{dt}=y(y-1)^2(y-3)
$$

Correct:

$$
\boxed{0\text{ stable},\quad1\text{ semistable},\quad3\text{ unstable}}
$$

---

### Very Hard Nonlinear ODE  
**Difficulty: Olympiad L3**

$$
\frac{dy}{dx}=y^2-x^2,\quad y(0)=0
$$

Correct conclusions:

$$
\boxed{y(-x)=-y(x)}
$$

$$
\boxed{
y(x)
=
-\frac{x^3}{3}
+
\frac{x^7}{63}
-
\frac{2x^{11}}{2079}
+
\frac{13x^{15}}{218295}
-
\frac{46x^{19}}{12442815}
+\cdots
}
$$

---

## Physics

### Variable Torque  
**Difficulty: JEE Adv L3**

$$
\tau(\theta)=\tau_0\cos\theta
$$

Correct:

$$
\boxed{\omega=\sqrt{\frac{\sqrt3\tau_0}{I}}}
$$

Mistake note: torque depended on angle, so work-energy was required.

---

### Rolling Solid Sphere  
**Difficulty: JEE Adv L3**

Correct:

$$
\boxed{v=\sqrt{\frac{10gh}{7}}}
$$

---

### Particle Angular Momentum  
**Difficulty: Olympiad L1**

Correct:

$$
\boxed{L=mvb}
$$

---

## Chemistry

### First Law  
**Difficulty: JEE Adv L2**

Correct:

$$
\boxed{\Delta U=500J}
$$

---

### \(\Delta H,\Delta U\)  
**Difficulty: JEE Adv L3**

Correct:

$$
\boxed{\Delta H=\Delta U-RT}
$$

---

### Temperature Spontaneity  
**Difficulty: Olympiad L1**

Correct:

$$
\boxed{T>400K}
$$

---

### Equilibrium Constant  
**Difficulty: JEE Adv L3**

Correct:

$$
\boxed{K\approx10}
$$

---

# 9. Short Ways and Memory Hooks

## ODEs

- Separable: put \(y\) with \(dy\), \(x\) with \(dx\).
- Linear: make product rule appear using integrating factor.
- Autonomous: draw phase line.
- IVP: general solution plus initial condition.
- Blow-up: check denominators and intervals.

## Rotation

- Torque = force times perpendicular lever arm.
- Moment of inertia = rotational mass.
- Angular momentum conserved only if external torque is zero.
- Rolling kinetic energy has two parts.
- If torque depends on angle, integrate \(\tau\,d\theta\).

## Thermodynamics

- \(U\): stored energy.
- \(H\): heat at constant pressure.
- \(S\): dispersal / microstates.
- \(G\): spontaneity at constant \(T,P\).
- \(\Delta G<0\): spontaneous.
- \(\Delta G=0\): equilibrium.
- \(\Delta G>0\): not spontaneous forward.

---

# 10. Common Traps

| Topic | Trap | Correction |
|---|---|---|
| ODE | forgetting \(+C\) | include arbitrary constant |
| ODE | using IF before standard form | first divide coefficient of \(dy/dx\) |
| ODE | ignoring solution interval | check blow-up points |
| Rotation | using \(rF\) always | use \(rF\sin\phi\) |
| Rotation | forgetting rotational KE | rolling has translational + rotational KE |
| Rotation | conserving \(L\) with external torque | check torque about chosen point |
| Thermodynamics | treating \(q,w\) as state functions | they are path functions |
| Thermodynamics | Celsius in \(\Delta G=\Delta H-T\Delta S\) | use kelvin |
| Thermodynamics | unit mismatch between \(\Delta H,\Delta S\) | convert J/kJ |
| Thermodynamics | \(\Delta G<0\) means fast | it means spontaneous, not kinetically fast |

---

# 11. Completion Checklist

| Item | Status |
|---|---|
| First-order ODE definition | Complete |
| Separable equations | Complete |
| Linear ODEs | Complete |
| Integrating factor derivation | Complete |
| Autonomous stability | Complete |
| Advanced nonlinear ODE exposure | Complete |
| Torque | Complete |
| Moment of inertia | Complete |
| Angular momentum | Complete |
| Rigid-body energy | Complete |
| Rolling without slipping | Complete |
| Internal energy \(U\) | Complete |
| Enthalpy \(H\) | Complete |
| Entropy \(S\) | Complete |
| Gibbs free energy \(G\) | Complete |
| ODE model sheet | Complete |

$$
\boxed{\text{Week 1 Day 6 Complete}}
$$
