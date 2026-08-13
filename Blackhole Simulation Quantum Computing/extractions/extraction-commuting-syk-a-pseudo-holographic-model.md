[<- All artifacts](<../index.md>)

# Extraction: Commuting SYK: a pseudo-holographic model

**Contents:**

  * Commuting SYK model (q-local bi-fermion X_i construction)
  * Traversable wormhole teleportation protocol (two-sided coupling e^{-i μ V})
  * N = 7 sparse SYK 5-term learned Hamiltonian (Google Sycamore experiment, referenced)
  * Size-winding property of operator growth (phase linear in operator size)



### Commuting SYK model (q-local bi-fermion X_i construction)

Field | Value  
---|---  
name_short | Commuting SYK  
name_full | Commuting SYK model (q-local bi-fermion X_i construction)  
brief_description | A q-local SYK-like model built from commuting bosonic bilinears X_i = psi_{2i-1} psi_{2i} (each X_i conserved), ensemble-averaged over Gaussian couplings; integrable, solvable after averaging and analyzed at arbitrary N and large-N.  
citation_title | here  
mention_or_use | use  
target_system_or_model | SYK-like model (commuting q-local generalization of the Sherrington–Kirkpatrick model formulated with Majorana fermions and X_i = psi_{2i-1} psi_{2i})  
black_hole_phenomena_targeted | Analogues of holographic phenomena: operator growth/size distribution and size-winding, scrambling (OTOCs), and applicability of the traversable-wormhole teleportation protocol (ER=EPR style test).  
simulation_paradigm | Theoretical/analytical ensemble-averaged calculation and numerical exact small-N evaluation (no hardware implementation in this paper); saddle-point approximations for large-N.  
quantum_hardware_platform | platform-agnostic (theoretical work); paper comments on small-N hardware experiments in the literature but does not run hardware itself.  
encoding_and_mapping | Majorana fermions grouped pairwise into commuting bosonic operators X_i = psi_{2i-1} psi_{2i} with eigenvalues ±i/2; Hamiltonian H = sum_I J_I X_{i1}...X_{i_{q/2}} (q multiple of 4) so that every term commutes; two-sided construction uses thermofield-double (TFD) / EPR state and size operator S = N/2 + sum_j i psi_j^l psi_j^r; mapping to operator-size basis Γ_I^r of right system used to define coefficients c_I(t) and generating functions K_μ, G_μ.  
algorithm_or_protocol | Analytic computations of time-evolution and correlators by exact exponentiation of commuting terms, ensemble averaging of Gaussian couplings, analytic continuation τ→it to get real-time dynamics; computation of generating functions K_μ(t) and G_μ(t) to obtain size distribution P_n(t) and average phase sums Q_n(t); saddle-point evaluation in large N; application of the traversable-wormhole teleportation protocol (prepare TFD, insert operator, apply two-sided coupling e^{-i μ V}, measure return correlator).  
resource_estimates | The paper presents no gate-level or explicit hardware resource estimates. It analyzes large-N analytically (scaling behavior) and presents small-N numerics (examples N=8 and N up to 100 in analytic/saddle plots); it references a prior small-N hardware demonstration using an N=7 learned 5-term Hamiltonian but provides no circuit depths or shot counts.  
noise_and_error_mitigation | Not applicable to the analytic calculations; no noise model or error-mitigation protocol is introduced for hardware. Theoretical results assume exact unitary dynamics and ensemble averaging.  
key_results_or_demonstrations | 1) Shows the commuting SYK model is non-holographic by spectrum (Gaussian), two-point function (Gaussian decay with oscillatory phase ~ J^2 β), and four-point/OTOC (slow-scrambling f(t) ∼ t^2). 2) Despite non-holographic status, the model exhibits near-perfect size-winding in high temperature and large-N regimes (average phase of Q_n linear in n and ratio r_n = |Q_n|/P_n ≈ 1 for relevant regimes). 3) Size distribution in this model is narrowly peaked (peaked-size mechanism) rather than broadly distributed as in holographic SYK; teleportation in large-N is governed primarily by peaked-size + thermalization rather than pure size-winding. 4) Application of the traversable-wormhole teleportation protocol in this model shows teleportation-like signals with parameter-regime-dependent features (sign of μ, signal ordering) and identifies the roles of thermalization and peaked-size effects.  
validation_and_benchmarks | Validation is via: exact ensemble-averaged analytic expressions (closed-form sums), saddle-point approximations (large-N), and small-N exact numerical evaluations (comparison of exact sums to saddle approximations shown in figures for N=100 and N=8). Comparisons are made against known behaviors of ordinary (non-commuting) SYK (e.g., exponential scrambling and spectral edge behavior) to highlight differences. No hardware cross-check performed in this paper; qualitative comparison/discussion with a prior small-N hardware simulation is provided.  
claimed_feasibility | Authors state small-N, sparse or learned Hamiltonians (e.g., the N=7 5-term case referenced) can display wormhole-like teleportation signatures accessible on near-term hardware, but emphasize that commuting, integrable Hamiltonians are not true gravitational duals and that full holographic behavior (large-N, non-commuting SYK) remains out of reach for current hardware without substantial increases in complexity and non-commutativity.  
limitations_and_open_problems | Explicit limitations: (i) model integrable and non-holographic (Gaussian density of states, no √E edge), (ii) slow-scrambling (quadratic OTOC growth), (iii) size-winding occurs only in particular regimes (high-T, large-N, near scrambling time) and is accompanied by a narrowly peaked size distribution unlike holographic SYK, (iv) ensemble-average / self-averaging approximations used and valid only above spin-glass temperature T_c, (v) small-N behavior differs qualitatively and requires thermalization interplay, (vi) many experimentally relevant questions remain such as preparing accurate TFD states, scaling beyond small learned Hamiltonians, and distinguishing genuine holographic dynamics from pseudo-holographic signatures.  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness claims made for quantum simulation of this commuting model; analytically tractable because of integrability and ensemble averaging. The paper contrasts slow (polynomial) operator growth with the exponential fast-scrambling conjecture for holographic systems, implying qualitatively easier classical simulability in many regimes.  
theory_context_keywords | SYK model, commuting SYK, Sherrington–Kirkpatrick generalization, thermofield double (TFD), ER=EPR, traversable wormhole teleportation, size distribution, size-winding, operator growth, OTOC, scrambling time, saddle-point, ensemble average, near-AdS2/Schwarzian (discussed by contrast).  
citations_to_prior_work | References (by citation numbers used in the paper): foundational SYK papers [1,2], traversable-wormhole teleportation protocol [14], size-winding literature [11,12], 'quantum gravity in the lab' motivation [10-12], sparse SYK analyses [16,17], the small-N hardware learned Hamiltonian experiment [18], debates on commuting learned Hamiltonian [19,20], SK model literature [21-23].  
  
