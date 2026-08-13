[<- All artifacts](<../index.md>)

# Extraction: Qubit models of black hole evaporation

**Contents:**

  * Qubit models of black hole evaporation (discrete pair-creation qubit framework)



### Qubit models of black hole evaporation (discrete pair-creation qubit framework)

Field | Value  
---|---  
name_short | Qubit evaporation framework  
name_full | Qubit models of black hole evaporation (discrete pair-creation qubit framework)  
brief_description | A family of discrete-time toy models that represent black hole evaporation as sequential pair-creation maps on qubits: initial 'internal' (hatted) n-qubit state, each emission adds an entangled pair (one internal hatted qubit and one external/unhatted radiation qubit), with pair-creation operators C_i built from a fixed pair basis |φ_j> and generalized measurement operators ĤP_j satisfying a completeness relation; allows description of both unitary and nonunitary evolutions and analytic study of entanglement growth.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime reduced to qubit toy models of black hole evaporation (discrete pair-creation model on a 'nice slice')  
black_hole_phenomena_targeted | Hawking pair production and Hawking radiation entanglement structure; entanglement entropy growth of emitted radiation (Page-curve behaviour), information loss versus unitary evaporation  
simulation_paradigm | Analytical and classical numerical simulation of discrete qubit toy models (not a gate-model quantum computation protocol) — analysis of quantum operations and entropies in small-n numerical examples  
quantum_hardware_platform | platform-agnostic (no hardware implementation; purely theoretical/toy-model work)  
encoding_and_mapping | Field modes truncated to two-level occupancy (|0>,|1>) mapped to qubits; initial black-hole degrees encoded in n hatted qubits; at step i a new hatted qubit and a new unhatted radiation qubit are appended; pair basis for newly created pair: |φ_1..φ_4> (entangled and product pair states) and creation operator written C_i = Σ_j |φ_j> ⊗ ĤP_j with operators ĤP_j acting on the existing hatted qubits; completeness constraint Σ_j ĤP_j^† ĤP_j = I (isometric mapping condition); purification viewpoint: nonunitary maps expressed as unitary on enlarged auxiliary space (auxiliary ≤ 2n qubits), final physical radiation recovered by tracing out auxiliary qubits  
algorithm_or_protocol | No quantum algorithm; formalism uses operator-sum (Kraus) representation and purification (embedding quantum operations as unitary on auxiliary space), analytic bounding techniques (strong subadditivity of von Neumann entropy), Fannes–Audenaert continuity bound, Gershgorin disk theorem for eigenvalue bounds; numerical simulation of small-n state evolution and computation of Rényi-2 entropies  
resource_estimates | Analytic model parameter: initial n black-hole qubits; at intermediate step i total Hilbert-space dimension corresponds to n+i unhatted + n+i hatted (enlarged accounting) so enlarged space up to 3n qubits by final step, with 2n auxiliary hatted qubits to be traced out. Numerical experiments in paper limited to small n (examples with n≈5); no circuit/gate counts, no runtime complexity for gate-model quantum hardware provided.  
noise_and_error_mitigation | Not applicable — paper presents idealized, noise-free theoretical models and classical numerical calculations; no noise model or mitigation strategies discussed for quantum hardware.  
key_results_or_demonstrations | 1) Unified formalism to express many existing toy models (Hawking model, burning-paper/unitary models, Mathur/Plumberg variants) in common notation C_i = Σ |φ_j> ⊗ ĤP_j. 2) Generalization of Mathur's bound: if ||C_i - C_i^H|| < ε (<1) then the marginal increase of radiation entanglement ΔS_i satisfies ΔS_i ≥ log 2 - k_ε, with k_ε positive and k_ε → 0 as ε → 0; asymptotically k_ε ∼ O(-ε log ε) (paper gives bound k_ε ≲ -9 ε log ε for small ε). 3) Construction of a one-parameter family of interpolating models (parameter θ) continuously deforming Hawking model (θ=0) to a manifestly unitary, nonlocal model (θ=π/2), with operator-norm distance ||C - C^H|| = 2|sin(θ/2)|. 4) Numerical small-n calculations of second Rényi entropies as function of θ illustrating that small deviations from Hawking do not produce turnover in entropy (no Page-curve) — only large deformations produce unitary-like rise-and-fall.  
validation_and_benchmarks | Analytical validation using information-theoretic inequalities: strong subadditivity, Audenaert's generalization of Fannes' inequality to bound entropy differences, Gershgorin's theorem to control eigenvalue perturbations; benchmark comparisons are conceptual: results compared to Hawking baseline (C^H), and to Page expectations for unitary evaporation; numerical validation limited to small n (explicit plots of Rényi-2 for specific initial states) to illustrate qualitative behaviour.  
claimed_feasibility | No claim of physical quantum-simulation feasibility on NISQ or fault-tolerant hardware — the work is theoretical/toy-model; numerical examples limited to small n due to classical computational cost; paper emphasizes that making the required 'large' corrections physically plausible in actual gravitational systems remains a major conceptual challenge.  
limitations_and_open_problems | Explicitly stated limitations: toy-model nature (modes truncated to 0/1 occupation), absence of dynamical spacetime/backreaction beyond parametrized ĤP_j choices, ambiguity in identifying auxiliary degrees of freedom at intermediate steps, small-size numerics (n small), models can be nonlocal (information transfer may require nonlocal dynamics or fuzzball-like microstructure), energy/conservation-law implementation not addressed in detail (caveated), many large corrections do not guarantee unitarity, and the physical mechanism to produce the order-unity corrections near the horizon remains unresolved.  
complexity_or_hardness_arguments | No computational-complexity theorems (BQP/QMA) are asserted. The paper's 'hardness' type statement is physical: small corrections to local pair-creation dynamics cannot accumulate to restore unitarity (an information-theoretic no-go), but it is not framed as computational complexity.  
theory_context_keywords | Hawking radiation; entanglement entropy; Page curve; Mathur's bound (small-correction theorem); operator-sum (Kraus) representation; purification/auxiliary Hilbert space; nice-slicing of Schwarzschild; fuzzball proposal; nonlocality; scrambling; burning-paper toy models; Rényi-2 entropy; strong subadditivity; semiclassical approximation.  
citations_to_prior_work | References (as cited in the paper): Hawking [1] (original Hawking calculation), Page [8] (Page curve arguments), Mathur [10] (Mathur's bound on small corrections), Giddings [12] (unitary models), Mathur & Plumberg [13], Mathur [15] (Ising toy model), and review/related discussions [11-15, 20-24, 28-32] mentioned in-text; the paper places its results in direct dialogue with Mathur's earlier work and with several unitary 'burning paper' toy models.  
  
## Citation

Cite this artifact as `\cite{ast-ext-avery-2026-08-13}`.
[code] 
    @misc{ast-ext-avery-2026-08-13,
      title        = {Extraction: Qubit models of black hole evaporation},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-qubit-models-of-black-hole-evaporation.md},
      crossref     = {avery2011qubit},
      note         = {Theorizer's extraction from \cite{avery2011qubit}. asta-artifact id: extraction-result-84},
    }
    
    @article{avery2011qubit,
      title     = {Qubit models of black hole evaporation},
      author    = {Steven G. Avery},
      year      = {2011},
      url       = {https://www.semanticscholar.org/paper/54967526},
    }
[/code]
