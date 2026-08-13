[<- All artifacts](<../index.md>)

# Extraction: Quantum information scrambling: from holography to quantum simulators

**Contents:**

  * Many-body wormhole-inspired teleportation circuit (Gao-Jafferis-Wall analog)
  * Sachdev–Ye–Kitaev (SYK) model
  * Thermofield-double state and its eternal black-hole dual
  * Hayden–Preskill recovery and Yoshida–Kitaev decoding protocols
  * Out-of-time-ordered correlator (OTOC) measurement protocols and thermal OTOC
  * Operator size distribution and size-winding mechanism
  * Trapped-ion and Rydberg-atom quantum simulators for holographic analogs



### Many-body wormhole-inspired teleportation circuit (Gao-Jafferis-Wall analog)

Field | Value  
---|---  
name_short | Wormhole teleportation circuit  
name_full | Many-body wormhole-inspired teleportation circuit (Gao-Jafferis-Wall analog)  
brief_description | A quantum-circuit protocol that mimics traversable-wormhole teleportation by preparing a two-copy thermofield-double (TFD) state, scrambling an inserted message on the left, applying a short two-sided coupling G = exp(i g V) between carrier subsystems at t=0, and then evolving the right copy to recover the message; the coupling imprints a size-dependent phase that enables teleportation when operator-size distributions are favorable.  
citation_title |   
mention_or_use | use  
target_system_or_model | Two-sided thermofield-double of finite many-body systems (spin chains, random circuits); also compared to SYK as a holographic toy model  
black_hole_phenomena_targeted | Wormhole teleportation (traversable-wormhole analog), information recovery, scrambling (OTOC), shockwave/negative-energy pulse analog via the two-sided coupling  
simulation_paradigm | Digital gate-based quantum simulation (circuit protocol) with numerical exact-unitary simulations for small N; conceptually NISQ-friendly protocol  
quantum_hardware_platform | platform-agnostic (discussed implementations / suitability for trapped ions and neutral-atom / Rydberg platforms)  
encoding_and_mapping | Two copies (L,R) of the many-body Hilbert space implement the TFD/EPR purification; message subsystem L_M (m qubits) swapped in at -t; carrier subsystem of K=N-m qubits on each side; coupling V implemented as a sum of local two-sided operators V=(1/K)∑ _j O_ (in practice chosen as Pauli products, e.g. σ^z_i σ^z_i); operator-state correspondence and Pauli-string expansion used to relate operator growth to states in doubled Hilbert space.} O_{j,R  
algorithm_or_protocol | Prepare TFD (or EPR at infinite temperature), backward-evolve left by U† to -t, insert message (swap), forward-evolve left with U, apply short two-sided unitary G=exp(i g V) between carrier qubits at t=0, forward-evolve right with U^T, apply optional decoder D (probabilistic EPR projection or deterministic Grover-style iteration) and measure target message subsystem; OTOC and two-point functions used to characterize success.  
resource_estimates | No rigorous large-scale resource counting given; numerical illustrations use small systems (spin-chain examples N=7 and N=10 qubits, message m=1). Protocolic bounds: probabilistic decoding success probability ≥ 1/d_A^2 (d_A dimension of input subsystem); deterministic decoding requires O(d_A) Grover iterations (m ≈ π d_A/4 for large d_A). K (carrier size) should be large compared to m for factorization approximations; condition d_D ≥ d_A^2 appears in decoding analysis.  
noise_and_error_mitigation | Paper discusses NISQ suitability qualitatively (high-fidelity gates, TFD preparation and coherent evolution are required) but does not present a detailed noise model; no quantified error budgets or explicit mitigation techniques (beyond referencing experimental realizations and standard needs for low gate error/high fidelity state preparation).  
key_results_or_demonstrations | Analytical derivation of the size-dependent phase induced by G and the criterion for successful teleportation (peaked-size distributions or perfect size-winding). Numerical demonstrations in spin-chain Hamiltonian (Eq. 37) showing single-qubit teleportation: examples with N=7 (EPR) and N=10 numerical OTOC behavior; teleportation peak occurs near scrambling time and is spatially localized on the message qubit (figures show signal recovery at the message site). Equivalence shown between late-time/high-temperature limit of this circuit and the Hayden–Preskill / Yoshida–Kitaev decoding circuit for single-qubit inputs.  
validation_and_benchmarks | Validation by exact numerical simulation on small spin chains and comparison to analytic expectations from operator-size arguments and known analytics for SYK/holographic models; comparisons to the Yoshida–Kitaev decoding construction and to Gao–Jafferis–Wall gravitational picture as conceptual benchmarks.  
claimed_feasibility | Authors argue single-qubit many-body teleportation is feasible on current small NISQ devices (and cite existing demonstrations of related protocols); multi-qubit/high-fidelity holographic-like teleportation requires better TFD preparation, deeper circuits and lower noise; low-temperature/holographic regime (e.g., SYK large-N) is identified as more challenging and likely beyond near-term devices.  
limitations_and_open_problems | Finite-size effects (small N) limit direct correspondence to large-N holography; preparing thermofield-double states at finite temperature is experimentally demanding; assumptions used in analytic arguments include large-K factorization and peaked size distributions (which may not hold generically); imperfect size-winding or broad size distributions degrade fidelity; lack of real dynamical gravity – only analog dynamics on fixed lattice; measurement/verification costs scale with system size but are not fully quantified.  
complexity_or_hardness_arguments | Protocol analysis uses information-theoretic constraints: probabilistic decoder success ∝ 1/d_A^2 and deterministic decoder requires O(d_A) Grover iterations (so decoding cost scales linearly with input Hilbert space dimension); no explicit formal claims of BQP/QMA hardness for simulating full gravitational dynamics, but decoding and scrambling tasks are linked to computationally hard thermalization/scrambling behavior in large Hilbert spaces.  
theory_context_keywords | AdS/CFT, thermofield double (TFD), ER=EPR, Gao–Jafferis–Wall traversable wormhole, Hayden–Preskill, Yoshida–Kitaev decoding, scrambling, OTOC, operator size, size-winding, peaked-size teleportation  
citations_to_prior_work | Gao–Jafferis–Wall [83]; Hayden–Preskill [72]; Yoshida–Kitaev decoding [73]; wormhole-teleportation circuit derivations and size-winding: [74, 75, 76]; high-temperature SYK analysis: [158]; experimental demonstrations of teleportation and OTOC measurement referenced (e.g., [98], [109–116]).  
  
### Sachdev–Ye–Kitaev (SYK) model

Field | Value  
---|---  
name_short | SYK  
name_full | Sachdev–Ye–Kitaev (SYK) model  
brief_description | A solvable all-to-all interacting Majorana (or complex fermion) model that at low temperature exhibits nearly-AdS2 dynamics and is a canonical toy model for black-hole-like quantum chaos and maximal scrambling; used as a target gravitational analog for teleportation and size-winding analyses.  
citation_title |   
mention_or_use | mention  
target_system_or_model | SYK model (all-to-all random fermionic model) as an analog of nearly-AdS2 black hole  
black_hole_phenomena_targeted | Fast scrambling, OTOC exponential growth with maximal Lyapunov exponent, wormhole teleportation (perfect teleportation at scrambling time in low-temperature SYK), size-winding and revival dynamics (t* and long-time revivals)  
simulation_paradigm | Analytic large-N calculations and small-N numerical simulations; proposals for quantum simulation on digital/analog platforms (discussed qualitatively)  
quantum_hardware_platform | platform-agnostic (discussed as a target for analog or digital quantum simulation; mapping to qubits/fermion-to-qubit encodings would be required)  
encoding_and_mapping | Model is fermionic/Majorana; mapping to qubits requires fermion-to-qubit transforms (Jordan–Wigner/Bravyi–Kitaev) and truncation for complex-fermion variants; large-N limit required to reproduce holographic features (not detailed in resource terms here).  
algorithm_or_protocol | Use of TFD preparation, measurement of OTOC, and wormhole-inspired coupling to test size-winding and teleportation; analytical evaluation of operator-size winding in low-temperature limit.  
resource_estimates | Paper does not provide concrete resource counts; notes that reproducing low-temperature/holographic SYK behavior requires large N (many fermions) and precise control – presenting this as challenging for near-term devices.  
noise_and_error_mitigation | Not discussed in detail for SYK simulation; general remarks that low-temperature regime and TFD are demanding experimentally.  
key_results_or_demonstrations | Summarizes prior analytic results: low-temperature SYK exhibits perfect size-winding that yields near-perfect teleportation at the scrambling time and distinct fidelity behavior from generic scramblers; at long times t>t* revivals yield fidelities consistent with peak-size mechanism.  
validation_and_benchmarks | Comparison to holographic gravity expectations (nearly-AdS2 dual) and analytical SYK calculations; not validated by new experiments in this review.  
claimed_feasibility | High-temperature SYK features are more accessible; low-temperature, large-N holographic SYK regime is stated as far from current experimental reach.  
limitations_and_open_problems | Large-N requirement for true holographic behavior; mapping to experimentally realistic qubit systems and TFD preparation at low temperature are major challenges; finite-N corrections can spoil idealized size-winding.  
complexity_or_hardness_arguments | No formal complexity proofs in this review; SYK is often used as a model of maximal quantum chaos and fast scramblers, implying rapid growth of operator complexity.  
theory_context_keywords | SYK, nearly-AdS2, holographic duality, maximal chaos, Lyapunov bound, size-winding, wormhole teleportation  
citations_to_prior_work | SYK–gravity duality references [59–64]; size-winding and teleportation in SYK [74, 75, 158]  
  
### Thermofield-double state and its eternal black-hole dual

Field | Value  
---|---  
name_short | Thermofield double (TFD)  
name_full | Thermofield-double state and its eternal black-hole dual  
brief_description | The TFD is a purification of a thermal density matrix realized as an entangled state across two copies of a system; holographically it is dual to an eternal two-sided black hole and forms the starting state for wormhole-teleportation circuits.  
citation_title |   
mention_or_use | use  
target_system_or_model | Two identical copies of a many-body system prepared in a thermofield-double (TFD) state representing an eternal black hole in holographic analogy  
black_hole_phenomena_targeted | Eternal black hole geometry (ER bridge), entanglement-geometry correspondence, starting point for traversable-wormhole protocols and teleportation experiments  
simulation_paradigm | State-preparation for digital quantum simulation; TFD preparation is a subroutine/component for teleportation-circuits and OTOC measurement protocols  
quantum_hardware_platform | platform-agnostic; protocols referenced for trapped ions and Rydberg implementations  
encoding_and_mapping | TFD is prepared by entangling two copies such that |TFD⟩ = (1/√Z) ∑_i e^{-β E_i/2} |E_i⟩_L ⊗ |E_i^*⟩_R; in practice requires either cooling, engineered dissipation, variational schemes or explicit purification circuits (refs [94–97] cited in review).  
algorithm_or_protocol | Preparation via purification circuits, variational constructions, or evolution by imaginary-time methods (surveyed in the review; details and experimental protocols discussed in later sections of the paper), then used as an initial resource for wormhole teleportation protocol and thermal OTOC measurement.  
resource_estimates | No general resource counts given; review emphasizes that TFD preparation is experimentally challenging and resource-intensive, particularly at finite (low) temperature where many energy eigenstates contribute.  
noise_and_error_mitigation | Not detailed beyond general statement that TFD preparation requires high-fidelity control; noise impacts thermal purification and fidelity of subsequent teleportation.  
key_results_or_demonstrations | TFD is used throughout the review as the canonical starting state; numerical examples use infinite-temperature EPR (TFD at β=0) for computational convenience in several demonstrations.  
validation_and_benchmarks | TFD observables (reduced density matrices, two-point functions) match thermal expectation values by construction; numerical TFD/EPR used to validate teleportation and OTOC computations on small systems.  
claimed_feasibility | Preparation of EPR/infinite-temperature states is straightforward; finite-temperature TFD at low temperature is identified as experimentally costly but several preparation protocols are surveyed in the literature (refs cited).  
limitations_and_open_problems | Practical TFD preparation at low temperatures and large system sizes is a key bottleneck; finite-size and imperfect purification limit fidelity of holographic analogies.  
complexity_or_hardness_arguments | Preparing exact TFD for many-body Hamiltonians may require exponential resources in general; no formal complexity bound given here.  
theory_context_keywords | TFD, purification, eternal black hole, entanglement-geometry, EPR  
citations_to_prior_work | Original TFD–eternal black hole dictionary [77]; protocols for TFD preparation referenced [94–97] (surveyed in the review).  
  
### Hayden–Preskill recovery and Yoshida–Kitaev decoding protocols

Field | Value  
---|---  
name_short | Hayden–Preskill / Yoshida–Kitaev  
name_full | Hayden–Preskill recovery and Yoshida–Kitaev decoding protocols  
brief_description | Information recovery protocols in which information thrown into a highly scrambled (old) black hole can be decoded from subsequent radiation; Yoshida and Kitaev provided concrete decoding circuits (probabilistic EPR projection and deterministic Grover-style iterative decoders) that are realizable as quantum circuits.  
citation_title |   
mention_or_use | use  
target_system_or_model | Generic quantum channels modeling black-hole interior dynamics (Haar-random-like scramblers) and circuit realizations of decoding on two-copy systems  
black_hole_phenomena_targeted | Information retrieval from Hawking radiation analog (Hayden–Preskill thought experiment), decoding of scrambled information, connections to teleportation through wormholes  
simulation_paradigm | Digital quantum-circuit decoding protocols; probabilistic and deterministic decoders described and linked to many-body teleportation circuits  
quantum_hardware_platform | platform-agnostic; experimental trapped-ion demonstration referenced in review  
encoding_and_mapping | Uses doubled Hilbert-space setup with EPR pairs as resource; decoding acts on subsystems D, D' etc. as in the circuit diagrams; condition d_D ≥ d_A^2 is required for decoding success in the analysis.  
algorithm_or_protocol | Probabilistic protocol: evolve with U and U*, then project DD' onto EPR (success prob ≥ 1/d_A^2) to retrieve message in N'; Deterministic protocol: replace projection with Grover-style iterations using oracles G_D and G_A defined from EPR projectors, requiring m ≈ π d_A/4 iterations for high success probability.  
resource_estimates | Probabilistic success probability ≥ 1/d_A^2; deterministic decoding requires ≈ π d_A/4 iterations (Grover scaling), so decoding cost scales as O(d_A) where d_A is input-subsystem dimension; numerical/experimental demonstrations performed for small d_A (single-qubit).  
noise_and_error_mitigation | Review notes trapped-ion experiments realize both probabilistic and deterministic variants, but does not quantify noise mitigation; decoding performance is sensitive to fidelity of U, U*, and projector implementations.  
key_results_or_demonstrations | Review explains equivalence between late-time many-body wormhole protocol and Yoshida–Kitaev decoder for single-qubit input; cites that both probabilistic and deterministic decoders have been demonstrated in trapped-ion experiments (details in later sections of review).  
validation_and_benchmarks | Protocol success bounds derived using averaged OTOC assumptions and Haar-random unitaries; experiments validate decoding on small systems and compare to theoretical success probabilities.  
claimed_feasibility | Single-qubit decoding/probabilistic retrieval feasible on current small-scale devices; deterministic decoding becomes costly as d_A increases due to Grover-step scaling.  
limitations_and_open_problems | Probabilistic decoder has rapidly decreasing success probability with input size; deterministic decoder requires many iterations and thus deep circuits; both sensitive to noise; applicability relies on scrambler being sufficiently mixing (Haar-like assumptions).  
complexity_or_hardness_arguments | Decoding cost scales with input dimension (1/d_A^2 success for probabilistic; O(d_A) Grover iterations for deterministic). No formal hardness theorems beyond these resource scalings presented in the review.  
theory_context_keywords | Hayden–Preskill, Yoshida–Kitaev, decoding, Haar-random unitaries, scrambling, OTOC  
citations_to_prior_work | Hayden–Preskill original proposal [72]; Yoshida–Kitaev decoding construction and analysis [73]; averaged-OTOC bounds used in derivations [73].  
  
### Out-of-time-ordered correlator (OTOC) measurement protocols and thermal OTOC

Field | Value  
---|---  
name_short | OTOC protocols  
name_full | Out-of-time-ordered correlator (OTOC) measurement protocols and thermal OTOC  
brief_description | Definitions and experimentally accessible regularizations of OTOCs (including thermal OTOC in TFD form) used to quantify scrambling; measurement protocols involving two copies / time-reversal appear feasible in NISQ platforms and have been implemented in small-scale experiments.  
citation_title |   
mention_or_use | use  
target_system_or_model | Many-body lattice models (spin chains), SYK and generic scramblers; thermal backgrounds via TFD or other regularizations  
black_hole_phenomena_targeted | Scrambling diagnostics analogous to black-hole behavior (butterfly effect, scrambling time, Lyapunov growth), and quantities entering the teleportation fidelity (averaged thermal OTOC relates to coupling phase)  
simulation_paradigm | Circuit-based measurement (two-copy protocols, echo sequences) and analog measurement techniques; experiments and proposals are surveyed  
quantum_hardware_platform | Trapped ions, Rydberg atoms, superconducting qubits, NMR, photonics—all mentioned as suitable platforms in the review  
encoding_and_mapping | Thermal OTOC measured via TFD (two-copy) mapping: O_th(β,t) = Tr[e^{-β H/2} W† V†(t) W e^{-β H/2} V(t)]/Z; infinite-temperature OTOC corresponds to EPR projection between copies; mapping to Pauli strings for experimental measurement.  
algorithm_or_protocol | Protocols include preparing two copies (EPR/TFD), evolving with forward/backward dynamics, local measurements of V† and V^T on copies; experimental echo/auxiliary-qubit techniques and many-body interferometric schemes (surveyed; detailed protocols in later sections of review).  
resource_estimates | No precise shot-count estimates given in this part of the review; requirement noted: ability to prepare two copies and implement time evolution for required durations; finite-temperature OTOC needs TFD preparation.  
noise_and_error_mitigation | Experiments cited have used techniques suited to platform (high-fidelity gates, echo sequences); review does not provide a unified mitigation plan but highlights accessibility of the particular TFD-regularized OTOC in experiments.  
key_results_or_demonstrations | Review cites many experiments that have measured infinite-temperature OTOCs and some finite-temperature OTOCs ([98, 109–116, 160] referenced), establishing experimental feasibility on small systems; connects averaged thermal OTOC to the coupling expectation value ⟨V⟩_Q used in teleportation-phase control (Eq. 63).  
validation_and_benchmarks | Comparison to exact diagonalization and theoretical expectations for small systems; OTOC decay and temperature dependence illustrated numerically for a transverse-field Ising chain (N=10 examples in review).  
claimed_feasibility | Infinite-temperature OTOCs are experimentally accessible and have been realized; finite-temperature OTOC measurement requires TFD preparation and is more challenging but also demonstrated in small systems.  
limitations_and_open_problems | Scaling to large system sizes and low temperatures remains experimentally demanding; preparation of accurate TFD states and long coherent evolution are bottlenecks.  
complexity_or_hardness_arguments | OTOC decay/behavior used as heuristic for scrambling complexity; no formal complexity lower bounds given here.  
theory_context_keywords | OTOC, thermal OTOC, scrambling, butterfly effect, scrambling time, experimental measurement protocols  
citations_to_prior_work | OTOC foundational references and experimental demonstrations cited in review [65, 67, 93, 98, 109–116, 120, 145, 149–153].  
  
### Operator size distribution and size-winding mechanism

Field | Value  
---|---  
name_short | Operator-size / size-winding  
name_full | Operator size distribution and size-winding mechanism  
brief_description | Framework to quantify operator growth by expanding time-evolved operators in Pauli-string basis, defining size distributions q(l) (probability a Pauli string has weight l) and complex winding distribution ṽq(l); size-dependent phases induced by two-sided coupling enable teleportation when size distributions are peaked or when perfect size-winding (linear phase vs size) occurs (the latter happens in holographic/SYK models).  
citation_title |   
mention_or_use | use  
target_system_or_model | Generic finite many-body systems (spin chains, random circuits) and holographic systems (SYK where perfect size-winding can occur)  
black_hole_phenomena_targeted | Mechanism underlying wormhole teleportation analogs (how gravitational negative-energy shock is mirrored by size-dependent phases), measure of scrambling and operator spreading  
simulation_paradigm | Analytic reasoning, small-scale numerical simulations (Pauli-basis decomposition), measurement via EPR projectors in doubled Hilbert space  
quantum_hardware_platform | Platform-agnostic; measurement of size via EPR projections requires two-copy operations realizable in trapped ions and other architectures  
encoding_and_mapping | Operator Q_L(t)ρ^{1/2} expanded as ∑_P c_P(t) P; size l = number of non-identity single-site Paulis in string; EPR single-site projectors P_EPR,i and counting operator Ṽ = (1/N) ∑_i P_EPR,i used to extract average size from overlaps on doubled state.  
algorithm_or_protocol | Compute or measure coefficients c_P via tomography or measure Ṽ expectation value on Q_L(t)|TFD⟩ (practical measurement via local two-copy correlators); use coupling G=exp(i g V) with V proportional to counting operator to produce size-dependent phase.  
resource_estimates | Paper gives formulas relating expectation values to size but no general scaling/resource counts for measuring full size distribution; measurement of average size requires two-copy correlations across carriers (K qubits).  
noise_and_error_mitigation | Not detailed; size measurement sensitive to state-prep and two-copy operations fidelity; peak-size criterion may be spoiled by noise broadenings.  
key_results_or_demonstrations | Derives relation between coupling expectation ⟨V⟩_Q and average operator size (Eq. 56), shows how G implements a size-dependent global phase (Eq. 57), and explains two distinct teleportation mechanisms: peaked-size teleportation (generic scramblers) and perfect size-winding (holographic/SYK) that yields near-perfect teleportation.  
validation_and_benchmarks | Validated by exact numerical simulations of spin chains and comparison to analytic expectations; size-winding behavior linked to known analytic SYK results from prior literature.  
claimed_feasibility | Measuring average operator size via two-copy correlators is claimed to be accessible on current platforms for small K; full size distributions and size-winding verification in large systems remain challenging.  
limitations_and_open_problems | Perfect linear-in-size phase (size-winding) seems limited to holographic-like models (e.g., low-T SYK) and may not arise in generic many-body models; noise and finite-size broaden distributions and reduce teleportation fidelity.  
complexity_or_hardness_arguments | Operator growth is associated with increasing Pauli-string complexity, but no explicit computational hardness proofs are provided here.  
theory_context_keywords | operator growth, Pauli-string expansion, operator size, size distribution q(l), size-winding, peaked-size teleportation, EPR projectors  
citations_to_prior_work | Size and teleportation mechanism discussion based on Refs. [74, 75, 76]; operator growth literature [159].  
  
### Trapped-ion and Rydberg-atom quantum simulators for holographic analogs

Field | Value  
---|---  
name_short | Experimental platforms  
name_full | Trapped-ion and Rydberg-atom quantum simulators for holographic analogs  
brief_description | Survey of two experimental platforms suitable for implementing teleportation/OTOC/TFD protocols: trapped ions (high-fidelity digital gates and analog spin interactions via normal modes and Mølmer–Sørensen schemes) and neutral atoms with Rydberg excitations (strong van-der-Waals/Rydberg-blockade interactions enabling fast entangling gates).  
citation_title |   
mention_or_use | mention  
target_system_or_model | Spin-chain Hamiltonians, engineered all-to-all or nearest-neighbor interactions, and small-scale realizations of many-body protocols (teleportation, OTOC measurement, TFD preparation)  
black_hole_phenomena_targeted | Experimental tests of scrambling (OTOC), Hayden–Preskill / Yoshida–Kitaev decoding circuits, many-body teleportation circuits, and TFD/preparation protocols as laboratory analogs of black-hole phenomena  
simulation_paradigm | Both analog quantum simulation (effective spin-spin interactions, Rydberg blockade) and digital gate-based simulation (high-fidelity single- and two-qubit gates) are considered applicable  
quantum_hardware_platform | Trapped ions (e.g., ^171Yb^+, ^40Ca^+), neutral atoms / Rydberg arrays (e.g., ^87Rb, ^88Sr, ^171Yb), superconducting qubits also mentioned elsewhere as candidate platforms  
encoding_and_mapping | Trapped ions: qubits encoded in long-lived electronic states, entangling gates via Mølmer–Sørensen or Cirac–Zoller schemes mediated by motional modes; Rydberg atoms: qubits in hyperfine ground states with entangling gates via Rydberg excitation and blockade, CZ or controlled-phase through blockade-mediated schemes.  
algorithm_or_protocol | Implement many-body Hamiltonians (e.g., transverse-field Ising with longitudinal fields) via native analog interactions or trotterized gates; perform echo/time-reversal sequences for OTOC and implement two-copy TFD/EPR preparations for teleportation circuits; perform local projective measurements and conditional operations for the two-sided coupling implementation.  
resource_estimates | Platform-level metrics cited qualitatively: entangling gate fidelities in Rydberg experiments ≳99% reported for some gates; single-qubit fidelities up to 99.6% noted (ref in review); trapped-ion systems provide highest gate fidelities among current platforms — no global resource count for teleportation tasks is provided.  
noise_and_error_mitigation | Platform-specific techniques referenced (e.g., cooling and motional-mode control for ions, Rydberg blockade error mitigation strategies) but no unified noise budget; review points to experimental demonstrations that include practical error sources and mitigation in cited works.  
key_results_or_demonstrations | Review notes that both probabilistic and deterministic Yoshida–Kitaev decoders have been demonstrated in trapped-ion experiments (details in later sections/cited refs), and that OTOC and teleportation variants have been measured in multiple NISQ platforms (refs [98, 109–116]).  
validation_and_benchmarks | Experimental validations referenced: comparisons to exact simulations on small system sizes; high-fidelity gate benchmarks and observed OTOC decay/fidelity trends used to benchmark implementations.  
claimed_feasibility | Authors argue near-term feasibility for small-scale demonstrations (single-qubit teleportation, OTOC measurement, small-T TFD) on trapped ions and Rydberg arrays; large-scale holographic regimes (large N, low T) remain out of reach.  
limitations_and_open_problems | State-preparation (TFD), coherent evolution to scrambling times, gate errors and readout errors, and measurement overheads for two-copy protocols are practical bottlenecks; scaling to large N and low temperatures remains difficult.  
complexity_or_hardness_arguments | No formal complexity claims for platforms; practical costs scale with gate depth and number of qubits; decoding costs (number of Grover iterations) grow quickly with input dimension.  
theory_context_keywords | Rydberg blockade, Mølmer–Sørensen gates, analog/digital simulation, NISQ, TFD preparation, OTOC measurement  
citations_to_prior_work | Platform and gate-fidelity references surveyed in review (Rydberg gate proposals and blockade refs [186–192]; trapped-ion gate schemes Cirac–Zoller [203], Mølmer–Sørensen [205]; experimental OTOC/teleportation demos referenced [98, 109–116, 160]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-bhattacharyya-2026-08-13}`.
[code] 
    @misc{ast-ext-bhattacharyya-2026-08-13,
      title        = {Extraction: Quantum information scrambling: from holography to quantum simulators},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-information-scrambling-from-holography-to-quantum-simulators.md},
      crossref     = {bhattacharyya2021quantum},
      note         = {Theorizer's extraction from \cite{bhattacharyya2021quantum}. asta-artifact id: extraction-result-38},
    }
    
    @article{bhattacharyya2021quantum,
      title     = {Quantum information scrambling: from holography to quantum simulators},
      author    = {Arpan Bhattacharyya and Lata Kh Joshi and Bhuvanesh Sundar},
      year      = {2021},
      journal   = {The European Physical Journal C},
      url       = {https://www.semanticscholar.org/paper/244488292},
    }
[/code]
