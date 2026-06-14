# Week 2 Day 3: Probability, Fluids, and General Organic Chemistry

## 0. Plan Row and Completion Status

| Block | Required topic | Status |
|---|---|---|
| Mathematics | Probability/statistics for measurement | Complete |
| Physics | Fluids: Bernoulli, viscosity, surface tension | Complete |
| Chemistry | GOC: resonance, induction, acidity/basicity | Complete |
| Required output | Mechanism glossary | Complete |

---

## 1. Day Purpose

Week 2 Day 3 connects measurement uncertainty, fluid mechanics, and organic electron-flow logic.

- Probability reveals uncertainty structure in measurements.
- Fluid mechanics connects pressure, flow speed, viscosity, and surface effects.
- General Organic Chemistry explains electron density, resonance, induction, acidity/basicity, and intermediate stability.

---

## 2. Mathematics: Probability and Statistics for Measurement

### 2.1 Measurement Model

Measurement can be modeled as:

$$x_{measured}=x_{true}+\epsilon$$

Here, $\epsilon$ is measurement error.

Statistics is used for repeated measurements, error bars, uncertainty propagation, calibration, random noise, and regression.

### 2.2 Probability Basics

A sample space is the set of possible outcomes. An event is a subset of the sample space.

For a die:

$$S=\{1,2,3,4,5,6\}$$

For the event of an even outcome:

$$E=\{2,4,6\}$$

$$P(E)=3/6=1/2$$

### 2.3 Probability Axioms

$$0\le P(A)\le 1$$

$$P(S)=1$$

For mutually exclusive events:

$$P(A\cup B)=P(A)+P(B)$$

For general events:

$$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$

### 2.4 Conditional Probability and Independence

Conditional probability:

$$P(A|B)=P(A\cap B)/P(B)$$

Independence condition:

$$P(A\cap B)=P(A)P(B)$$

Equivalent condition:

$$P(A|B)=P(A)$$

| Relation | Meaning |
|---|---|
| Independent | one event does not change probability of the other |
| Mutually exclusive | both events cannot occur together |

### 2.5 Expected Value, Variance, and Standard Deviation

Expected value for discrete $X$:

$$E[X]=\sum x_iP(X=x_i)$$

Variance:

$$Var(X)=E[(X-\mu)^2]$$

Equivalent form:

$$Var(X)=E[X^2]-(E[X])^2$$

Standard deviation:

$$\sigma=\sqrt{Var(X)}$$

### 2.6 Sample Statistics

Sample mean:

$$\bar{x}=(x_1+x_2+\cdots+x_n)/n$$

Sample standard deviation:

$$s=\sqrt{\sum (x_i-\bar{x})^2/(n-1)}$$

Standard error:

$$SE=s/\sqrt{n}$$

| Quantity | Meaning |
|---|---|
| $s$ | spread of individual measurements |
| $SE$ | uncertainty in estimated mean |

### 2.7 Random and Systematic Error

| Error type | Meaning | Reduced by repetition? |
|---|---|---|
| Random error | fluctuates unpredictably | yes, by averaging |
| Systematic error | shifts all measurements in one direction | no |

Repeated measurement reduces random error but does not remove systematic bias.

### 2.8 Error Propagation

For:

$$Q=x^ay^bz^c$$

maximum fractional error is approximately:

$$\Delta Q/Q=|a|\Delta x/x+|b|\Delta y/y+|c|\Delta z/z$$

### 2.9 Distribution Previews

Normal distribution is used when many small errors combine.

Binomial distribution:

$$P(X=k)=\binom{n}{k}p^k(1-p)^{n-k}$$

$$E[X]=np$$

$$Var(X)=np(1-p)$$

Poisson distribution:

$$P(X=k)=e^{-\lambda}\lambda^k/k!$$

$$E[X]=\lambda$$

$$Var(X)=\lambda$$

### 2.10 Regression Preview

For a linear model:

$$y=mx+c$$

least squares minimizes:

