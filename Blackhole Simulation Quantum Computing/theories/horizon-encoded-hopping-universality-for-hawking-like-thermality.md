[<- All artifacts](<../index.md>)

# Horizon-Encoded Hopping Universality for Hawking-like Thermality

**Contents:**

  * 2 Theory Statements
  * Predictions
  * Conflicting & Unaccounted Evidence



### 2 Theory Statements

### Surface-gravity-to-temperature mapping in hopping encodings

For static 1+1D horizon encodings realized by mapping a curved-spacetime wave equation to a nearest-neighbor hopping Hamiltonian with site-dependent κn derived from a metric function f(x) possessing a simple zero at xh, the exterior energy-resolved occupation (or transmission/emission) probability admits an intermediate-energy window in which Pout(E) ≈ A(E) exp(−E/Teff), with Teff proportional to a discrete surface-gravity analogue gh ≈ f′(xh)/2 (up to coordinate conventions and discretization-dependent prefactors). The window excludes: (i) sufficiently low E where finite-size/IR cutoffs and boundary reflections dominate; and (ii) sufficiently high E where lattice dispersion/truncation (UV completion) and nonidealities dominate. The mapping is kinematic (fixed background; no backreaction), and Teff is an effective parameter inferred from Pout(E), not necessarily a global thermodynamic temperature of a many-body steady state.

