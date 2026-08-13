[<- All artifacts](<../index.md>)

# Operational Equivalence Classes for Quantum Black-Hole Simulation (revised)

**Contents:**

  * 3 Theory Statements
  * Predictions
  * Conflicting & Unaccounted Evidence



### 3 Theory Statements

### Observable-first criterion for black-hole simulation

A quantum-simulation claim for “black-hole physics” is well-posed only after specifying (1) a target observable set O, (2) an explicit mapping M from a gravitational/toy-gravity model to device degrees of freedom such that M(O) is measurable, and (3) at least one validation relation R among observables in O that should be preserved under M within a defined regime W (e.g., detailed-balance/thermal form for horizon emission; chaos-bound-consistent OTOC growth; teleportation/decoding fidelity bounds tied to mutual information/OTOCs; Page-like entropy transition). Absent (O,M,R,W), the statement “we simulated a black hole” is underdetermined because different simulations can match a single signature while disagreeing on others.

**Supporting evidence:**

  * Superconducting ‘on-chip lattice black hole’ targets a mapped 1+1D Dirac-in-curved-spacetime → site-dependent XY chain and validates via occupation dynamics, Boltzmann-like emission probabilities, and entanglement measures, while explicitly not simulating dynamical gravity/backreaction. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



  * BEC Unruh simulator validates Unruh-like thermality via fitted temperature–acceleration proportionality and phase coherence/reversibility diagnostics, highlighting that the ‘thermal’ signature is local while the global state remains coherent. [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>)



  * FLRW BEC simulator validates cosmological particle creation via correlation functions and Sakharov oscillations in spectral modes, showing analogue-gravity simulations depend on specified observables and regime (phononic linearized field, no metric backreaction). [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-001>)



  * Dirac→XY / Hubbard mapping work shows different coordinate choices yield different operational signatures (infinite redshift in Schwarzschild coordinates vs smooth horizon crossing in Painlevé), underscoring that O must be defined operationally. [Liu et al., 2024](<../extractions/extraction-simulation-of-the-massless-dirac-field-in-11d-curved-spacetime.md#c-001>)



  * Trapped-ion multiphoton QRM mapping simulates a single-particle Dirac equation in a 1+1D black-hole background; it targets redshift/free-fall/squeezing rather than Hawking radiation, demonstrating that ‘black-hole simulation’ depends on the chosen observable set. [Pedernales et al., 2017](<../extractions/extraction-dirac-equation-in-11-dimensional-curved-spacetime-and-the-multiphoton.md#c-001>)



  * Hawking-radiation VQE-on-IBMQ study targets ground-state energies of a discretized Schwarzschild-derived Hamiltonian to infer T~1/M and P~1/M^2 scalings; it is a different operational target than horizon emission/OTOCs/decoding. [Dhaulakhandi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-using-vqe-algorithm-on-ibm-qu.md#c-001>)



  * SYK/wormhole teleportation protocols target teleportation fidelity/mutual information and two-sided correlators as operational signatures of traversability, rather than simulating spacetime geometry directly. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-005>) [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>) [Bousso et al., 2022](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md#c-005>) [Joshi et al., 2026](<../extractions/extraction-gravitational-wave-induced-scrambling-delay-in-syk-wormhole-teleporta.md#c-001>) [Bao et al., 2018](<../extractions/extraction-traversable-wormholes-as-quantum-channels-exploring-cft-entanglement.md#c-001>)



  * Probabilistic Hayden–Preskill decoding protocol is defined entirely by operational success probability and fidelity bounds involving scrambling/OTOCs and mutual information, illustrating observable-first formulation in holographic information tasks. [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-001>)



  * Non-isometric Hayden–Preskill model implements decoding protocols on 7-qubit IBM hardware and validates against Haar-averaged analytic predictions, exemplifying explicit (O,M,R,W) structure for a toy ‘black hole’ channel. [Li et al., 2023](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md#c-001>)



  * Petz-map/JT construction treats a quantum computer as a conceptual amplitude engine for reconstruction; lack of explicit encoding/algorithm highlights that specifying M and validation R is essential for any simulation claim. [Penington et al., 2019](<../extractions/extraction-replica-wormholes-and-the-black-hole-interior.md#c-001>)



  * Qubit evaporation frameworks and bit/qubit toy models emphasize that different discrete models can share entropic behavior (Page-curve-like) while differing in microscopic rules, reinforcing the need to specify which relations are being matched. [Avery, 2011](<../extractions/extraction-qubit-models-of-black-hole-evaporation.md#c-001>) [Giddings, 2011](<../extractions/extraction-models-for-unitary-black-hole-disintegration.md#c-001>) [Almheiri et al., 2012](<../extractions/extraction-black-holes-complementarity-or-firewalls.md#c-003>)



### Feasibility boundary: kinematic vs interior-reconstruction tasks

On near-term quantum hardware, kinematic QFT-on-fixed-background signatures (horizon scattering/thermal-like emission, Unruh thermality, single-particle curved-spacetime propagation) are feasible when one can engineer the mapped Hamiltonian and measure local correlators; by contrast, interior reconstruction / evaporation unitarity tasks require additional capabilities that scale more harshly: (i) two-copy entanglement resources (EPR/TFD), (ii) controllable time reversal or implementation of U* / U^T for the relevant dynamics, (iii) postselection with success probability typically decreasing rapidly with message size or deep amplification/decoding iterations (e.g., Grover-like), and (iv) an experimentally verifiable partition of ‘radiation’ subsystems. Therefore, feasibility splits into a ‘kinematic class’ and a ‘reconstruction/decoding class’ with different resource bottlenecks and verification burdens.

**Supporting evidence:**

  * Probabilistic Hayden–Preskill decoder requires implementing U and U* (and related conjugates) and has postselection success probability scaling as ~1/d_A^2 in symmetric cases; analysis assumes perfect scrambling and ideal operations, limiting feasibility to tiny systems. [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-001>) [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-007>)



  * Non-isometric Hayden–Preskill toy model demonstrates decoding on 7-qubit IBM hardware using postselection and Grover-like amplification, explicitly framed as proof-of-principle and requiring knowledge of the scrambling unitary. [Li et al., 2023](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md#c-001>)



  * Traversable-wormhole teleportation protocols rely on preparing TFD/EPR-like entanglement between two copies and applying a two-sided coupling; white-paper discussions emphasize TFD preparation/scaling as a major obstacle. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-005>) [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>) [Bousso et al., 2022](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md#c-005>) [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-005>) [Maldacena et al., 2015](<../extractions/extraction-a-bound-on-chaos.md#c-003>) [Penington, 2019](<../extractions/extraction-entanglement-wedge-reconstruction-and-the-information-paradox.md#c-005>)



  * Petz-map reconstruction proposal in JT gravity requires computing overlaps/amplitudes ⟨ψ_i|ψ_j⟩ to build a Petz map on radiation, but provides no concrete encoding/algorithm/resources, highlighting the extra demands of reconstruction beyond kinematic simulation. [Penington et al., 2019](<../extractions/extraction-replica-wormholes-and-the-black-hole-interior.md#c-001>)



  * Superconducting on-chip lattice black hole realizes a mapped fixed-background lattice Hamiltonian and validates thermal-like emission and entanglement dynamics, without attempting interior reconstruction/decoding. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



  * BEC Unruh simulator and other analogue platforms demonstrate horizon-related thermality via pair-creation/squeezing mappings, but do not implement decoding protocols requiring two-copy control and U*. [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>) [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-003>)



  * SYK digital simulation proposals explicitly give steep resource scaling for simulating SYK dynamics (many Pauli strings, Trotterization, controlled operations for OTOCs), indicating that moving toward holographic reconstruction scales significantly harder than kinematic analogues. [García-Álvarez et al., 2016](<../extractions/extraction-digital-quantum-simulation-of-minimal-adscft-1.md#c-001>)



### Validation by universality windows

A quantum black-hole simulation is robust when it reproduces a universal relation in a controlled ‘universality window’ W where the relation is expected to be insensitive to microscopic details and to certain implementation imperfections. Canonical examples include: (i) horizon thermality relations such as P(E) ∝ e^{−E/T_H} with T_H determined by a controllable surface-gravity analogue (or Unruh T ∝ acceleration with coefficient ħ/(2πk_B)), and (ii) scrambling relations such as early/intermediate-time OTOC growth consistent with λ_L ≲ 2πT and approaching λ_L ≈ 2πT in maximally chaotic regimes. Outside W (late times, strong finite-size cutoffs, bounded operator norms, strong dispersion, or heavy stimulation), the same observables can deviate without falsifying the simulation claim if W was specified.

**Supporting evidence:**

  * Mapped lattice black-hole numerics show early-time exponential OTOC growth with fitted λ_L ≈ 2π T_H (approximate chaos-bound saturation), and the exponential window grows as lattice spacing decreases; level statistics shift from Poisson in no-horizon case to non-Poisson when a horizon is present. [Yang et al., 2019](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md#c-005>)



  * Superconducting on-chip lattice black hole extracts energy-resolved emission probabilities consistent with an exponential Boltzmann form and identifies an effective Hawking temperature tied to a surface-gravity analogue; also tracks entanglement measures across the analogue horizon. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



  * BEC Unruh simulator measures effective temperature proportional to acceleration with coefficient consistent with ħ/(2πk_B), and probes coherence/reversibility to show unitary squeezed-state origin of apparent thermality. [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>)



  * Classical numerical Hawking-radiation simulations on site-dependent hopping lattices find P(E) ~ exp(−E/T_H) with low-energy deviations attributed to finite lattice/IR cutoff, illustrating windowed validity. [Yang et al., 2019](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md#c-003>)



  * Analogue BEC horizon literature (cited) reports Hawking-like correlations/entanglement measurements and emphasizes hydrodynamic/low-energy regime limitations, consistent with a universality-window notion. [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-003>)



### Predictions

### 3 Likely outcomes

  * If a new superconducting/ion/atom platform implements a horizon-mapped hopping (or equivalent Bogoliubov pair-creation/squeezing map) and scans the coupling gradient near the horizon, then within an intermediate energy/time window it will observe P(E) approximately Boltzmann with an effective T_H proportional to the local ‘surface gravity’ parameter, while deviations concentrate at the IR cutoff and at late times due to reflections/finite size.

  * If a platform implements an SYK-like or black-hole-metric-mapped scrambler and can prepare approximate thermal states, then an early-time regime with exponential OTOC growth will appear; decreasing discretization errors / increasing effective system size should widen the exponential window before saturation.

  * If a protocol claims interior reconstruction/decoding, then decoded fidelity will drop sharply when any one of these is removed: (i) two-copy entanglement (TFD/EPR), (ii) access to U* or reliable time reversal, (iii) postselection/amplification depth sufficient to overcome small success probability; this drop will occur even if the system still scrambles strongly.




### 2 Unknown outcomes

  * A fault-tolerant quantum computer implementing an explicit amplitude-estimation-based subroutine for overlaps needed by Petz-map-type reconstructions will exhibit a measurable threshold in reconstructable code-subspace dimension: beyond a device-dependent maximum, reconstruction error will grow rapidly, mirroring code-subspace size limits suggested in replica-wormhole/island arguments.

  * Hybrid classical–quantum tensor-network schemes (small quantum tensors + classical contraction) applied to holographic toy models will extend accessible system sizes for certain observables (e.g., coarse Page-curve proxies or averaged OTOCs), but it is uncertain whether they preserve the same universality class as direct many-body simulation for real-time scrambling and decoding.




### Conflicting & Unaccounted Evidence

### 3 Negative experiments

  * Build two simulator implementations that both match a Hawking/Unruh-like thermal spectrum but yield inconsistent predictions for a second independent relation in the claimed observable set (e.g., cross-horizon entanglement/correlations). If the same ‘black-hole phenomenon’ is claimed without narrowing O and W, the observable-first criterion is violated.

  * Demonstrate scaling of Hayden–Preskill-style decoding to larger diary size d_A without (a) shrinking postselection success probability, or (b) increasing amplification/iteration depth, while maintaining high fidelity—this would contradict the feasibility-boundary statement.

  * Observe λ_L significantly exceeding 2πT in a regime with a well-defined temperature and controlled early-time window in a purported black-hole fast-scrambler simulation—this would contradict the universality-window criterion for chaos diagnostics.




### 1 Unaccounted for

  * The theory notes—but does not fully specify—a general, platform-independent certification procedure that distinguishes genuine quantum Hawking-pair entanglement from classical-field or stimulated-emission correlations across all analogue platforms. [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Steinhauer, 2015](<../extractions/extraction-observation-of-quantum-hawking-radiation-and-its-entanglement-in-an-a.md#c-005>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-005>)



* * *

**Related Artifacts:**

  * [Extraction: Replica wormholes and the black hole interior](<../extractions/extraction-replica-wormholes-and-the-black-hole-interior.md>)
  * [Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md>)
  * [Extraction: Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer](<../extractions/extraction-quantum-simulation-of-hawking-radiation-using-vqe-algorithm-on-ibm-qu.md>)
  * [Extraction: Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md>)
  * [Extraction: Simulation of the massless Dirac field in 1+1D curved spacetime](<../extractions/extraction-simulation-of-the-massless-dirac-field-in-11d-curved-spacetime.md>)
  * [Extraction: Black holes: complementarity or firewalls?](<../extractions/extraction-black-holes-complementarity-or-firewalls.md>)
  * [Extraction: Simulating quantum field theory in curved spacetime with quantum many-body systems](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md>)
  * [Extraction: Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography](<../extractions/extraction-traversable-wormholes-as-quantum-channels-exploring-cft-entanglement.md>)
  * [Extraction: Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md>)
  * [Extraction: Gravitational Wave-Induced Scrambling Delay in SYK Wormhole Teleportation](<../extractions/extraction-gravitational-wave-induced-scrambling-delay-in-syk-wormhole-teleporta.md>)
  * [Extraction: Quantum information scrambling: from holography to quantum simulators](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md>)
  * [Extraction: Entanglement wedge reconstruction and the information paradox](<../extractions/extraction-entanglement-wedge-reconstruction-and-the-information-paradox.md>)
  * [Extraction: Commuting SYK: a pseudo-holographic model](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md>)
  * [Extraction: Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md>)
  * [Extraction: Analogue simulations of quantum gravity with fluids](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md>)
  * [Extraction: Models for unitary black hole disintegration](<../extractions/extraction-models-for-unitary-black-hole-disintegration.md>)
  * [Extraction: Qubit models of black hole evaporation](<../extractions/extraction-qubit-models-of-black-hole-evaporation.md>)
  * [Extraction: Digital Quantum Simulation of Minimal AdS/CFT.](<../extractions/extraction-digital-quantum-simulation-of-minimal-adscft-1.md>)
  * [Extraction: A bound on chaos](<../extractions/extraction-a-bound-on-chaos.md>)
  * [Extraction: Quantum simulation of Unruh radiation](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md>)
  * [Extraction: Dirac Equation in (1+1)-Dimensional Curved Spacetime and the Multiphoton Quantum Rabi Model.](<../extractions/extraction-dirac-equation-in-11-dimensional-curved-spacetime-and-the-multiphoton.md>)
  * [Extraction: Observation of quantum Hawking radiation and its entanglement in an analogue black hole](<../extractions/extraction-observation-of-quantum-hawking-radiation-and-its-entanglement-in-an-a.md>)
  * [Extraction: Quantum field simulator for dynamics in curved spacetime](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md>)
  * [Extraction: Efficient decoding for the Hayden-Preskill protocol](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md>)



* * *

## Entities

[Replica wormholes and the black hole interior](<https://www.semanticscholar.org/paper/208309801>)

Geoff Penington, S. Shenker, D. Stanford et al. | 2019 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/208309801>)

[Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer](<https://www.semanticscholar.org/paper/245634244>)

Ritu Dhaulakhandi, B. K. Behera | 2021 | [Semantic Scholar](<https://www.semanticscholar.org/paper/245634244>)

[Efficient decoding for the Hayden-Preskill protocol](<https://www.semanticscholar.org/paper/54805207>)

Beni Yoshida, A. Kitaev | 2017 | [Semantic Scholar](<https://www.semanticscholar.org/paper/54805207>)

[Simulating quantum field theory in curved spacetime with quantum many-body systems](<https://www.semanticscholar.org/paper/218502756>)

Run-Qiu Yang, Hui Liu, Shi-ning Zhu et al. | 2019 | Physical Review Research | [Semantic Scholar](<https://www.semanticscholar.org/paper/218502756>)

[Quantum field simulator for dynamics in curved spacetime](<https://www.semanticscholar.org/paper/247011689>)

C. Viermann, Marius Sparn, Nikolas Liebster et al. | 2022 | Nature | [Semantic Scholar](<https://www.semanticscholar.org/paper/247011689>)

[Black holes: complementarity or firewalls?](<https://www.semanticscholar.org/paper/55581818>)

Ahmed Almheiri, D. Marolf, J. Polchinski et al. | 2012 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/55581818>)

[Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<https://www.semanticscholar.org/paper/259341708>)

Ran Li, Xuanhua Wang, Kun Zhang et al. | 2023 | Physical Review D | [Semantic Scholar](<https://www.semanticscholar.org/paper/259341708>)

[Digital Quantum Simulation of Minimal AdS/CFT.](<https://www.semanticscholar.org/paper/5144368>)

L. García-Álvarez, Í. Egusquiza, L. Lamata et al. | 2016 | Physical Review Letters | [Semantic Scholar](<https://www.semanticscholar.org/paper/5144368>)

[Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<https://www.semanticscholar.org/paper/245837521>)

R. Bousso, Xi Dong, Netta Engelhardt et al. | 2022 | [Semantic Scholar](<https://www.semanticscholar.org/paper/245837521>)

[Entanglement wedge reconstruction and the information paradox](<https://www.semanticscholar.org/paper/160009640>)

Geoffrey Penington | 2019 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/160009640>)

[Commuting SYK: a pseudo-holographic model](<https://www.semanticscholar.org/paper/259262526>)

Ping Gao | 2023 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/259262526>)

[Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography](<https://www.semanticscholar.org/paper/53601332>)

N. Bao, A. Chatwin-Davies, Jason Pollack et al. | 2018 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/53601332>)

[A bound on chaos](<https://www.semanticscholar.org/paper/84832638>)

J. Maldacena, S. Shenker, D. Stanford | 2015 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/84832638>)

[Dirac Equation in (1+1)-Dimensional Curved Spacetime and the Multiphoton Quantum Rabi Model.](<https://www.semanticscholar.org/paper/21724556>)

J. S. Pedernales, M. Beau, S. Pittman et al. | 2017 | Physical Review Letters | [Semantic Scholar](<https://www.semanticscholar.org/paper/21724556>)

[Qubit models of black hole evaporation](<https://www.semanticscholar.org/paper/54967526>)

Steven G. Avery | 2011 | [Semantic Scholar](<https://www.semanticscholar.org/paper/54967526>)

[Quantum information scrambling: from holography to quantum simulators](<https://www.semanticscholar.org/paper/244488292>)

Arpan Bhattacharyya, Lata Kh Joshi, Bhuvanesh Sundar | 2021 | The European Physical Journal C | [Semantic Scholar](<https://www.semanticscholar.org/paper/244488292>)

[Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<https://www.semanticscholar.org/paper/259075712>)

Yun-hao Shi, Run-Qiu Yang, Zhongcheng Xiang et al. | 2021 | Nature Communications | [Semantic Scholar](<https://www.semanticscholar.org/paper/259075712>)

[Analogue simulations of quantum gravity with fluids](<https://www.semanticscholar.org/paper/261139644>)

S. Braunstein, M. Faizal, L. Krauss et al. | 2023 | Nature Reviews Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/261139644>)

[Simulation of the massless Dirac field in 1+1D curved spacetime](<https://www.semanticscholar.org/paper/274233763>)

Zhilong Liu, Run-Qiu Yang, Heng Fan et al. | 2024 | Science China Physics Mechanics and Astronomy | [Semantic Scholar](<https://www.semanticscholar.org/paper/274233763>)

[Observation of quantum Hawking radiation and its entanglement in an analogue black hole](<https://www.semanticscholar.org/paper/119197166>)

J. Steinhauer | 2015 | Nature Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/119197166>)

[Models for unitary black hole disintegration](<https://www.semanticscholar.org/paper/73549087>)

S. Giddings | 2011 | [Semantic Scholar](<https://www.semanticscholar.org/paper/73549087>)

[Quantum simulation of Unruh radiation](<https://www.semanticscholar.org/paper/182221423>)

Jiazhong Hu, Lei Feng, Zhendong Zhang et al. | 2018 | Nature Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/182221423>)

[Gravitational Wave-Induced Scrambling Delay in SYK Wormhole Teleportation](<https://www.semanticscholar.org/paper/286669725>)

Sudhanva Joshi, S. K. Mishra | 2026 | [Semantic Scholar](<https://www.semanticscholar.org/paper/286669725>)

[Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<https://www.semanticscholar.org/paper/287425539>)

Moongul Byun, Keun-Young Kim, Hyeonsoo Lee | 2026 | [Semantic Scholar](<https://www.semanticscholar.org/paper/287425539>)

## Citation

Cite this artifact as `\cite{ast-revised-2026-08-13}`.
[code] 
    @misc{ast-revised-2026-08-13,
      title        = {Operational Equivalence Classes for Quantum Black-Hole Simulation (revised)},
      author       = {{Asta Theorizer}},
      year         = {2026},
      month        = {8},
      howpublished = {Asta Theorizer artifact},
      url          = {theories/operational-equivalence-classes-for-quantum-black-hole-simulation-revised.md},
      note         = {asta-artifact id: theory-1},
    }
[/code]
