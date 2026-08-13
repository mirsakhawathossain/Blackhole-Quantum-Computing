[<- All artifacts](<../index.md>)

# Extraction: Hawking-Page transition on a spin chain

**Contents:**

  * Hawking–Page transition simulation via coupling-averaged Loschmidt echo in the Heisenberg XX spin chain
  * Fermionized lattice simulation via Jordan–Wigner mapping (free-fermion Loschmidt echo)
  * Generalized spin chain with longer-range hoppings to include higher Tr(U^n) operators and nested Gaussian averaging for finite 't Hooft coupling
  * Polyakov loop realization via impurity in spin-chain initial state (order-parameter probe)
  * Complex-coupling (fugacity) extension: complex-temperature Loschmidt echo and thimble deformation



### Hawking–Page transition simulation via coupling-averaged Loschmidt echo in the Heisenberg XX spin chain

Field | Value  
---|---  
name_short | XX-averaged Loschmidt simulation  
name_full | Hawking–Page transition simulation via coupling-averaged Loschmidt echo in the Heisenberg XX spin chain  
brief_description | Proposal to reproduce the Hawking–Page first-order transition (AdS5 thermal AdS to black hole dominance) by measuring the thermal Loschmidt echo of an XX spin-1/2 chain prepared in a domain-wall initial state and averaging over a Gaussian-distributed ferromagnetic coupling; mapping to the Gross-Witten-Wadia unitary matrix model yields the expected O(1) vs N^2 entropy scaling.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Hawking–Page transition in AdS_5 (black hole formation) as encoded by the thermal partition function of 4d N=4 SYM on S^3 x S^1; mapped to Gross-Witten-Wadia (GWW) unitary matrix model  
black_hole_phenomena_targeted | Hawking–Page transition (horizon formation dominance), jump in entropy between thermal AdS and black hole phase; Polyakov loop as deconfinement order parameter  
simulation_paradigm | analog quantum simulation / experimental measurement protocol (platform-agnostic spin-chain measurements) — measuring thermal Loschmidt echoes in a laboratory spin chain, repeated sampling of couplings (classical randomness) and post-processing averages  
quantum_hardware_platform | platform-agnostic (spin-1/2 chains); authors do not commit to a specific hardware, but the proposal fits trapped ions, neutral-atom/spin arrays or superconducting qubit chains implementing XX-type dynamics  
encoding_and_mapping | Direct spin-1/2 chain (Heisenberg XX) with periodic boundary conditions, initial domain-wall state |ψ0> = N adjacent ↓ followed by ↑; thermal (imaginary-time) evolution implemented via e^{-H_{XX}/\tilde{T}} (replace it -> 1/\tilde{T}); Loschmidt amplitude G_N(J) formed from that evolution; Toeplitz determinant representation (Heine–Szegő) maps the amplitude to the GWW matrix integral with identification J = Nσ; Jordan–Wigner fermionization maps the XX chain to free fermions and yields equivalent Loschmidt echo; for improved fidelity include longer-range couplings corresponding to higher Tr(U^n) operators in the matrix model; Polyakov loop realized as an impurity in the initial state (single-spin defect)  
algorithm_or_protocol | Prepare domain-wall initial state; thermal (imaginary-time) evolution for time t -> 1/\tilde{T} with Hamiltonian H_{XX} (depends only on J=\tilde{J}/\tilde{T}); measure Loschmidt echo L_N(J)=|<ψ0|e^{-H/\tilde{T}}|ψ0>|^2 (or its square root); repeat experiment many times sampling J from a Gaussian with variance 2a (a relates monotonically to BH temperature via AdS/CFT formula); compute average ⟨√Ĺ_N⟩_{2a} which maps to e^{ĤS} (matrix-model entropy); for finite 't Hooft coupling do nested Gaussian averaging over both J and its standard deviation; Polyakov loop measured via ratio of echoes with and without impurity  
resource_estimates | No gate-depth or explicit circuit-count provided. System-size guidance: regime 1 << N << L, authors note empirical minimal sizes quoted as N ≥ 4 and L ≥ 11 (figures use L up to 18). Resource scaling: need many repeated experimental runs to sample J (and for nested averages, sample the standard deviation distribution too); no fault-tolerant overheads or logical-qubit/T-count estimates provided.  
noise_and_error_mitigation | No detailed noise model or mitigation protocol is provided. Authors remark feasibility depends on experimental error budgets and finite-size effects; implicit mitigation: work with ratios Ĺ_N = L_N/L_1 and measure square roots (observable probabilities) to avoid complex phases. No explicit ZNE/PEC/symmetry-verification protocols discussed.  
key_results_or_demonstrations | Analytical exact mapping (identity (26)) linking averaged thermal Loschmidt echo to the reduced matrix-model entropy: e^{ĤS} ∼ ⟨√Ĺ_N⟩ _{2a}. Large-N matrix-model analysis (GWW) predicts first-order transition at a=1 (T_HP ≈ 0.38) producing entropy jump from O(1) to O(N^2). Numerical plots in paper show ln ⟨√L_N⟩_ vs N and vs a exhibiting sharp change consistent with Hawking–Page behaviour. The proposal is theoretical/mapping + numerics (no hardware experiment).  
validation_and_benchmarks | Validation by exact analytic mapping to Gross-Witten-Wadia unitary matrix model via Toeplitz determinant / Heine–Szegő identity and known analytic results for the GWW model (planar limit and saddle-point giving phase transition at a=1). Additional consistency: Jordan–Wigner mapping to free fermions (independent derivation), determinant identities and Szegő strong limit theorem, and finite-size numerical evaluations (figures). Comparison is primarily to established analytic matrix-model predictions rather than to hardware data.  
claimed_feasibility | Authors claim the proposal is experimentally realizable in principle on simple quantum systems; state the remaining practical challenge is to assess whether required system sizes and error budgets (N ≥ 4, L ≥ 11) and repeated sampling are feasible with current technology. No claim that fault tolerance is required; protocol intended to work on non-zero laboratory temperatures and NISQ-scale devices if errors and sampling allow.  
limitations_and_open_problems | Only a single observable (thermal partition-function/entropy via averaged Loschmidt echo) is mapped — not a complete holographic dual; averaging over couplings (classical disorder) is an added ingredient not present in gravitational system; finite-N corrections require more complicated Hamiltonians (longer-range couplings) which may be hard to implement; no dynamic spacetime or local gravitational degrees of freedom are simulated (only thermodynamic BH signature); absence of detailed experimental resource, noise, and error-mitigation analysis; verification at finite N is complicated by discarded operators from matrix-model truncation; implementing complex fugacities (complex temperature) requires complex-time evolution or contour deformations which are experimentally challenging.  
complexity_or_hardness_arguments | No explicit complexity-theoretic hardness claims (BQP/QMA) are made in the paper.  
theory_context_keywords | AdS/CFT, Hawking–Page transition, deconfinement, Gross-Witten-Wadia matrix model, Loschmidt echo, Polyakov loop, Jordan–Wigner, 't Hooft coupling corrections, matrix-model averages, Toeplitz determinant, Heine–Szegő identity  
citations_to_prior_work | Key references used as foundation: 'Thermodynamics of Black Holes in anti-de Sitter Space' (Hawking & Page, 1983); Aharony et al, 'The Hagedorn - deconfinement phase transition in weakly coupled large N gauge theories' (2004); Hong Liu, 'Fine structure of Hagedorn transitions' (2004); Gross and Witten 'Possible Third Order Phase Transition...' and Wadia 'N = Infinity Phase Transition...' (GWW); Jafferis et al, 'Traversable wormhole dynamics on a quantum processor' (Nature 2022) referenced as prior quantum-simulation of gravitational phenomena; works on Loschmidt echo in BH contexts (del Campo et al, Chenu et al); spin-chain–matrix model mappings and Toeplitz determinant techniques (Bogoliubov et al, Pérez-García & Tierz papers [95,96,99,103])  
  