**Supporting evidence:**

  * Superconducting on-chip ‘lattice black hole’ (10 transmons + 9 tunable couplers) encodes a horizon via site-dependent κj derived from f(x); the exterior (outside-horizon) reduced state in the energy basis yields probabilities Pn that are fit by P(E) ∝ exp(−E/TH), and TH is linked to surface-gravity formula TH = gh/(2π) with gh = f′(xh)/2 (via tunneling/detailed-balance picture). [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



  * Classical numerical simulation of a site-dependent hopping model with a chosen black-hole-like metric function reports that P(E) is consistent with a blackbody/Boltzmann form exp(−E/TH) for energies above a low-energy cutoff; TH is compared to the analytic Hawking temperature formula TH = gh/(2π). [Yang et al., 2019](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md#c-003>)



  * Mapping of 1+1D massless Dirac in curved spacetime to site-dependent tight-binding/XY model reports that tunneling rates match blackbody spectra; it explicitly finds coordinate-dependent outcomes (Schwarzschild vs Painlevé), including a factor-of-two difference in effective temperature fits (Schwarzschild giving ~2Tb while Painlevé yields Tb) and different horizon-crossing behavior. [Liu et al., 2024](<../extractions/extraction-simulation-of-the-massless-dirac-field-in-11d-curved-spacetime.md#c-001>)



  * The superconducting-chain experiment emphasizes it encodes the metric through κj ≈ f(xj+d/2)/(4d) and uses the standard tunneling/surface-gravity temperature relation in its validation, directly tying the fitted exponential spectrum to the local horizon gradient. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



### Finite-size IR cutoff and reflection law for breakdown of apparent thermality

In a finite-length horizon-encoded hopping chain (open boundaries and finite outer region), deviations from the exponential form Pout(E) ∝ exp(−E/Teff) appear first at low energies and late times. The lowest-energy portion of the spectrum is most sensitive to: chain length L, boundary conditions (e.g., Dirichlet/open), and the outer-region cutoff/box size, producing an effective IR scale EIR(L,BC) below which Pout(E) bends away from a Boltzmann line. Increasing L (or implementing absorbing/impedance-matched boundaries) lowers EIR and delays contamination from reflections, thereby widening the energy window and time window over which an exponential spectrum and clean inside/outside entanglement growth can be extracted.

**Supporting evidence:**

  * Classical lattice Hawking-radiation numerics explicitly report low-energy deviations from blackbody behavior due to finite lattice/IR cutoff and discuss that truncation/cutoffs affect the lowest-energy modes. [Yang et al., 2019](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md#c-003>)



  * The superconducting on-chip lattice black hole experiment lists finite-size lattice and boundary reflections as key limitations affecting long-time dynamics and extracted observables; it also references larger-chain numerics to assess finite-size effects. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



### Predictions

### 3 Likely outcomes

  * Temperature-slope scaling test: In a superconducting or trapped-ion hopping-chain horizon simulator, rescaling the local near-horizon gradient of κj (equivalently f′(xh)) by a factor s while holding the rest of the profile fixed will, over the same intermediate-energy window, rescale the fitted Teff by approximately s (within discretization-dependent prefactors).

  * IR-window widening: Increasing chain length L (or adding engineered absorbing boundaries) at fixed near-horizon gradient will push the onset of low-energy deviations to smaller E and allow exponential fits over a broader energy range and for longer evolution times before reflection-induced contamination.

  * Coordinate-encoding sensitivity: Implement two coupling profiles corresponding to different coordinate analogues (e.g., an encoding that yields smooth crossing vs one emphasizing tunneling). The qualitative existence of an intermediate-energy exponential window persists, but (i) the inferred prefactor relating Teff to f′(xh) can shift, and (ii) wavepacket dynamics near the horizon differ (slowing/trapping vs crossing).




### 2 Unknown outcomes

  * Emergent greybody analog from interactions: In a many-excitation regime (higher densities or added interactions beyond free hopping), the outgoing spectrum may factorize as Pout(E) ≈ Γ(E) exp(−E/Teff), where Γ(E) behaves like a device-tunable ‘greybody factor’ determined by interaction-induced mode-mixing and finite-density effects; whether Γ(E) exhibits universality classes across platforms is unclear.

  * Two-sided hopping-chain wormhole proxy: Coupling two horizon-encoded hopping chains and preparing an entangled (TFD-like) initial state might yield two-sided correlators whose decay rates and teleportation-like diagnostics correlate with the same near-horizon gradient that sets Teff in one-sided emission. If true, it would unify Hawking-spectrum inference with wormhole-teleportation observables within a single hopping-based simulator family; feasibility and scaling are uncertain.




### Conflicting & Unaccounted Evidence

### 3 Negative experiments

  * Hold f′(xh) fixed but change far-region profile: Build two coupling profiles with the same local horizon gradient and discretization near xh but significantly different outer-region structure. If fitted Teff in the intermediate-energy window differs beyond expected discretization/systematic errors, the ‘local surface-gravity control’ claim is weakened.

  * Length scaling falsification: Increase chain length (or reduce reflections via boundary engineering) while keeping the near-horizon region identical. If the low-energy deviation scale does not move to lower E or if reflections do not affect late-time contamination, the IR/reflection breakdown law is challenged.

  * No-horizon control: Implement a monotone κ profile with no horizon (no f(x) zero / no sign change in the relevant mapping) but otherwise similar bandwidth and disorder. If a robust intermediate-energy exponential spectrum with the same Teff–gradient relation appears, that would imply the mechanism is not horizon-specific (but rather generic thermalization or filtering), contradicting the horizon-centered interpretation.




### 3 Unaccounted for

  * Unruh/Hawking-Unruh thermality produced by parametric pair creation in a driven BEC yields thermal mode distributions without any spatial horizon encoded as a hopping zero; this theory intentionally does not cover non-horizon thermality mechanisms (acceleration-frame or time-dependent squeezing). [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>)



  * SQUID-array analogue Hawking radiation proposals create horizons by modulating propagation speed rather than by discrete hopping profiles; while conceptually related (effective metric via wave speed), it lies outside the nearest-neighbor hopping-chain domain of this theory. [Terrones et al., 2021](<../extractions/extraction-towards-quantum-simulation-of-black-holes-in-a-dc-squid-array.md#c-003>)



  * Sonic/BEC acoustic-horizon experiments that measure Hawking/partner correlations and entanglement involve quantum fields on an emergent acoustic metric with continuous modes and dispersion; they share ‘horizon → thermal-like emission’ themes but are not captured by the discrete hopping-chain surface-gravity law as stated. [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-003>) [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-005>)



* * *

**Related Artifacts:**

  * [Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md>)
  * [Extraction: Simulation of the massless Dirac field in 1+1D curved spacetime](<../extractions/extraction-simulation-of-the-massless-dirac-field-in-11d-curved-spacetime.md>)
  * [Extraction: Simulating quantum field theory in curved spacetime with quantum many-body systems](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md>)
  * [Extraction: Analogue simulations of quantum gravity with fluids](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md>)
  * [Extraction: Towards Quantum Simulation of Black Holes in a dc-SQUID Array](<../extractions/extraction-towards-quantum-simulation-of-black-holes-in-a-dc-squid-array.md>)
  * [Extraction: Quantum simulation of Unruh radiation](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md>)
  * [Extraction: Quantum field simulator for dynamics in curved spacetime](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md>)



* * *

## Entities

[Towards Quantum Simulation of Black Holes in a dc-SQUID Array](<https://www.semanticscholar.org/paper/239616504>)

Adri'an Terrones, C. Sab'in | 2021 | Universe | [Semantic Scholar](<https://www.semanticscholar.org/paper/239616504>)

[Simulating quantum field theory in curved spacetime with quantum many-body systems](<https://www.semanticscholar.org/paper/218502756>)

Run-Qiu Yang, Hui Liu, Shi-ning Zhu et al. | 2019 | Physical Review Research | [Semantic Scholar](<https://www.semanticscholar.org/paper/218502756>)

[Quantum field simulator for dynamics in curved spacetime](<https://www.semanticscholar.org/paper/247011689>)

C. Viermann, Marius Sparn, Nikolas Liebster et al. | 2022 | Nature | [Semantic Scholar](<https://www.semanticscholar.org/paper/247011689>)

[Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<https://www.semanticscholar.org/paper/259075712>)

Yun-hao Shi, Run-Qiu Yang, Zhongcheng Xiang et al. | 2021 | Nature Communications | [Semantic Scholar](<https://www.semanticscholar.org/paper/259075712>)

[Analogue simulations of quantum gravity with fluids](<https://www.semanticscholar.org/paper/261139644>)

S. Braunstein, M. Faizal, L. Krauss et al. | 2023 | Nature Reviews Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/261139644>)

[Simulation of the massless Dirac field in 1+1D curved spacetime](<https://www.semanticscholar.org/paper/274233763>)

Zhilong Liu, Run-Qiu Yang, Heng Fan et al. | 2024 | Science China Physics Mechanics and Astronomy | [Semantic Scholar](<https://www.semanticscholar.org/paper/274233763>)

[Quantum simulation of Unruh radiation](<https://www.semanticscholar.org/paper/182221423>)

Jiazhong Hu, Lei Feng, Zhendong Zhang et al. | 2018 | Nature Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/182221423>)

## Citation

Cite this artifact as `\cite{ast-horizon-2026-08-13}`.
[code] 
    @misc{ast-horizon-2026-08-13,
      title        = {Horizon-Encoded Hopping Universality for Hawking-like Thermality},
      author       = {{Asta Theorizer}},
      year         = {2026},
      month        = {8},
      howpublished = {Asta Theorizer artifact},
      url          = {theories/horizon-encoded-hopping-universality-for-hawking-like-thermality.md},
      note         = {asta-artifact id: theory-5},
    }
[/code]
