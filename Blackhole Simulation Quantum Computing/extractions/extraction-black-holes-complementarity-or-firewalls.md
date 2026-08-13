[<- All artifacts](<../index.md>)

# Extraction: Black holes: complementarity or firewalls?

**Contents:**

  * Quantum computation on the early Hawking radiation to predict late radiation modes (projection operator \hat{P}^i)
  * Qubit/bit toy models of black hole evaporation
  * Using external spins entangled with an AdS gauge theory (N=4 SYM on S^3) as a reference to avoid time/gravity constraints on quantum computation



### Quantum computation on the early Hawking radiation to predict late radiation modes (projection operator \hat{P}^i)

Field | Value  
---|---  
name_short | Early-radiation quantum computation  
name_full | Quantum computation on the early Hawking radiation to predict late radiation modes (projection operator \hat{P}^i)  
brief_description | Thought-experiment presented in this paper in which an observer performs an abstract quantum computation on the early Hawking radiation to implement a projection operator (Appendix A) that predicts occupation numbers of specified late outgoing modes, enabling tests of entanglement/monogamy and leading to the firewall paradox.  
citation_title | here  
mention_or_use | mention  
target_system_or_model | An 'old' evaporating black hole divided into early and late Hawking-radiation subsystems; localized outgoing Hawking mode b (width ~ r_s) and its infalling/inside partner c; effective quantum field theory outside the stretched horizon.  
black_hole_phenomena_targeted | Entanglement structure of Hawking radiation (early vs late), occupation-number measurements of specific outgoing modes (N_b), information retrieval at/after Page time, and tests of cloning/monogamy that lead to firewall conclusions.  
simulation_paradigm | Platform-agnostic abstract quantum computation / thought-experiment (no explicit digital/analog simulation protocol or gate-level algorithm is specified).  
quantum_hardware_platform | None  
encoding_and_mapping | No explicit qubit-level mapping is provided. Appendix A models the early/late radiation as finite-dimensional Hilbert spaces (dimensions E and L) and constructs an approximate projection operator \hat{P}^i acting on the early subsystem, but there is no specification of a qubit encoding, lattice discretization, or fermion-to-qubit mapping.  
algorithm_or_protocol | Abstract projection-based algorithm: implement operator \hat{P}^i (defined in Appendix A) on the early radiation to project onto a chosen late-radiation basis state; no explicit gate decomposition (Trotter, LCU, PE, etc.) or measurement protocol is given.  
resource_estimates | No quantitative resource estimates (qubit counts, gate counts, depth, number of measurements, or fault-tolerance overhead) are provided. The paper does discuss the parameter regime E >> L required for the projection approximation and qualitative concerns about computation time relative to black hole lifetime (citing Ref. [20]).  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Logical/information-theoretic argument only: if such a computation can be performed, one can predict the late-mode occupation and thereby derive the paradox (violation of entropic subadditivity / cloning) showing incompatibility of postulates 1,2,4. There is no numerical simulation or experimental demonstration.  
validation_and_benchmarks | Validation is conceptual/analytic: Appendix A computes the average projection error for random (microcanonical) states and shows the error ~ L/E (so projection is accurate for E >> L); the paradox is further supported by entropy/strong-subadditivity arguments and Page-time reasoning.  
claimed_feasibility | Authors treat the computation as plausible in principle but raise and discuss objections: gravitational constraints on measurability (Ref. [19]) and possible quantum-computation runtime exceeding black hole lifetime (Ref. [20]). They argue an AdS setup with an external spin reference can avoid the latter. No concrete feasibility timeline or NISQ vs FT distinction is given.  
limitations_and_open_problems | No concrete qubit mapping or gate-level protocol; no resource counts; unresolved questions about gravitational limitations, the time required to perform the computation relative to black hole lifetimes, requirement of knowledge of black hole S-matrix and initial state, and decoherence/measurement-basis issues; all remain open in the paper.  
complexity_or_hardness_arguments | No formal complexity-theoretic statements (BQP/QMA-hardness) are proven. The paper notes qualitative computational-time concerns (might exceed black hole lifetime) but does not give formal hardness proofs for the projection task.  
theory_context_keywords | Hawking radiation, Page time, entanglement monogamy, black hole complementarity, firewall, fast scrambling, projection operator, information retrieval  
citations_to_prior_work | Hayden and Preskill 'Black holes as mirrors: Quantum information in random subsystems' (JHEP 0709 (2007) 120); Refs. [19] (objections re: gravitational effects), [20] (objections re: computation time vs lifetime); AdS/CFT references [21,22] used to motivate an AdS thought-experiment with external spins.  
  
### Qubit/bit toy models of black hole evaporation

