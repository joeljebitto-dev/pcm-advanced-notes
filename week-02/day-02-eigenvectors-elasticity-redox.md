# Week 2 Day 2: Eigenvectors, Elasticity, and Redox Thermodynamics

## 0. Plan Row and Completion Status

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Eigenvectors and linear transformations | Complete |
| Physics | Solids and elasticity: stress-strain energy | Complete |
| Chemistry | Redox as electron bookkeeping and thermodynamics | Complete |
| Required output | Problem set | Complete |

---

## 1. Day Purpose

Week 2 Day 2 connects three ideas:

- Eigenvectors describe directions preserved by a linear transformation.
- Elasticity describes how solids store mechanical energy during deformation.
- Redox thermodynamics connects electron transfer with Gibbs free energy and cell potential.

The unifying idea is that physical and chemical systems often become simpler when we identify the correct variables: eigen-directions in mathematics, strain variables in elasticity, and electron-transfer variables in redox chemistry.

---

## 2. Mathematics: Eigenvectors and Linear Transformations

### 2.1 Linear Transformation

A linear transformation preserves addition and scalar multiplication.

$T$ is linear if:

$$T(u+v)=T(u)+T(v)$$

$$T(cv)=cT(v)$$

A matrix represents a linear transformation.

If $A=[(2,1),(0,3)]$, then $T(x)=Ax$ is a linear transformation.

A matrix can stretch, shrink, rotate, reflect, shear, project, or collapse vectors.

---

### 2.2 Eigenvector Definition

An eigenvector is a nonzero vector whose direction is unchanged by a transformation.

$$Av=\lambda v$$

Here:

| Symbol | Meaning |
|---|---|
| $A$ | transformation matrix |
| $v$ | nonzero eigenvector |
| $\lambda$ | eigenvalue |

The eigenvalue is the scale factor.

| Eigenvalue | Geometric effect |
|---:|---|
| $\lambda>1$ | stretch |
| $0<\lambda<1$ | shrink |
| $\lambda=1$ | unchanged |
| $\lambda=0$ | collapsed to zero |
| $\lambda<0$ | reversed and scaled |

The zero vector is not counted as an eigenvector.

---

### 2.3 Characteristic Equation

Start with:

$$Av=\lambda v$$

Move all terms to one side:

$$(A-\lambda I)v=0$$

For a nonzero vector $v$ to exist, the matrix $A-\lambda I$ must be singular.

Therefore:

$$\det(A-\lambda I)=0$$

This is the characteristic equation.

---

### 2.4 Trace-Determinant Shortcut

For $A=[(a,b),(c,d)]$:

$$\operatorname{tr}(A)=a+d$$

$$\det(A)=ad-bc$$

The characteristic polynomial is:

$$\lambda^2-\operatorname{tr}(A)\lambda+\det(A)=0$$

---

### 2.5 Eigenvectors and Powers

If $Av=\lambda v$, then:

$$A^2v=\lambda^2v$$

In general:

$$A^nv=\lambda^nv$$

This matters in repeated transformations, differential equations, stability, Markov chains, normal modes, and quantum mechanics.

---

### 2.6 Diagonalization Preview

If a matrix has enough independent eigenvectors, it can be diagonalized.

$$A=PDP^{-1}$$

Here:

- $P$ contains eigenvectors as columns.
- $D$ contains eigenvalues on the diagonal.

In an eigenvector basis, the transformation becomes pure scaling.

---

### 2.7 Math Drill Record

#### M1: Eigenvalues and Eigenvectors

Given:

$$A=[(3,1),(0,2)]$$

Since $A$ is upper triangular, the eigenvalues are the diagonal entries:

$$\lambda=3,2$$

For $\lambda=2$:

$$A-2I=[(1,1),(0,0)]$$

So:

$$x+y=0$$

One eigenvector is:

$$(1,-1)^T$$

For $\lambda=3$:

$$A-3I=[(0,1),(0,-1)]$$

