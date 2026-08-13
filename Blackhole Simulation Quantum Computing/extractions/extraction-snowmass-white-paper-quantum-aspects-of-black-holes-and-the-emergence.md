[<- All artifacts](<../index.md>)

# Extraction: Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime

**Contents:**

  * Sachdev-Ye-Kitaev model
  * Jackiw-Teitelboim gravity
  * Traversable wormhole / wormhole teleportation protocol
  * Quantum gravity in the lab / laboratory quantum simulation of holographic systems



### Sachdev-Ye-Kitaev model

Field | Value  
---|---  
name_short | SYK  
name_full | Sachdev-Ye-Kitaev model  
brief_description | A quantum-mechanical ensemble of N Majorana fermions with random all-to-all q-body interactions (often q=4) that is maximally chaotic and, at low energies, described by an emergent Schwarzian action whose gravitational dual is JT gravity.  
citation_title |   
mention_or_use | mention  
target_system_or_model | SYK model (N Majorana fermions with random 4-fermion couplings; ensemble averaged)  
black_hole_phenomena_targeted | fast scrambling / maximal chaos (OTOCs), spectral form factor (ramp), low-energy near-extremal black hole physics via JT gravity dual, wormhole-related nonperturbative effects  
simulation_paradigm | discussion/mention of numerical studies and mapping to low-dimensional gravity; connection to quantum simulation is referenced but no concrete gate/analog simulation protocol is given in this paper  
quantum_hardware_platform | platform-agnostic in this paper (the authors refer to 'noisy quantum simulators' and experimental work [173–175] but do not specify hardware)  
encoding_and_mapping | paper states the standard theoretical mapping: SYK low-energy dynamics map (via a change of variables) to Jackiw-Teitelboim (JT) gravity/Schwarzian mode; no qubit-level encoding (e.g. Jordan-Wigner or truncation schemes) or lattice discretization for SYK-to-qubit implementation is described here  
algorithm_or_protocol | not specified for quantum hardware in this paper; references to numerical exact diagonalization and ensemble averaging for SYK studies; conceptual use of teleportation/traversability protocols in SYK/JT context is discussed but without algorithmic detail  
resource_estimates | no resource estimates provided (no qubit counts, gate depths, measurement budgets, or FT assumptions given)  
noise_and_error_mitigation | not discussed in detail; only a general mention that experiments used 'noisy quantum simulators' in follow-up/related works (refs. [173–175]) without error budgets or mitigation techniques described  
key_results_or_demonstrations | this white paper summarizes prior results: SYK shows maximal chaos and fast scrambling, low-energy SYK maps to JT gravity where wormhole and replica phenomena can be analyzed, and ensemble-averaged wormhole saddles explain the ramp in the spectral form factor; the paper itself does not present new quantum-simulation experiments  
validation_and_benchmarks | validation described in the reviewed literature: comparison of SYK numerics to semiclassical JT gravity predictions, spectral form factor behavior compared to random matrix universality after ensemble averaging; the white paper points to these comparisons but does not perform them itself  
claimed_feasibility | authors state that SYK/JT systems have motivated quantum-simulation efforts and that 'quantum gravity in the lab' is an active direction; no concrete timeline or resource feasibility analysis (NISQ vs FTQC) is provided  
limitations_and_open_problems | finite-N effects and noise vs ensemble-averaged gravitational saddles; factorization vs ensemble interpretation (JT gravity dual to an ensemble); absence of a detailed qubit encoding and resource scaling; toy-model nature (low-dimensional gravity) limiting conclusions about higher-dimensional black holes  
complexity_or_hardness_arguments | paper emphasizes exponential complexity of decoding Hawking radiation and reconstruction (Hayden-Preskill, Python's Lunch conjecture) and discusses random-matrix behavior; no formal BQP/QMA hardness proofs for physical simulation tasks are given here  
theory_context_keywords | ['SYK', 'Schwarzian', 'JT gravity', 'maximal chaos', 'spectral form factor', 'random matrix universality', 'wormholes', 'ensemble duality']  
citations_to_prior_work | References in the paper: [26–31] (SYK foundational and reviews), [32,33] (JT gravity), [158,159,162] (spectral form factor / random matrix connections), [224,225] (JT as ensemble / matrix model connections)  
  
### Jackiw-Teitelboim gravity

Field | Value  
---|---  
name_short | JT gravity  
name_full | Jackiw-Teitelboim gravity  
brief_description | A two-dimensional dilaton gravity theory that captures universal low-energy dynamics of near-extremal black holes and is the effective gravitational dual of the low-energy sector of SYK-like models.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Two-dimensional dilaton gravity (JT gravity) as a model for near-extremal black holes and as the low-energy dual of SYK  
black_hole_phenomena_targeted | replica wormholes and islands (Page curve), spectral density and spectral form factor (ramp/plateau structure), semiclassical gravitational saddles and nonperturbative wormhole effects  
simulation_paradigm | theoretical/semi-classical path integral analysis and mapping from SYK; paper notes JT gravity has been used as a controlled model for studying wormholes and replica effects, and that it motivated quantum-simulation thinking, but does not present a quantum simulation protocol  
quantum_hardware_platform | platform-agnostic; no JW/ion/trapped-atom implementation specified  
encoding_and_mapping | paper describes conceptual mapping: SYK → low-energy Schwarzian mode → JT gravity; no discrete qubit encoding or truncation scheme to represent JT gravity on quantum devices is described  
algorithm_or_protocol | analysis techniques are gravitational: semiclassical path integral, replica trick; no gate-model algorithms or Trotterization schemes for JT gravity are given in the paper  
resource_estimates | none provided  
noise_and_error_mitigation | not discussed  
key_results_or_demonstrations | reviewed theoretical results: JT gravity provides precise computations of the density of states, captures replica wormholes that yield the Page curve, and connects to random matrix ensembles; these results motivated experimental/theoretical quantum-simulation proposals cited elsewhere but not detailed here  
validation_and_benchmarks | validation in the literature via exact computations in JT gravity matched to SYK numerics and random matrix predictions; the white paper summarizes these validations but does not perform them  
claimed_feasibility | JT gravity is presented as a theoretically tractable toy model useful for thinking about quantum-simulation prospects, but the paper does not claim concrete near-term feasibility of full JT gravity simulations on specific quantum hardware  
limitations_and_open_problems | JT is a low-dimensional toy model; ensemble duality vs single-system duality raises interpretational issues; the mapping to actual qubit experiments and scaling to realistic black holes is not provided  
complexity_or_hardness_arguments | discussions of nonperturbative wormhole saddles and ensemble averaging (factorization problem) highlight conceptual complexity; no explicit computational hardness proofs for simulating JT gravity are given  
theory_context_keywords | ['JT gravity', 'replica wormholes', 'islands', 'Page curve', 'dilaton gravity', 'random matrix duality']  
citations_to_prior_work | References in the paper: [32,33] (JT gravity foundational), [176–181], [224,225] (density of states and JT as ensemble/matrix model)  
  
### Traversable wormhole / wormhole teleportation protocol

Field | Value  
---|---  
name_short | Traversable wormhole teleportation  
name_full | Traversable wormhole / wormhole teleportation protocol  
brief_description | A theoretical protocol in which a small coupling between two entangled black holes (or between two boundary systems preparing a thermofield double) makes an otherwise non-traversable Einstein-Rosen bridge effectively traversable, enabling information transfer that is interpreted as teleportation through the wormhole.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Eternal two-sided black hole / thermofield double states in SYK and JT gravity (two copies coupled by a small interaction)  
black_hole_phenomena_targeted | wormhole traversability, teleportation of quantum information through the wormhole, dynamics of small perturbations and information transfer between entangled systems  
simulation_paradigm | paper reviews theoretical protocols in SYK/JT and explicitly notes that these ideas 'have been used to inspire and explain experiments carried out using noisy quantum simulators' (refs. [173–175]); however the white paper does not provide the experimental protocols or gate-level algorithms  
quantum_hardware_platform | not specified in this paper; cited experimental follow-ups used 'noisy quantum simulators' (platform unspecified in main text here)  
encoding_and_mapping | conceptual mapping: prepare thermofield double (TFD) state of two copies and apply a small coupling/measurement protocol; the paper notes difficulty of preparing TFD and scaling but gives no qubit-level mapping or fermion-to-qubit encoding  
algorithm_or_protocol | teleportation-through-wormhole protocol (theoretical); Petz map and modular-flow-based reconstruction discussed in the context of decoding, but no explicit quantum-circuit implementation is described in this paper  
resource_estimates | no quantitative resource estimates provided (qubits, gate depth, shots absent)  
noise_and_error_mitigation | not discussed here (the paper only references that noisy simulators have implemented proof-of-principle experiments in related works)  
key_results_or_demonstrations | the white paper summarizes theoretical findings that traversability can be induced and analyzed in SYK/JT and states that these ideas inspired laboratory experiments (refs. [173–175]) but it does not itself present experimental data or numerical simulation benchmarks  
validation_and_benchmarks | theoretical validation comparing SYK/JT computations and traversability calculations; referenced experiments (outside this paper) are implied to have benchmarked proof-of-principle teleportation against theory, but specifics are not provided here  
claimed_feasibility | authors assert that small-scale proof-of-principle experiments have been carried out on noisy quantum simulators and that quantum gravity-inspired protocols may be accessible on NISQ devices for limited tasks; no timeline or scaling claims are given  
limitations_and_open_problems | practical limitations: difficulty preparing thermofield double states at scale, small system sizes in experiments, toy-model nature (SYK/JT), ensemble vs single-instance interpretational issues, verification and scaling obstacles  
complexity_or_hardness_arguments | reconstruction/decoding of interior information is argued elsewhere in the paper to be exponentially complex (Hayden-Preskill, Python's Lunch); traversability/teleportation demonstrations on small systems do not bypass these complexity statements for generic decoding  
theory_context_keywords | ['traversable wormhole', 'teleportation', 'thermofield double', 'ER=EPR', 'Petz map', 'modular flow', 'SYK', 'JT gravity']  
citations_to_prior_work | Paper references theoretical works on traversability and teleportation in gravity and SYK [167–172] and points to experimental follow-up works [173–175] implementing inspired protocols on noisy quantum simulators (specific titles for these experimental refs are not listed in the main text of this white paper excerpt)  
  
### Quantum gravity in the lab / laboratory quantum simulation of holographic systems

Field | Value  
---|---  
name_short | Quantum gravity in the lab  
name_full | Quantum gravity in the lab / laboratory quantum simulation of holographic systems  
brief_description | The program of using controllable quantum many-body systems and NISQ devices to simulate models with holographic duals (e.g., SYK-like models) or to implement gravity-inspired protocols (e.g., traversable-wormhole teleportation) to gain experimental insight into quantum-gravitational phenomena.  
citation_title |   
mention_or_use | mention  
target_system_or_model | SYK models, coupled SYK (two copies), low-energy JT-gravity-related dynamics, small-scale toy-models of holography and teleportation protocols  
black_hole_phenomena_targeted | entanglement structure of thermofield double states, traversable-wormhole teleportation, signatures of scrambling (OTOCs), aspects of the Page-curve / information transfer in toy evaporating setups (conceptually)  
simulation_paradigm | NISQ / noisy-quantum-simulator proof-of-principle experiments are cited as the starting point; paper does not provide a detailed classification of paradigms (digital/analog/hybrid) for these experiments  
quantum_hardware_platform | referred to generically as 'noisy quantum simulators' in this paper; no explicit platform (superconducting, trapped ions, Rydberg, photonics) is specified in the provided text  
encoding_and_mapping | the white paper does not provide qubit-level encodings; it notes conceptual mappings (TFD preparation, coupling two copies) but leaves implementation details to the cited experimental/theoretical literature  
algorithm_or_protocol | no explicit circuit-level algorithms are described in this white paper; it references teleportation-through-wormhole protocols and Petz/map/modular-flow reconstruction as theoretical constructs motivating experiments  
resource_estimates | not provided here (no qubit counts, gate-depth, or measurement budgets given)  
noise_and_error_mitigation | not described in this paper; only general mention that experiments were performed on noisy devices  
key_results_or_demonstrations | the white paper reports that 'progress in this direction has started already with [173–175]' and frames quantum-simulation of holographic models as an active future direction, but it does not present experimental results itself  
validation_and_benchmarks | validation of experimental/theoretical works is referenced indirectly (comparison to SYK/JT theoretical predictions and teleportation/traversability calculations), but no benchmarks are presented in this white paper  
claimed_feasibility | authors express optimism that NISQ experiments can probe some holographic phenomena and that further laboratory work could inform quantum-gravity questions, but they emphasize many theoretical and practical open problems and do not give concrete feasibility thresholds  
limitations_and_open_problems | toy-model limitations, small system sizes, difficulty of preparing TFD states and representing dynamical spacetime, ensemble vs single Hamiltonian issues, verification and scaling, and conceptual gaps between low-dimensional models and full quantum gravity  
complexity_or_hardness_arguments | paper reiterates that decoding interior information can be exponentially hard in system entropy and that certain reconstruction tasks likely require exponential resources; no rigorous complexity-theoretic classification of the simulation tasks is provided  
theory_context_keywords | ['quantum simulation', 'NISQ', 'holography', 'SYK', 'JT gravity', 'traversable wormhole', 'teleportation', 'Page curve']  
citations_to_prior_work | The white paper points to experimental/theoretical follow-ups [167–175] (the specific titles for the experimental refs [173–175] are not provided in the excerpt) and to theoretical groundwork in SYK/JT and traversability [26–33, 167–172]  
  
## Citation

Cite this artifact as `\cite{ast-ext-bousso-2026-08-13}`.
[code] 
    @misc{ast-ext-bousso-2026-08-13,
      title        = {Extraction: Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-snowmass-white-paper-quantum-aspects-of-black-holes-and-the-emergence.md},
      crossref     = {bousso2022snowmass},
      note         = {Theorizer's extraction from \cite{bousso2022snowmass}. asta-artifact id: extraction-result-31},
    }
    
    @article{bousso2022snowmass,
      title     = {Snowmass White Paper: Quantum Aspects of Black Holes and the Emergence of Spacetime},
      author    = {R. Bousso and Xi Dong and Netta Engelhardt and T. Faulkner and Thomas Hartman and S. Shenker and D. Stanford},
      year      = {2022},
      url       = {https://www.semanticscholar.org/paper/245837521},
    }
[/code]
