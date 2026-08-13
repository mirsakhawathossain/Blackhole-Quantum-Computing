[<- All artifacts](<../index.md>)

# Extraction: Traversable wormholes via a double trace deformation

**Contents:**

  * Traversable Einstein-Rosen bridge of an eternal BTZ black hole via a double-trace deformation
  * Dynamical (unitary) model of quantum teleportation implemented as V = Σ_i P_i^{QA} U_i^{B}
  * Hayden–Preskill model: black holes as mirrors and information recovery from Hawking radiation



### Traversable Einstein-Rosen bridge of an eternal BTZ black hole via a double-trace deformation

Field | Value  
---|---  
name_short | Traversable BTZ wormhole (double-trace)  
name_full | Traversable Einstein-Rosen bridge of an eternal BTZ black hole via a double-trace deformation  
brief_description | Construction and 1-loop analysis showing that a relevant double-trace boundary coupling between the two CFT boundaries of the eternal BTZ (AdS_3) black hole produces negative averaged null energy on the horizon and renders the Einstein-Rosen bridge traversable at linear order in the coupling h.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Eternal BTZ black hole (AdS_3) with a bulk scalar field dual to a boundary scalar operator of dimension Δ; geometry treated semiclassically (classical background + 1-loop quantum stress tensor).  
black_hole_phenomena_targeted | Traversability of wormhole / violation of averaged null energy condition (ANEC) on horizon; backreaction of negative null energy on horizon generators; information transfer through ER bridge (qualitative teleportation analogy).  
simulation_paradigm | analytical semiclassical computation (not a quantum-computing simulation); perturbative 1-loop quantum field theory in curved spacetime around classical background.  
quantum_hardware_platform | None  
encoding_and_mapping | Not an encoding into qubits; the deformation corresponds in AdS/CFT to modified boundary conditions (double-trace) for a bulk scalar: β_L(t,φ)=h(-t,φ)α_R(-t,φ) and β_R(t,φ)=h(t,φ)α_L(-t,φ), i.e., a boundary-to-boundary coupling that activates the normally frozen falloff component of the bulk field.  
algorithm_or_protocol | Perturbative computation of modified bulk two-point function (first order in h) via large-N factorization and KMS relations; point-splitting to compute ⟨T_{μν}⟩ and integration of T_{UU} along horizon to test traversability. No digital/analog quantum algorithm proposed.  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Analytic expression for ∫ _{U0}^{∞} dU T_ (eq. 5.1). This is a theoretical (analytic + numerical integral) demonstration, not an experimental quantum simulation.} (equation (3.18)/(A.15)) showing it is negative for 0<Δ<1 for positive coupling h, numerically computed T_{UU}(U) demonstrating negative null energy after turn-on; conclusion that wormhole opens by an amount ΔV ∼ h G_N / R^{D-2  
validation_and_benchmarks | Internal consistency checks: large-N factorization, KMS conditions, Hadamard subtraction for renormalization, analytic limiting behavior at late times, numerical evaluation of integrals, and comparison to known classical linearized Einstein equations (equations (1.3)-(1.5)).  
claimed_feasibility | Feasible as a controlled semiclassical calculation in AdS/CFT for small h and 1-loop order; achieving the thermofield double state and boundary coupling in a physical experiment is acknowledged to be extremely fine-tuned and not addressed as an experimental implementation.  
limitations_and_open_problems | Requires fine-tuned thermofield double initial state; analysis is perturbative in h (linearized gravity + 1-loop quantum matter); backreaction beyond linear order not computed; extension to D>3 is expected but harder; practical preparation of the CFT state and implementation of boundary-boundary coupling not addressed; no operational quantum-computer implementation provided.  
complexity_or_hardness_arguments | No explicit computational-complexity class claims; qualitative statement that decoding/recovery of information in analogous setups relates to quantum computation (see separate Hayden–Preskill discussion) but no formal hardness proofs.  
theory_context_keywords | AdS/CFT, BTZ black hole, double-trace deformation, averaged null energy condition (ANEC), ER=EPR, quantum extremal surface, holographic entanglement entropy, perturbative 1-loop backreaction, thermofield double.  
citations_to_prior_work | Cites Maldacena (Eternal black holes in anti-de Sitter), papers on double-trace deformations (Witten, Berkooz et al.), Shenker & Stanford on shockwaves/butterfly effect, and holographic entanglement literature (Ryu-Takayanagi, Hubeny-Rangamani-Takayanagi, Faulkner-Lewkowycz-Maldacena).  
  
### Dynamical (unitary) model of quantum teleportation implemented as V = Σ_i P_i^{QA} U_i^{B}

Field | Value  
---|---  
name_short | Teleportation-as-unitary (microscopic)  
name_full | Dynamical (unitary) model of quantum teleportation implemented as V = Σ_i P_i^{QA} U_i^{B}  
brief_description | Authors describe a fully quantum, dynamical formulation of teleportation as a time-dependent interaction V built out of projectors on a QA system and conditional unitaries on B, and suggest that such a microscopic teleportation protocol can be dual to a qubit traversing a temporarily-open ER=EPR wormhole.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Two-CFT thermofield-double pair (left and right) dual to an eternal black hole; the 'Q' qubit is a small subsystem that falls into one black hole and is later recovered on the other side via a unitary interaction that acts like teleportation.  
black_hole_phenomena_targeted | Information transfer through wormhole (operational interpretation of ER=EPR); transmission/recovery of a single qubit via boundary-boundary interaction; connection to quantum teleportation protocols.  
simulation_paradigm | Conceptual quantum-information protocol (unitary dynamics), not instantiated as a digital/analog quantum-simulation algorithm.  
quantum_hardware_platform | None  
encoding_and_mapping | No explicit qubit encoding or mapping to hardware given; the description uses abstract projectors P_i^{QA} and conditional unitaries U_i^{B} as components of a time-dependent interaction, treated in the continuum CFT context.  
algorithm_or_protocol | Theoretical description of teleportation as a unitary V = Σ_i P_i^{QA} U_i^{B}; authors argue that treating V as a time-dependent interaction can produce negative averaged null energy and so render the wormhole traversable, thereby providing a gravity dual for a dynamical teleportation process.  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Conceptual claim: a microscopic unitary implementation of teleportation (not a projective instantaneous measurement) could correspond to physically sending a qubit through the traversable wormhole; no experimental or circuit-level demonstration is provided.  
validation_and_benchmarks | Argumentative/qualitative: matches expectations from holographic picture (qubit thermalizes then reappears when appropriate boundary interaction applied); no quantitative algorithmic benchmarks.  
claimed_feasibility | Authors note that if Alice's measurement is effectively instantaneous and classical, the traversable window is very small and semiclassical description may break down; they do not provide a timeline or resource-scale claims for quantum-computing realization.  
limitations_and_open_problems | No explicit microscopic CFT model or circuit is constructed; preparing the thermofield double and realizing the requisite time-dependent interaction are highly nontrivial; semiclassical description may fail for extremely narrow traversable windows.  
complexity_or_hardness_arguments | None  
theory_context_keywords | quantum teleportation, ER=EPR, thermofield double, boundary-boundary coupling, holographic dual of teleportation, information transfer, scrambling.  
citations_to_prior_work | References to quantum teleportation literature (standard teleportation protocol) and holographic teleportation discussions (e.g., works by Susskind and by Numasawa et al. referenced in the paper).  
  
### Hayden–Preskill model: black holes as mirrors and information recovery from Hawking radiation

Field | Value  
---|---  
name_short | Hayden–Preskill decoding (black hole as mirror)  
name_full | Hayden–Preskill model: black holes as mirrors and information recovery from Hawking radiation  
brief_description | Authors cite the Hayden–Preskill result to draw an analogy: given an auxiliary system maximally entangled with a black hole and under efficient scrambling, only a small additional fraction of Hawking radiation is needed for a quantum computation to reconstruct a thrown-in qubit; they relate this to boundary interactions that can make a qubit reappear via traversable-wormhole dynamics.  
citation_title | Black holes as mirrors: Quantum information in random subsystems  
mention_or_use | mention  
target_system_or_model | Model of an evaporating (or entangled) black hole treated as an efficient quantum scrambler interacting with Hawking radiation; in paper used as conceptual analogy to the traversable-wormhole + boundary-computation picture.  
black_hole_phenomena_targeted | Information recovery/decoding of a qubit thrown into a black hole; operational aspects of black hole information retrieval.  
simulation_paradigm | Conceptual quantum-computation model (decoding as a quantum computation on radiation), not a concrete quantum-simulation implementation in this paper.  
quantum_hardware_platform | None  
encoding_and_mapping | No explicit mapping to qubits or circuits provided here; narrative assumes abstract quantum computation acting on Hawking radiation system plus auxiliary entangled system.  
algorithm_or_protocol | Reference to decoding/computation on radiation required to reconstruct a qubit per Hayden–Preskill; no concrete algorithm, gate counts, or circuit decompositions provided in this paper.  
resource_estimates | The paper paraphrases Hayden–Preskill qualitatively: one needs only an 'order unity' additional amount of radiation (i.e. a small subsystem) to reconstruct the qubit given efficient scrambling, but no gate/circuit resource estimates are provided here.  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Used as conceptual support for interpreting boundary interaction as triggering a quantum computation that causes the qubit to reappear on the other side after ~scrambling time; no simulation or empirical demonstration in this paper.  
validation_and_benchmarks | No direct validation in this paper; appeal is to the existing Hayden–Preskill theoretical result.  
claimed_feasibility | Authors suggest conceptual feasibility in principle (given access to auxiliary entangled system and appropriate quantum computation), but practical realization is not discussed.  
limitations_and_open_problems | Does not address explicit decoding circuit construction or complexity, error tolerance, nor the realization of the required operations in a CFT or on a quantum device.  
complexity_or_hardness_arguments | No explicit complexity class statements in this paper beyond the qualitative invocation of quantum computation needed for decoding; the original Hayden–Preskill work discusses decoding complexity but specifics are not reproduced here.  
theory_context_keywords | black hole information, scrambling, Hayden–Preskill, quantum decoding of Hawking radiation, ER=EPR analogy.  
citations_to_prior_work | Direct citation to Hayden and Preskill (2007) 'Black holes as mirrors: Quantum information in random subsystems' and related literature on scrambling and information recovery.  
  
## Citation

Cite this artifact as `\cite{ast-ext-gao-2026-08-13}`.
[code] 
    @misc{ast-ext-gao-2026-08-13,
      title        = {Extraction: Traversable wormholes via a double trace deformation},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-traversable-wormholes-via-a-double-trace-deformation.md},
      crossref     = {gao2016traversabl},
      note         = {Theorizer's extraction from \cite{gao2016traversabl}. asta-artifact id: extraction-result-19},
    }
    
    @article{gao2016traversabl,
      title     = {Traversable wormholes via a double trace deformation},
      author    = {Ping Gao and D. Jafferis and Aron C. Wall},
      year      = {2016},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/119258660},
    }
[/code]