So:

$$y=0$$

One eigenvector is:

$$(1,0)^T$$

The user gave $(10,0)^T$, which is also valid because any nonzero scalar multiple of an eigenvector is again an eigenvector.

Status: correct.

#### M2: Characteristic Polynomial

Given:

$$B=[(1,4),(2,3)]$$

Characteristic equation:

$$\det(B-\lambda I)=0$$

$$\det[(1-\lambda,4),(2,3-\lambda)]=0$$

$$(1-\lambda)(3-\lambda)-8=0$$

Expand:

$$\lambda^2-4\lambda-5=0$$

Factor:

$$(\lambda-5)(\lambda+1)=0$$

Eigenvalues:

$$\lambda=5,-1$$

Status: correct.

#### M3: Rotation Matrix

Given:

$$C=[(0,-1),(1,0)]$$

This rotates vectors in the plane by $90^\circ$ counterclockwise.

Characteristic equation:

$$\det(C-\lambda I)=0$$

$$\det[(-\lambda,-1),(1,-\lambda)]=0$$

$$\lambda^2+1=0$$

So:

$$\lambda=\pm i$$

There are no real eigenvalues, so there are no real eigenvectors.

Status: correct.

---

## 3. Physics: Solids and Elasticity

### 3.1 Stress

Stress is internal restoring force per unit area.

$$\sigma=F/A$$

SI unit: pascal, or $N m^{-2}$.

Stress has the same unit as pressure, but stress may be tensile, compressive, or shear.

### 3.2 Strain

Strain measures fractional deformation.

For a wire of original length $L$ and extension $\Delta L$:

$$\epsilon=\Delta L/L$$

Strain is dimensionless.

| Type | Formula |
|---|---|
| Longitudinal strain | epsilon = Delta L / L |
| Volumetric strain | Delta V / V |
| Shear strain | approximately theta for small angle |

Important: strain is not extension. It is relative extension.

A 1 mm extension in a 1 cm wire is large. A 1 mm extension in a 10 m wire is small.

### 3.3 Young's Modulus

Young's modulus applies to longitudinal stretching or compression.

$$Y=(F/A)/(\Delta L/L)$$

Therefore:

$$Y=FL/(A\Delta L)$$

So:

$$\Delta L=FL/(AY)$$

A larger $Y$ means the material is harder to stretch.

### 3.4 Wire as an Effective Spring

For a wire:

$$\Delta L=FL/(AY)$$

Compare with Hooke's law:

$$F=k\Delta L$$

Then:

$$k=AY/L$$

Thus a thicker, shorter, stiffer wire has a larger effective spring constant.

### 3.5 Elastic Potential Energy

For Hooke-type deformation:

$$U=\frac{1}{2}k(\Delta L)^2$$

Using $k=AY/L$:

$$U=\frac{1}{2}(AY/L)(\Delta L)^2$$

Equivalent forms:

$$U=\frac{1}{2}F\Delta L$$

$$U=F^2L/(2AY)$$

The factor $1/2$ appears because force increases from $0$ to $F$ during stretching.

### 3.6 Strain Energy Density

Strain energy density means energy stored per unit volume.

$$u=U/(AL)$$

Using $\epsilon=\Delta L/L$:

$$u=\frac{1}{2}Y\epsilon^2$$

Since $\sigma=Y\epsilon$:

$$u=\frac{1}{2}\sigma\epsilon$$

Also:

$$u=\sigma^2/(2Y)$$

### 3.7 Stress-Strain Curve

In the linear elastic region:

$$\sigma=Y\epsilon$$

| Region | Meaning |
|---|---|
| Proportional limit | stress proportional to strain |
| Elastic limit | body returns to original shape when unloaded |
| Yield point | plastic deformation begins |
| Plastic region | permanent deformation occurs |
| Ultimate tensile strength | maximum stress material can withstand |
| Breaking point | material fractures |

Elastic deformation is reversible. Plastic deformation is permanent.

