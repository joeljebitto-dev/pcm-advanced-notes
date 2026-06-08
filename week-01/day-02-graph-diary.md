# Week 1 Day 2 - Graph Diary

## Plan row

| Subject | Required topic | Status |
|---|---|---|
| Math | Logs, exponentials, scaling laws | Complete |
| Physics | Kinematics as differential equations | Complete |
| Chemistry | Atomic structure: Bohr model to orbitals | Complete |
| Output | Graph diary | Complete |

## Summary

Day 2 connected exponential/log graphs, motion graphs, and atomic energy-level diagrams. The core theme is that changes in one variable can be represented by functions, derivatives, integrals, and discrete energy states.

## Math: logs, exponentials, scaling laws

Exponential function:

```math
f(x)=a^x,\quad a>0,\ a\ne1
```

Logarithm is its inverse:

```math
a^x=y\iff \log_a y=x
```

Natural log:

```math
\ln x=\log_e x
```

Inverse identities:

```math
\ln(e^x)=x,\quad e^{\ln x}=x
```

Scaling law:

```math
y\propto x^n
```

If `x` is multiplied by `k`, then `y` is multiplied by `k^n`.

Examples covered:

- `y=x^3`, doubling `x` multiplies `y` by 8.
- `A proportional r^2`, tripling `r` multiplies area by 9.

Short way: exponentials grow by repeated multiplication; logs ask for the exponent; scaling exponents tell how strongly size changes.

## Physics: kinematics as differential equations

Position, velocity, acceleration:

```math
v(t)=\frac{dx}{dt}
```

```math
a(t)=\frac{dv}{dt}=\frac{d^2x}{dt^2}
```

If acceleration is known, integrate to get velocity. If velocity is known, integrate to get position.

Example covered:

```math
x(t)=3t^2+2t+1
```

```math
v(t)=6t+2,\quad a(t)=6
```

Reverse reconstruction:

```math
a(t)=6,\ v(0)=2\Rightarrow v(t)=6t+2
```

```math
v(t)=6t+2,\ x(0)=1\Rightarrow x(t)=3t^2+2t+1
```

Short way: derivative moves from position to velocity to acceleration; integration moves back.

## Chemistry: Bohr model to orbitals

Hydrogen Bohr energy:

```math
E_n=-\frac{13.6}{n^2}\ \text{eV}
```

Values covered:

```math
E_1=-13.6\ \text{eV},\quad E_2=-3.4\ \text{eV},\quad E_3\approx -1.51\ \text{eV}
```

Transition energy:

```math
\Delta E=E_f-E_i
```

Examples:

```math
n=1\to2:\ \Delta E=10.2\ \text{eV}
```

```math
n=2\to3:\ \Delta E=1.89\ \text{eV}
```

Short way: higher `n` means higher energy, but energies are still negative until ionization.

## Graph diary output

Include these sketches:

1. `y=e^x` and `y=ln x` as inverse curves.
2. `y=x^2` and `y=x^3` for scaling comparison.
3. `x(t)`, `v(t)`, `a(t)` for `x=3t^2+2t+1`.
4. Hydrogen energy levels `E1`, `E2`, `E3`, showing levels getting closer as `n` increases.

## Important CBSE/JEE derivations

1. Derive velocity and acceleration by differentiation.
2. Reconstruct `x(t)` from `a(t)` using integration and initial conditions.
3. Calculate Bohr transition energy using `Delta E=E_f-E_i`.
4. Scaling factor derivation: `x->kx` implies `y->k^n y` for `y proportional x^n`.

## Completion checklist

- [x] Math covered
- [x] Physics covered
- [x] Chemistry covered
- [x] Graph diary produced
