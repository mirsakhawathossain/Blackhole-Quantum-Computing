[<- All artifacts](<../index.md>)

# Extraction: Spin systems as quantum simulators of quantum field theories in curved spacetimes

**Contents:**

  * Spin-1/2 chain as a quantum simulator of (1+1)-D quantum field theory in curved spacetime
  * Simulation of FLRW-expanding-universe Majorana particle production using the transverse-field Ising model with time-dependent transverse field
  * Observation of the Unruh effect through entanglement Hamiltonian mapping of the transverse-field Ising model
  * Hawking radiation / black-hole thermal radiation (motivational mention and future target)



### Spin-1/2 chain as a quantum simulator of (1+1)-D quantum field theory in curved spacetime

Field | Value  
---|---  
name_short | Spin-chain QFT simulator  
name_full | Spin-1/2 chain as a quantum simulator of (1+1)-D quantum field theory in curved spacetime  
brief_description | A constructive mapping showing that a one-dimensional spin-1/2 chain with site- and time-dependent XY-exchange and transverse fields reduces in the long-wavelength continuum limit to a free Majorana fermion QFT on an arbitrary two-dimensional metric; provides an explicit dictionary between metric functions and spin-chain parameters.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory of a free Majorana fermion in general (1+1)-dimensional curved spacetime (metric parametrized by α(t,x),β(t,x),γ(t,x))  
black_hole_phenomena_targeted | General curved-spacetime phenomena (motivates black-hole phenomena such as Hawking radiation and horizon physics) and specific horizon-analog phenomena (Rindler/Unruh effect); paper demonstrates expanding-universe particle production and Rindler mapping explicitly  
simulation_paradigm | Analogue quantum simulation with spin chains (platform-agnostic); also amenable to digital simulation via time-dependent Hamiltonian evolution (Trotterization) but no specific digital algorithm is implemented in the paper  
quantum_hardware_platform | platform-agnostic (authors mention superconducting qubits, trapped ions, neutral atoms/optical lattices, Rydberg arrays) as feasible experimental platforms  
encoding_and_mapping | Jordan–Wigner mapping: spin-1/2 operators σ_j mapped to fermionic operators c_j; continuum limit defined by lattice spacing ε with Ψ(x_j)=c_j/√ε giving Majorana field Ψ; dictionary: functions v,w,q,r,p,ζ in spin Hamiltonian relate to metric functions α,β,γ and field phase ζ via Eqs. (26),(28),(29)–(34); boundary conditions: even/odd fermion-number sectors map to anti-periodic/periodic fermion boundary conditions; long-wavelength limit κ≪1 required; p(t,x) is a free (Wilson-like) term to control doublers  
algorithm_or_protocol | Prepare spin chain in chosen initial state (e.g., ground state at early time) and evolve under specified time-dependent spin Hamiltonian; measure fermionic/spin correlators to extract particle number and other observables. For the Unruh mapping the entanglement Hamiltonian (corner transfer matrix result) is used analytically rather than an explicit circuit protocol.  
resource_estimates | No gate counts or circuit-depth estimates given; numerical classical simulations in paper used discrete spin chains with L up to 512 and show convergence; authors state systems "with up to hundreds of spins or qubits" suffice to reproduce continuum QFT qualitatively (L ≳ 100 gives good agreement). No fault-tolerant overheads quantified.  
noise_and_error_mitigation | No explicit noise model or mitigation protocol is used; paper discusses NISQ-era relevance and references general error-mitigation literature but gives no quantified error budgets or specific mitigation techniques for experiments.  
key_results_or_demonstrations | Provided an explicit, invertible dictionary between spin-chain parameters and metric functions; demonstrated that time- and space-dependent spin Hamiltonians reproduce the Hamiltonian density (Eq. (14)) of a Majorana QFT in curved spacetime; numerical (classical) simulations of the discrete spin model reproduce continuum particle-production spectra as L→∞ (examples up to L=512), showing O(1/L) convergence.  
validation_and_benchmarks | Validated mapping and dynamics by (i) analytic continuum solutions for an exactly solvable FLRW scale factor a(η) using hypergeometric-mode functions, (ii) constructing corresponding discrete-mode solutions (via parameter replacements) and comparing particle-number spectra, (iii) finite-size scaling of |n_k(L)−n_k^(QFT)| ~ O(1/L), and (iv) demonstrating that the known exact entanglement Hamiltonian of the TFIM (corner transfer-matrix result) maps to the Rindler Hamiltonian in the continuum limit.  
claimed_feasibility | Authors claim the protocol is experimentally viable on current/forthcoming quantum platforms for modest system sizes (tens-to-hundreds of qubits/spins) and that optical-lattice and superconducting platforms are promising; they note full, general-purpose simulations (larger size, interactions) will require further advances in control and error correction.  
limitations_and_open_problems | Mapping is for free (non-interacting) Majorana fields only; continuum limit assumes long-wavelength κ≪1 and controlled ε→0 limit; the free function p(t,x) must be chosen to control lattice doublers (fermion-doubling analog); experimental observation requires measurement of multi-point spin correlators (costly); no resource counts (gates, depth) given; extension to interacting fields and 2+1/3+1 gravity analogs is open; black-hole (Hawking) scenarios discussed only as future directions, not simulated here.  
complexity_or_hardness_arguments | No complexity-theoretic hardness claims (no BQP/QMA statements) are made.  
theory_context_keywords | QFT in curved spacetime, Majorana fermions, Jordan–Wigner, continuum limit, analogue gravity, transverse-field Ising mapping, metric dictionary, fermion doubling/Wilson term, Rindler/Unruh mapping, FLRW particle production  
citations_to_prior_work | Selected references cited as foundational/related: Unruh (1981) experimental black hole evaporation; Barcelo, Liberati & Visser (Living Rev Rel 2005) analogue gravity review; Yang et al., Phys. Rev. Research 2020 "Simulating quantum field theory in curved spacetime with quantum many-body systems"; Shi et al., Nat. Commun. 2023 "Quantum simulation of hawking radiation and curved spacetime with a superconducting on-chip black hole"; Fulgado-Claudio et al., Quantum 2023 "Fermion production at the boundary of an expanding universe: a cold-atom gravitational analogue"; Dalmonte et al. review on entanglement Hamiltonians (Annalen Phys. 2022); experimental platform/measurement references: optical-lattice Ising realization (Nature 2011), entanglement-Hamiltonian tomography (Kokail et al., Nature Phys. 2021).  
  