### 3.8 Bulk Modulus

Bulk modulus describes resistance to volume compression.

$$K=\Delta P/(-\Delta V/V)$$

The negative sign appears because volume decreases when pressure increases.

Compressibility is:

$$\beta=1/K$$

### 3.9 Shear Modulus

Shear modulus describes resistance to shape change.

Shear stress:

$$\tau=F/A$$

Shear strain for small angle:

$$\gamma\approx\theta$$

Shear modulus:

$$G=\tau/\gamma$$

### 3.10 Poisson's Ratio

When a wire is stretched lengthwise, it usually becomes thinner sideways.

$$\nu=-\frac{\text{lateral strain}}{\text{longitudinal strain}}$$

For most materials:

$$0<\nu<0.5$$

Useful relations:

$$Y=2G(1+\nu)$$

$$Y=3K(1-2\nu)$$

### 3.11 Rod Under Its Own Weight

For a uniform vertical rod of length $L$, density $\rho$, and Young's modulus $Y$, suspended from the top, tension varies with position.

At distance $x$ from the bottom:

$$T(x)=\rho A x g$$

Small extension of an element $dx$:

$$d\ell=T(x)dx/(AY)$$

So:

$$d\ell=\rho gx\,dx/Y$$

Total extension:

$$\Delta L=\int_0^L \rho gx\,dx/Y$$

Therefore:

$$\Delta L=\rho gL^2/(2Y)$$

Equivalent form using mass $M=\rho AL$:

$$\Delta L=MgL/(2AY)$$

### 3.12 Series and Parallel Wires

#### Series

Same force acts through both wires.

$$\Delta L=\Delta L_1+\Delta L_2$$

For each wire:

$$\Delta L_i=FL_i/(A_iY_i)$$

Compliance adds in series.

#### Parallel

Same extension occurs in both wires.

For each wire:

$$F_i=k_i\Delta L$$

where:

$$k_i=A_iY_i/L_i$$

Equivalent spring constant:

$$k_{eq}=k_1+k_2$$

### 3.13 Physics Drill Record

#### P1: Wire Extension

For a wire of length $L$, area $A$, Young's modulus $Y$, pulled by force $F$:

Extension:

$$\Delta L=FL/(AY)$$

Elastic energy:

$$U=F^2L/(2AY)$$

Effective spring constant:

$$k=AY/L$$

User gave $k=A/(YL)$, which is incorrect. Since a larger Young's modulus means a stiffer wire, $Y$ must be in the numerator.

#### P2: Two Wires in Series

Wire 1:

$$\Delta L_1=FL/(AY)$$

Wire 2 has length $2L$, area $2A$, and Young's modulus $Y$:

$$\Delta L_2=F(2L)/(2AY)=FL/(AY)$$

Total extension:

$$\Delta L_{total}=2FL/(AY)$$

Status: correct.

#### P3: Rod Under Own Weight

Correct result:

$$\Delta L=\rho gL^2/(2Y)$$

Status: correct.

#### P4: Strain Energy Density

In terms of stress and Young's modulus:

$$u=\sigma^2/(2Y)$$

In terms of stress and strain:

$$u=\frac{1}{2}\sigma\epsilon$$

Status: correct.

---

## 4. Chemistry: Redox as Electron Bookkeeping and Thermodynamics

### 4.1 Core Meaning of Redox

Redox reactions involve electron transfer.

| Process | Meaning | Oxidation number change |
|---|---|---|
| Oxidation | loss of electrons | increases |
| Reduction | gain of electrons | decreases |

Memory hook:

```text
OIL RIG
Oxidation Is Loss.
Reduction Is Gain.
```

Example oxidation:

$$Zn\rightarrow Zn^{2+}+2e^-$$

Example reduction:

$$Cu^{2+}+2e^-\rightarrow Cu$$

Overall reaction:

$$Zn+Cu^{2+}\rightarrow Zn^{2+}+Cu$$