$$S=\sum (y_i-mx_i-c)^2$$

| Law | Linear plot |
|---|---|
| Hooke law | $F$ vs $x$ |
| Ohm law | $V$ vs $I$ |
| First-order kinetics | $\ln[A]$ vs $t$ |
| Arrhenius equation | $\ln k$ vs $1/T$ |

### 2.11 Math Drill Record

#### M1: Mean, Standard Deviation, Standard Error

Data:

```text
9.8, 10.1, 10.0, 10.2, 9.9 cm
```

Sum:

$$9.8+10.1+10.0+10.2+9.9=50.0$$

Mean:

$$\bar{x}=50.0/5=10.0\ cm$$

Sum of squared deviations from $10.0$:

$$0.04+0.01+0+0.04+0.01=0.10$$

Sample standard deviation:

$$s=\sqrt{0.10/4}=0.1581\ cm$$

Standard error:

$$SE=0.1581/\sqrt{5}=0.0707\ cm$$

User values were corrected.

#### M2: Error Propagation

For:

$$Q=x^2y^3/z$$

with percentage errors $x=2\%$, $y=1\%$, and $z=3\%$:

$$2(2\%)+3(1\%)+3\%=10\%$$

Status: correct.

#### M3: Conditional Probability

Given first ball is not red, there are 3 red balls left out of 9 balls.

$$P(second\ red|first\ not\ red)=3/9=1/3$$

Status: correct.

#### M4: Poisson Model

Given $X$ has Poisson mean $\lambda=4$:

$$P(X=0)=e^{-4}=0.0183$$

$$P(X=2)=e^{-4}4^2/2!=8e^{-4}=0.1465$$

$$E[X]=4$$

$$Var(X)=4$$

User's $P(X=0)$ missed one decimal place. Other parts were correct.

---

## 3. Physics: Fluids

### 3.1 Density, Pressure, and Hydrostatics

Density:

$$\rho=m/V$$

Pressure:

$$P=F/A$$

Hydrostatic pressure:

$$P=P_0+\rho gh$$

Gauge pressure:

$$P_{gauge}=\rho gh$$

Absolute pressure:

$$P_{absolute}=P_{atm}+\rho gh$$

### 3.2 Pascal's Law and Buoyancy

Pascal's law:

$$F_1/A_1=F_2/A_2$$

Buoyant force:

$$F_B=\rho_{fluid}V_{displaced}g$$

For floating equilibrium:

$$F_B=mg$$

Floating fraction:

$$V_{immersed}/V_{total}=\rho_{object}/\rho_{fluid}$$

### 3.3 Continuity Equation

For incompressible steady flow:

$$A_1v_1=A_2v_2$$

Volume flow rate:

$$Q=Av$$

If area decreases, speed increases.

### 3.4 Bernoulli Equation

Bernoulli's equation is energy conservation per unit volume:

$$P+\rho gh+\frac{1}{2}\rho v^2=constant$$

Between two points:

$$P_1+\rho gh_1+\frac{1}{2}\rho v_1^2=P_2+\rho gh_2+\frac{1}{2}\rho v_2^2$$

For horizontal ideal flow, higher speed means lower static pressure.

### 3.5 Torricelli and Venturi Results

For a large tank with a hole at depth $h$:

$$v=\sqrt{2gh}$$

For a horizontal Venturi constriction, continuity and Bernoulli together show that narrower area produces higher speed and lower pressure.

### 3.6 Viscosity

Newton's law of viscosity:

$$F=\eta A(dv/dy)$$

Shear stress form:

$$\tau=\eta(dv/dy)$$

Reynolds number:

$$Re=\rho vD/\eta$$

| Reynolds number | Flow type |
|---:|---|
| $Re<2000$ | laminar |
| $Re>4000$ | turbulent |

### 3.7 Poiseuille's Law

For laminar flow through a cylindrical pipe:

$$Q=\pi r^4\Delta P/(8\eta L)$$

Key dependence:

