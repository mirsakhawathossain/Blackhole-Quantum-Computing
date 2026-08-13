[<- All artifacts](<../index.md>)

# Extraction: How to make a quantum black hole with ultra-cold gases

**Contents:**

  * Experimental realization of the Sachdev-Ye-Kitaev (SYK) model with ultra-cold fermionic atoms via photoassociation



### Experimental realization of the Sachdev-Ye-Kitaev (SYK) model with ultra-cold fermionic atoms via photoassociation

Field | Value  
---|---  
name_short | SYK ultracold proposal  
name_full | Experimental realization of the Sachdev-Ye-Kitaev (SYK) model with ultra-cold fermionic atoms via photoassociation  
brief_description | A concrete analog-quantum-simulation proposal to implement the (real) SYK model — a large-N strongly interacting quantum-mechanical model with a conjectured dual description as a two-dimensional black hole — by engineering random all-to-all four-fermion couplings in an optical-lattice system of ultracold fermions coupled to multiple molecular states via photoassociation/photodissociation.  
citation_title | How to make a quantum black hole with ultra-cold gases  
mention_or_use | use  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model (real-variant introduced in text; N spinless fermions with all-to-all random four-fermion interactions; dual to a 2D AdS black hole in large-N limit).  
black_hole_phenomena_targeted | Thermodynamics (entropy), low-energy correlation functions, and quantum chaos / scrambling as diagnosed by the Lyapunov exponent (OTOC behavior; saturation to 2\pi T in strong-coupling large-N limit).  
simulation_paradigm | Analog quantum simulation on optical lattice (experimental implementation of the target Hamiltonian rather than digital-gate algorithms).  
quantum_hardware_platform | Neutral atoms / ultracold fermionic atoms in optical lattices (explicitly mentions atoms such as 6Li) with bosonic molecular intermediate states; 'platform-agnostic' only in the sense of ultracold realizations.  
encoding_and_mapping | Physical encoding: N fermionic modes (spinless fermions) realized by atoms trapped in lattice sites; auxiliary bosonic molecular states m_s (n_s distinct molecular states) are coupled to pairs of atoms via photoassociation/photodissociation with random coupling coefficients g_{s,ij}; integrating out the molecular modes yields effective all-to-all four-fermion couplings J_{ij;kl} via J_{ij;kl}/(2N)^{3/2} = \sum_s g_{s,ij} g_{s,kl} / v_s. No qubit mapping (Jordan-Wigner/Bravyi-Kitaev) or digital fermion-to-qubit encoding is specified because the proposal is analog and uses atoms and molecules directly.  
algorithm_or_protocol | Analog Hamiltonian engineering: introduce laser frequencies to induce coherent photoassociation and photodissociation processes described by H_m (Eq. 3.1); choose a large number n_s of molecular states with controlled detunings v_s (sign-alternating pattern) and random g_{s,ij} to produce Gaussian-distributed J_{ij;kl} in the effective Hamiltonian H_eff (Eq. 3.2). No digital algorithms (Trotterization, LCU, VQE, etc.) are proposed in the paper.  
resource_estimates | No explicit numerical resource estimates (number of atoms N required, number of molecular states n_s needed in an actual experiment beyond qualitative 'large n_s', gate counts, circuit depths, measurement shots, or fault-tolerance overhead) are provided in this proceedings summary. The paper specifies scaling choices for variance: set variance of g_{s,ij} and v_s so that \sigma_g^2/\sigma_s = J/(2N)^{3/2} and takes v_s \propto \sqrt{n_s}, and identifies the limit n_s -> infinity as reproducing the real-SYK statistics.  
noise_and_error_mitigation | No quantitative noise model or explicit mitigation protocols are provided. The paper notes practical/technical experimental challenges (summarized in the referenced longer work [20]) but does not give error budgets, decoherence-rate tolerances, or mitigation techniques for analog implementation.  
key_results_or_demonstrations | This work is a theoretical/experimental proposal (concept and Hamiltonian-engineering recipe) rather than a performed experiment. Core demonstration: derivation that coupling atoms to many molecular states with appropriately randomized couplings and detunings yields, upon integrating out molecular modes, an effective real-SYK Hamiltonian H_eff (Eq. 3.2) which matches the desired random all-to-all four-fermion interaction distribution in the large-n_s limit; identification of parameter scalings to reproduce SYK disorder statistics and large-N equivalence to the complex SYK model at leading order.  
validation_and_benchmarks | Validation arguments are theoretical: (i) analytic mapping by integrating out molecular modes to obtain H_eff (Eq. 3.2); (ii) statistical central-limit / random-walk argument that the sum over many molecular-state-mediated products g_{s,ij} g_{s,kl}/v_s becomes Gaussian-distributed (with sign/variance control by alternating signs of v_s) in the large-n_s limit, reproducing the disorder moments chosen for the real-SYK model; (iii) argument that the real-SYK model matches the original complex SYK at large-N up to 1/N corrections. No experimental or numerical (ED) benchmarks are presented in this proceedings writeup (longer work [20] referenced for details).  
claimed_feasibility | Authors claim conceptual feasibility of realizing a quantum black hole experimentally by implementing the SYK model in ultracold-atom platforms, but emphasize many technical challenges and that immediate realization is not guaranteed. They indicate that large n_s and careful control of photoassociation couplings are required; practical challenges and experimental details are deferred to the longer article [20]. No concrete timeframe or NISQ vs fault-tolerant delineation is given.  
limitations_and_open_problems | Explicit limitations noted: (i) difficulty of engineering true all-to-all two-body hopping in lattice experiments; (ii) requirement of many molecular intermediate states n_s (exact finite-n_s effects not quantified in this summary); (iii) practical experimental technical challenges summarized in [20]; (iv) theoretical simplifications (they use a 'real' SYK variant and rely on large-n_s and large-N limits; 1/N corrections exist); (v) absence of a clean prescription here for measuring specific gravitational observables (e.g., direct measurement of Lyapunov exponent/OTOCs in experiment is not detailed here). The authors also note the desirability of simpler equivalent models (e.g., disorder-free variants) to ease implementation.  
complexity_or_hardness_arguments | No explicit complexity-theoretic statements (e.g., BQP-hardness, QMA-hardness) are made in this proceedings summary about the difficulty of simulating or verifying the SYK model. The paper does assert that non-gravitational theories dual to gravity are 'equivalent' in the holographic sense, but does not quantify computational complexity.  
theory_context_keywords | holographic principle, AdS/CFT (gauge/gravity duality), SYK model, large-N limit, fast scrambling, Lyapunov exponent, quantum chaos, disorder average, Sachdev-Ye model, Kitaev, dual black hole (AdS2), non-gravitational duals, photoassociation  
citations_to_prior_work | Key references cited in support of context and approach: Sachdev (original Sachdev-Ye model) [18], Kitaev talks (SYK) [19], Maldacena, Shenker and Stanford on Lyapunov bound and chaos [22], works on Monte Carlo/lattice evidence for holographic matrix models [9,11], related quantum-simulation proposal by Garcia-Álvarez et al. (Phys. Rev. Lett. 2017) [21], previous suggestions to engineer two-body hopping via intermediate states [27], photoassociation/photodissociation experimental reviews [28], and the longer technical paper by the authors with full proposal/results [20] (PTEP 2017).  
  
## Citation

Cite this artifact as `\cite{ast-ext-danshita-2026-08-13-2}`.
[code] 
    @misc{ast-ext-danshita-2026-08-13-2,
      title        = {Extraction: How to make a quantum black hole with ultra-cold gases},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-how-to-make-a-quantum-black-hole-with-ultra-cold-gases.md},
      crossref     = {danshita2017how},
      note         = {Theorizer's extraction from \cite{danshita2017how}. asta-artifact id: extraction-result-83},
    }
    
    @article{danshita2017how,
      title     = {How to make a quantum black hole with ultra-cold gases},
      author    = {I. Danshita and M. Hanada and Masaki Tezuka},
      year      = {2017},
      url       = {https://www.semanticscholar.org/paper/119098985},
    }
[/code]
