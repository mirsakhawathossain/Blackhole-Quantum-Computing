[<- All artifacts](<../index.md>)

# Extraction: Efficient decoding for the Hayden-Preskill protocol

**Contents:**

  * Probabilistic postselection-based decoder for Hayden-Preskill recovery
  * Deterministic decoder combining postselection idea with Grover-like search
  * Gao–Jafferis–Wall traversable wormhole decoding / wormhole teleportation protocol



### Probabilistic postselection-based decoder for Hayden-Preskill recovery

Field | Value  
---|---  
name_short | Probabilistic Hayden-Preskill decoder  
name_full | Probabilistic postselection-based decoder for Hayden-Preskill recovery  
brief_description | A quantum-circuit protocol that attempts to reconstruct a quantum diary thrown into a black hole by preparing a copy of the entangled input, applying U* to the copy, and projecting the captured Hawking radiation and its copy onto an EPR pair; successful postselection teleports the diary to an outside register with fidelity bounded by O(1) when scrambling conditions hold.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Idealized black hole modeled as a finite Hilbert space of dimension d = 2^S composed of subsystems A,B entangled with B' and evolving by a Haar-random (or 'perfectly scrambling') unitary U; black hole + partner represented by n EPR pairs.  
black_hole_phenomena_targeted | Information recovery from Hawking radiation (Hayden-Preskill problem), scrambling diagnostics via out-of-time-order correlators (OTOCs), Rényi-2 mutual information between reference and radiation.  
simulation_paradigm | Digital gate-based quantum-circuit protocol (thought-experiment); protocol specifies using unitary evolution U, its complex conjugate U*, transpose U^T, and projective measurements/postselection.  
quantum_hardware_platform | platform-agnostic (no specific hardware); assumes the ability to implement U, U^*, U^T and Bell projections.  
encoding_and_mapping | Black hole & entangled partner represented by n EPR pairs (system partitioned into labelled subsystems A,B,C,D and complementary B'); Hilbert space dimensions d_A,d_B,d_C,d_D with d = d_A d_B; no low-level fermion/qubit mapping (only abstract finite-d Hilbert-space representation: d=2^S implies S qubits).  
algorithm_or_protocol | Prepare copy of entangled state |ξ> on A'R', apply U* to A'B', then project DD' onto the canonical EPR (Bell) state (postselection). If projection succeeds, the reference R is (approximately) entangled with R' (teleportation of Alice's diary).  
resource_estimates | Success probability equals Δ (diagrammatic quantity); lower bound Δ ≥ 1/(d_A d_R) and for symmetric case d_R = d_A gives success ≈ 1/d_A^2; requires implementing U and U* once per trial; circuit cost per trial ~ C (circuit size to implement U); no explicit qubit/gate counts beyond Hilbert-space dims (number of logical qubits ≈ log2 d).  
noise_and_error_mitigation | No explicit noise model or error mitigation besides postselection; analysis assumes ideal unitaries and projective measurements and 'perfect' scrambling; generalization to thermal (non-maximally-mixed) states would require replacing diagrammatic dots with square roots of density matrices and is nontrivial.  
key_results_or_demonstrations | Protocol (proposal + analytic bounds) with fidelity F ≥ 1/(1+δ) (Eq. (24)), where δ = d_A d_R Δ - 1; under (approximate) perfect scrambling and d_D ≫ √(d_A d_R) one gets δ ≪ 1 and F ≈ 1. This is a theoretical proposal and analysis (no hardware experiment or numerical simulation reported).  
validation_and_benchmarks | Analytic diagrammatic derivations, Haar-average calculations (Appendix A, T_2 integral), relations between Δ and averaged OTOCs and Rényi-2 mutual information (Δ = 2^{-I^{(2)}(R,DB')}); bounds derived from OTOC asymptotics for Haar-random U.  
claimed_feasibility | Authors note protocol is information-theoretically possible but success probability is exponentially small in the diary size (in practice infeasible for large d_A); feasible only for very small toy systems on NISQ hardware; bottlenecks include extremely low postselection success, need to implement U and its conjugates exactly, and preparing required entangled initial states.  
limitations_and_open_problems | Uses idealized maximally-mixed/thermofield-double approximations and neglects energy fluctuations; generalization to realistic thermal density matrices is problematic because it requires factorization ρ_{AB}=ρ_A⊗ρ_B and ρ_{CD}=ρ_C⊗ρ_D (physically unrealistic); postselection probability scales poorly (∼1/d_A^2 for d_R=d_A); requires ability to implement U^*, U^T and perform Bell-projections; verification and 'soft partitioning' of radiation subsystem D are left open.  
complexity_or_hardness_arguments | Information-theoretically possible but likely computationally hard in general (classical analogue requires exhaustive search); Harlow–Hayden arguments cited that decoding Hawking radiation of an old black hole is exponentially hard; success probability and complexity tradeoffs discussed but no formal BQP/QMA hardness proof for the protocol itself.  
theory_context_keywords | Hayden-Preskill, scrambling, OTOC, Rényi-2 mutual information, Haar-random unitary, teleportation, EPR pairs, thermofield double, maximally-mixed black hole.  
citations_to_prior_work | Hayden and Preskill ("Black holes as mirrors"), Page, Harlow & Hayden ("Quantum Computation vs. Firewalls"), Gao-Jafferis-Wall (traversable wormhole), Maldacena–Stanford–Yang (wormhole decoding), Sekino & Susskind (fast scramblers), Kitaev, Roberts–Yoshida, Hosur et al.  
  
### Deterministic decoder combining postselection idea with Grover-like search

Field | Value  
---|---  
name_short | Deterministic Grover decoder  
name_full | Deterministic decoder combining postselection idea with Grover-like search  
brief_description | A deterministic decoding algorithm that replaces probabilistic postselection with Grover iterations using reflections built from the EPR projector and the pulled-through projector, applying U*, U^T and reflection operators ~O(√(d_A d_R)) times to rotate the state into the decoded subspace with fidelity 1 - O(δ).  
citation_title | here  
mention_or_use | use  
target_system_or_model | Same idealized black hole model as above: finite-dimensional Hilbert spaces A,B,C,D with unitary U modeling scrambling (Haar-random/perfectly scrambling limit); black hole and partner represented by EPR pairs.  
black_hole_phenomena_targeted | Information recovery from Hawking radiation (Hayden-Preskill decoding), higher-order scrambling (higher-point OTOCs), relation to multiple-shockwave gravitational geometries.  
simulation_paradigm | Digital gate-based circuit algorithm (conceptual): iterative application of unitary operators and reflections (constructed from projectors and U, U^*, U^T) analogous to Grover search.  
quantum_hardware_platform | platform-agnostic (assumes the ability to implement U, U^T, U^* and controlled reflections); no hardware specified.  
encoding_and_mapping | Abstract qubit/register partitioning into subsystems A,B,C,D,B',R,R' with Hilbert-space dimensions as parameters; black hole degrees of freedom are abstract qubits counted by S = log2 d; no explicit low-level encoding (no Jordan-Wigner etc.).  
algorithm_or_protocol | Initialize as in probabilistic decoder to obtain |Ψ_in⟩, define projectors P_D (EPR on DD') and ~ P_A (pulled-through projector using U _and U^T), construct reflections W_D = 1 - 2P_D and ~ W_A = 2~ P_A - 1, then iterate W = ~ W_A W_D ≈ rotation; perform m_ ≈ (π/4)√(d_A d_R) iterations to approximate the postselected output deterministically.  
resource_estimates | Number of uses of U, U*, U^T scales as O(√(d_A d_R)) (each Grover iteration uses these operations); total circuit complexity ≈ O(√(d_A d_R) · C) where C is complexity to implement U once; logical qubit count ~ log2 d; no explicit gate-counts, T-counts, or shot numbers provided.  
noise_and_error_mitigation | No explicit noise model; analysis assumes ideal, reversible application of U and its conjugates; error arises analytically via parameter δ which depends on OTOC decay; no concrete error-mitigation strategies or FT assumptions given (authors note practicality issues).  
key_results_or_demonstrations | Analytic construction and performance bound: after m* ≈ (π/4)√(d_A d_R) iterations the state approximates the ideal postselected output with norm error ≤ (1+π/2)√δ (Eq. (46)), so decoding fidelity is 1 - O(δ) under scrambling assumptions; theoretical proposal only.  
validation_and_benchmarks | Analytic, diagrammatic derivations using Schmidt decomposition of relevant operators, relations between Π^m expectation values and Rényi-2m mutual informations / 4m-point OTOCs; no numeric simulation or experimental benchmark provided.  
claimed_feasibility | Authors remark Grover is optimal for black-box search so protocol may be near-optimal in number of uses of U; still infeasible for realistic large black holes because √(d_A d_R) grows exponentially in qubit count; feasible only for very small toy models; main bottlenecks are ability to apply U* and U^T, circuit depth, and coherence across many Grover iterations.  
limitations_and_open_problems | Relies on idealized factorization/thermal-state approximations to generalize beyond maximally mixed inputs; requires U, U^*, U^T and projectors implementable with low error; higher-order OTOCs appear (4m-point) making physical interpretation and holographic mapping to bulk shockwave geometries an open direction; verifying optimality in the black-box model is left as an open question.  
complexity_or_hardness_arguments | Grover-like √(N) scaling where N ∼ d_A d_R is invoked; authors cite Harlow–Hayden hardness results as context for decoding complexity of old black holes (exponential in qubit count), and note Grover's known optimality for black-box search implying potentially near-optimal use-count of U; no formal BQP-completeness claims are made for full decoding.  
theory_context_keywords | Grover search, higher-order OTOCs, Rényi-2m mutual information, scrambling, Hayden-Preskill decoding, shockwaves, holography, traversable wormhole analogy.  
citations_to_prior_work | Grover (search), Harlow & Hayden (complexity of decoding), Shenker & Stanford (multiple shocks), Maldacena–Stanford–Yang, Roberts & Yoshida, Shenker–Stanford on OTOCs; Gao–Jafferis–Wall for traversable wormhole analogue.  
  
### Gao–Jafferis–Wall traversable wormhole decoding / wormhole teleportation protocol

Field | Value  
---|---  
name_short | Traversable-wormhole decoding (mentioned)  
name_full | Gao–Jafferis–Wall traversable wormhole decoding / wormhole teleportation protocol  
brief_description | A holographic, gravity-side mechanism (double-trace coupling between boundaries of an eternal AdS black hole) that can make an Einstein–Rosen bridge traversable and realize a decoding/teleportation effect in the dual boundary theory; mentioned as a physical realization related to Hayden–Preskill decoding for special operators at early times.  
citation_title | Traversable wormholes via a double trace deformation.  
mention_or_use | mention  
target_system_or_model | Eternal AdS black hole / thermofield double state in AdS/CFT (holographic gravity model rather than a direct quantum-circuit simulation).  
black_hole_phenomena_targeted | Traversability of wormholes, teleportation-through-wormhole phenomenon, early-time decoding of signals sent through bulk geometries, relation to scrambling/time-windows.  
simulation_paradigm | Holographic dual boundary description (field-theory description) rather than a gate-model quantum-simulation protocol; discussed conceptually and compared to the proposed circuit decoders.  
quantum_hardware_platform | N/A (gravity/holography theoretical construction); authors discuss conceptual boundary-only decoding without specifying quantum hardware.  
encoding_and_mapping | Holographic mapping: bulk traversable wormhole dynamics map to specific operations on boundary CFTs (double-trace deformation coupling the two boundaries); special structure of boundary operator U at early times enables simple decoding.  
algorithm_or_protocol | Turning on a momentary coupling (double-trace deformation) between opposite CFT boundaries at time 0 to generate negative energy, allowing signals sent earlier to traverse the wormhole and be received on the other boundary—holographically dual to a boundary decoding operation.  
resource_estimates | No quantum-resource estimates given in this paper (gravity/holography conceptual result cited), authors note the wormhole scheme achieves deterministic decoding without Grover iterations but only works for operators with special early-time properties.  
noise_and_error_mitigation | Not applicable here; discussed as a theoretical gravitational mechanism rather than an implemented quantum algorithm.  
key_results_or_demonstrations | Mentioned as a recently discovered physical process that is akin to Hayden-Preskill decoding and achieves deterministic decoding in one go for signals within a certain time window; authors contrast this with their generic decoding algorithms for late times.  
validation_and_benchmarks | Cited literature (Gao–Jafferis–Wall; Maldacena–Stanford–Yang) provides holographic analyses; in this paper the wormhole protocol is referenced qualitatively as a comparison point rather than validated within the circuit framework.  
claimed_feasibility | Authors note the wormhole protocol relies on special properties of U at early times and thermofield-double/thermal-state structure; it is conceptually feasible within AdS/CFT setups but distinct from the maximally-mixed, late-time black hole models the paper analyzes.  
limitations_and_open_problems | Works only for early-time operators and for eternal AdS black hole setups (thermofield-double states); not directly applicable to maximally-mixed or generic late-time Haar-random unitary models used in the paper; reconciliation with more realistic thermal-factorization issues remains open.  
complexity_or_hardness_arguments | Not presented as a computational algorithm complexity statement here; its simplicity depends on gravitational/holographic structure rather than computational-cost arguments.  
theory_context_keywords | AdS/CFT, thermofield double, traversable wormhole, double-trace deformation, holographic decoding, early-time operator structure.  
citations_to_prior_work | Gao, Jafferis & Wall ("Traversable wormholes via a double trace deformation"), Maldacena–Stanford–Yang ("Diving into traversable wormholes").  
  
## Citation

Cite this artifact as `\cite{ast-ext-yoshida-2026-08-13}`.
[code] 
    @misc{ast-ext-yoshida-2026-08-13,
      title        = {Extraction: Efficient decoding for the Hayden-Preskill protocol},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-efficient-decoding-for-the-hayden-preskill-protocol.md},
      crossref     = {yoshida2017efficient},
      note         = {Theorizer's extraction from \cite{yoshida2017efficient}. asta-artifact id: extraction-result-95},
    }
    
    @article{yoshida2017efficient,
      title     = {Efficient decoding for the Hayden-Preskill protocol},
      author    = {Beni Yoshida and A. Kitaev},
      year      = {2017},
      url       = {https://www.semanticscholar.org/paper/54805207},
    }
[/code]
