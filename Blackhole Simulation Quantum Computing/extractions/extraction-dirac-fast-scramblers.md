[<- All artifacts](<../index.md>)

# Extraction: Dirac fast scramblers

**Contents:**

  * Dirac Fast Scrambler: Gross–Neveu–Yukawa (GNY) large-N generalization of SYK in higher dimensions



### Dirac Fast Scrambler: Gross–Neveu–Yukawa (GNY) large-N generalization of SYK in higher dimensions

Field | Value  
---|---  
name_short | Dirac Fast Scrambler  
name_full | Dirac Fast Scrambler: Gross–Neveu–Yukawa (GNY) large-N generalization of SYK in higher dimensions  
brief_description | A family of large-N Gross–Neveu–Yukawa field theories with many boson and Dirac-fermion flavors, derived from local lattice low-rank SYK-like couplings, that yield Lorentz-invariant critical points in 1+1 and 2+1 dimensions and exhibit fast scrambling (maximal Lyapunov exponent) in 1+1d.  
citation_title | here  
mention_or_use | use  
target_system_or_model | SYK-like systems / Gross–Neveu–Yukawa (GNY) field theory with random Yukawa couplings (low-rank SYK lattice -> Dirac fermions + many bosons). This is the target 'black-hole-like' system because of its holographic/fast-scrambling properties.  
black_hole_phenomena_targeted | Quantum information scrambling as quantified by out-of-time-order correlators (OTOCs) and Lyapunov exponent (maximal chaos λ_L = 2πT); these are the black-hole-like phenomena targeted (analogy to black hole maximal chaos and holographic duals). The paper also discusses residual entropy (SYK-like zero-T entropy) relevant to black-hole entropy analogies.  
simulation_paradigm | Analytical large-N field-theory solution and diagrammatic calculation (Schwinger–Dyson equations for Green's functions; Bethe–Salpeter/ladder kernel eigenproblem for OTOCs). No digital/analog quantum-simulation protocol is proposed or implemented.  
quantum_hardware_platform | None  
encoding_and_mapping | Not applicable for quantum hardware: mapping described is from a microscopic lattice of low-rank SYK 'dots' (fermions with random low-rank four-fermion couplings) to a continuum GNY field theory (Dirac fermions + many bosons) via Hubbard–Stratonovich transformation and long-wavelength expansion. No mapping to qubits or fermion-to-qubit encodings (Jordan–Wigner/Bravyi–Kitaev) is given.  
algorithm_or_protocol | Analytical and semi-analytic techniques: large-N Schwinger–Dyson (SD) equations to obtain scale-invariant Green's functions; Bethe–Salpeter (ladder) kernel for four-point OTOCs to extract Lyapunov exponent; conformal mapping to finite temperature for correlators. No quantum-algorithm (Trotterization, LCU, VQE, etc.) is presented.  
resource_estimates | None provided for quantum simulation. Theoretical results rely on large-N limit (N, M → ∞ with fixed ratio γ); numerical solutions of SD equations performed but no qubit/gate/measurement counts or runtime/resource scalings are given.  
noise_and_error_mitigation | Not applicable — no quantum hardware experiment or noise model is discussed.  
key_results_or_demonstrations | 1) Found Lorentz-invariant critical solutions parameterized by fermion scaling dimension Δ and rank ratio γ in D=d+1<4\. 2) In (1+1)-d, explicitly computed OTOCs and showed exponential growth with maximal Lyapunov exponent λ_L = 2πT in the low-temperature limit (i.e., saturation of the chaos bound) and derived velocity-dependent behavior (butterfly/light-cone structure) with v_B = 1 and a v_* < 1 defining a regime of maximal growth near the light cone. 3) Derived rank–exponent relations relating γ and Δ (analytic expressions Eqs. (11),(16),(17)). 4) Computed residual entropy in (0+1)-d critical points. These are analytical/theoretical demonstrations (proposal & analysis), not quantum-simulation experiments.  
validation_and_benchmarks | Validation is via internal consistency of SD equations and conformal scaling, numerical solutions of SD equations, comparison of (2+1)-d Δ to conformal-bootstrap and known 1/N_f results (Table I), and checks that the ladder-kernel eigenvalue problem yields λ_L(p = ± i 2πT). No cross-platform quantum simulation benchmarks are present.  
claimed_feasibility | No claims about implementing these models on quantum hardware. The paper emphasizes theoretical solvability in the large-N limit; it suggests future theoretical directions (derivation of an effective low-energy action analogous to the Schwarzian) and the potential holographic interpretation, but does not make NISQ/FTQC feasibility claims.  
limitations_and_open_problems | Explicit limitations noted: results are at the large-N saddle-point (1/N corrections not fully treated), (1+1)-d critical solutions require minimal rank γ>1/4, (2+1)-d critical points are not self-tuned and require tuning of g^2, the paper does not derive the low-energy effective action (analogue of Schwarzian) — left as future work, uncertain whether (2+1)-d points are fast scramblers, and the models are field-theory toy models (no dynamical gravity): they only provide holographic-like behavior (fast scrambling) but do not simulate dynamical spacetime or full black hole physics. No protocol for preparing thermofield double or other holographic states on quantum devices is given. Verification beyond large-N and finite-N scaling/1/N corrections remain open.  
complexity_or_hardness_arguments | No complexity-theoretic claims (e.g., BQP/QMA-hardness) about simulating these models on quantum computers are made in the paper.  
theory_context_keywords | SYK, AdS/CFT, holographic correspondence, fast scrambling, chaos bound (λ_L ≤ 2πT), holographic CFT, dilaton gravity/AdS2 analogy, ladder kernel/OTOC, large-N, Gross–Neveu–Yukawa, conformal invariance, Schwarzian (as analogy), residual entropy.  
citations_to_prior_work | Primary prior works cited include the SYK literature and holography: Sachdev & Ye (1993), Kitaev talks (2015), Maldacena & Stanford (2016), Jensen (AdS2 chaos), Maldacena et al. on conformal symmetry and AdS2, and series of generalized-SYK and higher-dimensional SYK papers (e.g., Gu, Qi & Stanford 2016; Berkooz et al. 2016; Murugan et al. on 2d SYK analogs), as referenced in the paper (see refs. [5-17], [26], [31-38], [44]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-kim-2026-08-13}`.
[code] 
    @misc{ast-ext-kim-2026-08-13,
      title        = {Extraction: Dirac fast scramblers},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-dirac-fast-scramblers.md},
      crossref     = {kim2020dirac},
      note         = {Theorizer's extraction from \cite{kim2020dirac}. asta-artifact id: extraction-result-82},
    }
    
    @article{kim2020dirac,
      title     = {Dirac fast scramblers},
      author    = {Jaewon Kim and E. Altman and Xiangyu Cao},
      year      = {2020},
      journal   = {Physical review B},
      url       = {https://www.semanticscholar.org/paper/224818216},
    }
[/code]