Zinc is oxidized and acts as the reducing agent. Copper ion is reduced and acts as the oxidizing agent.

### 4.2 Oxidizing Agent and Reducing Agent

| Species | What it does | What happens to it |
|---|---|---|
| Oxidizing agent | oxidizes another species | gets reduced |
| Reducing agent | reduces another species | gets oxidized |

This is a common trap: the oxidizing agent is itself reduced.

### 4.3 Oxidation Number Rules

| Rule | Example |
|---|---|
| Element in free state has oxidation number 0 | $Na$, $O_2$, $Cl_2$, $Fe$ |
| Monoatomic ion oxidation number equals charge | $Na^+$ is $+1$, $S^{2-}$ is $-2$ |
| Oxygen is usually $-2$ | $H_2O$, $CO_2$ |
| Hydrogen is usually $+1$ with nonmetals | $H_2O$, $HCl$ |
| Hydrogen is $-1$ in metal hydrides | $NaH$ |
| Fluorine is always $-1$ | $HF$, $OF_2$ |
| Sum in neutral compound is 0 | $H_2SO_4$ |
| Sum in polyatomic ion equals ion charge | $SO_4^{2-}$ |

### 4.4 Oxidation Number Examples

#### Sulfur in Sulfuric Acid

For $H_2SO_4$:

$$2(+1)+x+4(-2)=0$$

$$x=+6$$

So sulfur is $+6$.

#### Manganese in Permanganate

For $MnO_4^-$:

$$x+4(-2)=-1$$

$$x=+7$$

So manganese is $+7$.

#### Chromium in Dichromate

For $Cr_2O_7^{2-}$:

$$2x+7(-2)=-2$$

$$x=+6$$

So chromium is $+6$.

### 4.5 Identifying Redox

A reaction is redox if oxidation numbers change.

For $Fe^{2+}\rightarrow Fe^{3+}$:

Iron changes from $+2$ to $+3$, so it is oxidized.

For $Cl_2\rightarrow 2Cl^-$:

Chlorine changes from $0$ to $-1$, so it is reduced.

### 4.6 Half-Reaction Method

In acidic medium:

1. Split into oxidation and reduction half-reactions.
2. Balance all atoms except hydrogen and oxygen.
3. Balance oxygen using $H_2O$.
4. Balance hydrogen using $H^+$.
5. Balance charge using electrons.
6. Multiply half-reactions so electrons cancel.
7. Add and simplify.

For basic medium, first balance as acidic, then add $OH^-$ to both sides to neutralize $H^+$ into $H_2O$.

### 4.7 Permanganate Oxidizing Ferrous Ion in Acid

Skeleton:

$$MnO_4^-+Fe^{2+}\rightarrow Mn^{2+}+Fe^{3+}$$

Oxidation:

$$Fe^{2+}\rightarrow Fe^{3+}+e^-$$

Reduction:

$$MnO_4^-\rightarrow Mn^{2+}$$

Balance oxygen:

$$MnO_4^-\rightarrow Mn^{2+}+4H_2O$$

Balance hydrogen:

$$8H^++MnO_4^-\rightarrow Mn^{2+}+4H_2O$$

Balance charge by adding 5 electrons to the left:

$$5e^-+8H^++MnO_4^-\rightarrow Mn^{2+}+4H_2O$$

Multiply iron oxidation by 5:

$$5Fe^{2+}\rightarrow 5Fe^{3+}+5e^-$$

Add:

$$MnO_4^-+8H^++5Fe^{2+}\rightarrow Mn^{2+}+4H_2O+5Fe^{3+}$$

### 4.8 Basic Medium Example

For $MnO_4^-\rightarrow MnO_2$ in basic medium:

Balanced final half-reaction:

$$MnO_4^-+2H_2O+3e^-\rightarrow MnO_2+4OH^-$$

### 4.9 Electrochemical Cells

A redox reaction can be separated into two half-cells.

