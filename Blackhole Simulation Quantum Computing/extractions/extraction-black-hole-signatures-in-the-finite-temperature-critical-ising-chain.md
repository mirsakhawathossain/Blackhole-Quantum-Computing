[<- All artifacts](<../index.md>)

# Extraction: Black-Hole Signatures in the Finite-Temperature Critical Ising Chain

**Contents:**

  * Finite-temperature critical transverse-field Ising chain as a holographic simulator of BTZ black hole physics



### Finite-temperature critical transverse-field Ising chain as a holographic simulator of BTZ black hole physics

Field | Value  
---|---  
name_short | Critical Ising chain holography  
name_full | Finite-temperature critical transverse-field Ising chain as a holographic simulator of BTZ black hole physics  
brief_description | The paper shows that the 1D critical transverse-field Ising chain (g=1) exhibits quantitative boundary signatures that match a dual (2+1)-D gravitational description consisting of thermal AdS3 plus a BTZ black hole saddle, and identifies transport, relaxation and thermodynamic observables that map to horizon absorption, black-hole quasi-normal modes, and the Hawking–Page transition.  
citation_title | Black-Hole Signatures in the Finite-Temperature Critical Ising Chain  
mention_or_use | use  
target_system_or_model | Critical transverse-field Ising chain (1D spin-1/2 ring at g=1) whose low-energy continuum limit is the Ising CFT (free massless Majorana fermion, c = 1/2); dual gravitational model is (2+1)-D AdS3 with competing thermal-AdS and BTZ black-hole saddles (Z_grav = Z_AdS + Z_BTZ).  
black_hole_phenomena_targeted | Horizon absorption (antipodal excitation transport suppressed by BTZ saddle), quasi-normal modes (exponential relaxation governed by lowest BTZ QNM), Hawking–Page transition (thermodynamic signature in dS/dT of von Neumann entropy).  
simulation_paradigm | Analytic and classical numerical simulation based on exact solution (Jordan–Wigner + Bogoliubov) and thermal linear-response calculation (retarded Green's function) for large finite L (up to L=10^3); the paper also identifies the spin chain as an experimentally accessible target for programmable analog and digital quantum simulators (platform-agnostic proposal), but presents no gate-level quantum algorithm or hardware experiment.  
quantum_hardware_platform | platform-agnostic (paper cites programmable analog simulators and digital quantum computing platforms; references include trapped-ion and neutral-atom/Rydberg experimental platforms in refs.), but no experiment on actual quantum hardware in this work.  
encoding_and_mapping | Lattice spin-1/2 chain mapped to fermions via the Jordan–Wigner transformation; Bogoliubov transform diagonalizes the fermion Hamiltonian; continuum (low-energy) limit yields free Majorana fermion (Ising CFT) on a spatial circle of circumference 2π. Finite-system boundary conditions: Ramond (periodic) and Neveu–Schwarz (antiperiodic) fermion sectors are treated explicitly. On the holographic side, boundary thermal state maps to bulk partition Z_grav(T)=Z_AdS(T)+Z_BTZ(T) with Z_AdS(T)=exp[1/(8G T)] and Z_BTZ(T)=exp[π^2 ℓ^2 T/(2G)]. The local lattice operator n_j=(1-X_j)/2 flows to the CFT energy operator (scaling dimension Δ=1) in the continuum.  
algorithm_or_protocol | Compute linear-response observables from the exact finite-temperature retarded propagator G_R(t,s) derived from the fermionic diagonalization (see Supplemental S1): (i) generate a spatiotemporally localized source J_j(t) and evaluate δ⟨n_j(t)⟩_T = -Σ_j ∫ dt J_j(t) G_R(t_trans - t, j_antipode - j) to obtain antipodal transport at t_trans=π; (ii) compute spatially summed retarded response R(t)= -i θ(t) Σ_j ⟨[n_j(t), n_1(0)]⟩ and analyze long-time decay for QNM behavior; (iii) compute thermal von Neumann entropy S(T) = -tr[ρ(T) ln ρ(T)] from exact diagonalization/thermal ensemble. Numerical methods: exact diagonalization/closed-form sums over Bogoliubov modes, Pfaffian methods and large-L evaluation; no Trotterization/quantum gates or quantum Gibbs-state preparation protocols are used.  
resource_estimates | No quantum-resource estimates (qubits, gate counts, fault-tolerance thresholds) are provided. Classical numerical resources: system sizes reported up to L = 10^3 for R(t) and entropy calculations. No measurement-shot or circuit-depth accounting for quantum hardware proposals is given.  
noise_and_error_mitigation | Not applicable to presented classical/analytic calculations; the paper does not specify noise models or error-mitigation strategies for the suggested experimental realization on quantum hardware.  
key_results_or_demonstrations | Three core, mutually consistent signatures obtained via analytic theory + classical numerics: (1) Antipodal transport amplitude at t_trans=π collapses for various L and angular momenta M onto the universal curve |δ⟨n_antipode⟩ _T|/|δ⟨n⟩_ | = Z_AdS(T)/Z_grav(T) with fitted effective parameters ℓ_eff = 1.28 and G_eff = 1.33; (2) In the high-T, BTZ-dominated regime, |R(t)| shows exponential decay |R(t)| ∝ exp[-(2πTΔ) t] with Δ = 1 (prediction ω_QNM = -i 2π T Δ), plus a small temperature-dependent offset ≈ exp(-π^2 T/2)/2; (3) Von Neumann entropy derivative dS/dT develops a pronounced minimum at T = 0.16±0.01, matching the Hawking–Page temperature T_HP = 1/(2πℓ) ≈ 0.16 for ℓ_classical=1. These are theoretical/numerical demonstrations (not hardware experiments).  
validation_and_benchmarks | Multiple consistency checks and validations: direct comparison of lattice/numerical results to gravitational predictions (universal partition-weight formula eq. (3)), analytic QNM prediction ω_QNM = -i2πTΔ for Δ=1 and observed exponential relaxation, entropy behavior compared to S_grav(T) from Z_grav(T); exact solution via Jordan–Wigner and Bogoliubov transformations (Supplemental S1); Pfaffian/ED-based numerical methods and finite-size scaling up to L=10^3; consistency check of fitted (ℓ_eff,G_eff) with higher-curvature correction relation (Eq. S44) and SSE analysis (Supplemental S4).  
claimed_feasibility | Authors argue that critical quantum spin chains are minimal and experimentally accessible platforms for probing dynamical and thermodynamic aspects of black-hole physics, citing the maturity of programmable analog simulators and digital quantum platforms; however, they do not provide quantitative resource/timeline claims, and note that small central charge (c=1/2) places the bulk in a strongly quantum regime requiring renormalized effective gravitational parameters.  
limitations_and_open_problems | Explicit limitations noted: (i) small central charge (c = 1/2) means semiclassical bulk gravity is not strictly valid and higher-curvature / quantum-gravity corrections are important—authors treat these via renormalized (ℓ_eff,G_eff); (ii) work uses a phenomenological dual (thermal-AdS + BTZ saddle) rather than a controlled semiclassical derivation for c small; (iii) results are from analytic/classical numerics on lattice spin chains, not from quantum-hardware implementations—no circuit/resource/noise analysis; (iv) finite-size and continuum-limit approximations apply (finite L, mapping of lattice n_j to CFT operator is approximate with subleading corrections); (v) bulk spacetime is not dynamical in experiment—only boundary observables are accessed; (vi) no complexity/hardness or verification protocols for quantum realizations are provided.  
complexity_or_hardness_arguments | None presented. The paper does not make explicit complexity-theoretic claims (BQP/QMA hardness or classical intractability) about simulating these phenomena on quantum devices.  
theory_context_keywords | AdS/CFT, holographic duality, Ising CFT (c=1/2), BTZ black hole, thermal AdS, Hawking–Page transition, quasi-normal modes (QNMs), horizon absorption, Jordan–Wigner transform, Majorana fermion, higher-curvature corrections, gravitational partition-saddle competition.  
citations_to_prior_work | Key referenced works include: Maldacena 'The Large-N Limit of Superconformal Field Theories and Supergravity' (AdS/CFT foundational work), traversable-wormhole quantum processor experiment 'Traversable Wormhole Dynamics on a Quantum Processor' (Nature 2022, Jafferis et al.), Kitaev 'A Simple Model of Quantum Holography' (SYK context), works on holography in spin chains (e.g., 'Spacetime-Localized Response in Quantum Critical Spin Systems: Insights from Holography' Phys. Rev. D 2024, and related refs 26–29), Hawking & Page 'Thermodynamics of Black Holes in Anti-de Sitter Space' (1983), BTZ black hole original papers (Bañados, Teitelboim & Zanelli), and 'Quantum BTZ Black Hole' (Emparan, Frassino & Way, JHEP 2020).  
  
## Citation

Cite this artifact as `\cite{ast-ext-wang-2026-08-13}`.
[code] 
    @misc{ast-ext-wang-2026-08-13,
      title        = {Extraction: Black-Hole Signatures in the Finite-Temperature Critical Ising Chain},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-black-hole-signatures-in-the-finite-temperature-critical-ising-chain.md},
      crossref     = {wang2026blackhole},
      note         = {Theorizer's extraction from \cite{wang2026blackhole}. asta-artifact id: extraction-result-47},
    }
    
    @article{wang2026blackhole,
      title     = {Black-Hole Signatures in the Finite-Temperature Critical Ising Chain},
      author    = {Zuo Wang and Liang He},
      year      = {2026},
      url       = {https://www.semanticscholar.org/paper/286377042},
    }
[/code]
