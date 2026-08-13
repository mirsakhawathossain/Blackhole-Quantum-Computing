[<- All artifacts](<../index.md>)

# Extraction: Entanglement wedge reconstruction and the information paradox

**Contents:**

  * Sachdev-Ye-Kitaev (SYK) model
  * Haar-random unitary qubit toy model (random unitary model of boundary dynamics)
  * Thermofield Double (TFD) state



### Sachdev-Ye-Kitaev (SYK) model

Field | Value  
---|---  
name_short | SYK  
name_full | Sachdev-Ye-Kitaev (SYK) model  
brief_description | A many-body quantum mechanical model of N fermions with random all-to-all interactions that serves as a toy model of holographic quantum gravity and nearly-AdS2 dynamics; used in the paper as an explicit toy model for black-hole microstates and interior reconstruction.  
citation_title |   
mention_or_use | use  
target_system_or_model | SYK model as a toy model of nearly-AdS2 black holes / quantum gravity microstates  
black_hole_phenomena_targeted | Interior reconstruction/state-dependence of bulk operators, black hole microstates, aspects of the Page curve and Hayden–Preskill decoding in toy-model context  
simulation_paradigm | platform-agnostic / theoretical many-body model analysis (no quantum-computing simulation protocol described in this paper)  
quantum_hardware_platform | platform-agnostic (no hardware platform assumed or used)  
encoding_and_mapping | No explicit qubit/fermion-to-qubit mapping, lattice discretization, or Jordan-Wigner/Bravyi-Kitaev prescription is provided in this paper; the SYK model is discussed at the level of many-fermion Hilbert spaces and overcomplete bases of pure microstates (Kourkoulou–Maldacena states referenced and extended in Appendix C).  
algorithm_or_protocol | No quantum algorithm given; the paper uses analytic and quantum-information arguments (entanglement wedge reconstruction, quantum extremal surfaces) applied to SYK toy-model states rather than circuit implementations. It cites/random-unitary toy models as conceptual models for boundary dynamics.  
resource_estimates | None provided (no qubit counts, depth, or gate counts are discussed for realizing SYK on quantum hardware in this paper).  
noise_and_error_mitigation | Not discussed (paper is analytic/theoretical; no experimental or NISQ proposals with noise models are given).  
key_results_or_demonstrations | Appendix C argues that the Kourkoulou–Maldacena SYK construction can be extended to produce minimally state-dependent interior reconstructions for code spaces with entropy nearly as large as the Bekenstein–Hawking entropy; the SYK model is used to illustrate how interior reconstructions can be state-dependent and how minimal state-dependence suffices to avoid typical-state firewall paradoxes.  
validation_and_benchmarks | Validation is theoretical: consistency checks against entanglement wedge reconstruction criteria, comparisons to random-unitary toy-model expectations and known SYK microstate constructions. No numerical quantum-simulation benchmarks are presented.  
claimed_feasibility | No claims about feasibility of quantum simulation on NISQ or fault-tolerant devices are made; the discussion is conceptual and analytic about holographic encoding and state dependence in SYK.  
limitations_and_open_problems | SYK is a toy model: while it captures some qualitative features of near-AdS2 gravity and black-hole microstates, it is not a full higher-dimensional gravitational model; no explicit mapping to qubits/gates or experimental proposals are given; graviton modes and certain realistic greybody/curvature effects are not modelled in SYK toy treatment here.  
complexity_or_hardness_arguments | No explicit complexity-theoretic statements about the hardness of simulating SYK or decoding procedures on quantum computers are provided in this paper. The paper discusses decoding in information-theoretic terms (Hayden–Preskill) but does not quantify computational complexity for decoding.  
theory_context_keywords | SYK, nearly-AdS2, toy model, Kourkoulou–Maldacena states, entanglement wedge reconstruction, state dependence, Hayden–Preskill  
citations_to_prior_work | Referenced: Kourkoulou–Maldacena construction and SYK literature (cited as [37] in the paper); SYK used as example in Almheiri's work [31] and related SYK discussions in the holography literature (paper gives ref numbers but not explicit titles).  
  
### Haar-random unitary qubit toy model (random unitary model of boundary dynamics)