### Traversable wormhole teleportation protocol (two-sided coupling e^{-i μ V})

Field | Value  
---|---  
name_short | Traversable wormhole teleportation  
name_full | Traversable wormhole teleportation protocol (two-sided coupling e^{-i μ V})  
brief_description | Protocol that prepares two copies of a system in a thermofield-double-like entangled state, injects an input operator into one side, turns on a two-sided coupling V = i sum_j psi_j^l psi_j^r with sign-tuned strength μ, and measures the recovery/teleportation at the other side—diagnosed by two-sided correlators.  
citation_title |   
mention_or_use | use  
target_system_or_model | Two-sided commuting SYK models in thermofield-double (TFD) / EPR state; analysis also compared to ordinary (non-commuting) SYK where protocol is dual to traversable wormhole.  
black_hole_phenomena_targeted | Operational test of ER=EPR by producing a traversable wormhole analog and observing teleportation/fidelity, causal connection between two sides, signal ordering, and sign-of-μ effects analogous to gravitational backreaction.  
simulation_paradigm | Protocol is applied analytically/theoretically in the commuting-SYK model (no new hardware implementation in this paper); authors analyze resulting correlators and teleportation signatures using ensemble averages and saddle methods; the protocol has been implemented experimentally in prior small-N work referenced.  
quantum_hardware_platform | platform-agnostic in this paper; prior referenced implementation used superconducting qubit processor (Google Sycamore) but this paper itself performs analytic and small-N numerical study.  
encoding_and_mapping | Two copies of the commuting SYK, TFD constructed as ρ_r^{1/2}|0⟩ with EPR condition ψ_j^l + i ψ_j^r |0⟩ = 0; coupling V = i sum_j ψ_j^l ψ_j^r; size operator S = N/2 + V used to analyze operator-size-based mechanisms.  
algorithm_or_protocol | Prepare TFD, evolve operator ψ_j^r(t), apply e^{-i μ V} coupling (or e^{-μ V} in generating functions), measure two-sided correlators such as ⟨ψ_l(-t) e^{-i μ V} ψ_r(t)⟩ to infer teleportation fidelity; compute size generating functions K_μ and G_μ, and P_n/Q_n to analyze mechanisms.  
resource_estimates | Paper provides no low-level resource costs; references a prior small-N experimental demonstration with an N=7 5-term Hamiltonian (no gate counts provided here).  
noise_and_error_mitigation | Not analyzed in this theoretical work; noise and mitigation discussed in referenced experimental papers but not detailed here.  
key_results_or_demonstrations | Applied the teleportation protocol to commuting SYK and found wormhole-like teleportation signatures in several parameter regimes; demonstrated that teleportation success in large-N/high-T arises mainly from a peaked-size mechanism (narrow size distribution) supplemented by thermalization and partial size-winding; for early times and small N the interplay between size-winding and thermalization determines optimal μ and ordering preservation.  
validation_and_benchmarks | Validation via analytic ensemble-averaged expressions, saddle approximations and explicit small-N numerics; comparison (conceptual/qualitative) to known results from ordinary SYK and prior experimental implementations.  
claimed_feasibility | Authors suggest small-N/sparse learned Hamiltonians can exhibit teleportation signals and are accessible to near-term devices (as in referenced experiments), but emphasize that reproducing genuine semiclassical gravitational behavior requires larger, non-commuting Hamiltonians and remains beyond near-term capability.  
limitations_and_open_problems | Main caveats: need for accurate TFD preparation, commuting learned Hamiltonians may not capture true holographic dynamics, teleportation in commuting SYK can be driven by non-holographic mechanisms (peaked-size, thermalization), and scaling to larger N and non-commuting interactions is challenging.  
complexity_or_hardness_arguments | No complexity-theoretic claims for the protocol's simulation cost are made in this paper; the commuting model is analytically tractable, making it easier to analyze/classically simulate in many regimes.  
theory_context_keywords | ER=EPR, thermofield double (TFD), traversable wormhole, size-winding, operator size, two-sided coupling, teleportation fidelity, scrambling.  
citations_to_prior_work | References in paper: original traversable-wormhole teleportation protocol literature [14], size-winding and teleportation mechanism works [11,12], experimental small-N implementation referenced [18].  
  
