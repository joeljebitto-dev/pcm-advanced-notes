# Important Derivations for JEE Advanced and CBSE Boards

## 1. Dimension of gravitational constant

From:

```math
F=\frac{Gm_1m_2}{r^2}
```

```math
G=\frac{Fr^2}{m_1m_2}
```

```math
[G]=\frac{[MLT^{-2}][L^2]}{[M^2]}=[M^{-1}L^3T^{-2}]
```

## 2. Error propagation for products and powers

For:

```math
Q=a^p b^q c^r
```

take logarithms:

```math
\ln Q=p\ln a+q\ln b+r\ln c
```

Differentiate approximately:

```math
\frac{dQ}{Q}=p\frac{da}{a}+q\frac{db}{b}+r\frac{dc}{c}
```

Maximum relative error:

```math
\frac{\Delta Q}{Q}=|p|\frac{\Delta a}{a}+|q|\frac{\Delta b}{b}+|r|\frac{\Delta c}{c}
```

## 3. Projectile motion formulae

Resolve velocity:

```math
u_x=u\cos\theta,\quad u_y=u\sin\theta
```

Vertical motion:

```math
y=u_y t-\frac12gt^2
```

For same launch and landing height, set `y=0`:

```math
t(u_y-\frac12gt)=0
```

Nonzero root:

```math
T=\frac{2u_y}{g}=\frac{2u\sin\theta}{g}
```

Range:

```math
R=u_xT=u\cos\theta\cdot\frac{2u\sin\theta}{g}=\frac{u^2\sin2\theta}{g}
```

Maximum height occurs when `v_y=0`:

```math
v_y^2=u_y^2-2gH
```

```math
H=\frac{u_y^2}{2g}=\frac{u^2\sin^2\theta}{2g}
```

## 4. Work-energy theorem

Start:

```math
F=ma
```

Use:

```math
a=\frac{dv}{dt}=\frac{dv}{dx}\frac{dx}{dt}=v\frac{dv}{dx}
```

Then:

```math
F=mv\frac{dv}{dx}
```

Multiply by `dx`:

```math
Fdx=mv dv
```

Integrate:

```math
\int Fdx=\int mv dv
```

```math
W=\frac12mv_f^2-\frac12mv_i^2
```

```math
W_{net}=\Delta K
```

## 5. Conservative force and potential energy

Definition:

```math
F=-\frac{dU}{dx}
```

Then:

```math
dU=-Fdx
```

Integrate:

```math
\Delta U=-\int Fdx=-W_c
```

```math
W_c=-\Delta U
```

If only conservative forces act:

```math
\Delta K=-\Delta U
```

```math
K+U=\text{constant}
```

## 6. Spring potential energy

For spring:

```math
F=-kx
```

Using:

```math
F=-\frac{dU}{dx}
```

```math
-kx=-\frac{dU}{dx}
```

```math
\frac{dU}{dx}=kx
```

Integrate:

```math
U=\frac12kx^2+C
```

Choose `U(0)=0`:

```math
U=\frac12kx^2
```

## 7. Bond order from MO theory

Bonding electrons stabilize; antibonding electrons destabilize. Bond order is half the excess of bonding electrons:

```math
BO=\frac{N_b-N_a}{2}
```

Consequences:

- Higher BO means shorter, stronger bond.
- Removing antibonding electron increases BO.
- Adding antibonding electron decreases BO.

Example:

```math
BO(O_2^+)=2.5>BO(O_2)=2>BO(O_2^-)=1.5
```

## 8. Resonance bond order

For equivalent resonance structures, average bond order is total bond order distributed over equivalent bonds.

For nitrite:

```text
O=N-O- <-> -O-N=O
```

Average N-O bond order:

```math
\frac{2+1}{2}=1.5
```
