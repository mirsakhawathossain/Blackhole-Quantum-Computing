[<- All artifacts](<../index.md>)

# Extraction: Replica wormholes and the black hole interior

**Contents:**

  * Quantum-computer simulation of black-hole amplitudes to implement the Petz map for entanglement-wedge reconstruction



### Quantum-computer simulation of black-hole amplitudes to implement the Petz map for entanglement-wedge reconstruction

Field | Value  
---|---  
name_short | Petz-map quantum simulation (conceptual)  
name_full | Quantum-computer simulation of black-hole amplitudes to implement the Petz map for entanglement-wedge reconstruction  
brief_description | A conceptual proposal/usage in this paper where a (platform-agnostic) quantum computer is imagined to simulate the black-hole system B (compute amplitudes ⟨ψ_i|ψ_j⟩) so as to build the Petz-map reconstruction operator acting only on the radiation system R; the gravitational path integral with replica wormholes is used to argue this procedure reconstructs interior operators in the post-Page (connected-wormhole) phase.  
citation_title | here  
mention_or_use | use  
target_system_or_model | The simple JT gravity model with an End-Of-the-World (EOW) brane behind the horizon (two-dimensional JT gravity toy model used throughout section 2) — the construction is also discussed in the context of more general bulk field excitations and conceptually related to the SYK model discussed in section 5.  
black_hole_phenomena_targeted | Entanglement-wedge reconstruction / information recovery from Hawking radiation, Page transition / Page curve, non-orthogonality of black-hole microstates (small overlaps induced by replica wormholes), and explicit insertion/reconstruction of bulk operators behind the horizon.  
simulation_paradigm | Conceptual universal quantum computation / quantum simulation (platform-agnostic) used to compute amplitudes of the black-hole theory in order to construct a Petz-map-like operator on the radiation; the paper does not frame this as a specific NISQ or fault-tolerant protocol.  
quantum_hardware_platform | platform-agnostic (no specific hardware platform is assumed or analyzed).  
encoding_and_mapping | Not specified in the paper. The paper only states at a conceptual level that the quantum computer would compute gravitational amplitudes ⟨ψ_{ai}|ψ_{bj}⟩ (i,j label EOW-brane internal states, a,b label bulk-field code states), which implicitly requires an encoding of black-hole microstates, brane internal states, and bulk-field excitations into the quantum computer; no discretization, fermion mapping, gauge constraint handling, or holographic encoding is provided.  
algorithm_or_protocol | Not specified concretely. The described operation is: the quantum computer evaluates the same inner-product amplitudes that appear in the gravitational path integral so that one can form the partial-trace / Petz (or 'Petz Lite') operator on R (see eqs. (3.7)–(3.11)). No explicit quantum algorithms (e.g. Trotterization, LCU, phase estimation, tomography, shadow estimation) are given.  
resource_estimates | No resource estimates are provided in the paper — there are no numbers for qubits, gate counts, circuit depth, measurement shot counts, T-gate counts, or fault-tolerance overheads.  
noise_and_error_mitigation | Not discussed. The paper does not include a noise model, error-mitigation strategies, or quantified error budgets for the imagined quantum computation.  
key_results_or_demonstrations | This is a theoretical/conceptual demonstration: by computing gravitational path integrals (with replica wormholes) for matrix elements of the Petz-map-type reconstruction operator, the authors show that in the post-Page (connected replica-wormhole) phase the Petz reconstruction matrix elements computed via the simulated amplitudes agree with the original bulk operator matrix elements — i.e. operators behind the horizon can be reconstructed on R. This is not an actual quantum simulation experiment nor a classical emulation; it is a gravity-path-integral/replica-based argument that a simulation of B amplitudes could realize Petz reconstruction.  
validation_and_benchmarks | Validation is gravitational/theoretical: matrix elements of the proposed R-operator are evaluated using gravitational path integrals with and without replica-wormhole topologies, and compared to the expected bulk operator matrix elements and to the island/island-formula (EW/QES) results. The paper uses consistency with the island prescription, the replica trick, and semiclassical expectations as validation; there is no numerical quantum-hardware benchmarking or exact-diagonalization cross-check of a quantum-simulation implementation.  
claimed_feasibility | No concrete feasibility statement for quantum-hardware implementation is given. The discussion is at the conceptual level: the quantum computer is an abstract device that can compute the amplitudes needed to construct the Petz map. The paper does not claim this is feasible on NISQ devices nor estimate the resources needed for fault-tolerant implementation.  
limitations_and_open_problems | Explicit limitations noted in the paper include: (1) the 'quantum computer' is only a conceptual tool in the argument — no mapping or algorithmic detail is given; (2) the gravitational path integral appears to compute ensemble-averaged quantities (factorization/ensemble issues) which complicates the interpretation of reconstructed operators in a single theory; (3) state-dependence and code-subspace-size limits: reconstruction error grows with code-subspace dimension, so only sufficiently small code subspaces can be reconstructed reliably (state dependence/Hayden-Preskill-related limitation); (4) no dynamical quantum-gravity evolution or full spacetime dynamics are simulated — the argument uses Euclidean path integrals and replica geometries rather than real-time unitary simulation; (5) no practical verification recipe for an experimental quantum simulation is provided.  
complexity_or_hardness_arguments | No formal complexity-theoretic statements (e.g., BQP- or QMA-hardness) are given for performing the required simulations. The paper does invoke concepts related to decoding complexity and information recovery (citing Hayden-Preskill) and emphasizes that reconstruction has a code-subspace-size-dependent error (which ties into discussions of decoding difficulty), but it does not present rigorous complexity-class claims about simulating black-hole amplitudes or performing the Petz reconstruction.  
theory_context_keywords | JT gravity, EOW branes, replica wormholes, island formula, Page curve, entanglement wedge reconstruction, Petz map, entanglement entropy, semiclassical gravitational path integral, SYK (UV-complete example), ensemble averaging/factorization problem, Hayden-Preskill/decoding, state dependence.  
citations_to_prior_work | The discussion builds on the Petz map literature [refs. cited in paper as 41,42], Hayden-Preskill decoding arguments [47], the island/RT/QES literature (Ryu-Takayanagi, Engelhardt-Wall, earlier island proposals [13-16]), and references about replica wormholes and spectral form factor wormholes [24,25]; the SYK model analysis is referenced in section 5. The paper also mentions closely related independent work by Almheiri, Hartman, Maldacena, Shaghoulian and Tajdini [49]. (Reference numbers correspond to those used in the paper.)  
  
## Citation

Cite this artifact as `\cite{ast-ext-penington-2026-08-13}`.
[code] 
    @misc{ast-ext-penington-2026-08-13,
      title        = {Extraction: Replica wormholes and the black hole interior},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-replica-wormholes-and-the-black-hole-interior.md},
      crossref     = {penington2019replica},
      note         = {Theorizer's extraction from \cite{penington2019replica}. asta-artifact id: extraction-result-14},
    }
    
    @article{penington2019replica,
      title     = {Replica wormholes and the black hole interior},
      author    = {Geoff Penington and S. Shenker and D. Stanford and Zhenbin Yang},
      year      = {2019},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/208309801},
    }
[/code]
