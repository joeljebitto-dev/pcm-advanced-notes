# Week 1 — Day 3
## Trigonometry, Complex Exponentials, Vectors, Projectile Motion, Electronic Configuration

## 0. Plan Row

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Trigonometry, radians, and complex exponentials | Complete |
| Physics | Vectors, dot/cross products, and projectile motion | Complete |
| Chemistry | Electronic configuration and quantum numbers | Complete |
| Required output | Vector drill | Complete |

---

# 1. Mathematics Detailed Reading
## Radians, Trigonometry, Complex Exponentials

Radians measure angle by arc length:

$$
\theta=\frac sr
$$

A full circle has angle:

$$
2\pi\text{ rad}=360^\circ
$$

Thus:

$$
60^\circ=\frac\pi3
$$

Radians are essential because calculus formulas like

$$
\frac{d}{dx}\sin x=\cos x
$$

are valid only when $x$ is in radians.

## 1.1 Unit Circle

On the unit circle:

$$
(x,y)=(\cos\theta,\sin\theta)
$$

Key values:

$$
\sin\frac\pi6=\frac12,
\qquad
\cos\frac\pi3=\frac12,
\qquad
\tan\frac\pi4=1
$$

## 1.2 Complex Numbers

$$
z=a+bi,
\qquad i^2=-1
$$

Modulus:

$$
|z|=\sqrt{a^2+b^2}
$$

Argument:

$$
\arg z=\theta,
\qquad \tan\theta=\frac ba
$$

Examples:

$$
|6+8i|=10
$$

$$
1+i=\sqrt2e^{i\pi/4}
$$

## 1.3 Euler Formula

$$
\boxed{e^{i\theta}=\cos\theta+i\sin\theta}
$$

Thus:

$$
e^{i\pi/2}=i
$$

and:

$$
2e^{i\pi/2}=2i
$$

Euler form converts trigonometry into exponential algebra. It is central to waves, rotations, alternating current, quantum mechanics, and complex-number geometry.

---

# 2. Physics Detailed Reading
## Vectors, Dot Product, Cross Product, Projectile Motion

A vector has magnitude and direction.

$$
\vec A=3\hat i+4\hat j
$$

Magnitude:

$$
|\vec A|=\sqrt{3^2+4^2}=5
$$

Direction:

$$
\theta=\tan^{-1}\frac43\approx53.13^\circ
$$

## 2.1 Components

A vector of magnitude $A$ at angle $\theta$:

$$
A_x=A\cos\theta
$$

$$
A_y=A\sin\theta
$$

For projectile launch:

$$
u_x=u\cos\theta,
\qquad
u_y=u\sin\theta
$$

Example:

$$
u=20,\quad\theta=30^\circ
$$

$$
u_x=10\sqrt3,
\qquad
u_y=10
$$

## 2.2 Dot Product

$$
\boxed{\vec A\cdot\vec B=AB\cos\theta}
$$

Component form:

$$
\vec A\cdot\vec B=A_xB_x+A_yB_y+A_zB_z
$$

Example:

$$
\vec A=3\hat i+4\hat j,
\quad
\vec B=2\hat i-\hat j
$$

$$
\vec A\cdot\vec B=3(2)+4(-1)=2
$$

The dot product measures parallel overlap. It appears in work:

$$
W=\vec F\cdot\vec s
$$

## 2.3 Cross Product

$$
\boxed{|\vec A\times\vec B|=AB\sin\theta}
$$

Direction is given by the right-hand rule.

$$
\hat i\times\hat j=\hat k,
\qquad
\hat j\times\hat i=-\hat k
$$

The cross product measures rotational effect. It appears in:

$$
\vec\tau=\vec r\times\vec F
$$

$$
\vec L=\vec r\times\vec p
$$

Example:

$$
A=5,
\quad B=4,
\quad \theta=90^\circ
$$

$$
|\vec A\times\vec B|=20
$$

## 2.4 Projectile Motion

Assumptions: no air resistance, constant $g$, horizontal acceleration zero.

Equations:

$$
x(t)=u\cos\theta\,t
$$

$$
y(t)=u\sin\theta\,t-\frac12gt^2
$$

$$
v_x=u\cos\theta
$$

$$
v_y=u\sin\theta-gt
$$

For same launch/landing height:

$$
T=\frac{2u\sin\theta}{g}
$$

$$
H=\frac{u^2\sin^2\theta}{2g}
$$

$$
R=\frac{u^2\sin2\theta}{g}
$$

For $u=20,\theta=30^\circ,g=10$:

$$
T=2s,
\qquad R=20\sqrt3m,
\qquad H=5m
$$

---

# 3. Chemistry Detailed Reading
## Electronic Configuration and Quantum Numbers

Electronic configuration describes how electrons fill orbitals.

Rules:

1. Aufbau principle: lower energy orbitals fill first.
2. Pauli principle: maximum two electrons per orbital with opposite spins.
3. Hund's rule: degenerate orbitals fill singly before pairing.

Common filling order:

$$
1s,2s,2p,3s,3p,4s,3d,4p,5s,4d,5p
$$

## 3.1 Configurations Completed

Carbon:

$$
\boxed{1s^2 2s^2 2p^2}
$$

Oxygen:

$$
\boxed{1s^2 2s^2 2p^4}
$$

Sodium:

