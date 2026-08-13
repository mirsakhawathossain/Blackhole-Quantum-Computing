[<- All artifacts](<../index.md>)

# Extraction: Escape of quantum information across an analogue black hole horizon

**Contents:**

  * Analogue black hole realized via a position-dependent isotropic XY spin chain



### Analogue black hole realized via a position-dependent isotropic XY spin chain

Field | Value  
---|---  
name_short | XY chain BH analogue  
name_full | Analogue black hole realized via a position-dependent isotropic XY spin chain  
brief_description | A (1+1)-D analogue black hole constructed by engineering site-dependent nearest-neighbor XY couplings κ_n that change sign across an effective horizon (metric function f(x) -> κ_n = f([(n-1/2)d])/(4d)), allowing simulation of quantum-field-in-curved-spacetime phenomena such as Hawking-like radiation and Page-curve entanglement dynamics.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime simulated by a discretized (1+1)-D black-hole-like metric mapped to an XY spin chain with site-dependent couplings  
black_hole_phenomena_targeted | Hawking-like particle radiation, entanglement entropy dynamics (Page-curve-like behavior), information transfer across a horizon, transport of entanglement and quantum coherence from interior to exterior  
simulation_paradigm | Classical numerical simulation of unitary many-body dynamics corresponding to a proposed analog quantum simulator; model motivated as an analog quantum simulation platform (analogue quantum simulation proposal / numerics)  
quantum_hardware_platform | Platform-agnostic proposal with explicit mention that parameters are calibrated to be compatible with superconducting-qubit on-chip implementations (superconducting circuits mentioned); no hardware experiment reported in this paper  
encoding_and_mapping | Spatial discretization (lattice) of a (1+1)-D metric with metric function f(x) -> nearest-neighbor hopping/coupling κ_n = f([(n-1/2)d])/(4d); lattice spacing d; horizon located where f(x)=0 so κ_n changes sign (κ<0 inside, κ>0 outside); system–bath split at site n_h with weak coupling κ_c across the horizon; spin-1/2 degrees of freedom (Pauli operators σ^x,σ^y,σ^z) represent the field on lattice sites. No fermion-to-qubit transform (Jordan-Wigner etc.) is discussed because model is directly a spin chain.  
algorithm_or_protocol | Unitary time evolution of the full spin chain via solution of the Liouville–von Neumann (Schrödinger) equation for the total density matrix; observables computed from reduced density matrices (entanglement entropy, concurrence, l1-norm coherence). The paper performs direct numerical time evolution (exact many-body evolution for small chains) rather than gate-level quantum algorithms (no Trotter/LCU/PEA protocols specified).  
resource_estimates | No formal resource-counts for fault-tolerant quantum computation are provided. Numerical examples use chain length L = 10 and lattice spacing d = 2 for plotted results; statement that simulation parameters are 'carefully calibrated to align with existing experimental platforms (superconducting circuits)' but without numerical qubit/gate-depth estimates, measurement counts, or runtime scaling. No T/T-gate, depth, or FT overhead numbers given.  
noise_and_error_mitigation | Not addressed for an actual quantum device; the paper's results are unitary, noiseless numerical simulations. The analogue proposal highlights a weak coupling (small κ_c) near the horizon as a physical regime but does not discuss device noise models, readout errors, error mitigation, or fault-tolerance strategies.  
key_results_or_demonstrations | Numerical demonstration (simulation-only) that an XY spin-chain analogue with κ_n derived from f(x)=β tanh(x) exhibits Page-curve-like entanglement entropy between an interior 'system' and exterior 'bath': early-time linear growth consistent with semiclassical Hawking prediction, a Page-time coinciding with ~half the particle leakage, and subsequent decrease of entanglement toward zero (finite-size residual due to finite bath). Also demonstrated transport of bipartite entanglement (concurrence) and coherence (l1-norm) from interior to exterior; dependence of transmitted quantum resources on initial interior state (examples for α parametrized states, maximally entangled Bell state, and coherent |+⟩ states). Numerical figures use L=10.  
validation_and_benchmarks | Validation by comparison to semiclassical expectation (early-time linear entanglement growth / Hawking prediction) and Page-curve qualitative behavior from Page's analysis; diagnosed Page time by tracking particle-number leakage (Page time when ~half of initial excitations have escaped). The study cites and situates results relative to prior analytic and open-system results (Kehrein, Glatthard) and discusses finite-size effects (nonzero residual entropy attributed to finite bath). No cross-platform experimental validation or gate-level benchmarking is included; numerical methods presumably exact diagonalization / full Schrödinger evolution for small L but not explicitly benchmarked against alternative numerical schemes in the text.  
claimed_feasibility | Authors state the model's simulation parameters are aligned with 'existing experimental platforms, such as superconducting circuits', suggesting near-term laboratory feasibility for analog quantum simulation; they do not provide timelines or explicit NISQ vs fault-tolerant resource thresholds. Identified practical regime feature: weak coupling across horizon (suppressed κ_c) and empty exterior acting as low-temperature bath—conditions considered achievable in many-body quantum simulators.  
limitations_and_open_problems | Explicitly acknowledged: finite-size effects (residual entropy due to finite bath), toy-model nature (1+1D discretized metric, fixed background metric, no backreaction/dynamical spacetime), lack of explicit hardware implementation or device-level noise analysis, no quantitative resource/gate-depth estimates for digital quantum implementations, and idealized initial state preparations. Open problems include scaling to larger baths (thermodynamic limit), implementing on actual hardware with noise, and extending to richer gravitational models (higher dimensions or dynamical gravity/islands).  
complexity_or_hardness_arguments | No complexity-theoretic claims are made (no statements about BQP/QMA hardness or classical intractability); the paper focuses on a constructive mapping and numerical demonstration rather than computational complexity analysis.  
theory_context_keywords | Page curve, Hawking radiation, quantum field in curved spacetime, analogue black hole, system–bath decomposition, entanglement entropy, concurrence, quantum coherence (l1-norm), AdS/CFT (mentioned in intro as context), island rule, semiclassical prediction, finite-size effects  
citations_to_prior_work | References and related works cited in the paper include Page (1993) on Page curve [15]; Kehrein (Page-curve dynamics solvable model) [24]; Glatthard (Page-curve-like entanglement in open systems) [25]; simulation proposals/experiments for curved-spacetime or Hawking-analogue systems such as Shi et al., 'Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole' (Nature Commun. 2023) [39]; Yang et al. 'Simulating quantum field theory in curved spacetime with quantum many-body systems' (Phys. Rev. Res. 2020) [41]; Viermann et al. 'Quantum field simulator for dynamics in curved spacetime' (Nature 2022) [38]; Wang et al. 'Quantum simulation of particle pair creation near the event horizon' (Natl. Sci. Rev. 2020) [36]. The paper cites many context-setting works (Maldacena/AdS-CFT, Hawking, island/wormhole literature) but does not rely on a previously established digital quantum algorithm for the simulation.  
additional_notes | Observables used and reported explicitly: von Neumann entanglement entropy S_ent (system vs bath), local occupation numbers (particle number inside system), concurrence C(ρ_AB) for bipartite entanglement in the bath (outermost qubits), l1-norm coherence C_l1(ρ) for coherence transport, and Bloch-sphere trajectories for local qubits. The horizon is implemented by a sign reversal in κ_n (f(x)=β tanh(x) chosen in examples). Numerical parameter examples: chain length L=10, d=2 (figures).  
  
## Citation

Cite this artifact as `\cite{ast-ext-liu-2026-08-13}`.
[code] 
    @misc{ast-ext-liu-2026-08-13,
      title        = {Extraction: Escape of quantum information across an analogue black hole horizon},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-escape-of-quantum-information-across-an-analogue-black-hole-horizon.md},
      crossref     = {liu2026escape},
      note         = {Theorizer's extraction from \cite{liu2026escape}. asta-artifact id: extraction-result-11},
    }
    
    @article{liu2026escape,
      title     = {Escape of quantum information across an analogue black hole horizon},
      author    = {Zhilong Liu and Wentao Liu and Zehua Tian and Jieci Wang},
      year      = {2026},
      url       = {https://www.semanticscholar.org/paper/285451742},
    }
[/code]
