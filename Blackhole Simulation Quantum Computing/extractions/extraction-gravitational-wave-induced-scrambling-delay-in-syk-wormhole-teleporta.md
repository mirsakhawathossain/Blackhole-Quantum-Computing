[<- All artifacts](<../index.md>)

# Extraction: Gravitational Wave-Induced Scrambling Delay in SYK Wormhole Teleportation

**Contents:**

  * Gravitational-Wave-Inspired Wormhole-Influenced Teleportation Protocol in the SYK model
  * Boundary Strain Bilinear Operator H_strain (i γ_i γ_j projection of SYK_4)



### Gravitational-Wave-Inspired Wormhole-Influenced Teleportation Protocol in the SYK model

Field | Value  
---|---  
name_short | GW-WITP (SYK)  
name_full | Gravitational-Wave-Inspired Wormhole-Influenced Teleportation Protocol in the SYK model  
brief_description | A numerical study (exact-diagonalisation + time-dependent Trotter evolution) of a two-sided SYK_4 thermofield-double implementing a traversable-wormhole-inspired teleportation protocol, subject to a gravitational-wave-inspired time-dependent bilinear (fermion-pair) Floquet perturbation; diagnostics include teleportation fidelity spectroscopy and OTOC scrambling-time measurements that demonstrate a drive-induced scrambling delay and low-pass frequency sensitivity.  
citation_title | Gravitational Wave-Induced Scrambling Delay in SYK Wormhole teleportation  
mention_or_use | use  
target_system_or_model | Two-sided SYK_4 model (N Majorana fermions per side) prepared in a thermofield-double state with JT-gravity holographic interpretation (AdS2/Schwarzian low-energy dual).  
black_hole_phenomena_targeted | Traversable-wormhole teleportation (wormhole-inspired quantum teleportation), many-body scrambling (OTOC), scrambling-time shifts/delays, dynamical boundary response to metric-like (GW) perturbations (holographic bulk interpretation: perturbation of bulk geometry / wormhole interior dynamics).  
simulation_paradigm | Classical exact diagonalisation and numerically Trotterised time evolution of the quantum many-body SYK Hamiltonian (i.e., classical simulation of the quantum dynamics); analysis and diagnostics are framed as a quantum/quantum-information protocol (teleportation circuit) that is directly implementable on quantum processors in principle.  
quantum_hardware_platform | platform-agnostic (discussion/implication for near-term quantum processors; no hardware experiment presented here).  
encoding_and_mapping | Majorana-to-qubit mapping via Jordan-Wigner: N Majorana modes per boundary represented by N/2 complex fermions (f_k) with JW strings; single-boundary Hilbert space dimension d = 2^{N/2}; two-sided system constructed from two identical disorder-realisation Hamiltonians (right side uses charge-conjugation convention). The GW-like metric perturbation is implemented as a bilinear operator H_strain^α = sum_{i<j} ̃J_{ij} (i γ_i^α γ_j^α) with ̃J_{ij} given by partial contraction of the four-body SYK tensor (Eq. 13). Thermofield-double (TFD) state preparation is assumed as initial condition (constructed via imaginary-time single-side evolution of maximally entangled |I⟩).  
algorithm_or_protocol | Hayden–Preskill style encoding of a message qubit into the left boundary (Pauli-channel map); backward/forward time evolution under H_α(t) with a piecewise-constant Trotter integrator (first-order Lie–Trotter used, Strang midpoint used as cross-check); instantaneous double-trace coupling U_g = exp(i g sum n_i) applied at t=0 to open traversable window; right-side readout and fidelity computation (Bell-pair overlap formula); independent OTOC measurement protocol (compute F_OTOC(t) and normalized C(t)). Chirp and monochromatic Floquet drives implemented via multiplicative envelope h(t) with dimensionless amplitude ε coupling to H_strain.  
resource_estimates | Reported classical/numerical resources and explicit system sizes: simulated N ∈ {10,12,14,16} Majorana modes (per side), corresponding to single-boundary Hilbert-space dimensions d = 2^{N/2} (32,64,128,256) and two-sided spaces of size d^2; disorder averaging N_avg = 20 for main results (N_avg = 50 used in scaling tests); time-integration step size δt = 0.05 J^{-1} (adaptive scheme δt = 0.05/(1+0.5 ε)J^{-1} for large ε), with step-size halving checks; no quantum circuit gate counts, logical qubit counts, T-gate counts, or fault-tolerant overheads are provided (the study is a classical simulation). Exact-diagonalisation and expm_multiply were used; authors note classical exact diagonalisation becomes intractable beyond these sizes and suggest tensor-network or large-N saddle-point methods for N ≫ 16.  
noise_and_error_mitigation | No physical quantum noise model is simulated; numerical error control via integrator convergence tests (Lie–Trotter global O(δt) error, Strang midpoint O(δt^2) cross-check), adaptive step sizes, step-size halving, and comparison to Strang integrator; statistical uncertainty handled via disorder averaging and reporting of disorder standard error σ_dis/√N_avg. No quantum noise mitigation (ZNE/PEC/symmetry verification) is used because simulation is noiseless.  
key_results_or_demonstrations | Simulation-only (classical numerics) demonstration of: (1) amplitude-dependent teleportation-fidelity suppression with two regimes separated near ε ∼ J (perturbative sensing regime ε ≲ J with fidelity decreasing ≈ α ε^2, and non-perturbative strong-drive regime for ε ≳ J where protocol-optimum shifts); (2) frequency spectroscopy showing low-pass response with maximum sensitivity in quasi-static regime ω ≲ ω_T = β^{-1} (βJ=2 → ω_T = 0.50 J) and recovery above ω_T, with empirical recovery near ω_L = 2π/β = 3.14 J; (3) inspiral chirp drive (ε_0 = 0.50 J applied to right boundary during readout) produces teleportation-fidelity peak delay Δt_scr^(fid) = +0.11 J^{-1} and peak suppression ΔF = 0.030; (4) independent OTOC diagnostic under monochromatic drives finds Δt_scr^(OTOC) = +0.20 J^{-1} at ε = 0.20 J (and +0.85 J^{-1} at ε = 0.50 J) confirming genuine scrambling delay; (5) the calibrated teleportation baseline F_0 ≈ 0.626 (N=12, βJ=2), with channel remaining above classical limit F = 1/4 across scanned parameter ranges; (6) re-optimisation analysis shows most fidelity loss is genuine in sensing regime (re-optimisation recovers ≲2% in sensing regime, up to ≲15% recovery only in strong slow-drive corner); (7) system-size scan N=10–16 shows effects persist (no systematic suppression) across these finite sizes.  
validation_and_benchmarks | Validation methods used in the paper: (i) integrator convergence (step-size halving) and cross-check with second-order Strang scheme to bound time-discretisation error; (ii) disorder averaging (N_avg = 20 or 50) with standard-error reporting; (iii) re-optimisation (compare fixed-calibration vs re-optimised (g,t) to separate protocol mismatch from genuine effects); (iv) independent observable cross-checks: teleportation fidelity vs OTOC (half-saturation criterion) yield consistent sign of scrambling delay; (v) system-size scaling (N=10–16) to check finite-size artifacts; (vi) analytic justification from Schwarzian effective-theory in Appendix A predicting Δt_scr ∝ ε^2 and identification of bilinear operator as dominant coupling via BF-bound argument.  
claimed_feasibility | Authors argue WITP and OTOC diagnostics are within reach of near-term quantum processors (citing recent experimental implementations) for small N, and that the effects studied (in sensing regime ε ≲ J) are operationally accessible; however, full quantitative extrapolation to holographic large-N requires methods beyond ED (tensor networks or large-N saddle points). They do not claim that large-N holographic bulk dynamics are implementable on current NISQ hardware without substantial further development.  
limitations_and_open_problems | Explicit limitations stated: (i) 0+1D SYK/JT duality lacks propagating GW modes—boundary bilinear strain is a phenomenological analogue derived via holographic dictionary (Appendix A) but not a full dynamical bulk GW; (ii) finite-N exact-diagonalisation limited to N ≤ 16 (classical simulation bottleneck), so large-N extrapolation is unresolved; (iii) normalization choice for H_strain (‖H_strain‖_sp = 5J) is a convention that rescales ε; (iv) the Schwarzian analytical predictions apply at βJ ≫ 1 while simulations at βJ = 2 are finite-temperature and finite-N; (v) preparing TFD states on hardware is nontrivial (assumed constructed here); (vi) no quantum-noise or hardware-specific error modelling is included—mapping to actual gate depths/gates for hardware is not provided.  
complexity_or_hardness_arguments | No explicit formal complexity-theoretic proofs, but practical statements: classical ED scales exponentially (d = 2^{N/2} per boundary) and becomes intractable for N ≫ 16; authors propose tensor-network or large-N saddle-point methods for larger N; no claims of BQP/QMA hardness or rigorous complexity lower bounds are made in the text.  
theory_context_keywords | SYK, JT gravity, AdS/CFT, Schwarzian effective action, traversable wormhole, Gao-Jafferis-Wall double-trace coupling, Hayden-Preskill encoding, fast scrambling, Lyapunov exponent (MSS bound), OTOC, thermofield double (TFD), bilinear operator (fermion bilinear), Breitenlöhner-Freedman bound.  
citations_to_prior_work | Key cited works used as context or building blocks: Sachdev & Ye (1993) and Kitaev (SYK foundational refs), Maldacena & Stanford and MSS bound (chaos), Gao-Jafferis-Wall (traversable wormhole construction), Maldacena & Qi (SYK wormhole realizations), Jafferis et al. (Nature 2022) quantum-processor implementation of traversable-wormhole protocol, prior baseline wormhole-teleportation protocol by the authors (Ref. [26]), and references on Trotter/Strang integrators and numerical methods (expm_multiply).  
  
