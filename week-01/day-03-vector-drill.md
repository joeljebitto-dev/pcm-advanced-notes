# Week 1 Day 3 - Vector Drill

## Plan row

| Subject | Required topic | Status |
|---|---|---|
| Math | Trigonometry, radians, complex exponentials | Complete |
| Physics | Vectors, dot/cross products, projectile motion | Complete |
| Chemistry | Electronic configuration, quantum numbers | Complete |
| Output | Vector drill | Complete |

## Summary

Day 3 joined trigonometry, complex numbers, vectors, projectile motion, and quantum-number notation. The recurring geometry is component resolution: a vector, complex number, projectile velocity, or orbital state is decomposed into structured coordinates.

## Math: radians, trig, complex exponentials

Radians:

```math
\theta=\frac{s}{r}
```

Key conversions:

```math
180^\circ=\pi,\quad 90^\circ=\frac{\pi}{2},\quad 60^\circ=\frac{\pi}{3},\quad 45^\circ=\frac{\pi}{4},\quad 30^\circ=\frac{\pi}{6}
```

Euler identity:

```math
e^{i\theta}=\cos\theta+i\sin\theta
```

Special values:

```math
e^{i\pi/2}=i,\quad e^{i\pi}=-1
```

Complex number:

```math
z=a+bi
```

Modulus and argument:

```math
|z|=\sqrt{a^2+b^2},\quad \theta=\tan^{-1}\left(\frac{b}{a}\right)
```

Polar form:

```math
z=r(\cos\theta+i\sin\theta)=re^{i\theta}
```

Short way: rectangular form is best for addition; polar/exponential form is best for multiplication and rotation.

## Physics: vectors, dot/cross product, projectile motion

Vector magnitude:

```math
|\vec A|=\sqrt{A_x^2+A_y^2}
```

Dot product:

```math
\vec A\cdot\vec B=A_xB_x+A_yB_y=AB\cos\theta
```

Cross product magnitude:

```math
|\vec A\times\vec B|=AB\sin\theta
```

Unit vector rules:

```math
\hat i\times\hat j=\hat k,\quad \hat j\times\hat i=-\hat k
```

Projectile components:

```math
u_x=u\cos\theta,\quad u_y=u\sin\theta
```

Projectile equations:

```math
x(t)=u_x t
```

```math
y(t)=u_y t-\frac12gt^2
```

For launch and landing at same height:

```math
T=\frac{2u\sin\theta}{g},\quad R=\frac{u^2\sin2\theta}{g},\quad H=\frac{u^2\sin^2\theta}{2g}
```

Example covered: `u=20 m/s`, `theta=30 deg`, `g=10 m/s^2`:

```math
u_x=10\sqrt3,\quad u_y=10,\quad T=2s,\quad R=20\sqrt3m,\quad H=5m
```

Short way: split motion into independent horizontal and vertical components.

## Chemistry: electronic configuration and quantum numbers

Configurations covered:

```math
C:1s^2 2s^2 2p^2
```

```math
O:1s^2 2s^2 2p^4
```

```math
Na:1s^2 2s^2 2p^6 3s^1
```

```math
Cl:1s^2 2s^2 2p^6 3s^2 3p^5
```

Quantum numbers:

| Symbol | Meaning | Allowed values |
|---|---|---|
| `n` | shell | `1,2,3,...` |
| `l` | subshell | `0` to `n-1` |
| `m_l` | orbital orientation | `-l` to `+l` |
| `m_s` | spin | `+1/2`, `-1/2` |

Subshell mapping:

```math
s:l=0,\quad p:l=1,\quad d:l=2,\quad f:l=3
```

Number of orbitals in a subshell:

```math
2l+1
```

Maximum electrons:

```math
2(2l+1)
```

Example: `p` has `l=1`, so `2l+1=3` orbitals and 6 electrons maximum.

## Important CBSE/JEE derivations

1. Convert complex number `a+bi` to polar form.
2. Projectile time, range, and height derivations from kinematics.
3. Derive subshell capacity from `2(2l+1)`.
4. Use cross product signs through cyclic order `i,j,k`.

## Completion checklist

- [x] Math covered
- [x] Physics covered
- [x] Chemistry covered
- [x] Vector drill produced
