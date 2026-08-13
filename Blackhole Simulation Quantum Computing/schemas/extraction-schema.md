[<- All artifacts](<../index.md>)

# Extraction Schema

**Contents:**

  * Schema



### Schema

Field | Type | Description  
---|---|---  
target_system_or_model | str | What black-hole-related system/model is being simulated? (e.g., SYK model, JT gravity, AdS/CFT toy model, quantum field theory in curved spacetime, Rindler/Unruh effect analog, spin-chain holography, lattice gauge theory with gravity-inspired features).  
black_hole_phenomena_targeted | str | Which black-hole phenomena/observables are targeted? (e.g., Hawking radiation spectrum, entanglement entropy, Page curve, scrambling/OTOC, information recovery, shockwaves, wormhole teleportation, quasi-normal modes, horizon formation analog, Unruh effect).  
simulation_paradigm | str | Type of simulation/computation used: digital gate-based, analog quantum simulation, hybrid/variational (VQE/QAOA), quantum annealing, tensor-network-assisted quantum computation, error-corrected/FTQC algorithm, or classical-quantum comparison.  
quantum_hardware_platform | str | Hardware platform used or assumed (if any): superconducting qubits, trapped ions, neutral atoms/Rydberg, photonics, spin qubits, NMR, quantum annealer, or 'platform-agnostic'.  
encoding_and_mapping | str | How is the target model mapped to qubits/operations? Include degrees of freedom, discretization (lattice, truncation), fermion-to-qubit mapping (Jordan-Wigner/Bravyi-Kitaev), gauge constraints, boundary conditions, or holographic encoding.  
algorithm_or_protocol | str | Main quantum algorithm/protocol (e.g., Trotterized time evolution, LCU/qubitization, phase estimation, Gibbs-state preparation, teleportation-through-wormhole protocol, measurement of OTOCs, shadow tomography).  
resource_estimates | str | Reported resource requirements: number of qubits, circuit depth/gate counts, T gates, number of measurements/shots, runtime scaling with system size/precision, and any FT overhead assumptions (code distance, logical error rates).  
noise_and_error_mitigation | str | Noise model and mitigation/correction used or discussed: depolarizing/readout errors, dynamical decoupling, ZNE, PEC, symmetry verification, post-selection, fault tolerance assumptions; include quantified error budgets if given.  
key_results_or_demonstrations | str | Core findings: what was successfully simulated/measured, with concise quantitative outcomes where available (e.g., fidelity, correlation functions, entropy estimates, agreement with theory). Include whether it is a proposal, simulation-only, or hardware experiment.  
validation_and_benchmarks | str | How do authors validate correctness? (e.g., comparison to exact diagonalization, semiclassical predictions, conformal limit, known analytic results, finite-size scaling, cross-platform verification).  
claimed_feasibility | str | Statements about feasibility and timeframe: what regime is feasible on NISQ vs requires fault tolerance; identified bottlenecks (depth, measurement cost, noise, state preparation).  
limitations_and_open_problems | str | Explicit limitations/caveats: toy-model nature, finite size, lack of dynamical spacetime, difficulty preparing thermofield double states, sign/complexity barriers, scaling issues, verification limits, ambiguity of 'simulating a black hole'.  
complexity_or_hardness_arguments | str | Any complexity-theoretic claims: BQP-hardness, QMA-hardness, classical intractability arguments, complexity of decoding/holographic reconstruction, or no-go results about efficient simulation/verification.  
theory_context_keywords | str | Key theory framing used by the paper (extract notable terms): AdS/CFT, holographic duality, ER=EPR, quantum error correction in holography, fast scrambling conjecture, firewalls, islands, replica wormholes.  
citations_to_prior_work | str | Notable referenced prior works central to the approach (names/titles if present), especially earlier quantum-simulation proposals for SYK/JT gravity, wormhole teleportation experiments, or algorithms for measuring entanglement/OTOCs.
