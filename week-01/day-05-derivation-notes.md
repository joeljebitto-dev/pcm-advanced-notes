# Week 1 Day 5 - Derivation Notes

## Plan row

| Subject | Required topic | Status |
|---|---|---|
| Math | Integrals as accumulation; integration tools | Complete |
| Physics | Work-energy theorem and conservative fields | Complete |
| Chemistry | Chemical bonding: VSEPR, hybridization, MO intro | Complete |
| Output | Derivation notes | Complete |

## Summary

Day 5 connected integration, work, energy, conservative fields, and bonding models. The shared structure is energy: integrals accumulate local quantities, work changes kinetic energy, conservative forces define potential energy, and chemical bonds form when electronic energy decreases.

## Math: integrals as accumulation

If:

```math
\frac{dQ}{dx}=f(x)
```

then:

```math
Q(b)-Q(a)=\int_a^b f(x)\,dx
```

Riemann sum:

```math
\int_a^b f(x)\,dx=\lim_{n\to\infty}\sum_{k=1}^{n}f(x_k^*)\Delta x
```

Definite integral:

```math
\int_a^b f(x)\,dx=F(b)-F(a)
```

FTC with variable upper limit:

```math
\frac{d}{dx}\int_a^{g(x)} f(t)\,dt=f(g(x))g'(x)
```

Leibniz rule for variable limits:

```math
\frac{d}{dx}\int_{a(x)}^{b(x)}f(t)\,dt=f(b(x))b'(x)-f(a(x))a'(x)
```

Signed displacement vs total distance:

```math
\text{displacement}=\int_a^b v(t)\,dt
```

```math
\text{distance}=\int_a^b |v(t)|\,dt
```

Advanced correction covered:

```math
v(t)=t^2-5t+6,\quad 0\le t\le4
```

```math
\text{net displacement}=\frac{16}{3},\quad \text{total distance}=\frac{17}{3}
```

Short way: integral = accumulated signed quantity; absolute value is needed for total travelled amount.

## Physics: work-energy theorem and conservative fields

Work:

```math
W=\vec F\cdot\vec s=Fs\cos\theta
```

Variable force work:

```math
W=\int_{x_i}^{x_f}F(x)\,dx
```

Line integral:

```math
W=\int_C\vec F\cdot d\vec r
```

Work-energy theorem:

```math
W_{net}=\Delta K=\frac12mv_f^2-\frac12mv_i^2
```

Conservative force:

```math
\oint \vec F\cdot d\vec r=0
```

Potential energy relation:

```math
F(x)=-\frac{dU}{dx}
```

Work by conservative force:

```math
W_c=-\Delta U
```

Mechanical energy conservation:

```math
K+U=\text{constant}
```

Spring potential:

```math
U=\frac12kx^2
```

Equilibrium:

```math
F=0\iff \frac{dU}{dx}=0
```

Stability:

```math
U''(x)>0\Rightarrow \text{stable}
```

```math
U''(x)<0\Rightarrow \text{unstable}
```

```math
U''(x)=0\Rightarrow \text{higher-order analysis required}
```

Important advanced example:

```math
U(x)=x^6-3x^4
```

Equilibria:

```math
x=0,\ \pm\sqrt2
```

`x=+-sqrt2` stable; `x=0` has `U''(0)=0`, requires higher-order analysis, and is unstable because near zero `U(x) approx -3x^4 < 0`.

Short way: speed thresholds come from total energy reaching the highest potential barrier.

## Chemistry: chemical bonding, VSEPR, hybridization, MO intro

### Formal charge

```math
FC=V-\left(N+\frac{B}{2}\right)
```

### VSEPR

Steric number:

```math
SN=\text{sigma bonds}+\text{lone pairs}
```

AXE notation:

```text
AX_mE_n
```

Electron-domain geometry by steric number:

| SN | Geometry | Ideal angle |
|---:|---|---:|
| 2 | linear | 180 deg |
| 3 | trigonal planar | 120 deg |
| 4 | tetrahedral | 109.5 deg |
| 5 | trigonal bipyramidal | 90/120 deg |
| 6 | octahedral | 90 deg |

Lone-pair repulsion:

```text
LP-LP > LP-BP > BP-BP
```

### Hybridization

```text
SN=2 -> sp
SN=3 -> sp2
SN=4 -> sp3
```

Corrected examples:

```text
NH3: sp3, trigonal pyramidal, about 107 deg
H2O: sp3, bent, about 104.5 deg
BF3: sp2, trigonal planar, 120 deg
CO2: sp, linear, 180 deg
```

Angle ranking:

```text
H2O < NH3 < BF3 < CO2
```

### Sigma and pi bonds

```text
single bond = 1 sigma
double bond = 1 sigma + 1 pi
triple bond = 1 sigma + 2 pi
```

### MO theory

Bonding and antibonding combinations:

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

MO comparison covered:

| Species | Bond order | Magnetic behavior | Relative length |
|---|---:|---|---|
| O2+ | 2.5 | paramagnetic | shortest |
| O2 | 2 | paramagnetic | intermediate |
| O2- | 1.5 | paramagnetic | longest |

```math
BO(O_2^+)>BO(O_2)>BO(O_2^-)
```

```text
bond length: O2+ < O2 < O2-
```

### NO2- resonance

Two equivalent resonance forms:

```text
O=N-O- <-> -O-N=O
```

Average N-O bond order:

```math
\frac{1+2}{2}=1.5
```

Because of resonance, the two N-O bonds are equal in real nitrite.

## Important CBSE/JEE derivations

1. Integral as accumulation from `dQ=f(x)dx`.
2. Work-energy theorem from `F=ma` and `a=v dv/dx`.
3. Conservative force relation `F=-dU/dx` and `W_c=-Delta U`.
4. Spring potential `U=1/2 kx^2`.
5. Stability classification by second derivative of potential.
6. Bond order formula from bonding-antibonding electron count.
7. Bond-angle ranking using steric number and lone-pair repulsion.
8. Resonance bond order for equivalent bonds.

## Completion checklist

- [x] Math covered
- [x] Physics covered
- [x] Chemistry covered
- [x] Derivation notes produced
