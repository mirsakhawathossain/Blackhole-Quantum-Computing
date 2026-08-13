[<- All artifacts](<../index.md>)

# Operator-Size Phase Coherence as the Mechanism for Wormhole Teleportation Signals (refined)

**Contents:**

  * 2 Theory Statements
  * Predictions
  * Conflicting & Unaccounted Evidence



### 2 Theory Statements

### Mechanism certification criterion: coherent size-winding is a discriminant for holographic-style teleportation

In two-sided teleportation protocols based on SYK-like dynamics with a two-sided coupling G(\mu)=e^{i\mu V} that induces size-dependent phases, a sufficient operational discriminator for the size-winding (holographic) mechanism is the existence of a time/coupling window in which: (1) the winding size distribution q(l) has phase arg q(l) approximately linear in size l across the dominant support of the (real) size distribution P(l); (2) the coherence ratio R(l)=|q(l)|/P(l) is near unity in that support (phase alignment across strings of the same size); and (3) changing the sign of \mu reverses/cancels the slope of arg q(l) and produces a correspondingly strong sign-asymmetry in teleportation figures of merit (e.g., mutual information I_PT or teleportation fidelity) with enhancement for the sign that cancels the winding. Teleportation signals observed without conditions (1)–(2) should not be attributed to the size-winding mechanism; they are more consistent with alternative mechanisms (e.g., peaked-size or thermalization-driven interference).

