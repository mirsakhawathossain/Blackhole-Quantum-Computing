[<- All artifacts](<../index.md>)

# Extraction: Models for unitary black hole disintegration

**Contents:**

  * Effective Hilbert-space qubit model for unitary black hole evaporation



### Effective Hilbert-space qubit model for unitary black hole evaporation

Field | Value  
---|---  
name_short | Qubit toy model for BH evaporation  
name_full | Effective Hilbert-space qubit model for unitary black hole evaporation  
brief_description | An abstract, platform-agnostic quantum-information toy model that represents the black hole internal and external Hilbert spaces as strings of qubits and models evaporation as discrete-time unitary maps that create entangled pairs and (in modified rules) relay internal qubits to the exterior to restore unitarity while minimally relaxing locality.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime (Schwarzschild black hole) represented by an effective Hilbert-space decomposition into internal (Ĥ) and external (H) degrees of freedom and mapped to strings of qubits; modes described using a wavepacket basis (eq. 2.5) with frequency ~1/R.  
black_hole_phenomena_targeted | Hawking pair production / Hawking radiation, entanglement between interior and exterior, information transfer (black hole information recovery), Page-time/evaporation time scaling (T_evap ~ R S_BH), and modeling of scrambling/retention time T_r.  
simulation_paradigm | platform-agnostic theoretical qubit-model / abstract quantum-information model (discrete time-step unitary maps); not presented as an implementation on a particular quantum simulator or gate model.  
quantum_hardware_platform | platform-agnostic (no specific hardware assumed or used)  
encoding_and_mapping | Internal Hilbert space Ĥ and external Hilbert space H are each represented as bases of strings of qubits (occupation numbers of wavepacket modes). A wavepacket basis (eq. 2.5) with choice ε ≳ 1/R, keeping k=1 (ω≈1/R) and occupation numbers 0/1, is used to coarse-grain field modes into qubits; time evolution proceeds in steps δt ~ R. Entangled horizon pairs are represented as 1/√2(|ĥ0⟩|0⟩ + |ĥ1⟩|1⟩) until a transition/relay occurs. No fermion-to-qubit mapping, gauge constraints, lattice discretization, or boundary-condition prescriptions for hardware implementation are given—this is an abstract information-theoretic mapping.  
algorithm_or_protocol | Discrete time-step unitary update rules (eq. 2.6 for Hawking evolution; modified unitary maps eqs. 3.1–3.3 for unitary nonlocal evolution). Models include: (a) standard pair-creation update producing entangled interior-exterior qubit pairs; (b) modified maps that erase/relay one internal qubit per time-step to the exterior (unitary information transfer); (c) variants with random/unitary scrambling (fast-scrambling modeled by random Ĥ unitaries) and parameters controlling retention time T_r. No gate-level algorithms (Trotterization, LCU, phase estimation, etc.) are specified.  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Proposes concrete unitary toy evolutions that (i) preserve unitarity by relaying one qubit of information per time-step from the interior to the exterior, (ii) parameterize minimal nonlocal departures from LQFT localized to modes of wavelength ~R and energy ~1/R per emission, and (iii) introduce a retention time T_r and evaporation time scaling T_evap ~ R S_BH. These are theoretical constructions/proposals (not numerical simulations or hardware experiments).  
validation_and_benchmarks | Conceptual validation by comparison to semiclassical Hawking evolution: (a) baseline Hawking evolution is eq. 2.6 producing thermal mixed state when tracing interior (Hawking's argument); (b) modified maps (3.1–3.3) are argued to reproduce desired features (e.g., same average outward flux in some variants) while enabling information recovery. No numerical benchmarks, exact-diagonalization, or quantum-hardware validation are provided.  
claimed_feasibility | No claims about direct implementation on NISQ or fault-tolerant quantum hardware; models are presented as theoretical toy models to guide thinking about nonlocal unitary evolution. The paper notes model-dependence and that these are minimal nonlocal modifications rather than proposals for experimental quantum simulation.  
limitations_and_open_problems | Explicitly noted limitations: toy-model nature (abstract qubit encoding, coarse-graining), lack of dynamical spacetime degrees of freedom, departure from local QFT (necessity of some nonlocality), ambiguity in choice of Ĥ and U (many possible unitary choices), no concrete mapping to physical quantum hardware or resource counts, problems with perturbative LQFT on 'nice slices', and open questions about microscopic principles that would produce such maps; also the timing/scale of deviations (e.g. whether they appear early or near Page time) is model-dependent.  
complexity_or_hardness_arguments | No formal complexity-theoretic proofs (e.g., BQP/QMA hardness) are provided. The paper references fast-scrambling behavior and models Ĥ as random unitaries to capture scrambling dynamics (Hayden–Preskill, Sekino & Susskind), but does not assert computational complexity statements about simulatability or decoding.  
theory_context_keywords | Hawking radiation, Bekenstein-Hawking entropy, black hole information paradox, nonlocality vs. complementarity, fast-scrambling, retention time T_r, evaporation time T_evap ~ R S_BH, nice slicing, fuzzballs, remnants, semiclassical LQFT, entangled pair production, unitarity-restoring evolution  
citations_to_prior_work | Hawking 1975 (particle creation by black holes) [1]; Page (information in black hole radiation) [14]; Hayden & Preskill (black holes as mirrors; fast information retrieval) [16]; Mathur (information paradox and fuzzballs) [7,30]; Braunstein & Zyczkowski / Braunstein & Patra (information-theoretic approaches) [17]; Sekino & Susskind (fast scramblers) [28]; Horowitz & Maldacena (final-state proposal) [26]; Giddings earlier works on nonlocality and locality in quantum gravity [11-13]; Czech et al. "Black Holes as Rubik's Cubes" [18].  
  
## Citation

Cite this artifact as `\cite{ast-ext-giddings-2026-08-13}`.
[code] 
    @misc{ast-ext-giddings-2026-08-13,
      title        = {Extraction: Models for unitary black hole disintegration},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-models-for-unitary-black-hole-disintegration.md},
      crossref     = {giddings2011models},
      note         = {Theorizer's extraction from \cite{giddings2011models}. asta-artifact id: extraction-result-81},
    }
    
    @article{giddings2011models,
      title     = {Models for unitary black hole disintegration},
      author    = {S. Giddings},
      year      = {2011},
      url       = {https://www.semanticscholar.org/paper/73549087},
    }
[/code]