$$Q\propto r^4$$

If radius doubles, flow rate becomes 16 times.

### 3.8 Stokes' Law and Terminal Velocity

Stokes drag:

$$F_v=6\pi\eta rv$$

Terminal velocity of a sphere:

$$v_t=2r^2g(\rho_s-\rho_f)/(9\eta)$$

### 3.9 Surface Tension and Capillarity

Surface tension:

$$T=F/L$$

Surface energy form:

$$T=\Delta E/\Delta A$$

Liquid drop excess pressure:

$$\Delta P=2T/R$$

Soap bubble excess pressure:

$$\Delta P=4T/R$$

Capillary rise:

$$h=2T\cos\theta/(\rho gr)$$

### 3.10 Physics Drill Record

#### P1: Torricelli Efflux

$$v=\sqrt{2gh}$$

Status: correct.

#### P2: Continuity and Bernoulli

Area changes from $A$ to $A/4$.

$$Av=(A/4)v_2$$

$$v_2=4v$$

Horizontal Bernoulli gives:

$$P_1-P_2=(1/2)\rho(16v^2-v^2)$$

$$P_1-P_2=(15/2)\rho v^2$$

Status: correct.

#### P3: Poiseuille Radius Dependence

$$Q\propto r^4$$

Doubling radius gives:

$$2^4=16$$

Status: correct.

#### P4: Excess Pressure

Liquid drop:

$$\Delta P_d=2T/R$$

Soap bubble:

$$\Delta P_b=4T/R$$

Ratio:

$$\Delta P_b/\Delta P_d=2$$

Status: correct.

---

## 4. Chemistry: GOC

### 4.1 GOC Framework

General Organic Chemistry explains electron-rich sites, electron-poor sites, charge stability, acidity/basicity, mechanism direction, leaving-group ability, and intermediate stability.

Central idea: organic chemistry is electron-flow chemistry.

### 4.2 Electron Displacement Effects

| Effect | Symbol | Path | Role |
|---|---|---|---|
| Inductive effect | +I or -I | sigma bonds | permanent polarization |
| Resonance effect | +M or -M | pi system | delocalization |
| Hyperconjugation | sigma-to-p overlap | adjacent sigma bonds | stabilizes cations, radicals, alkenes |
| Electromeric effect | +E or -E | pi bond during attack | temporary displacement |

### 4.3 Inductive Effect

Inductive effect is permanent electron displacement through sigma bonds.

A -I group withdraws electron density. A +I group donates electron density.

A -I group stabilizes negative charge and increases acidity.

A +I group stabilizes positive charge and increases basicity.

Example:

$$ClCH_2COOH>CH_3COOH$$

### 4.4 Resonance

Resonance is delocalization of pi electrons or lone pairs over adjacent atoms.

Rules:

1. Atom positions do not change.
2. Only electrons move.
3. Sigma bonds usually do not break.
4. Total charge remains constant.
5. Better contributors have complete octets and less charge separation.
6. Negative charge is better on more electronegative atoms.

The real molecule is a resonance hybrid.

### 4.5 +M and -M Effects

A +M group donates electron density by resonance.

Common +M groups: -OH, -OR, -NH2, -NHR, -NR2, and halogens.

A -M group withdraws electron density by resonance.

Common -M groups: -NO2, -CN, -CHO, -COR, -COOH, -COOR, -CONH2, and -SO3H.

### 4.6 Hyperconjugation

Hyperconjugation is sigma electron donation into an adjacent empty p orbital, pi orbital, or radical center.

It stabilizes carbocations, radicals, and alkenes.

### 4.7 Stability Trends

Carbocation stability:

$$benzylic/allylic>3^\circ>2^\circ>1^\circ>methyl$$

Carbanion stability for alkyl carbanions:

$$methyl>1^\circ>2^\circ>3^\circ$$

Hybridization effect for carbanions:

$$sp>sp^2>sp^3$$

Radical stability:

