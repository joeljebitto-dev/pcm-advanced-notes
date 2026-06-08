# Week 1 Day 5 — Derivation Notes

## Topics covered

- Math: integrals as accumulation
- Physics: work-energy theorem and conservative fields
- Chemistry: chemical bonding — VSEPR, hybridization, MO intro

## Summary

Day 5 connected accumulation in calculus, energy transfer in mechanics, and energy lowering in chemical bonding. The unifying idea is that local interactions accumulate into global state changes.

## Key formulas

### Integrals

```math
\int_a^b f(x)\,dx=\lim_{n\to\infty}\sum_{k=1}^n f(x_k^*)\Delta x
```

```math
\int x^n dx=\frac{x^{n+1}}{n+1}+C,\quad n\ne -1
```

```math
\int \frac1x dx=\ln|x|+C
```

FTC:

```math
\frac{d}{dx}\int_a^x f(t)dt=f(x)
```

```math
\frac{d}{dx}\int_a^{g(x)} f(t)dt=f(g(x))g'(x)
```

Leibniz rule:

```math
\frac{d}{dx}\int_{a(x)}^{b(x)} f(t)dt=f(b)b'-f(a)a'
```

### Work and energy

```math
W=\vec F\cdot\vec s=Fs\cos\theta
```

```math
W=\int_{x_i}^{x_f}F(x)dx
```

```math
W_{net}=\Delta K
```

```math
K=\frac12mv^2
```

```math
F=-\frac{dU}{dx}
```

```math
W_c=-\Delta U
```

```math
K+U=\text{constant}
```

```math
U_{spring}=\frac12kx^2
```

### Bonding

Formal charge:

```math
FC=V-\left(N+\frac{B}{2}\right)
```

Steric number:

```math
SN=\text{sigma bonds}+\text{lone pairs}
```

Bond order:

```math
BO=\frac{N_b-N_a}{2}
```

## Short ways to understand

- Integral = accumulated change.
- Work = accumulated force along displacement.
- Conservative force = path-independent work.
- Potential energy is a stored-energy function whose negative slope gives force.
- VSEPR predicts geometry by minimizing electron-domain repulsion.
- Hybridization is a directional bonding model.
- MO theory explains delocalization, bond order, and magnetism.

## Important derivations

### Integral as accumulation

If:

```math
\frac{dQ}{dx}=f(x)
```

then:

```math
dQ=f(x)dx
```

Accumulate:

```math
Q(b)-Q(a)=\int_a^b f(x)dx
```

### Work-energy theorem

Start with:

```math
F=ma
```

Use:

```math
a=v\frac{dv}{dx}
```

Then:

```math
F=mv\frac{dv}{dx}
```

```math
Fdx=mvdv
```

Integrate:

```math
\int Fdx=\int mvdv
```

```math
W=\frac12mv_f^2-\frac12mv_i^2
```

```math
W_{net}=\Delta K
```

### Conservative force relation

```math
F=-\frac{dU}{dx}
```

```math
dU=-Fdx
```

```math
U_f-U_i=-\int_{x_i}^{x_f}Fdx
```

```math
W_c=-\Delta U
```

If only conservative forces act:

```math
\Delta K+\Delta U=0
```

```math
K+U=\text{constant}
```

### Spring potential

```math
F=-kx
```

```math
-kx=-\frac{dU}{dx}
```

```math
\frac{dU}{dx}=kx
```

```math
U=\frac12kx^2+C
```

With `U(0)=0`:

```math
U=\frac12kx^2
```

### Bond order

Bonding and antibonding molecular orbitals form from linear combinations:

```math
\psi_+=\psi_A+\psi_B
```

```math
\psi_-=\psi_A-\psi_B
```

Bond order:

```math
BO=\frac{N_b-N_a}{2}
```

For oxygen species:

```text
O2+ : BO = 2.5, paramagnetic, shortest
O2  : BO = 2.0, paramagnetic, intermediate
O2- : BO = 1.5, paramagnetic, longest
```

## Chemistry model notes

### VSEPR examples

| Species | Electron domains | Shape |
|---|---:|---|
| CH4 | 4 | tetrahedral |
| NH3 | 4 | trigonal pyramidal |
| H2O | 4 | bent |
| BF3 | 3 | trigonal planar |
| CO2 | 2 | linear |

### Hybridization

| Steric number | Hybridization | Geometry |
|---:|---|---|
| 2 | sp | linear |
| 3 | sp2 | trigonal planar |
| 4 | sp3 | tetrahedral electron geometry |

### MO theory insight

- `O2` is paramagnetic due to two unpaired electrons in antibonding pi-star orbitals.
- `He2` has bond order zero and is not a stable ordinary molecule.
- For `B2`, `C2`, `N2`, MO ordering differs from `O2`, `F2` because of s-p mixing.

## JEE Advanced / Olympiad problem record

- FTC + chain rule repair completed.
- Signed displacement vs total distance corrected.
- Variable-force work-energy problem completed.
- Conservative potential equilibrium and stability completed.
- VSEPR / hybridization / MO theory drill completed.

## Completion checklist

- [x] Integrals as accumulation
- [x] Riemann sums
- [x] Definite vs indefinite integrals
- [x] FTC and Leibniz rule
- [x] Work-energy theorem
- [x] Conservative fields
- [x] Potential energy relation
- [x] Equilibrium and stability
- [x] VSEPR
- [x] Hybridization
- [x] MO theory intro
- [x] Bond order and magnetism
- [x] Derivation notes