$$
\boxed{1s^2 2s^2 2p^6 3s^1}
$$

Chlorine:

$$
\boxed{1s^2 2s^2 2p^6 3s^2 3p^5}
$$

## 3.2 Quantum Numbers

| Quantum number | Symbol | Meaning |
|---|---|---|
| Principal | $n$ | shell |
| Azimuthal | $l$ | subshell/shape |
| Magnetic | $m_l$ | orbital orientation |
| Spin | $m_s$ | spin |

Allowed values:

$$
n=1,2,3,\ldots
$$

$$
l=0,1,2,\ldots,n-1
$$

$$
m_l=-l,-l+1,\ldots,+l
$$

$$
m_s=\pm\frac12
$$

Subshell labels:

$$
l=0\to s,
\quad l=1\to p,
\quad l=2\to d,
\quad l=3\to f
$$

Number of orbitals:

$$
\boxed{2l+1}
$$

Maximum electrons:

$$
\boxed{2(2l+1)}
$$

Examples:

$$
3p:\quad n=3,l=1
$$

$$
d\text{ subshell}:l=2,\ 5\text{ orbitals},\ 10\text{ electrons max}
$$

$$
p\text{ subshell}:3\text{ orbitals}
$$

---

# 4. Formula Sheet

## Mathematics

$$
\theta_{rad}=\frac\pi{180^\circ}\theta_{deg}
$$

$$
e^{i\theta}=\cos\theta+i\sin\theta
$$

$$
|a+bi|=\sqrt{a^2+b^2}
$$

$$
z=re^{i\theta}
$$

## Physics

$$
|\vec A|=\sqrt{A_x^2+A_y^2+A_z^2}
$$

$$
\vec A\cdot\vec B=AB\cos\theta
$$

$$
|\vec A\times\vec B|=AB\sin\theta
$$

$$
T=\frac{2u\sin\theta}{g},\quad H=\frac{u^2\sin^2\theta}{2g},\quad R=\frac{u^2\sin2\theta}{g}
$$

## Chemistry

$$
l=0,1,\ldots,n-1
$$

$$
m_l=-l,\ldots,+l
$$

$$
\text{orbitals}=2l+1
$$

$$
\text{max electrons}=2(2l+1)
$$

---

# 5. Important Derivations

## 5.1 Projectile Range

$$
T=\frac{2u\sin\theta}{g}
$$

$$
R=u\cos\theta\cdot T
$$

$$
R=u\cos\theta\cdot \frac{2u\sin\theta}{g}
$$

$$
\boxed{R=\frac{u^2\sin2\theta}{g}}
$$

## 5.2 Subshell Electron Capacity

For given $l$, allowed $m_l$ values are $-l$ to $+l$, giving $2l+1$ orbitals. Each orbital holds two spins:

$$
\boxed{\text{max electrons}=2(2l+1)}
$$

---

# 6. Solved Examples and Corrections

| Area | Problem | Correct answer |
|---|---|---|
| Math | $60^\circ$ | $\pi/3$ |
| Math | $e^{i\pi/2}$ | $i$ |
| Math | $|6+8i|$ | 10 |
| Physics | $3i+4j$ | magnitude 5 |
| Physics | $(3i+4j)\cdot(2i-j)$ | 2 |
| Physics | projectile $u=20,30^\circ$ | $u_x=10\sqrt3,u_y=10$ |
| Physics | same projectile | $T=2,R=20\sqrt3,H=5$ |
| Chemistry | C | $1s^22s^22p^2$ |
| Chemistry | O | $1s^22s^22p^4$ |
| Chemistry | Na | $1s^22s^22p^63s^1$ |
| Chemistry | Cl | $1s^22s^22p^63s^23p^5$ |

---

# 7. Required Output — Vector Drill

| Skill | Status |
|---|---|
| Resolve vector into components | Complete |
| Compute magnitude and direction | Complete |
| Dot product and projection meaning | Complete |
| Cross product and right-hand rule | Complete |
| Projectile component method | Complete |
| Time of flight/range/height | Complete |
| Connect cross product to torque and angular momentum | Complete |

---

# 8. Short Ways and Traps

## Short Ways

- Radian = arc length/radius.
- Unit circle = $(\cos\theta,\sin\theta)$.
- Dot product = parallel part.
- Cross product = rotational/perpendicular part.
- Projectile = independent horizontal + vertical motions.
- $s,p,d,f$ correspond to $l=0,1,2,3$.

## Traps

| Trap | Fix |
|---|---|
| Using degrees in calculus | use radians |
| Ignoring quadrant for argument | check signs of $a,b$ |
| Confusing dot and cross | dot scalar, cross vector |
| Using range formula on uneven ground | derive from equations |
| Pairing p electrons too early | use Hund's rule |
| Confusing orbit and orbital | orbital is probability cloud |

---

# 9. Completion Checklist

| Item | Status |
|---|---|
| Radians | Complete |
| Trig values | Complete |
| Complex numbers | Complete |
| Euler formula | Complete |
| Vector magnitude/components | Complete |
| Dot product | Complete |
| Cross product | Complete |
| Projectile motion | Complete |
| Electronic configuration | Complete |
| Quantum numbers | Complete |
| Vector drill | Complete |

$$
\boxed{\text{Week 1 Day 3 Complete}}
$$

