# Week 1 Day 1 - Symbol Sheet

## Plan row

| Subject | Required topic | Status |
|---|---|---|
| Math | Sets/functions as maps; functions and graphs; notation | Complete |
| Physics | Measurement, dimensions, error propagation | Complete |
| Chemistry | Moles, stoichiometry, concentration as state variables | Complete |
| Output | Build symbol sheet | Complete |

## Summary

Day 1 established the language of advanced PCM: functions as precise maps, dimensions as physical type-checking, and moles/concentration as chemical state variables.

## Math: functions as maps

A function is not just a formula. It is a map with declared domain and codomain:

```math
f:A \to B
```

Key distinction:

- Domain: allowed inputs.
- Codomain: declared target set.
- Range: outputs actually reached.

Example:

```math
f:\mathbb R\to\mathbb R,\quad f(x)=x^2
```

```math
\operatorname{Range}(f)=[0,\infty)
```

### Injective, surjective, bijective

- Injective: different inputs never collide.
- Surjective: every codomain element is reached.
- Bijective: both injective and surjective.

A bijection has an inverse.

### Inverse examples covered

```math
f(x)=5x+7 \Rightarrow f^{-1}(x)=\frac{x-7}{5}
```

```math
f:[0,\infty)\to[0,\infty),\ f(x)=x^2 \Rightarrow f^{-1}(x)=\sqrt{x}
```

```math
f:(-\infty,0]\to[0,\infty),\ f(x)=x^2 \Rightarrow f^{-1}(x)=-\sqrt{x}
```

Short way: inverse functions undo operations in reverse order, but only exist when the map is one-to-one onto its codomain.

## Physics: dimensions and error propagation

Base dimensions:

| Quantity | Dimension |
|---|---|
| Mass | `[M]` |
| Length | `[L]` |
| Time | `[T]` |

Common derived dimensions:

| Quantity | Dimension |
|---|---|
| Velocity | `[LT^-1]` |
| Acceleration | `[LT^-2]` |
| Force | `[MLT^-2]` |
| Energy/work | `[ML^2T^-2]` |
| Gravitational constant `G` | `[M^-1L^3T^-2]` |

Important result derived:

```math
F=\frac{Gm_1m_2}{r^2}\Rightarrow [G]=[M^{-1}L^3T^{-2}]
```

### Error propagation

For products and powers:

```math
Q=a^p b^q c^r
```

percentage error:

```math
\frac{\Delta Q}{Q}=|p|\frac{\Delta a}{a}+|q|\frac{\Delta b}{b}+|r|\frac{\Delta c}{c}
```

Example:

```math
Q=\frac{a^2b}{c^3},\quad \%\Delta a=1,\ \%\Delta b=2,\ \%\Delta c=3
```

```math
\%\Delta Q=2(1)+2+3(3)=13\%
```

Short way: dimensions are physics type-checking; percentage errors add with powers as multipliers.

## Chemistry: mole, stoichiometry, concentration

Mole formula:

```math
n=\frac{m}{M}
```

Molarity:

```math
C=\frac{n}{V}
```

Mole fraction:

```math
x_i=\frac{n_i}{\sum n_i}
```

Stoichiometry is conservation accounting. Coefficients in a balanced equation are mole ratios.

Example:

```math
N_2+3H_2\to 2NH_3
```

For `2 mol N2` and `3 mol H2`, hydrogen is limiting because 2 mol nitrogen would require 6 mol hydrogen.

## Symbol sheet

| Symbol | Meaning |
|---|---|
| `f:A->B` | function from domain A to codomain B |
| `Dom(f)` | domain |
| `Range(f)` | actual output set |
| `f o g` | composition |
| `f^-1` | inverse function |
| `[M],[L],[T]` | base dimensions |
| `Delta x` | absolute uncertainty |
| `Delta x/x` | relative uncertainty |
| `n` | moles |
| `m` | mass |
| `M` | molar mass |
| `C` | molarity |
| `V` | volume |
| `N_A` | Avogadro constant |
| `nu_i` | stoichiometric coefficient |

## Important CBSE/JEE derivations

1. Dimension of `G` from Newton's gravitation law.
2. Error propagation for products and powers.
3. Limiting reagent by mole-ratio comparison.
4. Inverse function by solving `y=f(x)` and swapping variables.

## Completion checklist

- [x] Math covered
- [x] Physics covered
- [x] Chemistry covered
- [x] Symbol sheet produced