$$benzylic/allylic>3^\circ>2^\circ>1^\circ>methyl$$

### 4.8 Acidity and Basicity

Stronger acid means more stable conjugate base.

$$HA\rightarrow H^++A^-$$

Factors stabilizing conjugate base include electronegativity, resonance, -I effect, s-character, solvation, and aromaticity.

Stronger base means more available lone pair.

Factors decreasing basicity include resonance delocalization, electron-withdrawing groups, greater s-character, steric hindrance, and poor solvation.

Pyridine is more basic than pyrrole because pyridine's lone pair is available, while pyrrole's lone pair is part of aromaticity.

### 4.9 Electrophiles, Nucleophiles, and Leaving Groups

Electrophiles accept electron pairs. Nucleophiles donate electron pairs.

Good leaving groups are weak bases.

Typical leaving-group order:

$$I^->Br^->Cl^-\gg F^-$$

### 4.10 Chemistry Drill Record

#### C1: Inductive Effect

Strongest to weakest acidity:

$$CCl_3COOH>ClCH_2COOH>CH_3COOH$$

Increasing acidity:

$$CH_3COOH<ClCH_2COOH<CCl_3COOH$$

Reason: chlorine withdraws electron density by -I effect and stabilizes the carboxylate conjugate base.

Status: correct.

#### C2: Resonance and Acidity

More acidic compound:

$$CH_3COOH$$

Reason: acetate is resonance stabilized over two oxygen atoms. Ethoxide has localized negative charge.

Status: correct.

#### C3: Carbocation Stability

Decreasing stability:

$$(CH_3)_3C^+>(CH_3)_2CH^+>CH_3CH_2^+>CH_3^+$$

Reason: +I effect and hyperconjugation increase with alkyl substitution.

Status: correct.

#### C4: Basicity Trap

Pyridine is more basic than pyrrole.

Reason: pyridine's lone pair is available for protonation. Pyrrole's lone pair is part of aromaticity.

Status: correct.

---

## 5. Required Output: Mechanism Glossary

| Term | Definition | High-yield note |
|---|---|---|
| Inductive effect | Permanent electron polarization through sigma bonds | Decreases rapidly with distance |
| +I effect | Electron donation through sigma bonds | Stabilizes positive charge |
| -I effect | Electron withdrawal through sigma bonds | Stabilizes negative charge |
| Resonance | Delocalization of pi electrons or lone pairs | Atom positions do not change |
| +M effect | Electron donation by resonance | Common for lone-pair donors |
| -M effect | Electron withdrawal by resonance | Common for nitro, carbonyl, cyano groups |
| Hyperconjugation | Sigma electron donation into adjacent p or pi system | Stabilizes carbocations and radicals |
| Electrophile | Electron-pair acceptor | Electron-deficient species |
| Nucleophile | Electron-pair donor | Electron-rich species |
| Leaving group | Species that departs with an electron pair | Good leaving groups are weak bases |
| Carbocation | Positively charged carbon intermediate | Stabilized by +I, hyperconjugation, resonance |
| Carbanion | Negatively charged carbon intermediate | Stabilized by -I, resonance, and s-character |
| Radical | Species with unpaired electron | Stabilized by resonance and hyperconjugation |
| Transition state | High-energy structure along reaction path | Not isolable |
| Intermediate | Real species formed between steps | Local energy minimum |
| Rate-determining step | Slowest step in mechanism | Controls overall rate |
| Conjugate base | Species formed after acid loses H+ | More stable conjugate base means stronger acid |
| Conjugate acid | Species formed after base gains H+ | Useful for comparing basicity |
| Aromaticity | Cyclic, planar, fully conjugated system with 4n+2 pi electrons | Strongly stabilizing |
| Anti-aromaticity | Cyclic, planar, conjugated system with 4n pi electrons | Strongly destabilizing |
| Steric hindrance | Crowding that blocks approach or reaction | Can reduce nucleophilicity/basicity |
| Solvation | Stabilization by solvent molecules | Important in acidity/basicity |
| Regioselectivity | Preference for one constitutional product | Controlled by stability and electronics |
| Stereoselectivity | Preference for one stereoisomer | Controlled by geometry and mechanism |