Daniell cell notation:

$$Zn|Zn^{2+}||Cu^{2+}|Cu$$

Overall reaction:

$$Zn+Cu^{2+}\rightarrow Zn^{2+}+Cu$$

Anode:

$$Zn\rightarrow Zn^{2+}+2e^-$$

Cathode:

$$Cu^{2+}+2e^-\rightarrow Cu$$

Memory hook:

```text
AN OX, RED CAT
Anode = oxidation.
Cathode = reduction.
```

In a galvanic cell:

- anode is negative
- cathode is positive
- electrons flow from anode to cathode
- conventional current flows opposite electron flow

### 4.10 Standard Cell Potential

Electrode potentials are tabulated as standard reduction potentials.

The more positive the reduction potential, the stronger the oxidizing agent.

For a cell:

$$E^\circ_{cell}=E^\circ_{cathode}-E^\circ_{anode}$$

For the Daniell cell:

$$E^\circ_{cell}=0.34-(-0.76)=1.10\ V$$

Positive cell potential means spontaneous under standard conditions.

### 4.11 Thermodynamic Link

Electrical work connects redox with Gibbs free energy.

$$\Delta G=-nFE_{cell}$$

Under standard conditions:

$$\Delta G^\circ=-nFE^\circ_{cell}$$

| Symbol | Meaning |
|---|---|
| $n$ | moles of electrons transferred |
| $F$ | Faraday constant, approximately $96500\ C\ mol^{-1}$ |
| $E_{cell}$ | cell potential |

Spontaneity rule:

| $E_{cell}$ | $\Delta G$ | Meaning |
|---:|---:|---|
| positive | negative | spontaneous |
| zero | zero | equilibrium |
| negative | positive | non-spontaneous |

### 4.12 Link with Equilibrium Constant

From thermodynamics:

$$\Delta G^\circ=-RT\ln K$$

From electrochemistry:

$$\Delta G^\circ=-nFE^\circ_{cell}$$

Equate:

$$-nFE^\circ_{cell}=-RT\ln K$$

So:

$$\ln K=nFE^\circ_{cell}/RT$$

At $298\ K$:

$$\log K=nE^\circ_{cell}/0.0591$$

### 4.13 Nernst Equation Preview

For non-standard conditions:

$$E_{cell}=E^\circ_{cell}-(RT/nF)\ln Q$$

At $298\ K$:

$$E_{cell}=E^\circ_{cell}-(0.0591/n)\log Q$$

At equilibrium:

$$E_{cell}=0$$

and:

$$Q=K$$

### 4.14 Disproportionation and Comproportionation

Disproportionation: the same element is both oxidized and reduced.

Example:

$$2H_2O_2\rightarrow 2H_2O+O_2$$

Comproportionation: two different oxidation states of the same element combine to form an intermediate oxidation state.

Example:

$$Fe+2Fe^{3+}\rightarrow 3Fe^{2+}$$

### 4.15 Chemistry Drill Record

#### C1: Oxidation Number

For $Cr_2O_7^{2-}$:

$$2x+7(-2)=-2$$

$$x=+6$$

Status: correct.

#### C2: Identify Agents

Reaction:

$$Zn+Cu^{2+}\rightarrow Zn^{2+}+Cu$$

| Item | Correct answer |
|---|---|
| Species oxidized | $Zn$ |
| Species reduced | $Cu^{2+}$ |
| Oxidizing agent | $Cu^{2+}$ |
| Reducing agent | $Zn$ |

User idea was correct, but notation should be $Cu^{2+}$ rather than $Cu$.

#### C3: Redox Balancing in Acid

Correct balanced equation:

$$MnO_4^-+8H^++5Fe^{2+}\rightarrow Mn^{2+}+4H_2O+5Fe^{3+}$$

Status: correct.

#### C4: Redox Thermodynamics

Given:

$$n=2$$

$$F=96500\ C\ mol^{-1}$$