### N = 7 sparse SYK 5-term learned Hamiltonian (Google Sycamore experiment, referenced)

Field | Value  
---|---  
name_short | Google Sycamore sparse SYK (referenced)  
name_full | N = 7 sparse SYK 5-term learned Hamiltonian (Google Sycamore experiment, referenced)  
brief_description | A prior experimental demonstration learned a 5-term sparse SYK-like Hamiltonian for N=7 and implemented a traversable-wormhole teleportation protocol on Google's Sycamore processor; the learned Hamiltonian's five terms are mutually commuting, provoking debate about its holographic interpretation.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Sparse SYK (small-N learned Hamiltonian) used as a proxy for SYK in teleportation experiments.  
black_hole_phenomena_targeted | Traversal/teleportation signatures analogous to traversable wormholes; empirical test of ER=EPR-inspired teleportation protocol.  
simulation_paradigm | Digital gate-based quantum experiment (superconducting qubit processor) as described in the referenced work; this paper only comments on it.  
quantum_hardware_platform | superconducting qubits (Google Sycamore) as cited in the paper's discussion.  
encoding_and_mapping | A learned sparse Hamiltonian with only five terms (all mutually commuting) acting on N=7 Majorana/qubit degrees of freedom; details of fermion-to-qubit mapping and circuit encoding are in the referenced experimental work (not provided here).  
algorithm_or_protocol | Prepare thermofield-double-like entangled state for two copies, time-evolve under the learned Hamiltonian, apply two-sided coupling e^{-i μ V}, measure two-sided correlators/teleportation fidelity; specific gate decomposition and Trotterization details are in the experimental reference.  
resource_estimates | Reported in this paper only as: N = 7 qubits and 5 Hamiltonian terms; no further gate counts, depths, or shot numbers are provided in the present paper.  
noise_and_error_mitigation | Not discussed in detail in this paper; referenced experiment would contain the hardware noise model and mitigation strategies but are not reproduced here.  
key_results_or_demonstrations | Mentioned as a motivating example: the small-N commuting learned Hamiltonian produced teleportation-like behavior on Sycamore, but because its terms commute, its relation to genuine holographic dynamics was questioned.  
validation_and_benchmarks | This paper does not provide validation data for that experiment; it cites debates in the literature [19,20] about the interpretation of the commuting learned Hamiltonian's results.  
claimed_feasibility | Used by the referenced experiment to argue near-term feasibility of demonstrating wormhole-teleportation-like phenomena at small N; this paper notes that such demonstrations probe pseudo-holographic or non-holographic mechanisms.  
limitations_and_open_problems | The 5-term commuting Hamiltonian is integrable and does not display full SYK holography; scaling to larger N, non-commuting interactions, and genuine gravitational dual behavior remain open.  
complexity_or_hardness_arguments | Not addressed; small-N commuting models are comparatively easier to simulate classically, raising questions about how 'gravitational' the observed phenomena are.  
theory_context_keywords | sparse SYK, learned Hamiltonian, small-N experiment, Sycamore, commuting Hamiltonians, pseudo-holographic simulation.  
citations_to_prior_work | Referenced in text as [18] (experiment) and discussed in relation to debate references [19,20].  
  
