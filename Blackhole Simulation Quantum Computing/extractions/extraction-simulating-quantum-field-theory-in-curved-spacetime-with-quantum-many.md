[<- All artifacts](<../index.md>)

# Extraction: Simulating quantum field theory in curved spacetime with quantum many-body systems

**Contents:**

  * One-to-one mapping between massless quantum fields in static 1+1 curved spacetime and site-dependent bosonic/fermionic hopping models
  * Numerical simulation of analogue Hawking radiation on the lattice site-dependent hopping model
  * Study of quantum chaos and fastest scrambling via OTOCs and level statistics in the mapped lattice models



### One-to-one mapping between massless quantum fields in static 1+1 curved spacetime and site-dependent bosonic/fermionic hopping models

Field | Value  
---|---  
name_short | 1+1 QFT -> site-dependent hopping  
name_full | One-to-one mapping between massless quantum fields in static 1+1 curved spacetime and site-dependent bosonic/fermionic hopping models  
brief_description | A constructive mapping showing that a massless scalar field in any static 1+1 curved spacetime discretizes to a site-dependent bosonic hopping Hamiltonian, and a massless Dirac field maps to a site-dependent free fermionic Hubbard model which via Jordan–Wigner equals a site-dependent isotropic XY spin chain.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in static 1+1 dimensional curved spacetime (massless scalar and massless Dirac) mapped to lattice many-body models: site-dependent bosonic hopping model, free Hubbard (fermionic) model, and site-dependent isotropic XY spin model.  
black_hole_phenomena_targeted | General black-hole phenomena in 1+1: horizon physics encoding (metric into hopping), enabling study of Hawking radiation (thermal spectrum), entanglement across horizon, and chaotic behavior/scrambling in black-hole backgrounds.  
simulation_paradigm | Analog quantum simulation proposal (quantum many-body system realizes lattice Hamiltonian corresponding to the curved-space QFT) plus classical numerical simulation (exact diagonalization/time evolution) of the lattice model.  
quantum_hardware_platform | Primary proposal: trapped-ion phonon modes (linear Paul trap); authors also mention other platforms as possible (optical lattices, superconducting qubits) — but trapped ions are the concrete suggested platform.  
encoding_and_mapping | Spatial discretization x = n d; central-difference approximation of continuum evolution equation (massless limit) yields single-particle Schrödinger-like evolution i d/dv w_n = -kappa_n w_{n-1} - kappa_{n+1} w_{n+1} - mu w_n. For bosons: field operator tilde{w}_n - > a_n / sqrt(d) giving bosonic hopping Hamiltonian H = sum_n [-kappa_n(a_n^† a_)/(8 d) — thus metric function f(x) directly encoded into site-dependent hopping. For Dirac: replace by fermionic operators c_n with same hopping coefficients; Jordan–Wigner maps fermions to spin operators yielding an isotropic XY model with site-dependent couplings. Low-energy/continuum limit, finite cutoff (|n|<=L) and single-particle truncation (N=1) used in numerics; chemical potential mu corresponds to arbitrary constant in continuum reduction.}+h.c.) - mu a_n^† a_n]. kappa_n = (f_n + f_{n-1  
algorithm_or_protocol | Analog Hamiltonian simulation (engineer site-dependent hopping and let system evolve under natural Hamiltonian); diagnostics performed by (classical) exact diagonalization and unitary time evolution of the lattice Hamiltonian to compute spectral probabilities, reduced density matrices (entanglement entropy), and OTOCs. Experimental protocol suggested: implement site-dependent hopping via Raman-laser-induced phonon hopping between axial modes in a linear ion chain (use N ions and N-1 laser pairs). Measurement protocols: projective measurements of site occupation/probabilities, reconstruction of reduced density matrices for entropy, and time-resolved operator measurements to construct OTOCs.  
resource_estimates | No gate-counts or qubit numbers for a digital device are given. Experimental-resource statements: to simulate n-site Hubbard modes need to trap N ions and use N-1 pairs of Raman lasers to drive transitions between N axial phonon modes. Numerical resource examples: finite-lattice cutoff with 2L+1 sites; example L=300, d=0.1 used in some numerics; Hilbert-space dimension example: for many-particle case 2L+1 = N = 13 gives D ~ 5e6, motivating the use of N=1 simplification (single-particle) with D = 2L+1. No fault-tolerance overheads, shot counts, circuit depths, or explicit scaling laws for qubits/circuit complexity are provided.  
noise_and_error_mitigation | No quantitative noise model or error-mitigation protocol is provided. Paper neglects gravitational backreaction (G -> 0) and treats continuum trans-Planckian issues by truncation/cutoff; experimental imperfections (decoherence, heating in trapped ions, laser phase noise) are not modeled or mitigated in the manuscript.  
key_results_or_demonstrations | Proposal + classical numerical demonstrations on the lattice mapping: (1) Hawking-radiation analogue: starting from a single particle inside the analog horizon, the probability P(E) of finding a particle outside follows approximately a thermal (blackbody) spectrum P(E) ~ exp(-E/T_H) for low-energy modes, with fitted temperature T approximately equal to the analytic Hawking temperature T_H of the chosen metric (e.g., f(x)=alpha tanh x, T_H = alpha/(4 pi)). (2) Entanglement: entanglement entropy between inner and outer regions increases during emission and saturates for single-particle initial conditions. (3) Chaos / scrambling: computed OTOC C(v) = -Tr(rho [N_{n0}(v), N_{n0}]^2) shows early-time exponential growth with fitted Lyapunov exponent lambda_L ≈ 2 pi T_H, approximately saturating the chaos bound; (4) Level statistics: nearest-neighbor spacing P(s) shows Poisson-like distribution in pure-AdS (no horizon) but deviates (non-Poisson) when horizon is present, indicating a transition towards non-integrability. All demonstrations are numerical simulations of the discretized many-body Hamiltonians (classical computations), with an experimental implementation suggested but not performed.  
validation_and_benchmarks | Analytic tunneling calculation in Appendix A yields Hawking temperature T_H = g_h/(2 pi); numerical P(E) is compared to this blackbody law (Eq. 23) and deviations at very low energies are attributed to finite-size/IR cutoff. OTOC growth is benchmarked against the theoretical chaos bound (Maldacena–Shenker–Stanford) and fitted to exponential behaviour C(t) ~ exp(lambda_L t). Level-spacing distributions are compared against Poisson statistics (integrable) and referenced distributions (Wigner/Brody) to identify non-integrable signatures. Numerical methods: exact diagonalization / direct time evolution on finite lattices with explicit cutoffs; single-particle Hilbert-space checks where feasible.  
claimed_feasibility | Authors claim experimental feasibility in trapped-ion systems by engineering site-dependent phonon hopping via Raman lasers; the mapping is conceptually platform-agnostic (optical lattices, superconducting qubits also mentioned). They emphasize that low-energy Hawking physics is robust under truncation and thus accessible in analog simulators. However, large-N many-body simulations (multiple particles, full thermofield double states, or backreaction) are limited by Hilbert-space growth and control requirements; no explicit NISQ vs FTQC timeline is provided.  
limitations_and_open_problems | Explicit limitations discussed: analysis restricted to massless fields in static 1+1 spacetimes (toy-model), neglect of matter backreaction on geometry (semiclassical fixed background, G->0), discretization valid only in low-energy smooth limit (d << effective wavelength), trans-Planckian problem handled by truncation/cutoff which affects very-low/high-energy modes, numerical results simplified to N=1 (single-particle) due to exponential Hilbert-space growth, no experimental noise/error analysis, and no construction of full many-body thermofield-double states or dynamical spacetime. Authors note that finite-size cutoffs cause deviations from analytic predictions at the lowest energies.  
complexity_or_hardness_arguments | No explicit complexity-theoretic hardness claims (no BQP/QMA statements). The paper references scrambling time scaling t_* ≥ (1/(2 pi T)) ln N_f^2 from the holographic literature, but does not provide reductions or complexity lower bounds for simulating these models.  
theory_context_keywords | analog gravity, AdS/CFT, Hawking radiation, entanglement entropy, fast scrambling conjecture, out-of-time-order correlator (OTOC), chaos bound (Maldacena-Shenker-Stanford), site-dependent hopping, Jordan-Wigner mapping, trans-Planckian problem  
citations_to_prior_work | Key referenced works include: W. G. Unruh, "Experimental black-hole evaporation?"; Parikh & Wilczek, "Hawking radiation as tunneling"; Maldacena, "The Large N limit of superconformal field theories and supergravity"; Maldacena, Shenker & Stanford, "A bound on chaos"; Sekino & Susskind, "Fast Scramblers"; J. S. Pedernales et al., "Dirac Equation in (1+1)-Dimensional Curved Space-time and the Multiphoton Quantum Rabi Model"; Porras & Cirac, "Bose-einstein condensation and strong-correlation behavior of phonons in ion traps"; reviews on analogue gravity by Barceló, Liberati & Visser and others. (These titles and authors are cited in the paper's bibliography.)  
  
### Numerical simulation of analogue Hawking radiation on the lattice site-dependent hopping model

Field | Value  
---|---  
name_short | Hawking-radiation numerics  
name_full | Numerical simulation of analogue Hawking radiation on the lattice site-dependent hopping model  
brief_description | Classical numerical experiments on the discretized site-dependent hopping Hamiltonian showing that single-particle emission across an encoded horizon produces an approximately thermal energy distribution and increases entanglement between inside and outside regions.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Discretized bosonic hopping model with hopping coefficients set by a chosen static 1+1 black-hole metric (examples: f(x)=alpha tanh x with horizon at x=0).  
black_hole_phenomena_targeted | Hawking radiation spectrum (thermal emission), entanglement growth between inside and outside regions (von Neumann entropy).  
simulation_paradigm | Classical numerical simulation of finite lattice Hamiltonian (exact diagonalization and time evolution) representing the analog quantum-many-body model; experimental implementation proposed but not executed.  
quantum_hardware_platform | Concrete experimental suggestion: trapped-ion phonon modes implementing Bose-Hubbard-like phonon hopping; numerical work is platform-independent (classical computation).  
encoding_and_mapping | Choose metric f(x)=alpha tanh x, discretize space x_n = n d, compute kappa_n = (f_{n}+f_{n-1})/(8 d), impose finite cut-off n in [-L,L] with kappa_n=0 outside cutoff. Map single-particle field to basis states |e_n> (occupation at site n) giving Hilbert-space dimension 2L+1; initial state |e_{n0}> places a particle inside horizon. Chemical potential set mu=0 for number conservation. Single-particle approximation used in numerics (N=1).  
algorithm_or_protocol | Construct finite Hamiltonian matrices (H_in, H_out, H_0) and evolve initial single-particle state |Ψ(0)⟩ = |e_{n0}⟩ via |Ψ(v)⟩ = exp(-i H v) |Ψ(0)⟩. Compute probability of finding particle in outer-region eigenmodes and histogram energies E_n to obtain P(E). Compute reduced density matrix for outer region by tracing inner degrees and compute S(v) = -Tr[rho ln rho].  
resource_estimates | Numerical parameters provided: example d=0.1, L=300, alpha=10 for Hawking plots. Hilbert-space growth: for many-particle cases (e.g., 2L+1 = N =13) dimension D ~ 5x10^6 prevented full many-particle numerics; thus authors use N=1. No experimental counts of measurements or laser resources beyond statement 'N ions and N-1 pairs of lasers for N sites'.  
noise_and_error_mitigation | Not discussed for numerics beyond noting finite-size cutoffs cause low-energy deviations; experimental noise not modeled.  
key_results_or_demonstrations | Numerical P(E) fits blackbody form P(E) ∼ exp(-E/T_H) for early times and energies above finite-size low-energy cutoff; entanglement entropy between inner and outer regions increases during emission and saturates for single-particle case; deviations at lowest energies attributed to finite lattice/IR cutoff.  
validation_and_benchmarks | Comparison of numerical P(E) with analytic tunneling-derived blackbody spectrum (Appendix A) and the Hawking temperature formula T_H = g_h/(2 pi); finite-size cutoff effects analyzed qualitatively.  
claimed_feasibility | Authors argue low-energy Hawking features are robust to truncation and therefore accessible in analogue simulators; however, many-particle simulations are numerically hard and require more resources experimentally.  
limitations_and_open_problems | Single-particle simulations (N=1) only; finite lattice cutoff induces low-energy deviations; no experimental demonstration; backreaction ignored; truncation required to avoid trans-Planckian issues.  
complexity_or_hardness_arguments | No complexity statements; numerical cost limited by exponential growth of many-body Hilbert space.  
theory_context_keywords | Hawking radiation, tunneling derivation, site-dependent hopping lattice, entanglement entropy, continuum cutoff  
citations_to_prior_work | Analytic tunneling references and analogue gravity literature: Damour & Ruffini "Black Hole Evaporation in the Klein-Sauter-Heisenberg-Euler Formalism"; Parikh & Wilczek "Hawking radiation as tunneling"; reviews by Unruh and analogue-gravity experiments (e.g., Steinhauer observations) are cited.  
  
### Study of quantum chaos and fastest scrambling via OTOCs and level statistics in the mapped lattice models

Field | Value  
---|---  
name_short | Chaos/OTOC analogue  
name_full | Study of quantum chaos and fastest scrambling via OTOCs and level statistics in the mapped lattice models  
brief_description | Numerical study showing early-time exponential growth of an out-of-time-order correlator in the lattice analogue of a black-hole background with a Lyapunov exponent approximately saturating the chaos bound, and a change in level-spacing statistics when a horizon is present.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Site-dependent bosonic hopping / free fermionic Hubbard / isotropic XY lattice models with hopping coefficients given by black-hole-like metrics (example f(x)=x^2(1-x_h/x) to model an asymptotically AdS_2 black hole).  
black_hole_phenomena_targeted | Quantum chaos diagnostics: OTOC growth (Lyapunov exponent), scrambling time scaling, and spectral statistics (nearest-neighbor level spacing) as analogues of black-hole fast scrambling and chaoticity.  
simulation_paradigm | Classical numerical simulation (exact diagonalization/time evolution) of finite lattice Hamiltonians; conceptual analog quantum simulation (same Hamiltonian) could realize dynamics in hardware.  
quantum_hardware_platform | Numerics are platform-agnostic; experimental mapping suggested to trapped-ion phonon modes but no hardware experiment performed.  
encoding_and_mapping | Same discretization and mapping as main framework: kappa_n from chosen f(x); define smooth local operator N_{n0} as Gaussian-weighted sum of site occupations around n0 to avoid delta-like singularities in continuum limit. Initial state for thermal OTOC is a thermal state rho_out over positive-energy outer-region eigenmodes.  
algorithm_or_protocol | Compute OTOC C(v) = -Tr(rho [N_{n0}(v), N_{n0}]^2) with Heisenberg evolution N_{n0}(v) = exp(-i H v) N_{n0} exp(i H v). Numerically evaluate C(v) and fit early-time growth to exponential form C(v) ~ exp(lambda_L v) to extract lambda_L. Compute level-spacing distribution P(s) from diagonalization of H_out and compare to Poisson/Wigner/Brody distributions.  
resource_estimates | Numerical parameter examples: d values scanned (0.01,0.02,0.04,0.08), x_h choices (1,10), cut-off boundary x_m = 5 x_h used in level statistics; thermal initial states built by summing over positive-energy outer-region eigenmodes. No qubit/gate counts or measurement budgets provided.  
noise_and_error_mitigation | Not discussed beyond finite-size/cutoff considerations; no noise modeling for experiments.  
key_results_or_demonstrations | Numerical OTOCs show an early-time exponential increase with fitted slope lambda_L ≈ 2 pi T_H, thereby approximately saturating the chaos bound. Level-spacing statistics: pure-AdS (x_h=0) yields Poisson distribution (integrable), while nonzero horizon (x_h != 0) yields deviation from Poisson, indicating non-integrability/chaotic signatures. The time window of exponential growth increases as lattice spacing d decreases, consistent with continuum limit expectations.  
validation_and_benchmarks | OTOC exponential growth is benchmarked against theoretical chaos bound lambda_L <= 2 pi T and literature on scrambling; level-spacing distributions compared to Poisson statistics for integrable systems. Dependence on lattice spacing and cutoffs is studied numerically.  
claimed_feasibility | Authors suggest these chaos diagnostics could be probed in analogue many-body systems implementing the site-dependent couplings; however, large degrees of freedom and long-time dynamics may be constrained by hardware and finite-size effects. No specific NISQ/FT thresholds provided.  
limitations_and_open_problems | Results based on finite lattices and often on single-particle or small-size numerics; neglect backreaction; bounded operator norms on lattice imply exponential growth must stop at finite time (authors discuss that continuum limit d->0 would push scrambling time to infinity under neglected backreaction). Preparation of thermal states for many-body experiments and measurement of OTOCs in hardware are not addressed in experimental detail.  
complexity_or_hardness_arguments | No formal complexity arguments. The paper references the conjectured scaling of scrambling time with degrees of freedom from holographic literature but does not present computational hardness proofs.  
theory_context_keywords | OTOC, Lyapunov exponent, chaos bound, fast scrambling, level-spacing statistics, Poisson vs Wigner, AdS_2 black hole analogue, holographic chaos  
citations_to_prior_work | Relevant citations include Maldacena, Shenker & Stanford "A bound on chaos"; Sekino & Susskind "Fast Scramblers"; random-matrix literature on level statistics (e.g., Guhr et al. "Random-matrix theories in quantum physics"); and earlier analogue gravity and QFT-in-curved-space references.  
  
## Citation

Cite this artifact as `\cite{ast-ext-yang-2026-08-13}`.
[code] 
    @misc{ast-ext-yang-2026-08-13,
      title        = {Extraction: Simulating quantum field theory in curved spacetime with quantum many-body systems},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-simulating-quantum-field-theory-in-curved-spacetime-with-quantum-many.md},
      crossref     = {yang2019simulating},
      note         = {Theorizer's extraction from \cite{yang2019simulating}. asta-artifact id: extraction-result-28},
    }
    
    @article{yang2019simulating,
      title     = {Simulating quantum field theory in curved spacetime with quantum many-body systems},
      author    = {Run-Qiu Yang and Hui Liu and Shi-ning Zhu and L. Luo and R. Cai},
      year      = {2019},
      journal   = {Physical Review Research},
      url       = {https://www.semanticscholar.org/paper/218502756},
    }
[/code]
