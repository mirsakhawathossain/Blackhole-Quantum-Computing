[<- All artifacts](<../index.md>)

# Extraction: Tunneling to Holographic Traversable Wormholes

**Contents:**

  * Holographic simulation of AdS4 traversable wormholes via a coupled-pair-of-CFTs dual to Einstein–Maxwell + charged fermion



### Holographic simulation of AdS4 traversable wormholes via a coupled-pair-of-CFTs dual to Einstein–Maxwell + charged fermion

Field | Value  
---|---  
name_short | Holographic wormhole simulation (proposal)  
name_full | Holographic simulation of AdS4 traversable wormholes via a coupled-pair-of-CFTs dual to Einstein–Maxwell + charged fermion  
brief_description | The paper proposes that nonperturbative quantum-gravity predictions for an AdS4 system (two coupled CFT3s dual to Einstein–Maxwell theory with a charged fermion) can in principle be tested by quantum simulation of the boundary CFTs; it gives concrete gravitational observables (wormhole mass, Casimir energy, tunnelling/nucleation rates) that such simulations could measure and specifies the boundary Hamiltonian that would be simulated.  
citation_title |   
mention_or_use | mention  
target_system_or_model | AdS4/CFT3 holographic system: two coupled CFTs (boundary) dual to 4D Einstein–Maxwell gravity with a charged Dirac fermion (bulk). The bulk geometries of interest are an eternal AdS traversable wormhole, a pair of extremal AdS Reissner–Nordström (RN) black holes, and empty AdS.  
black_hole_phenomena_targeted | Topological transitions between two black holes and a traversable wormhole (nucleation/tunnelling rates), wormhole mass deficit ΔM (Casimir energy effects), nucleation rates/instanton actions, phase structure (which geometry is dominant), correlators/two-point functions sourced by the boundary coupling, and thermodynamic quantities (mass, entropy, free energy, critical temperature).  
simulation_paradigm | platform-agnostic holographic simulation proposal (simulate the boundary coupled CFTs and measure boundary observables to infer bulk processes). The paper does not commit to a specific quantum algorithmic paradigm (no explicit VQE/Trotter/PEA etc. given).  
quantum_hardware_platform | platform-agnostic (the paper only says 'on quantum computers' / 'holographic simulation' in general; no hardware platform specified).  
encoding_and_mapping | Explicit boundary Hamiltonian is provided (eqs. (1) and (88)): H = H_L + H_R - (i h/ℓ) ∫ dΩ2 ( ̅Ψ_-^R Ψ_+^L + ̅Ψ_+^L Ψ_-^R ) + μ(Q_L - Q_R). The target for simulation is the coupled pair-of-CFTs (operators Ψ_{±}^{L,R} dual to the bulk fermion). The paper describes the bulk↔boundary mapping conceptually (AdS/CFT) and provides the precise boundary coupling to be simulated, but it does not provide a concrete qubit encoding (no lattice discretization, fermion-to-qubit mapping, Jordan–Wigner/Bravyi–Kitaev prescription, or finite-volume truncation). Boundary conditions and chemical potential terms are specified; the proposal is to measure boundary correlators/two-point functions and energy to infer bulk stress tensor/Casimir and tunnelling.  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | This is a theoretical proposal (not a quantum-simulation experiment). Concrete gravity results are given that a holographic simulation could test: analytic closed-form expressions (in various limits) for the wormhole mass correction ΔM (eqs. (58),(64),(65),(66)), the shift in fermionic mode frequencies ω_k (eq. (17)) and corresponding Casimir energy (eq. (68)), and tunnelling/nucleation rates: fixed-energy result Γ ∼ exp(−2 S_BH) (eq. (3)) and canonical-ensemble rate Γ(β) ∼ exp(−2 S_BH + 2 β (M_BH − M_o)) (eq. (4)). The paper also provides computed fermion two-point functions (eq. (20)) which are concrete boundary observables that a simulation could measure to reconstruct the bulk stress tensor (eq. (21)).  
validation_and_benchmarks | Validation is internal to the gravity calculation: the paper tests its semiclassical instanton 'recipe' by computing emission rates of thin radiation shells from RN black holes via two independent methods — a probe calculation and a full gravity calculation — and comparing them (sections 4.2.1 and 4.2.2); they also cross-check the Casimir energy via two approaches (point-split stress tensor/backreaction and summing over shifted fermionic frequencies) and find agreement in the regime where each method applies. There is no comparison to any quantum-computation benchmark (no ED, tensor-network numerics, nor hardware results are presented).  
claimed_feasibility | Qualitative claim: 'these non-perturbative results can in principle be tested in a holographic simulation' (Introduction and Summary). The paper notes that microcanonical (fixed-energy) simulations are more natural/feasible for preparing the wormhole phase than canonical (fixed-temperature) because the canonical transition temperature is extremely low and cooling black holes to that regime invalidates semiclassical approximations; however it provides no quantitative resource/timeframe estimates for NISQ or fault-tolerant devices. It also gives parameter-regime constraints needed for semiclassical validity (e.g., large q, small ζ, lower bounds on boundary coupling h so wormhole throat is not too long).  
limitations_and_open_problems | Explicitly stated limitations include: (1) the paper offers only a conceptual proposal for holographic simulation — it does not supply any concrete qubit encoding, discretization, or quantum algorithm; (2) semiclassical approximation breaks down for long wormholes (gives explicit bound on throat length and coupling regimes; see section 2.3); (3) the wormhole requires large q (many lowest-Landau-level fermions) and small ζ for linearized Einstein equations to hold, constraining parameter regimes accessible to simulation; (4) in the canonical ensemble the wormhole is hard to prepare because the critical temperature T_c at which the wormhole begins to dominate is extremely low (below the semiclassical validity bound); (5) backreaction effects important for large black holes are not captured by the pure QFT Casimir calculation (sum-over-frequencies) and require full gravity treatment; (6) no discussion of practical measurement overheads (shot counts), state preparation procedures (e.g., thermofield-double), or verification/encoding complexity — these remain open problems.  
complexity_or_hardness_arguments | None given — the paper does not provide complexity-theoretic statements (no claims of BQP/QMA hardness or formal classical intractability related to simulating the boundary CFTs).  
theory_context_keywords | AdS/CFT, holographic duality, traversable wormholes, Einstein–Maxwell theory, Casimir energy, gravitational instantons, semiclassical gravity, Reissner–Nordström (AdS-RN) black holes, phase diagram (canonical/microcanonical), thermofield-double-like coupled CFTs, negative null energy (ANEC violation).  
citations_to_prior_work | The paper explicitly situates itself among prior works including: (i) the traversable-wormhole construction lineage (Gao, Jafferis and Wall; Maldacena and Qi are referenced in text), (ii) the Maldacena–Milekhin–Popov construction inspiring the NEC-violating mechanism [10], (iii) lower-dimensional SYK/JT gravity studies of wormhole production (refs. [7,8] in the paper), (iv) the original traversable wormhole model used here (ref. [9]), and (v) prior tunnelling-as-Hawking-radiation calculations and thin-wall instanton literature (refs. [13–16], [18–20]). (The paper cites many of these by number in the text; exact bibliographic titles are not printed in the excerpt.)  
  
## Citation

Cite this artifact as `\cite{ast-ext-bintanja-2026-08-13}`.
[code] 
    @misc{ast-ext-bintanja-2026-08-13,
      title        = {Extraction: Tunneling to Holographic Traversable Wormholes},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-tunneling-to-holographic-traversable-wormholes.md},
      crossref     = {bintanja2023tunneling},
      note         = {Theorizer's extraction from \cite{bintanja2023tunneling}. asta-artifact id: extraction-result-18},
    }
    
    @article{bintanja2023tunneling,
      title     = {Tunneling to Holographic Traversable Wormholes},
      author    = {Suzanne Bintanja and Ben Freivogel and A. Rolph},
      year      = {2023},
      url       = {https://www.semanticscholar.org/paper/260378826},
    }
[/code]
