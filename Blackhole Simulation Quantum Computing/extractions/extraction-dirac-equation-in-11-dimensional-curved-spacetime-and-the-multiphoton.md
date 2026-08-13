[<- All artifacts](<../index.md>)

# Extraction: Dirac Equation in (1+1)-Dimensional Curved Spacetime and the Multiphoton Quantum Rabi Model.

**Contents:**

  * Multiphoton Quantum Rabi Model simulation of a (1+1)-dimensional black hole with a trapped ion
  * Naked-source (constant-acceleration) weak-gravity mapping to QRM



### Multiphoton Quantum Rabi Model simulation of a (1+1)-dimensional black hole with a trapped ion

Field | Value  
---|---  
name_short | QRM-BH-TrapIon  
name_full | Multiphoton Quantum Rabi Model simulation of a (1+1)-dimensional black hole with a trapped ion  
brief_description | Exact mapping of the (1+1)-dimensional Dirac equation in the background of a (1+1)-D black hole metric to a multiphoton quantum Rabi model (QRM) enabling an analog trapped-ion quantum simulation of a Dirac particle in curved spacetime; proposes implementation via first and second sideband laser drivings and validates predictions with numerically exact simulations.  
citation_title | here  
mention_or_use | use  
target_system_or_model | (1+1)-dimensional black hole in a semiclassical gravity theory with diagonal metric g_{\mu\nu}=diag[\alpha(x), -1/\alpha(x)], where for the black-hole solution \alpha(x)=|x|/r_s - 1 and r_s=1/(2M). The dynamical object is a single-particle Dirac equation (first-quantization) in this fixed curved background.  
black_hole_phenomena_targeted | Free-fall trajectories of a Dirac particle toward the horizon; gravitational redshift (mapped to bosonic quadrature X/r_s); persistence and decay of Zitterbewegung in curved spacetime; spatial squeezing of the particle wavefunction induced by the gravitational metric. (The proposal does NOT target Hawking radiation, Page curve, or QFT particle-creation at the level of second quantization.)  
simulation_paradigm | Analog quantum simulation (continuous-time Hamiltonian engineering). The target Dirac-in-curved-spacetime Hamiltonian is encoded as a multiphoton quantum Rabi Hamiltonian implemented directly in the trapped-ion analog device.  
quantum_hardware_platform | Trapped-ion platform: a single trapped ion with one motional (bosonic) mode and two internal levels (qubit) is assumed.  
encoding_and_mapping | Canonical mapping: define operator X = r_s sqrt(\alpha(\hat{x})), P = -i\hbar \partial/\partial X with [X,P]=i\hbar. Map bosonic quadratures to ion motional mode: \hat{X} = (\lambda/\sqrt{2})(a + a^{\dagger}), \hat{P} = (\hbar/(i\lambda\sqrt{2}))(a - a^{\dagger}). The two-component Dirac spinor maps to the ion's two internal states (Pauli operators). Under this mapping the Dirac Hamiltonian becomes H_D = (c/(4i r_s))\sigma_x (a^2 - a^{\dagger 2}) + (m c^2 \lambda/(\sqrt{2} r_s)) \sigma_z (a + a^{\dagger}) (Eq. (6)); a local Pauli rotation is used to change \sigma_z to \sigma_y for implementation convenience. Boundary/region: particle restricted to x>r_s (mapping uses X>0). The mapping is exact for the (1+1)-D black hole metric used; for the naked-source case a weak-field approximation (M|x| << 1) is used and a displacement relates it to the black-hole mapping.  
algorithm_or_protocol | Analog Hamiltonian engineering using laser-driven sideband interactions: implement linear (a + a^{\dagger}) coupling with first red/blue sidebands and the two-photon squeezing term (a^2 - a^{\dagger 2}) with second red/blue sidebands. Time evolution is continuous under the engineered Hamiltonian (no digital Trotterization). Measurement protocol: reconstruct motional density and moments by mapping motional state to internal state via sideband techniques (as in Refs. cited) to obtain observables (\langle X^2\rangle, reconstructed x via x = X^2/r_s + r_s, variances, density profiles).  
resource_estimates | No explicit qubit/gate counts or circuit-depth estimates are provided. Experimental resources described qualitatively: a single trapped ion, one motional mode (bosonic Hilbert space, truncated in practice by motional state energy), two-level internal state, ability to drive first and second sidebands independently with controllable Rabi frequencies and Lamb-Dicke parameters (relations given: \eta\Omega_{r,b} = ± m c^2 \lambda/(\sqrt{2} r_s) and \eta_2^2\Omega_{r,2}=\eta_2^2\Omega_{b,2}=\hbar c/(4 r_s)). The paper emphasizes parameter tunability but gives no numeric counts of shots, gates, or FT overhead.  
noise_and_error_mitigation | No detailed noise model or quantitative error-mitigation protocol is provided. Experimental constraints/assumptions mentioned: operation in the Lamb-Dicke regime, independent control of first/second sideband Rabi frequencies and Lamb-Dicke parameters, and the possibility to vary drive amplitudes (including time dependence) to simulate time-dependent metrics. No explicit mitigation methods (ZNE, PEC, error-correcting codes) or error budgets are given.  
key_results_or_demonstrations | Proposal + numerically exact simulations (no hardware demo). Core numerical demonstrations: (i) simulation of free fall of a massive Dirac particle using H_D with parameters m\lambda=0.3, M\lambda=0.01, c=1 and initial Gaussian motional state displaced to X_0/\lambda=8 and internal state |+>_x; (ii) observation of oscillatory trajectory (Zitterbewegung) in the simulated particle position that decreases in amplitude approaching the horizon; (iii) persistent interference pattern in density (interpreted as overlap of positive and negative energy components trapped by gravity) and suppression for massless case; (iv) pronounced squeezing of motional state as evidenced by decreasing \Delta X(t) and exponentially growing \Delta P(t) as the particle approaches horizon (Fig. 2). The demonstration is theoretical/numerical and an experimental implementation recipe is given.  
validation_and_benchmarks | Validation methods used in the paper: (i) numerically exact integration of the proposed Hamiltonian and comparison with analytic/semi-analytic expectations; (ii) comparison of massless-case dynamics to analytic geodesic solutions (closed-form solutions for massless trajectories are derived and matched numerically); (iii) use of derived Heisenberg equations and semiclassical limits (requirement \lambda_c = h/(mc) \ll r_s) to check regimes of validity; (iv) mathematical arguments (e.g., Cauchy-Schwarz) to show decay of Zitterbewegung near horizon; (v) cross-reference to standard trapped-ion state measurement/tomography protocols (Refs. [42,56,61]) as feasible measurement tools. No cross-platform/hardware benchmarks or experimental noise simulations presented.  
claimed_feasibility | Authors claim feasible implementation with current trapped-ion technology: single-ion experiments with first and second sideband drivings are standard, Lamb-Dicke and Rabi controls available, motional-state preparation techniques (displacements, Bang-Bang) referenced. They emphasize the mapping's parameter rescaling freedom (1/r_s is an overall timescale factor) which relaxes some experimental constraints. No explicit timeline or resource threshold (NISQ vs fault-tolerant) is given; proposal is positioned as a near-term analog experiment rather than requiring FTQC.  
limitations_and_open_problems | Explicit limitations called out: (i) model limited to (1+1)-dimensional modified gravity where all metrics are conformally flat — extension to higher dimensions appears difficult; (ii) semiclassical gravity, fixed background metric (no backreaction, no dynamical spacetime quantization); (iii) first-quantization single-particle Dirac equation only — does not capture quantum field effects such as Hawking radiation or particle creation in second quantization; (iv) for the 'naked source' solution mapping is only valid in weak-field approximation (M|x| << 1); (v) requirement for semiclassical approximation: Compton wavelength << Schwarzschild radius (\lambda_c \ll r_s); (vi) horizon is a coordinate boundary in the mapping (particle does not cross x=r_s in the mapping); (vii) no explicit resource scaling, error budgets, or noise robustness analysis provided.  
complexity_or_hardness_arguments | No complexity-theoretic claims (no BQP/QMA hardness statements or classical-intractability proofs) are made in the paper.  
theory_context_keywords | Dirac equation in curved spacetime, (1+1)-dimensional black hole, semiclassical gravity, multiphoton quantum Rabi model, trapped-ion quantum simulation, squeezing, Zitterbewegung, gravitational redshift, anticommutator generator of squeezing, bosonic quadratures mapping.  
citations_to_prior_work | Paper situates itself with references to analog gravity literature (Unruh 1981 and reviews), trapped-ion simulations of Dirac fermions in flat spacetime (Refs. [41-45], Gerritsma et al. Nature 2010 [42], Pedernales et al. Sci Rep 2015 [43], Gerritsma et al. PRL 2011 [56]), prior works on squeezing and cosmological particle creation in analog systems (Schützhold et al. PRL 2007 [49], Jacobson lectures [47], Barceló/Liberati/Visser [11]), and the (1+1)-dimensional black hole solution used (R. B. Mann et al. Phys. Rev. D 1991 [46]).  
  