**Supporting evidence:**

  * Numerical size-winding diagnostics explicitly define q(l) and R(l) and report (for a chosen small-N sparse SYK instance) approximately linear arg q(l) near the mutual-information peak, with slope reversal under a negative \mu kick, supporting teleportation-by-size-winding interpretation for that instance. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-007>)



  * The gate-based traversable-wormhole teleportation protocol reports sign-dependent mutual-information asymmetry (\Delta I_PT larger for one sign of \mu) and interprets it via teleportation-by-size; it also notes vulnerability of later-time signals to noise and uses minimal Trotter depth, consistent with a phase-sensitive mechanism. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-005>)



  * Operator-size framework links a two-sided coupling to size-dependent phases and explicitly distinguishes two teleportation mechanisms: (a) peaked-size teleportation (generic scramblers) and (b) perfect size-winding (holographic/SYK), establishing the conceptual basis for using coherence/linearity as a mechanism classifier. [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-011>)



  * Commuting-SYK teleportation analysis finds that teleportation-like signatures can arise from mechanisms such as peaked-size distributions and thermalization rather than uniquely holographic dynamics, implying that teleportation signals alone are not sufficient evidence for a holographic size-winding mechanism. [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>)



  * General traversable-wormhole/teleportation reviews emphasize that small-scale noisy-simulator demonstrations exist but are toy-model-limited and face verification/scaling obstacles (including TFD preparation), reinforcing the need for mechanism-level certification beyond observing a signal. [Bousso et al., 2022](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md#c-005>) [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-005>)



### Mechanism-dependent noise fragility: phase-coherent size-winding degrades faster under dephasing than peaked-size teleportation

In NISQ implementations of two-sided wormhole-teleportation protocols, teleportation signatures that rely on coherent size-winding (phase alignment across operator-size sectors) are predicted to be more sensitive to noise channels that randomize relative phases between size sectors (dephasing, coherent control errors, Trotter errors that act like phase diffusion) than teleportation signatures dominated by peaked-size/thermalization mechanisms. Operationally: adding controlled dephasing that scrambles size-dependent phases should suppress sign-of-\mu asymmetry and mutual-information/fidelity peaks disproportionately in regimes where R(l)\approx 1 and arg q(l) is linear, compared to regimes where teleportation arises without such coherence.

**Supporting evidence:**

  * Size-winding diagnostic work notes that direct reconstruction of size-winding structure is challenging and that hardware noise suppresses teleportation signal amplitude, indicating practical fragility of phase-sensitive diagnostics on hardware. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-007>)



  * Gate-based traversable-wormhole protocol emphasizes noise sensitivity of later-time signals and uses minimal-depth Trotterization to limit noise, consistent with a phase-coherent mechanism being depth/noise limited. [Byun et al., 2026](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md#c-005>)



  * Commuting-SYK analysis identifies teleportation regimes explained by peaked-size/thermalization mechanisms, which conceptually do not require perfect phase winding and therefore motivate expecting different robustness profiles. [Gao, 2023](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md#c-003>)



  * Broader decoding/teleportation protocol literature highlights postselection-based protocols with exponentially small success probabilities and strong sensitivity to implementing U and U* accurately, consistent with phase/coherence demands increasing fragility in practice. [Yoshida et al., 2017](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md#c-001>) [Bhattacharyya et al., 2021](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md#c-007>) [Li et al., 2023](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md#c-001>)



### Predictions

### 3 Likely outcomes

  * Controlled size-sector dephasing test: introduce random Z rotations whose angle variance scales with Pauli-string weight (or an experimentally accessible proxy) during evolution. Prediction: in runs where numerical diagnostics indicate size-winding coherence (high R(l), linear arg q(l)), the sign-of-\mu mutual-information asymmetry collapses rapidly with dephasing strength, faster than in parameter regimes where teleportation is explained by peaked-size/thermalization.

  * Sign-tuning optimum: in a size-winding-dominated regime, scanning \mu should show a clear optimum near the value that cancels the measured winding slope (from classical numerics), and that same \mu should optimize both (i) mutual information/fidelity peak height and (ii) ordering/causal-window diagnostics more tightly than in peaked-size regimes.

  * Commutator-structure dependence: for two Hamiltonians with comparable size distributions P(l) but different phase coherence (different R(l) profiles), the more coherent one should show stronger \mu-sign asymmetry at fixed depth/noise.




### 2 Unknown outcomes

  * Proxy certification observables: there may exist scalable proxies for size-winding coherence using only low-order two-copy correlators (e.g., moments of the size operator and a small set of phase-sensitive correlators) that correlate strongly with R(l) and linear arg q(l), enabling mechanism certification without exponential tomography.

  * Large-N/low-T sharpening: as one approaches lower temperature and larger N regimes expected to better match Schwarzian/JT physics, size-winding coherence might become sufficiently sharp that teleportation becomes less sensitive to small \mu miscalibrations (a ‘plateau’ of near-optimal \mu), but whether this survives realistic noise and finite-N effects is unclear.




### Conflicting & Unaccounted Evidence

### 3 Negative experiments

  * Find a parameter regime where arg q(l) is clearly non-linear and R(l) is far from 1 (by numerical reconstruction for the implemented model), yet teleportation remains strongly sign-asymmetric and remains robust under targeted dephasing. This would undercut the claim that coherent size-winding is a key discriminator for holographic-like interpretation.

  * Conversely, find a regime with strong size-winding coherence (linear arg q(l), R(l) near 1) but no \mu-sign-dependent teleportation enhancement for any scanned \mu; this would challenge the link between winding cancellation and teleportation gain.

  * Perform a controlled dephasing experiment and observe that purported size-winding regimes are not more fragile than peaked-size regimes; this would falsify the mechanism-dependent noise fragility law.




### 2 Unaccounted for

  * Analogue-gravity Hawking/Unruh simulations (BEC, SQUID, optical analogues) target horizon thermality and pair production without two-sided entangled copies, operator-size decompositions, or size-dependent couplings; they are outside this theory’s explanatory scope. [Hu et al., 2018](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md#c-001>) [Shi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md#c-001>) [Terrones et al., 2021](<../extractions/extraction-towards-quantum-simulation-of-black-holes-in-a-dc-squid-array.md#c-003>) [Braunstein et al., 2023](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md#c-001>) [Viermann et al., 2022](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md#c-001>)



  * Digital/variational Hawking-radiation toy simulations (e.g., VQE Schwarzschild discretization) and qubit evaporation models address thermodynamics or Page-curve-like entanglement growth rather than two-sided wormhole teleportation-by-size; they are not explained here. [Dhaulakhandi et al., 2021](<../extractions/extraction-quantum-simulation-of-hawking-radiation-using-vqe-algorithm-on-ibm-qu.md#c-001>) [Avery, 2011](<../extractions/extraction-qubit-models-of-black-hole-evaporation.md#c-001>) [Giddings, 2011](<../extractions/extraction-models-for-unitary-black-hole-disintegration.md#c-001>)



* * *

**Related Artifacts:**

  * [Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<../extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md>)
  * [Extraction: Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer](<../extractions/extraction-quantum-simulation-of-hawking-radiation-using-vqe-algorithm-on-ibm-qu.md>)
  * [Extraction: Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<../extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md>)
  * [Extraction: Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<../extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md>)
  * [Extraction: Quantum information scrambling: from holography to quantum simulators](<../extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md>)
  * [Extraction: Commuting SYK: a pseudo-holographic model](<../extractions/extraction-commuting-syk-a-pseudo-holographic-model.md>)
  * [Extraction: Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<../extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md>)
  * [Extraction: Analogue simulations of quantum gravity with fluids](<../extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md>)
  * [Extraction: Towards Quantum Simulation of Black Holes in a dc-SQUID Array](<../extractions/extraction-towards-quantum-simulation-of-black-holes-in-a-dc-squid-array.md>)
  * [Extraction: Models for unitary black hole disintegration](<../extractions/extraction-models-for-unitary-black-hole-disintegration.md>)
  * [Extraction: Qubit models of black hole evaporation](<../extractions/extraction-qubit-models-of-black-hole-evaporation.md>)
  * [Extraction: Quantum simulation of Unruh radiation](<../extractions/extraction-quantum-simulation-of-unruh-radiation.md>)
  * [Extraction: Quantum field simulator for dynamics in curved spacetime](<../extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md>)
  * [Extraction: Efficient decoding for the Hayden-Preskill protocol](<../extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md>)



* * *

## Entities

[Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer](<https://www.semanticscholar.org/paper/245634244>)

Ritu Dhaulakhandi, B. K. Behera | 2021 | [Semantic Scholar](<https://www.semanticscholar.org/paper/245634244>)

[Efficient decoding for the Hayden-Preskill protocol](<https://www.semanticscholar.org/paper/54805207>)

Beni Yoshida, A. Kitaev | 2017 | [Semantic Scholar](<https://www.semanticscholar.org/paper/54805207>)

[Towards Quantum Simulation of Black Holes in a dc-SQUID Array](<https://www.semanticscholar.org/paper/239616504>)

Adri'an Terrones, C. Sab'in | 2021 | Universe | [Semantic Scholar](<https://www.semanticscholar.org/paper/239616504>)

[Quantum field simulator for dynamics in curved spacetime](<https://www.semanticscholar.org/paper/247011689>)

C. Viermann, Marius Sparn, Nikolas Liebster et al. | 2022 | Nature | [Semantic Scholar](<https://www.semanticscholar.org/paper/247011689>)

[Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation](<https://www.semanticscholar.org/paper/259341708>)

Ran Li, Xuanhua Wang, Kun Zhang et al. | 2023 | Physical Review D | [Semantic Scholar](<https://www.semanticscholar.org/paper/259341708>)

[Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime](<https://www.semanticscholar.org/paper/245837521>)

R. Bousso, Xi Dong, Netta Engelhardt et al. | 2022 | [Semantic Scholar](<https://www.semanticscholar.org/paper/245837521>)

[Commuting SYK: a pseudo-holographic model](<https://www.semanticscholar.org/paper/259262526>)

Ping Gao | 2023 | Journal of High Energy Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/259262526>)

[Qubit models of black hole evaporation](<https://www.semanticscholar.org/paper/54967526>)

Steven G. Avery | 2011 | [Semantic Scholar](<https://www.semanticscholar.org/paper/54967526>)

[Quantum information scrambling: from holography to quantum simulators](<https://www.semanticscholar.org/paper/244488292>)

Arpan Bhattacharyya, Lata Kh Joshi, Bhuvanesh Sundar | 2021 | The European Physical Journal C | [Semantic Scholar](<https://www.semanticscholar.org/paper/244488292>)

[Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole](<https://www.semanticscholar.org/paper/259075712>)

Yun-hao Shi, Run-Qiu Yang, Zhongcheng Xiang et al. | 2021 | Nature Communications | [Semantic Scholar](<https://www.semanticscholar.org/paper/259075712>)

[Analogue simulations of quantum gravity with fluids](<https://www.semanticscholar.org/paper/261139644>)

S. Braunstein, M. Faizal, L. Krauss et al. | 2023 | Nature Reviews Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/261139644>)

[Models for unitary black hole disintegration](<https://www.semanticscholar.org/paper/73549087>)

S. Giddings | 2011 | [Semantic Scholar](<https://www.semanticscholar.org/paper/73549087>)

[Quantum simulation of Unruh radiation](<https://www.semanticscholar.org/paper/182221423>)

Jiazhong Hu, Lei Feng, Zhendong Zhang et al. | 2018 | Nature Physics | [Semantic Scholar](<https://www.semanticscholar.org/paper/182221423>)

[Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model](<https://www.semanticscholar.org/paper/287425539>)

Moongul Byun, Keun-Young Kim, Hyeonsoo Lee | 2026 | [Semantic Scholar](<https://www.semanticscholar.org/paper/287425539>)

## Citation

Cite this artifact as `\cite{ast-refined-2026-08-13}`.
[code] 
    @misc{ast-refined-2026-08-13,
      title        = {Operator-Size Phase Coherence as the Mechanism for Wormhole Teleportation Signals (refined)},
      author       = {{Asta Theorizer}},
      year         = {2026},
      month        = {8},
      howpublished = {Asta Theorizer artifact},
      url          = {theories/operator-size-phase-coherence-as-the-mechanism-for-wormhole-teleportation-signal.md},
      note         = {asta-artifact id: theory-6},
    }
[/code]