### Fermionized lattice simulation via Jordan–Wigner mapping (free-fermion Loschmidt echo)

Field | Value  
---|---  
name_short | Jordan-Wigner fermionic variant  
name_full | Fermionized lattice simulation via Jordan–Wigner mapping (free-fermion Loschmidt echo)  
brief_description | Equivalent formulation of the XX spin-chain proposal after Jordan–Wigner transformation: the domain-wall spin initial state maps to N adjacent fermions on an L-site lattice; the free-fermion Hamiltonian with general dispersion gives a unitary matrix-model amplitude whose potential equals the dispersion, preserving the mapping to matrix models.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Same Hawking–Page transition in AdS_5 via dual matrix model; represented by a free-fermion lattice Hamiltonian with general dispersion ε_k  
black_hole_phenomena_targeted | Hawking–Page entropy jump; ability to tune dispersion to reproduce generalized matrix-model potentials (i.e., codify higher operators)  
simulation_paradigm | analog quantum simulation / fermionic lattice measurement; theoretical mapping rather than hardware run  
quantum_hardware_platform | platform-agnostic (fermionic lattice realizable in cold atoms, fermionic quantum simulators) but discussed primarily as mathematical equivalence  
encoding_and_mapping | Jordan–Wigner transformation: spin up ↔ empty, spin down ↔ occupied; domain-wall state ↔ N adjacent fermions; free-fermion Hamiltonian H_ferm = (1/L) Σ_k ε_k c_k^† c_k; Loschmidt amplitude rewritten as a unitary matrix integral with potential Tr V_ε(U) where V_ε encodes ε_k (equation B27–B29); periodic boundary conditions considered and large-L limit maps integrals to matrix model  
algorithm_or_protocol | Compute or measure return amplitude G_N^{ferm} = ⟨ψ0|e^{-H_ferm/\hat{T}}|ψ0⟩; same averaging over coupling parameters (dispersion amplitudes) as spin-chain J variables to reproduce matrix-model averages  
resource_estimates | No explicit hardware resource accounting; system size mapping identical to spin-chain case (L sites, N particles).  
noise_and_error_mitigation | Not discussed beyond equivalence remarks; fermion parity conservation plays role in equality of echoes between inequivalent models.  
key_results_or_demonstrations | Analytical derivation that Loschmidt amplitude of a generic free-fermion dispersion reduces to a unitary matrix model (B27–B29), showing equivalence of return amplitudes with generalized spin chains for the specific domain-wall initial state; provides consistency check of main mapping.  
validation_and_benchmarks | Validated via Slater-determinant expression for overlaps, integral expressions turning into unitary matrix integrals, and by explicit argument showing return amplitudes match those of spin-chain Toeplitz determinants in the large-L limit.  
claimed_feasibility | Authors note fermionic models provide a useful perspective and possible experimental realizations (fermionic cold atoms), but do not provide concrete experimental parameter estimates.  
limitations_and_open_problems | Although Loschmidt echoes match, the full fermionic Hamiltonian and spin-chain Hamiltonian are not equivalent for K>1 interactions (string operators appear under inverse JW), so equality is limited to the return amplitude for the chosen initial state; implementing arbitrary dispersion in hardware may be hard.  
complexity_or_hardness_arguments | No complexity claims.  
theory_context_keywords | Jordan–Wigner, free fermions, dispersion relation → matrix-model potential, Slater determinant, Toeplitz determinant  
citations_to_prior_work | References on Jordan–Wigner mapping (Jordan & Wigner 1928), free-fermion Loschmidt literature (Krapivsky, Luck & Mallick 2018 [101]), and prior spin-chain–matrix model mappings (Pérez-García & Tierz [96,99])  
  