### Naked-source (constant-acceleration) weak-gravity mapping to QRM

Field | Value  
---|---  
name_short | NakedSource-WeakField  
name_full | Naked-source (constant-acceleration) weak-gravity mapping to QRM  
brief_description | A related mapping for the 'naked source' solution (no horizon) in the weak-gravity limit M|x| << 1 maps the Dirac equation to a QRM with additional mass-position term; can be implemented in trapped ions in the weak-field (constant acceleration) regime and is equivalent to the black-hole mapping up to a displacement.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Naked-source (no black hole) diagonal metric with \alpha(x)=2M|x|+1 (or small perturbation of Minkowski), approximated for weak gravity M|x| << 1; effectively models a constant acceleration field in a small region.  
black_hole_phenomena_targeted | Models free-fall under a constant acceleration (weak gravity) and can be used to study equivalence-principle-like scenarios and free-fall of Dirac particles in a Newtonian potential analog; not targeting horizon phenomena.  
simulation_paradigm | Analog quantum simulation via trapped-ion Hamiltonian engineering; mapping is approximate (perturbative weak-field expansion).  
quantum_hardware_platform | Trapped ions (single ion: motional mode + two-level internal state).  
encoding_and_mapping | Use small-M expansion of metric; expand anticommutator to linear order in M and map position and momentum to mode operators via x = (\lambda/\sqrt{2})(a + a^{\dagger}), p = (\hbar/(i\lambda\sqrt{2}))(a - a^{\dagger}). The result is a one- and two-photon QRM plus an extra mass-position coupling term m c^2 M x. Up to a displacement X\mapsto X-X_d (X_d=-1/(2M)) this is equivalent to the black-hole mapping in the main text (valid only in the weak-field regime).  
algorithm_or_protocol | Same analog trapped-ion protocol: first and second sideband drivings realize the linear and squeezing terms; motional-state preparation and readout as for the black-hole mapping.  
resource_estimates | Qualitative only: single ion, motional truncation required in practice; no explicit numeric resource counts.  
noise_and_error_mitigation | Not discussed beyond standard trapped-ion operational assumptions (Lamb-Dicke, sideband control).  
key_results_or_demonstrations | Analytical derivation of mapping in weak-field limit (Eq. (34) in Supplemental), and statement that this mapping matches the black-hole mapping up to a displacement; suggests possibility to study free-fall and equivalence-principle aspects in trapped ions.  
validation_and_benchmarks | Analytic perturbative derivation and demonstration of equivalence with the displaced black-hole Hamiltonian; referenced standard trapped-ion motional-state preparation/measurement methods for experimental validation.  
claimed_feasibility | Presented as implementable with current trapped-ion techniques in the weak-field regime; emphasizes the mapping is approximate and valid only when M|x| << 1.  
limitations_and_open_problems | Validity limited to weak-gravity (small M) and small spatial region; extra mass-position term appears (not present in exact black-hole mapping) and must be handled experimentally; not applicable to horizon physics.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | Weak-field expansion, constant acceleration analog, equivalence principle tests, displaced QRM mapping.  
citations_to_prior_work | References include the same trapped-ion Dirac-simulation literature and analog-gravity works; mapping related to derivations in Refs. [41-43,55] and canonical trapped-ion implementations.  
  
## Citation

Cite this artifact as `\cite{ast-ext-pedernales-2026-08-13}`.
[code] 
    @misc{ast-ext-pedernales-2026-08-13,
      title        = {Extraction: Dirac Equation in (1+1)-Dimensional Curved Spacetime and the Multiphoton Quantum Rabi Model.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-dirac-equation-in-11-dimensional-curved-spacetime-and-the-multiphoton.md},
      crossref     = {pedernales2017dirac},
      note         = {Theorizer's extraction from \cite{pedernales2017dirac}. asta-artifact id: extraction-result-90},
    }
    
    @article{pedernales2017dirac,
      title     = {Dirac Equation in (1+1)-Dimensional Curved Spacetime and the Multiphoton Quantum Rabi Model.},
      author    = {J. S. Pedernales and M. Beau and S. Pittman and Í. Egusquiza and L. Lamata and E. Solano and E. Solano and E. Solano and A. Campo},
      year      = {2017},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/21724556},
    }
[/code]