$$E^\circ_{cell}=1.10\ V$$

Use:

$$\Delta G^\circ=-nFE^\circ_{cell}$$

Substitute:

$$\Delta G^\circ=-(2)(96500)(1.10)$$

$$\Delta G^\circ=-212300\ J\ mol^{-1}$$

Convert to kJ:

$$\Delta G^\circ=-212.3\ kJ\ mol^{-1}$$

User answer had one extra factor of 10.

---

## 5. Required Output: Problem Set

### 5.1 Mathematics Problem Set

#### Problem M1: Diagonal Matrix Eigenvectors

**Difficulty: JEE Adv L2**

For $A=[(5,0),(0,-2)]$, find eigenvalues and one eigenvector for each.

Answer:

- Eigenvalue $5$, eigenvector $(1,0)^T$
- Eigenvalue $-2$, eigenvector $(0,1)^T$

#### Problem M2: Upper Triangular Matrix

**Difficulty: JEE Adv L3**

For $A=[(3,1),(0,2)]$, find eigenvalues and eigenvectors.

Answer:

- $\lambda=2$, eigenvector $(1,-1)^T$
- $\lambda=3$, eigenvector $(1,0)^T$

#### Problem M3: Rotation Matrix

**Difficulty: Olympiad L1**

For $C=[(0,-1),(1,0)]$, determine whether real eigenvectors exist.

Answer:

No real eigenvectors exist because the characteristic equation is $\lambda^2+1=0$, giving $\lambda=\pm i$.

---

### 5.2 Physics Problem Set

#### Problem P1: Wire Extension

**Difficulty: JEE Adv L2**

A wire of length $L$, area $A$, and Young's modulus $Y$ is pulled by force $F$. Find extension, energy, and effective spring constant.

Answer:

$$\Delta L=FL/(AY)$$

$$U=F^2L/(2AY)$$

$$k=AY/L$$

#### Problem P2: Two Wires in Series

**Difficulty: JEE Adv L3**

Wire 1 has length $L$, area $A$, Young's modulus $Y$. Wire 2 has length $2L$, area $2A$, Young's modulus $Y$. The series combination is pulled by force $F$. Find total extension.

Answer:

$$\Delta L_{total}=2FL/(AY)$$

#### Problem P3: Rod Under Its Own Weight

**Difficulty: Olympiad L1**

A uniform rod of length $L$, density $\rho$, and Young's modulus $Y$ is suspended vertically from its top. Find extension.

Answer:

$$\Delta L=\rho gL^2/(2Y)$$

#### Problem P4: Strain Energy Density

**Difficulty: JEE Adv L3**

Find strain energy density in terms of stress $\sigma$ and Young's modulus $Y$.

Answer:

$$u=\sigma^2/(2Y)$$

Also:

$$u=\frac{1}{2}\sigma\epsilon$$

---

### 5.3 Chemistry Problem Set

#### Problem C1: Oxidation Number

**Difficulty: JEE Adv L2**

Find chromium oxidation number in $Cr_2O_7^{2-}$.

Answer:

$$Cr=+6$$

#### Problem C2: Redox Agents

**Difficulty: JEE Adv L2**

For $Zn+Cu^{2+}\rightarrow Zn^{2+}+Cu$, identify oxidized species, reduced species, oxidizing agent, and reducing agent.

Answer:

| Item | Answer |
|---|---|
| Oxidized species | $Zn$ |
| Reduced species | $Cu^{2+}$ |
| Oxidizing agent | $Cu^{2+}$ |
| Reducing agent | $Zn$ |

#### Problem C3: Acidic Redox Balancing

**Difficulty: JEE Adv L3**

Balance $MnO_4^-+Fe^{2+}\rightarrow Mn^{2+}+Fe^{3+}$ in acidic medium.

Answer:

$$MnO_4^-+8H^++5Fe^{2+}\rightarrow Mn^{2+}+4H_2O+5Fe^{3+}$$