### Simulation of FLRW-expanding-universe Majorana particle production using the transverse-field Ising model with time-dependent transverse field

Field | Value  
---|---  
name_short | FLRW → TFIM protocol  
name_full | Simulation of FLRW-expanding-universe Majorana particle production using the transverse-field Ising model with time-dependent transverse field  
brief_description | Concrete example mapping the Majorana field on an FLRW metric (α=γ=a(η), β=0) to a transverse-field Ising chain whose transverse field is time-dependent (1−ε m a(η)) so that cosmic particle production maps to excitations produced by increasing transverse field.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Friedmann–Lemaître–Robertson–Walker (FLRW) metric in (1+1) dimensions; free Majorana fermion with time-dependent mass m a(η)  
black_hole_phenomena_targeted | Particle production due to time-dependent spacetime (analog of cosmological particle creation); by extension the methods are motivated for horizon-related thermal radiation (Hawking/Unruh analogs) though FLRW itself is cosmological rather than black-hole  
simulation_paradigm | Analog simulation via time-dependent transverse-field Ising chain; the discrete spin Hamiltonian is evolved in real time under the prescribed time-dependent transverse field (classical simulations performed numerically in paper)  
quantum_hardware_platform | platform-agnostic; authors note optical lattices, superconducting processors, trapped ions and Rydberg arrays as candidate platforms where TFIM or similar spin models can be implemented  
encoding_and_mapping | Set α=γ=a(η), β=ζ=0 and choose p=1 to obtain spin Hamiltonian Eq. (55): H = −(1/2ε) Σ_j [σ_j^x σ_{j+1}^x + (1−ε m a(η)) σ_j^z]; Jordan–Wigner maps spin operators to fermions with anti-periodic boundary conditions in the even sector; continuum-discrete mapping uses k = κ/ε and long-wavelength assumption κ≪1.  
algorithm_or_protocol | Prepare initial ground state at early time (a(η→−∞)=const), then evolve under time-dependent TFIM (transverse field increased according to a(η)); extract particle-number spectrum n_k via Bogoliubov-mode overlap (computed analytically for solvable a(η) and numerically for the discrete chain); experimentally would require measuring two-point fermionic correlators or multi-point spin correlators (via Jordan–Wigner relations).  
resource_estimates | Numerical convergence studied for L = 64, 128, 256, 512 (fixed physical length ℓ, ε=ℓ/L); qualitative agreement with continuum achieved for L ≳ 100. Authors state this aligns with current capabilities of quantum processors; no qubit/gate-depth numbers or measurement counts provided.  
noise_and_error_mitigation | No explicit noise model or mitigation protocol provided; paper notes experimental measurement strategies (e.g., measuring correlators or entanglement Hamiltonian tomography) and references general mitigation literature, but does not quantify error budgets.  
key_results_or_demonstrations | Analytical solution for a solvable tanh-profile scale factor a(η) (Eq. (66)) in continuum and its discrete counterpart via parameter substitution; computed n_k showing that discrete TFIM particle spectra converge to continuum QFT spectra with O(1/L) finite-size corrections; faster expansion (smaller Δη) produces more particles and shifts typical produced k upward.  
validation_and_benchmarks | Benchmark: direct comparison of discrete-chain numerical results to exact continuum-mode analytical results for the solvable a(η) model; finite-size scaling analysis (difference scales ~1/L) and plotting convergence (Figs. 1–2).  
claimed_feasibility | Authors claim the TFIM realization of expanding-universe particle production is experimentally feasible for chains of order hundreds of sites/qubits with current/near-term platforms; measuring produced particle number requires measuring correlators but is within reach (with caveats about measurement complexity).  
limitations_and_open_problems | Simulation captures only long-wavelength modes (κ≪1) due to continuum approximation; ultraviolet cutoff set by lattice spacing limits high-k modes; mapping is for free (non-interacting) Majorana fermions—interactions not included; measurement of multi-point correlators required for reconstructing n_k (costly); choice of p controls doublers—care needed to avoid extra low-energy modes.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | FLRW spacetime, particle production, transverse-field Ising model (TFIM), Jordan–Wigner, Bogoliubov transformation, finite-size scaling, long-wavelength continuum limit  
citations_to_prior_work | Related and cited works include: Fulgado-Claudio et al., Quantum 2023 "Fermion production at the boundary of an expanding universe: a cold-atom gravitational analogue"; Yang et al., Phys. Rev. Res. 2020 "Simulating quantum field theory in curved spacetime with quantum many-body systems"; experimental TFIM/optical-lattice realizations (Nature 2011).  
  