---

## 6. Formula Sheet

### Mathematics

$$P(A|B)=P(A\cap B)/P(B)$$

$$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$

$$E[X]=\sum x_iP(X=x_i)$$

$$Var(X)=E[X^2]-(E[X])^2$$

$$s=\sqrt{\sum (x_i-\bar{x})^2/(n-1)}$$

$$SE=s/\sqrt{n}$$

$$P(X=k)=e^{-\lambda}\lambda^k/k!$$

$$\Delta Q/Q=|a|\Delta x/x+|b|\Delta y/y+|c|\Delta z/z$$

### Physics

$$P=P_0+\rho gh$$

$$F_B=\rho_{fluid}V_{displaced}g$$

$$A_1v_1=A_2v_2$$

$$P+\rho gh+\frac{1}{2}\rho v^2=constant$$

$$v=\sqrt{2gh}$$

$$Q=\pi r^4\Delta P/(8\eta L)$$

$$F_v=6\pi\eta rv$$

$$v_t=2r^2g(\rho_s-\rho_f)/(9\eta)$$

$$\Delta P_{drop}=2T/R$$

$$\Delta P_{bubble}=4T/R$$

$$h=2T\cos\theta/(\rho gr)$$

### Chemistry

$$stronger\ acid=more\ stable\ conjugate\ base$$

$$stronger\ base=more\ available\ lone\ pair$$

$$3^\circ\ carbocation>2^\circ>1^\circ>methyl$$

$$methyl\ carbanion>1^\circ>2^\circ>3^\circ$$

$$sp\ carbanion>sp^2\ carbanion>sp^3\ carbanion$$

$$I^->Br^->Cl^-\gg F^-$$

---

## 7. Error Log

| Code | Topic | Error | Correction |
|---|---|---|---|
| M1 | Measurement statistics | Mean and standard deviation computed from wrong values | Correct values are $\bar{x}=10.0\ cm$, $s=0.1581\ cm$, $SE=0.0707\ cm$ |
| M4 | Poisson probability | $P(X=0)$ written as 0.183 | Correct is $e^{-4}=0.0183$ |
| Physics | Drill | No errors | Maintain continuity-Bernoulli logic |
| Chemistry | Drill | No errors | Continue adding explanatory reasoning |

---

## 8. Short Ways and Memory Hooks

### Mathematics

- Standard deviation is spread of individual measurements.
- Standard error is uncertainty in the mean.
- Repetition reduces random error, not systematic error.
- Poisson has mean equal to variance.
- Error propagation multiplies powers into percentage-error coefficients.

### Physics

- Narrow pipe means faster flow.
- Faster horizontal ideal flow means lower pressure.
- Poiseuille flow depends on radius to the fourth power.
- Soap bubble has two surfaces, so excess pressure is $4T/R$.
- Bernoulli is energy conservation per unit volume.

### Chemistry

- Induction travels through sigma bonds.
- Resonance travels through pi overlap.
- Stronger acid has more stable conjugate base.
- Stronger base has more available lone pair.
- Pyridine is basic; pyrrole protects aromaticity.
- Resonance often dominates simple degree-based stability.

---

## 9. Completion Checklist

| Item | Status |
|---|---|
| Probability and statistics for measurement | Complete |
| Error propagation | Complete |
| Poisson model | Complete |
| Hydrostatics | Complete |
| Continuity equation | Complete |
| Bernoulli equation | Complete |
| Viscosity and Poiseuille law | Complete |
| Surface tension and capillarity | Complete |
| Inductive effect | Complete |
| Resonance | Complete |
| Acidity and basicity | Complete |
| Carbocation stability | Complete |
| Mechanism glossary | Complete |

$$\boxed{\text{Week 2 Day 3 Complete}}$$
