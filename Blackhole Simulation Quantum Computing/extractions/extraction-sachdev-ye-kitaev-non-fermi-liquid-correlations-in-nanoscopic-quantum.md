[<- All artifacts](<../index.md>)

# Extraction: Sachdev-Ye-Kitaev Non-Fermi-Liquid Correlations in Nanoscopic Quantum Transport.

**Contents:**

  * Sachdev-Ye-Kitaev (complex) model



### Sachdev-Ye-Kitaev (complex) model

Field | Value  
---|---  
name_short | SYK  
name_full | Sachdev-Ye-Kitaev (complex) model  
brief_description | An all-to-all random-interaction fermion model (complex SYK variant here) exhibiting maximal chaos, non-Fermi-liquid infrared physics and a low-energy Schwarzian action that is holographically related to 2D dilaton gravity / near-AdS2 black holes.  
citation_title |   
mention_or_use | use  
target_system_or_model | Complex Sachdev-Ye-Kitaev (SYK) model; low-energy effective description via the Schwarzian action and its holographic relation to two-dimensional gravity / near-AdS2 black holes.  
black_hole_phenomena_targeted | Qualitative black-hole-like properties: maximal entanglement and quantum chaos (fast scrambling), emergent conformal symmetry and its weak breaking (Schwarzian action) that map to near-AdS2 black hole dynamics; the paper does not target direct gravitational observables such as Hawking radiation or Page curve.  
simulation_paradigm | None  
quantum_hardware_platform | None  
encoding_and_mapping | None  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | This is a theoretical condensed-matter analysis using the complex-SYK universality class to predict measurable transport signatures in nanoscopic devices: anomalous temperature power laws in conductance (direct tunneling g_dt ~ (J/T)^{1/2} for E_C < T < J; inelastic cotunneling g_it ~ J T for J/N < T < E_C and g_it ~ (J m^{1/2}) T^{3/2}/E_C^2 for T < J/N), and a RG argument for a quantum phase transition at W_c ~ J/N between SYK-governed NFL and a Fermi liquid. The paper does not perform or propose a quantum-computational simulation experiment.  
validation_and_benchmarks | Validation is analytic/theoretical: mean-field SYK correlators, dressing by reparameterization and U(1) phase fields, gradient expansions to obtain Schwarzian action, RG flow equations for couplings (m,w), comparison to known SYK results in literature (cited Refs. on Schwarzian correlators and 4-point functions), and internal consistency checks (crossover regimes, limiting behaviors), but no numerical quantum-simulation or hardware benchmarks are reported.  
claimed_feasibility | Paper discusses experimental feasibility only in the condensed-matter sense: that SYK universality-class signatures might be observable in nanoscopic devices (complex molecules, semiconductor 'artificial atoms', 2D flakes) provided interactions are strong and single-particle bandwidth W is sufficiently small (criterion J > W and W_c ~ J/N). The paper does not claim feasibility statements for quantum-simulation platforms or timelines for NISQ/fault-tolerant quantum computers.  
limitations_and_open_problems | No quantum-simulation implementation details are given. Limitations discussed for physical (condensed-matter) realization include need for narrow single-particle band (W < J), finite-N effects (crossovers at J/N), sensitivity to single-particle Hamiltonian which yields a quantum phase transition at W_c ~ J/N, and that detailed analysis of the critical regime is beyond the paper's scope. The paper does not address dynamical spacetime, explicit gravitational degrees of freedom, nor state-preparation or measurement challenges for quantum simulators.  
complexity_or_hardness_arguments | None  
theory_context_keywords | SYK, complex SYK, Schwarzian action, reparameterization Goldstone mode, non-Fermi liquid (NFL), holographic correspondence, AdS2 / near-AdS2, fast scrambling, quantum chaos, RG flow, quantum critical point (W_c ~ J/N)  
citations_to_prior_work | Key cited works relevant to SYK and holography include: Sachdev & Ye (1993) [original SY model]; Kitaev (KITP talks, 2015) introducing SYK/quantum holography; Maldacena & Stanford (2016) on SYK and 2D gravity; Bagrets, Altland & Kamenev (2016, 2017) on Schwarzian correlators; Cotler et al. and Engelsöy, Mertens & Verlinde on SYK / gravity connections; Lunkin, Tikhonov & Feigel'man (2018) on the transition. (These are cited in the paper's bibliography as central prior work.)  
  
## Citation

Cite this artifact as `\cite{ast-ext-altland-2026-08-13}`.
[code] 
    @misc{ast-ext-altland-2026-08-13,
      title        = {Extraction: Sachdev-Ye-Kitaev Non-Fermi-Liquid Correlations in Nanoscopic Quantum Transport.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-sachdev-ye-kitaev-non-fermi-liquid-correlations-in-nanoscopic-quantum.md},
      crossref     = {altland2019sachdevyek},
      note         = {Theorizer's extraction from \cite{altland2019sachdevyek}. asta-artifact id: extraction-result-53},
    }
    
    @article{altland2019sachdevyek,
      title     = {Sachdev-Ye-Kitaev Non-Fermi-Liquid Correlations in Nanoscopic Quantum Transport.},
      author    = {A. Altland and D. Bagrets and A. Kamenev},
      year      = {2019},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/201668391},
    }
[/code]