#### Problem C4: Redox Thermodynamics

**Difficulty: Olympiad L1**

A galvanic cell transfers $2$ mol electrons per mole reaction and has $E^\circ_{cell}=1.10\ V$. Use $F=96500\ C\ mol^{-1}$. Find $\Delta G^\circ$.

Answer:

$$\Delta G^\circ=-212.3\ kJ\ mol^{-1}$$

---

## 6. Formula Sheet

### Mathematics

$$Av=\lambda v$$

$$(A-\lambda I)v=0$$

$$\det(A-\lambda I)=0$$

$$\lambda^2-\operatorname{tr}(A)\lambda+\det(A)=0$$

$$A^nv=\lambda^nv$$

### Physics

$$\sigma=F/A$$

$$\epsilon=\Delta L/L$$

$$Y=(F/A)/(\Delta L/L)$$

$$\Delta L=FL/(AY)$$

$$k=AY/L$$

$$U=\frac{1}{2}F\Delta L$$

$$U=F^2L/(2AY)$$

$$u=\frac{1}{2}Y\epsilon^2$$

$$u=\frac{1}{2}\sigma\epsilon$$

$$u=\sigma^2/(2Y)$$

$$\Delta L_{self}=\rho gL^2/(2Y)$$

### Chemistry

$$\text{oxidation}=\text{loss of electrons}$$

$$\text{reduction}=\text{gain of electrons}$$

$$E^\circ_{cell}=E^\circ_{cathode}-E^\circ_{anode}$$

$$\Delta G=-nFE_{cell}$$

$$\Delta G^\circ=-nFE^\circ_{cell}$$

$$\Delta G^\circ=-RT\ln K$$

$$\ln K=nFE^\circ_{cell}/RT$$

$$E_{cell}=E^\circ_{cell}-(RT/nF)\ln Q$$

---

## 7. Error Log

| Code | Topic | Error | Correction |
|---|---|---|---|
| P1 | Elastic spring constant | Wrote $k=A/(YL)$ | Correct is $k=AY/L$ |
| C2 | Redox notation | Wrote $Cu$ for reduced species and oxidizing agent | Correct species is $Cu^{2+}$ |
| C4 | Redox thermodynamics | Extra factor of 10 in $\Delta G^\circ$ | Correct value is $-212300\ J\ mol^{-1}=-212.3\ kJ\ mol^{-1}$ |

---

## 8. Short Ways and Memory Hooks

### Mathematics

- Eigenvector = direction preserved by transformation.
- Eigenvalue = scale factor in that direction.
- Characteristic equation = $\det(A-\lambda I)=0$.
- Eigenvectors can be multiplied by any nonzero scalar.

### Physics

- Stress = load intensity.
- Strain = fractional deformation.
- Young's modulus = resistance to length change.
- Elastic energy = area under force-extension graph.
- A stiffer wire has larger $Y$, so $Y$ must be in numerator of $k=AY/L$.

### Chemistry

- OIL RIG: Oxidation Is Loss, Reduction Is Gain.
- AN OX, RED CAT: anode oxidation, cathode reduction.
- Oxidizing agent is reduced.
- Positive $E$ means negative $\Delta G$.
- Do not forget $n$ in $\Delta G=-nFE$.

---

## 9. Completion Checklist

| Item | Status |
|---|---|
| Linear transformations | Complete |
| Eigenvectors | Complete |
| Eigenvalues | Complete |
| Characteristic equation | Complete |
| Rotation matrix eigenvector concept | Complete |
| Stress and strain | Complete |
| Young's modulus | Complete |
| Elastic energy | Complete |
| Strain energy density | Complete |
| Rod under self-weight | Complete |
| Redox basics | Complete |
| Oxidation number | Complete |
| Half-reaction balancing | Complete |
| Electrochemical cells | Complete |
| Redox thermodynamics | Complete |
| Problem set | Complete |

$$\boxed{\text{Week 2 Day 2 Complete}}$$