### Boundary Strain Bilinear Operator H_strain (i γ_i γ_j projection of SYK_4)

Field | Value  
---|---  
name_short | H_strain (bilinear)  
name_full | Boundary Strain Bilinear Operator H_strain (i γ_i γ_j projection of SYK_4)  
brief_description | A constructed fermion-bilinear boundary operator obtained by partially contracting the SYK_4 four-body couplings (Eq. 13) that serves as the leading boundary response channel to a metric-like (GW) perturbation in the SYK/JT holographic dictionary; used as the time-dependent Floquet perturbation ε h(t) H_strain in the simulations.  
citation_title | Gravitational Wave-Induced Scrambling Delay in SYK Wormhole teleportation  
mention_or_use | use  
target_system_or_model | Bilinear sector of SYK_4 boundary theory (dual to a bulk scalar saturating the AdS_2 BF bound), used as the boundary manifestation of a metric perturbation in JT gravity.  
black_hole_phenomena_targeted | Encodes boundary response to metric perturbations (holographically representing bulk metric strain/GW-like perturbations) that affect scrambling, wormhole traversability window and teleportation fidelity.  
simulation_paradigm | Used explicitly in classical numerical time evolution (Floquet time-dependent Hamiltonian) to emulate boundary imprint of a GW; thus a classical simulation of a quantum operator perturbation.  
quantum_hardware_platform | platform-agnostic (operator expressed in Majorana/qubit basis via Jordan-Wigner mapping; directly implementable in principle on qubit hardware that can simulate fermionic bilinears).  
encoding_and_mapping | Defined by ̃J_{ij} = (1 / C(N-2,2)) Σ_{k<l, k,l≠i,j} J_{ijkl}; H_strain^α = Σ_{i<j} ̃J_{ij} (i γ_i^α γ_j^α). Spectrally normalized so ‖H_strain^α‖_sp = 5J; mapping to qubits is via Jordan-Wigner representation of Majoranas as f_k operators and Pauli strings.  
algorithm_or_protocol | Coupled multiplicatively as a Floquet perturbation H_α(t) = H_α + ε h(t) H_strain^α; used with monochromatic drives h(t)=cos(ωt) for spectroscopy and inspiral chirp h(t)=A(t) cos(ϕ(t)) for time-resolved scrambling diagnostics.  
resource_estimates | No gate-level resource counts provided; operator used in ED time evolution with piecewise-constant exponentials exp[-i δt (H + ε h(t) H_strain)], evaluated with expm_multiply. Operator norm chosen so ε is measured in units of J; peak perturbation ε_0‖H_strain‖_sp reported (e.g., ε_0 = 0.50J gives peak perturbation 2.5J).  
noise_and_error_mitigation | Operator used in noiseless classical simulation; numerical error control via Trotter step-size choices and Strang cross-checks; no hardware error mitigation discussed specifically for H_strain implementation.  
key_results_or_demonstrations | Constructed and normalized H_strain and demonstrated that coupling to it yields measurable fidelity suppression and scrambling-time delay; Appendix A provides holographic derivation (BF-bound argument) showing bilinear is the dominant low-frequency operator and predicts Δt_scr ∝ ε^2 with positive sign.  
validation_and_benchmarks | Analytic justification in Appendix A via JT gravity → Schwarzian effective action leading-order derivation identifying dimension-1/2 bilinear operator as boundary dual of bulk scalar at BF bound; numerical validation via consistency of quadratic ε-dependence (even powers), integrator convergence, disorder averaging, and concordance between teleportation-fidelity and OTOC diagnostics.  
claimed_feasibility | Authors claim H_strain is a natural and implementable boundary analogue of a metric perturbation and that the resulting Floquet deformation is experimentally relevant for near-term realizations of wormhole teleportation circuits on quantum processors (subject to TFD preparation and platform capabilities).  
limitations_and_open_problems | H_strain is a phenomenological representation of a metric perturbation in 0+1D (JT/SYK) rather than a full dynamical bulk gravitational wave; separation of bilinear and four-body sectors is finite-N and may mix at strong ε; normalization choice (‖H_strain‖_sp = 5J) is a convention; large-N limit and rigorous bulk identification require further Schwarzian/analytical work.  
complexity_or_hardness_arguments | No formal complexity claims; authors note that low-frequency enhancement of bilinear channel follows from scaling dimension Δ=1/2, making it the leading low-energy coupling—this selects H_strain on physical grounds but does not assert computational hardness statements.  
theory_context_keywords | Breitenlöhner-Freedman bound, AdS2 scalar dual, Hubbard-Stratonovich decoupling (bilinear sector), Schwarzian correction to scrambling time, low-frequency spectral dominance, Floquet bilinear perturbation.  
citations_to_prior_work | Appendix A and main text cite JT gravity and Schwarzian literature (Jackiw, Teitelboim, Maldacena/Stanford), BF-bound references, and prior SYK bilinear analyses (e.g., Jensen 2016, Eberlein et al. 2017); central conceptual prior works include Gao-Jafferis-Wall (traversable wormholes) and Maldacena-Qi (SYK wormhole realizations).  
  
## Citation

Cite this artifact as `\cite{ast-ext-joshi-2026-08-13}`.
[code] 
    @misc{ast-ext-joshi-2026-08-13,
      title        = {Extraction: Gravitational Wave-Induced Scrambling Delay in SYK Wormhole Teleportation},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-gravitational-wave-induced-scrambling-delay-in-syk-wormhole-teleporta.md},
      crossref     = {joshi2026gravitatio},
      note         = {Theorizer's extraction from \cite{joshi2026gravitatio}. asta-artifact id: extraction-result-34},
    }
    
    @article{joshi2026gravitatio,
      title     = {Gravitational Wave-Induced Scrambling Delay in SYK Wormhole Teleportation},
      author    = {Sudhanva Joshi and S. K. Mishra},
      year      = {2026},
      url       = {https://www.semanticscholar.org/paper/286669725},
    }
[/code]
