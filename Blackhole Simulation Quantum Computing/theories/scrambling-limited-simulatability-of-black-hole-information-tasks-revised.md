[<- All artifacts](<../index.md>)

# Scrambling-Limited Simulatability of Black-Hole Information Tasks (revised)

**Contents:**

  * 3 Theory Statements
  * Predictions
  * Conflicting & Unaccounted Evidence



### 3 Theory Statements

### Conjugate-control requirement for recovery (beyond forward simulation)

For generic black-hole-information recovery tasks (Hayden–Preskill decoding, teleportation-as-decoding, and entanglement-wedge/Petz-style reconstructions), implementing only the forward scrambler U is not sufficient: one also needs operational access to conjugate dynamics (U*, U^T, or U^{-1}) or an effective time-reversal/echo (e.g., Hamiltonian sign flip), together with two-copy entanglement resources and projective operations (e.g., Bell/EPR projections). Absent such conjugate control, recovery fidelity cannot generically approach unity even if forward-only scrambling diagnostics (e.g., OTOCs/level statistics) appear black-hole-like.

**Supporting evidence:**

  * Probabilistic Hayden–Preskill decoder requires applying U _to a copy and then an EPR projection; fidelity bounds depend on scrambling and subsystem sizes; need for U_ , U^T explicitly discussed as part of protocol. [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-001>)



  * Yoshida–Kitaev/Hayden–Preskill decoding protocols explicitly use U and U* and EPR projections; deterministic variant uses Grover-like iterations rather than relying solely on forward evolution. [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-007>)



  * Non-isometric Hayden–Preskill quantum simulations implement U and U* and use postselection/Grover-like strategies on IBM 7-qubit processors, underscoring that decoding is an additional control requirement beyond forward scrambling. [Li et al., 2023](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md#c-001>)



  * Ancilla-based n-time correlator / OTOC protocols require controlled operations plus the ability to implement forward and backward evolution (echo) to access scrambling correlators central to decoding-style diagnostics. [García-Álvarez et al., 2016](<../extractions/extraction-digital-quantum-simulation-of-minimal-adscft.md#c-005>) [Swingle et al., 2016](<../extractions/extraction-measuring-the-scrambling-of-quantum-information.md#c-001>) [Franz et al., 2018](<../extractions/extraction-mimicking-black-hole-event-horizons-in-atomic-and-solid-state-systems.md#c-013>)



  * Cold-atom SYK proposal’s OTOC measurement relies on implementing backward evolution by flipping PA detunings (Hamiltonian sign inversion), illustrating physical realization of conjugate control as a requirement for multi-time correlators relevant to scrambling/decoding. [Danshita et al., 2016](<../extractions/extraction-creating-and-probing-the-sachdev-ye-kitaev-model-with-ultracold-gases-1.md#c-001>)



  * Traversable-wormhole teleportation protocol descriptions require TFD preparation and a specific two-sided coupling; decoding/teleportation interpreted as boundary operation corresponding to bulk traversability, which is more than forward-only scrambling. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-005>) [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>) [Bousso et al., 2022](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md#c-005>) [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-005>) [Bao et al., 2018](<../extractions/extraction-traversable-wormholes-as-quantum-channels-exploring-cft-entanglement.md#c-001>)



  * Conceptual Petz-map reconstruction proposal presumes a quantum computer can compute amplitudes to build a Petz-like operator acting on radiation; this is explicitly a reconstruction task that goes beyond forward dynamics simulation and is sensitive to code-subspace size and factorization/ensemble issues. [Penington et al., 2019](<../extractions/extraction-replica-wormholes-and-the-black-hole-interior.md#c-001>)



### Postselection–depth–noise tradeoff for scalable recovery

In Hayden–Preskill-style recovery experiments on finite-dimensional scramblers, higher recovery fidelity can be achieved either by (i) postselection on a Bell/EPR projection whose success probability typically scales poorly with diary size (e.g., symmetric case success ~1/d_A^2), or by (ii) replacing postselection by amplitude amplification (Grover-like iterations) requiring circuit depth scaling O(d_A) (or comparable) in the diary dimension. On noisy hardware, these routes quickly become impractical as d_A increases because either the number of trials (postselection) or accumulated gate errors (deep Grover iterations) grows rapidly.

**Supporting evidence:**

  * Probabilistic postselection-based decoder analysis gives success probability lower bound and typical scaling (symmetric case ≈1/d_A^2) and fidelity bound in terms of scrambling conditions. [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-001>)



  * Review of Hayden–Preskill / Yoshida–Kitaev decoders states probabilistic success ≥1/d_A^2 and deterministic Grover-style decoding needs ~π d_A/4 iterations, i.e., depth scaling O(d_A). [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-007>)



  * Non-isometric HP quantum-simulation paper implements both probabilistic and Grover-like strategies on IBM 7-qubit devices and frames them as proof-of-principle with scaling limitations. [Li et al., 2023](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md#c-001>)



### Diagnostic–dynamics hierarchy: chaos is easier than semiclassical bulk emulation

Across quantum-simulation approaches to black-hole-like physics, forward-only scrambling diagnostics (OTOCs, level-spacing statistics, coarse thermal spectra) and kinematic horizon analogues can be demonstrated at substantially smaller system size and with looser control than protocols that aim for credible semiclassical holographic dynamics (e.g., large-N noncommuting SYK in the Schwarzian regime, high-fidelity finite-temperature TFD preparation, or interior reconstruction). Consequently, near-term quantum computers and analogue devices will preferentially realize (and validate) diagnostic signatures before they can realize scalable, bulk-interpretable decoding/reconstruction.

**Supporting evidence:**

  * Numerical lattice analogue study reports OTOC exponential growth with fitted λ_L ≈ 2π T_H and horizon-dependent level-spacing deviations from Poisson; no TFD preparation required for these forward diagnostics. [Yang et al., 2019](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md#c-005>)



  * SYK ‘on a chip’ proposal numerically reproduces level statistics and thermodynamics for finite N, but explicitly notes OTOC measurement remains an open experimental challenge and finite-N limits prevent extracting universal Lyapunov exponent. [Pikulin et al., 2017](<../extractions/extraction-black-hole-on-a-chip-proposal-for-a-physical-realization-of-the-sachd.md#c-001>)



  * Other analog SYK proposals (Majorana wires+dot; graphene LL0 cSYK) emphasize feasibility of spectroscopic/thermodynamic probes but highlight difficulty of measuring OTOCs in solid-state realizations. [Franz et al., 2018](<../extractions/extraction-mimicking-black-hole-event-horizons-in-atomic-and-solid-state-systems.md#c-009>)



  * Traversable wormhole/teleportation discussions emphasize the difficulty of preparing TFD states and scaling beyond small proof-of-principle experiments on noisy simulators. [Bousso et al., 2022](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md#c-005>) [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-005>)



  * Commuting SYK wormhole-teleportation analysis notes teleportation signatures can arise from non-holographic mechanisms (peaked size, thermalization), warning that small-N accessibility does not guarantee semiclassical gravity interpretation. [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>)



  * Referenced small-N learned/commuting Hamiltonian wormhole experiment (Sycamore) is noted as controversial precisely because commuting structure challenges holographic interpretation despite observable teleportation-like signal. [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-005>)



  * Superconducting ‘on-chip lattice black hole’ experiment demonstrates Hawking-like exponential spectrum and entanglement dynamics in a 10-qubit analogue horizon system—an accessible kinematic/field-on-fixed-background simulation, not a decoding/reconstruction task. [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>)



  * BEC Unruh/Hawking-Unruh simulator demonstrates thermal mode distributions and partial reversibility in an analog platform without requiring holographic ingredients like TFDs or decoding; reinforces separation between kinematic radiation signatures and information-recovery tasks. [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>)



### Predictions

### 3 Likely outcomes

  * On the same quantum platform, forward-only signatures (e.g., level statistics proxies; OTOC magnitude via projection-only methods) will scale to more qubits than any protocol requiring U* or high-quality echo/time reversal plus two-copy entanglement resources.

  * Improving the fidelity of Hamiltonian inversion / conjugate-control operations (e.g., better sign-flip calibration) will improve decoding/teleportation fidelities more steeply than it improves forward-only chaos metrics measured over the same time window.

  * For Grover-amplified decoding variants, there will be an experimentally observable optimal iteration count m _: fidelity rises with m for small m but then decreases beyond m_ due to noise accumulation; m* shifts upward as two-qubit gate error decreases.




### 2 Unknown outcomes

  * A hybrid approach that uses approximate unitary designs (scrambler U) plus efficient two-copy shadow/overlap estimation could demonstrate a scalable ‘synthetic Page-transition’ in a purely circuit-based random-unitary evaporation toy model at sizes beyond current HP/wormhole demonstrations, but whether the resulting transition correlates with island-like reconstruction in any operational sense is unclear.

  * If a platform achieves scalable finite-temperature TFD preparation with low error (e.g., via engineered dissipation or fault-tolerant imaginary-time), then wormhole-teleportation signatures should become robust against small coupling miscalibrations and should correlate more cleanly with operator-size winding proxies; it is unclear whether non-holographic mechanisms will still mimic this robustness.




### Conflicting & Unaccounted Evidence

### 3 Negative experiments

  * Demonstrate generic Hayden–Preskill-style decoding with high fidelity while provably lacking any effective conjugate control (no U*, no echo/sign-flip, no equivalent inversion primitive). Success would falsify the conjugate-control requirement as stated.

  * In a symmetric HP setting, show postselection success probability does not decrease ~1/d_A^2 with diary size (holding other assumptions fixed). This would contradict the postselection scaling premise.

  * Show semiclassical-regime signatures requiring low-temperature TFD structure (as defined within a given toy model, e.g., SYK Schwarzian predictions) arise at the same system size/control as basic forward OTOC/level-statistics diagnostics, contradicting the proposed hierarchy.




### 1 Unaccounted for

  * Some analogue-gravity Hawking-radiation experiments report entanglement-like Hawking-partner correlations without invoking any scrambling inversion or decoding. This theory intentionally focuses on information-recovery/reconstruction tasks and thus does not aim to explain certification of entanglement in kinematic analogue systems. [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-003>)



* * *

**Related Artifacts:**

  * [Extraction: Replica wormholes and the black hole interior](<../extractions/extraction-replica-wormholes-and-the-black-hole-interior.md>)
  * [Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md>)
  * [Extraction: Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md>)
  * [Extraction: Digital Quantum Simulation of Minimal AdS/CFT.](<../extractions/extraction-digital-quantum-simulation-of-minimal-adscft.md>)
  * [Extraction: Black Hole on a Chip: Proposal for a Physical Realization of the Sachdev-Ye-Kitaev model in a Solid-State System](<../extractions/extraction-black-hole-on-a-chip-proposal-for-a-physical-realization-of-the-sachd.md>)
  * [Extraction: Simulating quantum field theory in curved spacetime with quantum many-body systems](<../extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md>)
  * [Extraction: Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography](<../extractions/extraction-traversable-wormholes-as-quantum-channels-exploring-cft-entanglement.md>)
  * [Extraction: Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md>)
  * [Extraction: Quantum information scrambling: from holography to quantum simulators](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md>)
  * [Extraction: Mimicking black hole event horizons in atomic and solid-state systems](<../extractions/extraction-mimicking-black-hole-event-horizons-in-atomic-and-solid-state-systems.md>)
  * [Extraction: Commuting SYK: a pseudo-holographic model](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md>)
  * [Extraction: Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md>)
  * [Extraction: Analogue simulations of quantum gravity with fluids](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md>)
  * [Extraction: Quantum simulation of Unruh radiation](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md>)
  * [Extraction: Creating and probing the Sachdev-Ye-Kitaev model with ultracold gases: Towards experimental studies of quantum gravity](<../extractions/extraction-creating-and-probing-the-sachdev-ye-kitaev-model-with-ultracold-gases-1.md>)
  * [Extraction: Quantum field simulator for dynamics in curved spacetime](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md>)
  * [Extraction: Measuring the scrambling of quantum information](<../extractions/extraction-measuring-the-scrambling-of-quantum-information.md>)
  * [Extraction: Efficient decoding for the Hayden-Preskill protocol](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md>)



* * *

## Entities

[Replica wormholes and the black hole interior](<https://www.semanticscholar.org/paper/208309801>)

Geoff Penington, S. Shenker, D. Stanford et al. | 2019 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/208309801>)

[Efficient decoding for the Hayden-Preskill protocol](<https://www.semanticscholar.org/paper/54805207>)

Beni Yoshida, A. Kitaev | 2017 | [Semantic Scholar](<https://www.semanticscholar.org/paper/54805207>)

[Simulating quantum field theory in curved spacetime with quantum many-body systems](<https://www.semanticscholar.org/paper/218502756>)

Run-Qiu Yang, Hui Liu, Shi-ning Zhu et al. | 2019 | Physical Review Research | [Semantic Scholar](<https://www.semanticscholar.org/paper/218502756>)

[Quantum field simulator for dynamics in curved spacetime](<https://www.semanticscholar.org/paper/247011689>)

C. Viermann, Marius Sparn, Nikolas Liebster et al. | 2022 | Nature | [Semantic Scholar](<https://www.semanticscholar.org/paper/247011689>)

[Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<https://www.semanticscholar.org/paper/259341708>)

Ran Li, Xuanhua Wang, Kun Zhang et al. | 2023 | Physical Review D | [Semantic Scholar](<https://www.semanticscholar.org/paper/259341708>)

[Measuring the scrambling of quantum information](<https://www.semanticscholar.org/paper/34365945>)

Brian Swingle, Gregory S. Bentsen, M. Schleier-Smith et al. | 2016 | [Semantic Scholar](<https://www.semanticscholar.org/paper/34365945>)

[Digital Quantum Simulation of Minimal AdS/CFT.](<https://www.semanticscholar.org/paper/5144368>)

L. García-Álvarez, Í. Egusquiza, L. Lamata et al. | 2016 | Physical Review Letters | [Semantic Scholar](<https://www.semanticscholar.org/paper/5144368>)

[Mimicking black hole event horizons in atomic and solid-state systems](<https://www.semanticscholar.org/paper/119189958>)

M. Franz, M. Rozali | 2018 | Nature Reviews Materials | [Semantic Scholar](<https://www.semanticscholar.org/paper/119189958>)

[Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<https://www.semanticscholar.org/paper/245837521>)

R. Bousso, Xi Dong, Netta Engelhardt et al. | 2022 | [Semantic Scholar](<https://www.semanticscholar.org/paper/245837521>)

[Commuting SYK: a pseudo-holographic model](<https://www.semanticscholar.org/paper/259262526>)

Ping Gao | 2023 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/259262526>)

[Matters of Gravity, The Newsletter of the Division of Gravitational Physics of the American Physical Society, Volume 50, December 2017](<https://www.semanticscholar.org/paper/264969650>)

David Garfinkle | 2017 | [Semantic Scholar](<https://www.semanticscholar.org/paper/264969650>)

[Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography](<https://www.semanticscholar.org/paper/53601332>)

N. Bao, A. Chatwin-Davies, Jason Pollack et al. | 2018 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/53601332>)

[Creating and probing the Sachdev-Ye-Kitaev model with ultracold gases: Towards experimental studies of quantum gravity](<https://www.semanticscholar.org/paper/119300030>)

I. Danshita, M. Hanada, Masaki Tezuka | 2016 | [Semantic Scholar](<https://www.semanticscholar.org/paper/119300030>)

[Quantum information scrambling: from holography to quantum simulators](<https://www.semanticscholar.org/paper/244488292>)

Arpan Bhattacharyya, Lata Kh Joshi, Bhuvanesh Sundar | 2021 | The European Physical Journal C | [Semantic Scholar](<https://www.semanticscholar.org/paper/244488292>)

[Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<https://www.semanticscholar.org/paper/259075712>)

Yun-hao Shi, Run-Qiu Yang, Zhongcheng Xiang et al. | 2021 | Nature Communications | [Semantic Scholar](<https://www.semanticscholar.org/paper/259075712>)

[Analogue simulations of quantum gravity with fluids](<https://www.semanticscholar.org/paper/261139644>)

S. Braunstein, M. Faizal, L. Krauss et al. | 2023 | Nature Reviews Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/261139644>)

[Black Hole on a Chip: Proposal for a Physical Realization of the Sachdev-Ye-Kitaev model in a Solid-State System](<https://www.semanticscholar.org/paper/119099352>)

D. Pikulin, M. Franz | 2017 | [Semantic Scholar](<https://www.semanticscholar.org/paper/119099352>)

[Quantum simulation of Unruh radiation](<https://www.semanticscholar.org/paper/182221423>)

Jiazhong Hu, Lei Feng, Zhendong Zhang et al. | 2018 | Nature Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/182221423>)

[Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<https://www.semanticscholar.org/paper/287425539>)

Moongul Byun, Keun-Young Kim, Hyeonsoo Lee | 2026 | [Semantic Scholar](<https://www.semanticscholar.org/paper/287425539>)

## Citation

Cite this artifact as `\cite{ast-revised-2026-08-13-2}`.
[code] 
    @misc{ast-revised-2026-08-13-2,
      title        = {Scrambling-Limited Simulatability of Black-Hole Information Tasks (revised)},
      author       = {{Asta Theorizer}},
      year         = {2026},
      month        = {8},
      howpublished = {Asta Theorizer artifact},
      url          = {theories/scrambling-limited-simulatability-of-black-hole-information-tasks-revised.md},
      note         = {asta-artifact id: theory-3},
    }
[/code]