Field | Value  
---|---  
name_short | Bit models  
name_full | Qubit/bit toy models of black hole evaporation  
brief_description | Referenced class of toy models (cited literature) that model black hole degrees of freedom and emitted radiation as discrete bits/qubits to study information flow, entanglement structure, and implications for complementarity and firewalls.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Toy discrete qubit/bit representations of black hole microstates and emitted Hawking radiation (simple finite-dimensional Hilbert-space models).  
black_hole_phenomena_targeted | Purity vs mixedness of Hawking radiation, entanglement transfer during evaporation, Page curve-type behavior in toy models, and theorems that purity implies horizon cannot be information-free.  
simulation_paradigm | Conceptual toy-model analysis (not presented as an implemented quantum-simulation protocol in this paper).  
quantum_hardware_platform | None  
encoding_and_mapping | Bits/qubits represent black hole microstates and emitted radiation sectors; the paper references prior models but does not spell out a specific encoding to physical qubits or operations.  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Paper uses results/theorems from the bit-model literature (refs [12–16]) as inspiration; specifically invokes the theorem that purity of Hawking radiation requires O(1) corrections to low-energy evolution at the horizon. No simulation/demo in this paper.  
validation_and_benchmarks | Validation in cited works comes from analytic toy-model calculations and entropic arguments; this paper leverages those conclusions but does not itself perform numerical checks.  
claimed_feasibility | None  
limitations_and_open_problems | Toy character with limited fidelity to semiclassical gravity; unclear extension to macroscopic nonextremal black holes; do not capture dynamical spacetime geometry.  
complexity_or_hardness_arguments | None  
theory_context_keywords | bit models, qubit toy models, fuzzball, entanglement, information transfer, Page time  
citations_to_prior_work | Refs [12–16] (S.D. Mathur and others) including discussions of bit/qubit toy models and the fuzzball program.  
  
### Using external spins entangled with an AdS gauge theory (N=4 SYM on S^3) as a reference to avoid time/gravity constraints on quantum computation

Field | Value  
---|---  
name_short | AdS/CFT reference-spin thought experiment  
name_full | Using external spins entangled with an AdS gauge theory (N=4 SYM on S^3) as a reference to avoid time/gravity constraints on quantum computation  
brief_description | The paper describes a thought-experiment replacing the early Hawking radiation by an external spin system entangled with N=4 Yang-Mills on S^3 (dual to AdS black hole), arguing that processing those external spins with a quantum computation removes gravitational/time limits that might otherwise prevent the measurement-before-fall-in scenario.  
citation_title | here  
mention_or_use | mention  
target_system_or_model | AdS black hole / N=4 SYM on S^3 (gauge/gravity duality) with an auxiliary external spin reference system entangled with the gauge theory.  
black_hole_phenomena_targeted | Information retrieval from the system dual to the AdS black hole and prediction of late radiation bits without gravitational/time constraints; conceptual test of complementarity/firewall by replacing early radiation with an externally accessible system.  
simulation_paradigm | Thought-experiment using holographic duality; not an explicit quantum-simulation proposal or hardware implementation.  
quantum_hardware_platform | None  
encoding_and_mapping | No explicit mapping to qubits is given; the construction is conceptual: external spins (outside AdS) stand in for early radiation and are used as classical/quantum inputs to computations.  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Conceptual conclusion: using a non-geometric external reference removes the argument that gravitational constraints prohibit the required quantum computation; no simulation or resource analysis presented.  
validation_and_benchmarks | Argument relies on holographic reasoning (gauge/gravity duality) and conceptual substitution rather than computational benchmarking.  
claimed_feasibility | Authors claim that in principle the external-spin thought-experiment could be carried out without gravitational/time limitation; no operational protocol or experimental feasibility analysis is given.  
limitations_and_open_problems | Requires ability to prepare the specific entangled state between gauge theory and spins and knowledge of the S-matrix; does not provide operational encoding or error/resource analysis.  
complexity_or_hardness_arguments | None  
theory_context_keywords | AdS/CFT, gauge/gravity duality, N=4 SYM on S^3, Hawking-Page transition, holography, information retrieval  
citations_to_prior_work | Refs [21,22] on AdS/CFT and the dual description of black holes; Hayden-Preskill style information arguments.  
  
## Citation

Cite this artifact as `\cite{ast-ext-almheiri-2026-08-13}`.
[code] 
    @misc{ast-ext-almheiri-2026-08-13,
      title        = {Extraction: Black holes: complementarity or firewalls?},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-black-holes-complementarity-or-firewalls.md},
      crossref     = {almheiri2012black},
      note         = {Theorizer's extraction from \cite{almheiri2012black}. asta-artifact id: extraction-result-24},
    }
    
    @article{almheiri2012black,
      title     = {Black holes: complementarity or firewalls?},
      author    = {Ahmed Almheiri and D. Marolf and J. Polchinski and J. Sully},
      year      = {2012},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/55581818},
    }
[/code]
