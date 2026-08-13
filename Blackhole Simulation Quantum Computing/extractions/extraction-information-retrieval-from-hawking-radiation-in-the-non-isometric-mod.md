[<- All artifacts](<../index.md>)

# Extraction: Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation

**Contents:**

  * Quantum simulation of decoding Hawking radiation in the non-isometric model of black hole interior (modified Hayden-Preskill)



### Quantum simulation of decoding Hawking radiation in the non-isometric model of black hole interior (modified Hayden-Preskill)

Field | Value  
---|---  
name_short | Non-isometric HP QSim (this paper)  
name_full | Quantum simulation of decoding Hawking radiation in the non-isometric model of black hole interior (modified Hayden-Preskill)  
brief_description | This work implements and analyses decoding protocols (Yoshida–Kitaev probabilistic decoding and a Grover-like deterministic decoding) for a modified Hayden–Preskill thought experiment built from the AEHPV non-isometric holographic map; the authors both derive analytic formulas for projection probability and decoding fidelity (Haar-averaged) and perform proof-of-principle experiments on 7-qubit IBM superconducting quantum processors to validate the theory.  
citation_title | Information retrieval from Hawking radiation in the non-isometric model of black hole interior: theory and quantum simulations  
mention_or_use | use  
target_system_or_model | Non-isometric holographic model of black hole interior (AEHPV-style non-isometric map combined with final-state/post-selection dynamics) used in a modified Hayden–Preskill evaporation thought experiment  
black_hole_phenomena_targeted | Information recovery from Hawking radiation; Page curve / Page transition; entanglement entropy (Renyi and von Neumann via island formula); scrambling of interior modes and transmission-channel transition at Page time  
simulation_paradigm | Digital gate-based quantum experiments on NISQ (proof-of-principle circuits implemented on IBM 7-qubit processors); analytic Haar-average calculations for random scrambling unitaries underpin the theory  
quantum_hardware_platform | superconducting qubits (IBM 7-qubit processors) for experiments; theory/results otherwise platform-agnostic  
encoding_and_mapping | Effective interior Hilbert space (l, f, r, message A) is modeled as finite-dimensional qudits; mapping to fundamental description realized by applying a scrambling unitary U on input systems (A,f,r) and projecting an auxiliary subsystem P onto a fixed state (post-selection) to realize the non-isometric map V = sqrt(|P|) <0|_P U |psi0>_f. In experiments the roles of EPR pairs, copies of EPR (for reference and prepared systems), and explicit circuits for U and its complex conjugate U* are implemented; the decoding teleports the message to a prepared register via projection onto EPR pairs (post-selection). (No detailed fermion mappings, lattices, or continuum discretization are used — the model is finite-dimensional/qudit toy model.)  
algorithm_or_protocol | Yoshida–Kitaev probabilistic decoding (prepare copies, apply U* as time-reversal, project R' & R'' onto EPR and post-select) and a Grover-like decoding strategy (use an additional projector ~tPi and Grover iterations to amplify success probability); analytical evaluation uses Haar averages and Weingarten functions to compute projection probability P_EPR and decoding fidelity F_EPR.  
resource_estimates | Reported experimental resource: demonstration on IBM 7-qubit devices. Theoretical resource formulas expressed in Hilbert-space dimensions (|A|, |f|, |r|, |B|, |P|, |R'|). No explicit gate counts, circuit depths, T-count, number of shots, or fault-tolerance overhead numbers are provided in the text excerpt; normalization constant C and success probability scale with these subsystem dimensions (e.g., P_EPR ~ min(1, |P|/(|f||A|^2)) under decoupling approximations).  
noise_and_error_mitigation | Paper reports runs on IBM NISQ hardware but the provided text does not specify a detailed noise model or explicit error-mitigation techniques; the decoding protocol uses post-selection (projection onto EPR pairs) which acts as probabilistic filtering. No quantified error budgets or error-correction/fault-tolerant assumptions are given in the excerpt.  
key_results_or_demonstrations | Analytical: derived Haar-averaged expressions for normalization, Renyi entropies (showing island/quantum-extremal-surface-like min formula), decoupling condition (|R'| >> sqrt(|f|/|P|) |A|), projection probability P_EPR and decoding fidelity F_EPR; identified a transition in information transmission channels at Page time via behavior of P_EPR. Experimental: performed proof-of-principle tests of both probabilistic (Yoshida–Kitaev) and Grover-like decoding strategies on 7-qubit IBM processors and report validation of analytical findings and feasibility of retrieving information in the non-isometric toy model. (The excerpt does not list numerical fidelities or raw experimental statistics.)  
validation_and_benchmarks | Validation is done by comparing experimental outcomes to the paper's analytic predictions computed via Haar averages (Weingarten calculus) and to the derived decoupling condition; the Page-time transition is identified by analytical formulas and illustrated numerically (plots of P_EPR vs subsystem dimensions) and then tested experimentally on small (7-qubit) hardware. No explicit cross-platform or exact-diagonalization benchmarks are described in the provided excerpt, though analytical averages serve as the theoretical benchmark.  
claimed_feasibility | Authors claim feasibility of recovering information in this non-isometric toy model on current small-scale superconducting quantum processors (demonstrated on IBM 7-qubit devices). They also emphasize assumptions required: outside decoder must know the interior dynamics (the scrambling unitary U). Large-scale, high-fidelity recovery for realistic black-hole-sized Hilbert spaces would require scaling beyond NISQ; the paper presents the experiments as proof-of-principle only.  
limitations_and_open_problems | Explicit limitations in the text include: toy finite-dimensional model (not a dynamical gravitational simulation), small system sizes in hardware experiments, reliance on full knowledge of the interior dynamics (U) by the decoder, reliance on post-selection (probabilistic step) unless resource-intensive Grover amplification is used, and use of Haar-typical random unitaries rather than dynamics derived from a specific gravitational Hamiltonian. The approach does not simulate spacetime or semiclassical gravity directly and uses non-unitary post-selection to represent the non-isometric map.  
complexity_or_hardness_arguments | Discussion-level complexity points: decoding requires the decoder to know the scrambling unitary; Yoshida–Kitaev decoding and Grover amplification are used to make decoding efficient in toy settings. The paper invokes quantum computational complexity as motivation for holographic models (scrambling complexity), but no formal proof (e.g., BQP/QMA hardness) is given in the provided excerpt. The need for exponential Hilbert-space dimensions for macroscopic black holes implies classical intractability in the large-size limit, motivating quantum protocols.  
theory_context_keywords | AEHPV non-isometric holographic map, final-state/post-selection model, Hayden–Preskill thought experiment, Yoshida–Kitaev decoding, Grover search, scrambling unitary, EPR projection, decoupling condition, Page curve, island formula, Weingarten functions, Haar-average, quantum error correction in holography, fast scrambling  
citations_to_prior_work | Paper builds on and cites Hayden–Preskill (decoding Hawking radiation), AEHPV non-isometric holographic model of black hole interior, Yoshida & Kitaev decoding strategy, Horowitz–Maldacena final-state proposal, island rule/quantum extremal surface literature, and works on interactions of infalling agents such as Kim & Preskill; the provided excerpt lists these by reference numbers (e.g., [1],[9],[10],[36],[17-21],[25]) but does not include full bibliographic titles in the excerpt.  
  
## Citation

Cite this artifact as `\cite{ast-ext-li-2026-08-13}`.
[code] 
    @misc{ast-ext-li-2026-08-13,
      title        = {Extraction: Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-information-retrieval-from-hawking-radiation-in-the-non-isometric-mod.md},
      crossref     = {li2023informatio},
      note         = {Theorizer's extraction from \cite{li2023informatio}. asta-artifact id: extraction-result-17},
    }
    
    @article{li2023informatio,
      title     = {Information retrieval from Hawking radiation in the non-isometric model of black hole interior: Theory and quantum simulation},
      author    = {Ran Li and Xuanhua Wang and Kun Zhang and Jin Wang},
      year      = {2023},
      journal   = {Physical Review D},
      url       = {https://www.semanticscholar.org/paper/259341708},
    }
[/code]