### Observation of the Unruh effect through entanglement Hamiltonian mapping of the transverse-field Ising model

Field | Value  
---|---  
name_short | Unruh via TFIM entanglement  
name_full | Observation of the Unruh effect through entanglement Hamiltonian mapping of the transverse-field Ising model  
brief_description | Demonstrates that the exact entanglement (modular) Hamiltonian of the infinite TFIM ground state (corner transfer-matrix result) maps in the continuum limit to the Rindler Hamiltonian, providing a spin-system realization/confirmation of the Unruh effect.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Rindler spacetime Hamiltonian (accelerating observer) and the entanglement Hamiltonian K_A of the semi-infinite TFIM partition  
black_hole_phenomena_targeted | Unruh effect (thermal perception of vacuum by accelerated observer) — horizon-local thermal behavior; closely related to black-hole Hawking radiation as a horizon-thermal phenomenon  
simulation_paradigm | Analytic mapping and theoretical correspondence rather than a performed hardware experiment; could be probed experimentally by preparing TFIM ground state and reconstructing modular Hamiltonian (entanglement-Hamiltonian tomography)  
quantum_hardware_platform | platform-agnostic in principle; experimental proposals reference quantum-simulator platforms able to realize TFIM and measure entanglement Hamiltonian (optical lattices, superconducting processors, trapped ions).  
encoding_and_mapping | Start from known exact expression for entanglement Hamiltonian K_A for TFIM in the ordered phase (Eq. (69)); identify varying couplings proportional to site index j; use mapping formulas (Eq. (34)) and continuum limit (ε→0) to read off metric functions α(x)=2πT_U x, γ=1 yielding Rindler metric ds^2=−(2πT_U x)^2 dt^2 + dx^2; uses corner-transfer-matrix result and Jordan–Wigner continuum mapping.  
algorithm_or_protocol | No time-evolution algorithm is executed; reasoning is analytic: relate exact lattice entanglement Hamiltonian to continuum Rindler generator; experimental probing would require entanglement-Hamiltonian tomography (e.g., protocols like Kokail et al.).  
resource_estimates | No resource-counting provided; authors note entanglement-Hamiltonian tomography proposals and that measuring modular Hamiltonian has experimental proposals but no qubit/gate counts are given.  
noise_and_error_mitigation | Not discussed beyond general references to experimental measurement protocols and tomography techniques.  
key_results_or_demonstrations | Analytic demonstration that the TFIM entanglement Hamiltonian multiplied by Unruh temperature tends to the Rindler Hamiltonian in the continuum limit (Eqs. (73)–(76)), establishing a direct lattice-to-continuum confirmation of the Unruh effect in the spin model framework.  
validation_and_benchmarks | Validation is analytic: uses exact lattice entanglement Hamiltonian from literature (corner transfer-matrix results) and asymptotic expansion I(r')≈π/2(1+ε m/2+...) to identify continuum metric; no numerical experiment performed for this mapping in the paper.  
claimed_feasibility | Authors argue experimental observation is feasible because entanglement Hamiltonians for spin systems can be (in principle) reconstructed and because TFIM is implementable in current platforms; practical tomography challenges remain.  
limitations_and_open_problems | Entanglement Hamiltonian is non-local and its experimental tomography is demanding; mapping performed in ordered TFIM phase and in the continuum limit, so finite-size/finite-ε corrections require careful analysis; no explicit experimental protocol or error analysis offered.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | Entanglement Hamiltonian, Rindler spacetime, Unruh temperature, corner transfer matrix, modular Hamiltonian, TFIM ordered phase, continuum limit  
citations_to_prior_work | Key references used include corner-transfer-matrix and TFIM entanglement results: Davies 1988; Truong & Peschel 1989; entanglement-Hamiltonian reviews and tomography proposals (Dalmonte et al. 2022 review; Kokail et al. 2021 "Entanglement Hamiltonian tomography in quantum simulation").  
  
### Hawking radiation / black-hole thermal radiation (motivational mention and future target)

Field | Value  
---|---  
name_short | Hawking-radiation mention  
name_full | Hawking radiation / black-hole thermal radiation (motivational mention and future target)  
brief_description | Hawking radiation and black-hole evaporation are cited as motivating examples of QFT in curved spacetime that could in principle be probed by analogue quantum simulations; the paper suggests future application of its mapping to black-hole spacetimes to study thermal radiation.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Black hole spacetime (qualitative mention) — Hawking radiation from black-hole horizons (not explicitly mapped or simulated in the present work)  
black_hole_phenomena_targeted | Hawking radiation spectrum, black-hole evaporation, and horizon-related thermal phenomena (proposed as future applications)  
simulation_paradigm | Proposed/foreshadowed use of spin-system analogue simulations (no protocol provided in the paper for black holes specifically)  
quantum_hardware_platform | platform-agnostic; authors mention superconducting chips and other platforms as potentially able to realize single-particle black-hole dynamics in references, but do not give a concrete experimental plan here  
encoding_and_mapping | No explicit mapping to black-hole metrics is derived in this paper; authors state the dictionary (Eqs. (28),(29),(32)) is general and could be applied to other metrics (including black-hole spacetimes) by suitable choice of α,β,γ and ζ, but do not provide an explicit black-hole parameterization or a worked example.  
algorithm_or_protocol | Not provided in this paper for black holes.  
resource_estimates | None provided for black-hole simulations; paper only remarks that small-scale single-particle black-hole dynamics have been realized on superconducting chips (refs. [24]–[26]) and that spin-chain simulations for field-theory phenomena may be feasible with hundreds of qubits.  
noise_and_error_mitigation | Not discussed.  
key_results_or_demonstrations | Only motivational: Hawking radiation mentioned in introduction and summary as an important target area for QFT-in-curved-spacetime simulations; no demonstration in this work.  
validation_and_benchmarks | Not applicable (no black-hole simulation performed).  
claimed_feasibility | Authors suggest the general dictionary could be used to probe horizon/thermal radiation phenomena in tabletop experiments, but give no timeline or resource analysis; practical realization left as future work.  
limitations_and_open_problems | No explicit black-hole metric is realized; extension to interacting fields and higher dimensions is open; preparation of relevant quantum states and measurement of Hawking-like radiation would face the same issues of long-wavelength regime, multi-point correlator measurement, and experimental control over spatially/time-dependent couplings.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | Hawking radiation, black hole evaporation, analogue gravity, QFT in curved spacetime (motivational context)  
citations_to_prior_work | Motivating references include Hawking 1975 "Particle Creation by Black Holes" and analogue-gravity literature (Unruh 1981, Visser 1998, Barcelo et al. 2005), as well as recent superconducting-chip black-hole simulations (Shi et al., Nat. Commun. 2023).  
  
## Citation

Cite this artifact as `\cite{ast-ext-kinoshita-2026-08-13}`.
[code] 
    @misc{ast-ext-kinoshita-2026-08-13,
      title        = {Extraction: Spin systems as quantum simulators of quantum field theories in curved spacetimes},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-spin-systems-as-quantum-simulators-of-quantum-field-theories-in-curve.md},
      crossref     = {kinoshita2024spin},
      note         = {Theorizer's extraction from \cite{kinoshita2024spin}. asta-artifact id: extraction-result-52},
    }
    
    @article{kinoshita2024spin,
      title     = {Spin systems as quantum simulators of quantum field theories in curved spacetimes},
      author    = {Shunichiro Kinoshita and Keiju Murata and D. Yamamoto and Ryosuke Yoshii},
      year      = {2024},
      journal   = {Physical Review Research},
      url       = {https://www.semanticscholar.org/paper/273233799},
    }
[/code]