### Size-winding property of operator growth (phase linear in operator size)

Field | Value  
---|---  
name_short | Size-winding  
name_full | Size-winding property of operator growth (phase linear in operator size)  
brief_description | A diagnostic for holographic-like operator growth where phases of coefficients of operator expansions are approximately linear in operator size, enabling constructive interference under the two-sided coupling and supporting traversable-wormhole teleportation.  
citation_title |   
mention_or_use | use  
target_system_or_model | Operator growth in two-sided SYK-like systems (here analyzed in commuting SYK and compared to ordinary SYK/holographic models).  
black_hole_phenomena_targeted | Mechanism underpinning traversable-wormhole teleportation (bulk null-momentum correspondence to operator size) and the associated phase alignment needed for teleportation.  
simulation_paradigm | Analytic calculation of generating functions G_μ and K_μ, exact ensemble averages, and saddle-point approximations to compute P_n and Q_n (magnitude and phase aggregates) and to quantify r_n = |Q_n|/P_n and φ_n = arg Q_n.  
quantum_hardware_platform | platform-agnostic/theoretical; the property is used to interpret small-N experiments but not implemented as an algorithm on hardware in this paper.  
encoding_and_mapping | Operator-size basis Γ_I^r with size |I|; size operator S measures size; Q_n and P_n are computed from generating functions G_μ and K_μ obtained from two-sided correlators on the TFD state.  
algorithm_or_protocol | Compute ensemble-averaged G_μ(t) and K_μ(t), extract coefficients Q_n and P_n via power-series in e^{-μ}, evaluate phase linearity and r_n closeness to unity; apply saddle approximations for large N to obtain analytic estimates (eqs. (3.46),(3.49),(3.50),(3.51)).  
resource_estimates | Not applicable (analytic quantities). Numerical examples provided for N up to 100 in analytic plots and exact small-N totals (N=8) for illustrative comparison.  
noise_and_error_mitigation | Not applicable.  
key_results_or_demonstrations | Finds near-perfect size-winding (phase of Q_n linear in n and r_n ≈ 1) for commuting SYK at high temperature and large N; however, this occurs together with a narrowly peaked size distribution (distinct from ordinary SYK), and teleportation success in commuting SYK often relies more on the peaked-size mechanism and thermalization than pure size-winding.  
validation_and_benchmarks | Comparison of exact finite-N sums to saddle approximations (plots for N=100 and N=8), analytic expressions for slopes (eq. (3.50)), and comparisons to known holographic expectations (bulk SL(2) arguments) to highlight differences.  
claimed_feasibility | Authors argue size-winding signatures can appear in integrable commuting models and thus may be observed in small-N experiments; distinguishing genuine holographic origin vs pseudo-holographic appearance requires further work.  
limitations_and_open_problems | Size-winding in commuting SYK is parameter dependent (high-T, large-N, near-scrambling time); phases dephase as temperature is lowered and in regimes outside saddle validity; the narrowly peaked size distribution indicates a different teleportation mechanism than the bulk null-momentum picture.  
complexity_or_hardness_arguments | No complexity claims; behavior observed here arises in an integrable, analytically tractable model rather than in a classically hard-to-simulate chaotic one.  
theory_context_keywords | size-winding, operator size, null momentum correspondence, SL(2) isometry in near-AdS2, peaked-size mechanism, Q_n/P_n, generating functions K_μ/G_μ, saddle approximation.  
citations_to_prior_work | Cites prior works on size-winding and teleportation mechanism [11,12], and the bulk/SL(2) arguments relating size to null momentum [42,44]; compares to ordinary SYK literature [1-3].  
  
## Citation

Cite this artifact as `\cite{ast-ext-gao-2026-08-13-2}`.
[code] 
    @misc{ast-ext-gao-2026-08-13-2,
      title        = {Extraction: Commuting SYK: a pseudo-holographic model},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-commuting-syk-a-pseudo-holographic-model.md},
      crossref     = {gao2023commuting},
      note         = {Theorizer's extraction from \cite{gao2023commuting}. asta-artifact id: extraction-result-44},
    }
    
    @article{gao2023commuting,
      title     = {Commuting SYK: a pseudo-holographic model},
      author    = {Ping Gao},
      year      = {2023},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/259262526},
    }
[/code]