### Generalized spin chain with longer-range hoppings to include higher Tr(U^n) operators and nested Gaussian averaging for finite 't Hooft coupling

Field | Value  
---|---  
name_short | Generalized long-range chain / nested averaging  
name_full | Generalized spin chain with longer-range hoppings to include higher Tr(U^n) operators and nested Gaussian averaging for finite 't Hooft coupling  
brief_description | Extension that adds up-to-K-th neighbor spin-flip couplings (H_gen) whose Loschmidt amplitude maps to a unitary matrix model with multiple Tr(U^n) terms, enabling progressively improved approximations to the full SYM thermal partition function and black-hole entropy; finite 't Hooft-coupling corrections are implemented by nested Gaussian averages over coupling parameters.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Improved effective matrix-model description of N=4 SYM thermal partition function (including higher a_n terms) and finite-λ corrections to AdS_5 black-hole entropy  
black_hole_phenomena_targeted | More accurate BH entropy estimates near/above the Hawking–Page transition including subleading corrections in operators and 't Hooft coupling  
simulation_paradigm | analog quantum simulation with engineered longer-range spin interactions and classical averaging (nested sampling) over couplings  
quantum_hardware_platform | platform-agnostic; would require ability to implement variable-range spin-exchange terms (e.g., engineered interactions in trapped ions or Rydberg arrays)  
encoding_and_mapping | Generalized Hamiltonian H_gen = -1/2 Σ_j Σ_{n=1}^K (\tilde{J}_n/n) (σ_j^- σ_ ^+ + h.c.); mapping proceeds via differentiating generalized correlators obeying recurrence relations of generalized Bessel functions, Heine–Szegő identity yields matrix model with multiple Tr(U^n) terms; identification J_n = Nσ_n and Gaussian averaging over each J_n with variance 2a_n reproduces contributions of the corresponding a_n in matrix model (equation B9, B16)  
algorithm_or_protocol | Implement H_gen experimentally for chosen K (hardware-dependent); measure Loschmidt echoes as functions of the set {J_n}; perform Gaussian averages over the vector of couplings to reconstruct e^{S} up to order K; for finite 't Hooft coupling include an outer Gaussian sampling over the variance parameter (nested averaging) to capture corrections (equations B32–B34)  
resource_estimates | No explicit gate or time resources; complexity increases with K (more distinct coupling parameters to control and more classical sampling dimensions); nested averaging multiplies number of required runs by sampling factors for J_n and for outer μ-distribution (authors emphasize measurement repetition cost but give no concrete counts).  
noise_and_error_mitigation | Not detailed; more complex Hamiltonians and nested averages exacerbate experimental sampling noise and control-error sensitivity.  
key_results_or_demonstrations | Analytical extension showing that including up to K couplings and averaging over them reproduces truncated matrix-model entropy (B9–B18); demonstration that finite-λ corrections studied in previous matrix-model literature map to nested averages over coupling standard deviations and hence can in principle be tested on the spin chain (B32–B34).  
validation_and_benchmarks | Validation is theoretical: comparison to matrix-model results including known finite-λ analysis from Aharony et al and Alvarez-Gaume et al; no experimental benchmarks.  
claimed_feasibility | Authors claim conceptual simplicity of implementation (same type of measurements repeated with additional sampling), but acknowledge practical difficulty: implementing many independent long-range couplings and performing high-dimensional averages may be challenging experimentally.  
limitations_and_open_problems | Engineering Hamiltonians with many controlled coupling terms may be infeasible in practice; sampling (curse of dimensionality) and finite-size corrections limit quantitative extraction of full BH entropy; inverse Jordan–Wigner introduces string operators for K>1, meaning spin and fermion pictures are not fully equivalent beyond K=1.  
complexity_or_hardness_arguments | No formal complexity-theoretic statements, but practical sampling complexity implied (many repeated runs scale with number of coupling dimensions and nested averaging levels).  
theory_context_keywords | higher multi-trace operators, Hubbard–Stratonovich Gaussian integrals, finite 't Hooft coupling corrections, nested averages, generalized Bessel functions, Toeplitz determinants  
citations_to_prior_work | Aharony et al 'The Hagedorn - deconfinement phase transition...' (2004) and Alvarez-Gaume et al 'Finite temperature effective action, AdS(5) black holes, and 1/N expansion' (2005) used for finite-λ corrections; Pérez-García & Tierz mappings for generalized chains [99]  
  