Field | Value  
---|---  
name_short | Haar-random qubit model  
name_full | Haar-random unitary qubit toy model (random unitary model of boundary dynamics)  
brief_description | A toy-model description of boundary dynamics in which the CFT dynamics are modelled by Haar-random unitaries acting on many qubits; used in the paper as an illustrative model that reproduces the Page curve and Hayden–Preskill-style random-decoding behaviour.  
citation_title |   
mention_or_use | use  
target_system_or_model | Boundary CFT dynamics modelled as a Haar-random unitary on a large number of qubits; a random-unitary toy model of black-hole evaporation and information scrambling  
black_hole_phenomena_targeted | Page curve (entropy vs time), Hayden–Preskill decoding criterion, scrambling and information recovery  
simulation_paradigm | classical-theoretical random-unitary toy model; conceptual model rather than an implemented quantum simulation  
quantum_hardware_platform | platform-agnostic / theoretical (no hardware specified)  
encoding_and_mapping | Described abstractly as qubits undergoing a Haar-random unitary; no explicit low-level encoding, fermion mappings, or circuit constructions are given in this paper.  
algorithm_or_protocol | No quantum algorithm for implementing Haar-random dynamics is provided; the model is used analytically to motivate expected entropic behaviour (Page curve) and decoding thresholds.  
resource_estimates | None provided (no qubit counts, gate depths, or measurement budgets specified).  
noise_and_error_mitigation | Not applicable / not discussed (toy-model analytic usage).  
key_results_or_demonstrations | The paper states that modelling boundary dynamics with a Haar-random unitary reproduces the Page curve and Hayden–Preskill-type decoding behaviour and uses this as motivation; the paper derives the Page curve directly from bulk quantum extremal surface arguments, and notes agreement with random-unitary toy models.  
validation_and_benchmarks | Validation is conceptual: the Haar-random model reproduces previously known toy-model results (Page curve, decoding thresholds) and matches the bulk RT/q.e.s. calculations presented in the paper.  
claimed_feasibility | No experimental feasibility claims; model is conceptual and used for intuition rather than as a concrete quantum-simulation proposal.  
limitations_and_open_problems | Haar-random dynamics are an idealization (not physically realistic dynamics for a local CFT), and implementing exact Haar randomness is exponentially costly; the model omits greybody factors and local field-theory structure unless supplemented.  
complexity_or_hardness_arguments | The paper notes that Page-curve behaviour can be modelled by Haar-random unitaries (a common toy assumption) but does not discuss complexity-theoretic hardness of sampling or implementing such unitaries on quantum hardware.  
theory_context_keywords | Haar random unitary, Page curve, Hayden–Preskill, random-unitary toy model, scrambling  
citations_to_prior_work | Paper references prior toy-model literature on Page curve and random unitaries (cited generically in the text; specific refs include Hayden–Preskill [8] and Page's original conjecture [9]).  
  
### Thermofield Double (TFD) state

Field | Value  
---|---  
name_short | TFD  
name_full | Thermofield Double (TFD) state  
brief_description | An entangled purification of a thermal density matrix commonly used in holography; in AdS/CFT the TFD of two CFTs is dual to a two-sided eternal black hole and is used in the paper as an example to illustrate ER=EPR and firewall-resolution arguments.  
citation_title |   
mention_or_use | use  
target_system_or_model | Two-sided Schwarzschild/eternal AdS black hole dual to a thermofield double entangled state of two boundary CFTs  
black_hole_phenomena_targeted | Entanglement structure across the horizon, firewall paradox discussion, ER=EPR conceptual examples  
simulation_paradigm | analytical state construction (thermofield double), not presented as a quantum-simulation protocol in this paper  
quantum_hardware_platform | platform-agnostic (no hardware or experimental TFD-preparation protocol discussed here)  
encoding_and_mapping | TFD is given by the standard Schmidt-sum form sum_i e^{-βE_i/2}|~i>|i>; no mapping to qubits or circuit to prepare TFD is provided in this paper.  
algorithm_or_protocol | No quantum-circuit preparation protocol is described; TFD is used as an analytic/physical example illustrating entanglement between two boundaries.  
resource_estimates | None provided.  
noise_and_error_mitigation | Not discussed.  
key_results_or_demonstrations | TFD is used to argue that when a black hole is maximally entangled with an external system (e.g., second CFT) the firewall paradox is resolved because interior modes are encoded in the external system; TFD serves as conceptual evidence for entanglement-wedge-style resolutions.  
validation_and_benchmarks | Argument is conceptual and based on known AdS/CFT duality (TFD ↔ two-sided black hole); no empirical or simulation benchmarks are provided.  
claimed_feasibility | No claims about preparing TFD on quantum hardware are made in this paper; TFD is discussed purely as a theoretical state.  
limitations_and_open_problems | TFD describes an eternal two-sided black hole and does not model an evaporating one; the TFD example is not directly applicable to one-sided evaporating black holes without additional machinery.  
complexity_or_hardness_arguments | No complexity-theoretic statements about preparing TFD states on quantum devices are made here.  
theory_context_keywords | thermofield double, ER=EPR, two-sided black hole, entanglement, firewall  
citations_to_prior_work | TFD introduced in holography context (ref. [18] ER=EPR and standard literature on TFD and two-sided AdS black holes are cited in the paper).  
  
## Citation

Cite this artifact as `\cite{ast-ext-penington-2026-08-13-2}`.
[code] 
    @misc{ast-ext-penington-2026-08-13-2,
      title        = {Extraction: Entanglement wedge reconstruction and the information paradox},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-entanglement-wedge-reconstruction-and-the-information-paradox.md},
      crossref     = {penington2019entangleme},
      note         = {Theorizer's extraction from \cite{penington2019entangleme}. asta-artifact id: extraction-result-42},
    }
    
    @article{penington2019entangleme,
      title     = {Entanglement wedge reconstruction and the information paradox},
      author    = {Geoffrey Penington},
      year      = {2019},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/160009640},
    }
[/code]
