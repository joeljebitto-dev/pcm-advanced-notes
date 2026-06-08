# Week 1 Day 1 — Symbol Sheet

## Topics covered

- Math: sets/functions as maps, domain, codomain, range, inverse functions
- Physics: measurement, dimensions, error propagation
- Chemistry: mole concept, stoichiometry, concentration variables

## Summary

Day 1 built the notation layer for advanced PCM. Functions were treated as maps, physical equations as dimensionally typed statements, and chemistry equations as conservation constraints.

## Key formulas

### Math

```math
f:A\to B
```

```math
(f\circ g)(x)=f(g(x))
```

```math
f^{-1}(f(x))=x
```

### Physics

```math
[v]=[LT^{-1}]
```

```math
[a]=[LT^{-2}]
```

```math
[F]=[MLT^{-2}]
```

```math
[G]=[M^{-1}L^3T^{-2}]
```

For `Q=a^p b^q c^r`:

```math
\frac{\Delta Q}{Q}=|p|\frac{\Delta a}{a}+|q|\frac{\Delta b}{b}+|r|\frac{\Delta c}{c}
```

### Chemistry

```math
n=\frac{m}{M}
```

```math
C=\frac{n}{V}
```

```math
x_i=\frac{n_i}{\sum n_i}
```

## Short ways to understand

- A function is a map with declared input and output sets.
- The range is the actual output set; the codomain is the declared output set.
- Dimensions are the type system of physics.
- Stoichiometry is conservation accounting.

## Important derivations

### Inverse of affine function

For `f(x)=ax+b`, `a != 0`:

```math
y=ax+b
```

```math
x=\frac{y-b}{a}
```

```math
f^{-1}(x)=\frac{x-b}{a}
```

### Dimension of gravitational constant

```math
F=\frac{Gm_1m_2}{r^2}
```

```math
G=\frac{Fr^2}{m_1m_2}
```

```math
[G]=[M^{-1}L^3T^{-2}]
```

## Completion checklist

- [x] Functions as maps
- [x] Domain/codomain/range
- [x] Injective/surjective/bijective
- [x] Inverses and domain restrictions
- [x] Dimensions and error propagation
- [x] Mole, stoichiometry, molarity
- [x] Symbol sheet