### Polyakov loop realization via impurity in spin-chain initial state (order-parameter probe)

Field | Value  
---|---  
name_short | Polyakov-loop impurity probe  
name_full | Polyakov loop realization via impurity in spin-chain initial state (order-parameter probe)  
brief_description | Implementation of the CFT Polyakov loop (order parameter of deconfinement/Hawking–Page transition) as a single-spin impurity/defect in the prepared initial state of the chain; the ratio of averaged echoes with and without the impurity corresponds to the Polyakov loop expectation value.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Polyakov loop in N=4 SYM (holographic order parameter for deconfinement/Hawking–Page transition)  
black_hole_phenomena_targeted | Order-parameter detection of BH phase (vanishing Polyakov loop below T_HP, non-zero above T_HP)  
simulation_paradigm | measurement-protocol within spin-chain experiment: prepare modified initial state with impurity then measure averaged Loschmidt echoes and take ratio  
quantum_hardware_platform | platform-agnostic spin-chain implementations (requires single-site state preparation and measurement capability)  
encoding_and_mapping | Initial state with impurity |ψ_×> defined by moving one ↓ spin away from the block of N-1 ↓ spins (equation (27)); corresponding amplitude G_N^×(J) and echo Ĺ_N^×(J) defined analogously; Polyakov loop P = ⟨Tr U⟩ computed as ratio of Gaussian-averaged amplitudes or, experimentally, ratio of averaged square-root echoes (equation B8)  
algorithm_or_protocol | Prepare |ψ_0> and |ψ_×>; for each sampled J measure √Ĺ_N and √Ĺ_N^×; compute P = ⟨√Ĺ_N^×⟩ _{2a} / ⟨√Ĺ_N⟩_ ; repeat sampling over J to explore phases across a  
resource_estimates | Same size requirements as main protocol (L and N) plus the need to prepare and measure two slightly different initial states; sampling overhead doubled for impurity runs.  
noise_and_error_mitigation | No detailed mitigation discussed; authors note that measuring real probabilities (square-root echoes) removes centre-symmetry phase ambiguities and implicitly regularizes the order-parameter measurement.  
key_results_or_demonstrations | Theoretical derivation linking the impurity echo ratio to the Polyakov loop; prediction that Polyakov loop vanishes for a<1 (low disorder) and becomes non-zero for a>1 (high disorder) after Gaussian averaging, matching matrix-model expectations.  
validation_and_benchmarks | Validated analytically via matrix-model source-term method (B3–B5) and mapping to impurity amplitudes using prior spin-chain results [93]; numerical averaging examples shown in the paper.  
claimed_feasibility | Authors suggest this is experimentally accessible with current technologies in principle (requires single-site control) but stress need to check feasibility with respect to noise and system sizes.  
limitations_and_open_problems | Subtlety of centre symmetry and requirement of implicit regulator discussed; measurement requires high precision to detect vanishing vs small non-zero values; finite-size and averaging effects may blur sharpness of order-parameter jump.  
complexity_or_hardness_arguments | No complexity-theoretic claims.  
theory_context_keywords | Polyakov loop, Wilson loop, deconfinement order parameter, impurity/defect, centre symmetry  
citations_to_prior_work | References include foundational Polyakov/’t Hooft deconfinement literature (Polyakov 1978, 't Hooft 1978) and matrix-model methods (Aharony et al 2004), and spin-chain impurity-to-matrix-model mapping work (reference [93])  
  
### Complex-coupling (fugacity) extension: complex-temperature Loschmidt echo and thimble deformation

Field | Value  
---|---  
name_short | Complex-fugacity / complex-temperature variant  
name_full | Complex-coupling (fugacity) extension: complex-temperature Loschmidt echo and thimble deformation  
brief_description | Extension of the protocol to complex couplings a_n ∈ ℂ (complex fugacities for BH charges) corresponding to complex-temperature/time-evolution in the lab; average of Loschmidt echoes with complexified coupling implements matrix models with complex saddles via contour/thimble deformations.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Matrix models with complex couplings that better capture BH physics with arbitrary fugacities (more realistic AdS black-hole features)  
black_hole_phenomena_targeted | More realistic BH thermodynamics including charged/rotating branches encoded by complex fugacities; richer Hawking–Page-like behaviour  
simulation_paradigm | analog quantum simulation with real-time evolution component (complex temperature translates into a combination of finite temperature and real time evolution) plus classical averaging over complexified coupling phases  
quantum_hardware_platform | platform-agnostic; requires coherent time evolution (control over both imaginary- and real-time components) and stable phase control  
encoding_and_mapping | Write a = |a| e^{iφ}; mapping (B35) shows e^{ĤS} ∼ ⟨Ĺ_N(e^{-iφ/2} J)⟩_{2|a|} meaning the system must be run at complex effective temperature e^{iφ/2} \hat{T}, implemented by combining finite-temperature preparation and real-time evolution for time t satisfying arg(i t + \tilde{T}_R^{-1}) = -φ/2 (equation B36); classical average over J remains Gaussian in magnitude but sampling includes complex phase via time evolution  
algorithm_or_protocol | Prepare thermal state at laboratory temperature \tilde{T}_R and evolve for real time t set by φ, then measure Loschmidt echo for sampled real coupling values J, followed by Gaussian averaging; mathematical equivalence to GWW with complex coupling relies on analytic continuation and thimble deformation methods  
resource_estimates | No quantitative resource claims; added requirement is coherent control for non-negligible real-time evolution and ability to stabilize phases across many runs, increasing experimental sensitivity to decoherence.  
noise_and_error_mitigation | Paper notes experimental challenge; complex-time evolution exacerbates decoherence sensitivity; no mitigation protocols are provided.  
key_results_or_demonstrations | Analytical statement (B35–B36) showing how complex fugacities map to complex-temperature Loschmidt echoes and how experimental protocol could realize the required complex coupling integrals via combined real and imaginary time evolution; no experimental demonstration.  
validation_and_benchmarks | Validation is conceptual and mathematical via extension of earlier mapping and references to literature on complex saddles in GWW (Álvarez et al, Santilli & Tierz), not empirical.  
claimed_feasibility | Authors describe this as conceptually straightforward but experimentally more challenging; require control of real-time evolution and averaging over couplings; no timeline given.  
limitations_and_open_problems | Implementing coherent complex-time evolution and controlling phases under decoherence is difficult; need contour deformation (thimble) analysis for steepest-descent saddles which complicates interpretation and experimental realization.  
complexity_or_hardness_arguments | No complexity statements.  
theory_context_keywords | complex fugacities, complex temperature, thimble/steepest-descent, analytic continuation of matrix models, delayed deconfinement  
citations_to_prior_work | Copetti et al 'Delayed deconfinement and the Hawking-Page transition' (2022) and works on complex saddles in GWW (Álvarez, Martínez Alonso & Medina 2016; Santilli & Tierz 2022) are cited as motivations/methods  
  
## Citation

Cite this artifact as `\cite{ast-ext-prezgarca-2026-08-13}`.
[code] 
    @misc{ast-ext-prezgarca-2026-08-13,
      title        = {Extraction: Hawking-Page transition on a spin chain},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-hawking-page-transition-on-a-spin-chain.md},
      crossref     = {prezgarca2024hawkingpag},
      note         = {Theorizer's extraction from \cite{prezgarca2024hawkingpag}. asta-artifact id: extraction-result-66},
    }
    
    @article{prezgarca2024hawkingpag,
      title     = {Hawking-Page transition on a spin chain},
      author    = {David Pérez-García and Leonardo Santilli and M. Tierz},
      year      = {2024},
      journal   = {Physical Review Research},
      url       = {https://www.semanticscholar.org/paper/267212049},
    }
[/code]
