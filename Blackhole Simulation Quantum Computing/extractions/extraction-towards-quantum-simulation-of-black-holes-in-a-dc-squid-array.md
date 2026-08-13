[<- All artifacts](<../index.md>)

# Extraction: Towards Quantum Simulation of Black Holes in a dc-SQUID Array

**Contents:**

  * Quantum simulation of 1+1D radial black-hole sections using a dc-SQUID array embedded in an open transmission line
  * Analogue Hawking Radiation in a dc-SQUID Array Transmission Line (Nation, Blencowe, Rimberg, Buks, 2009)
  * One-dimensional sections of exotic spacetimes with superconducting circuits (Sabín, New J. Phys. 2018)



### Quantum simulation of 1+1D radial black-hole sections using a dc-SQUID array embedded in an open transmission line

Field | Value  
---|---  
name_short | dc-SQUID array BH sim  
name_full | Quantum simulation of 1+1D radial black-hole sections using a dc-SQUID array embedded in an open transmission line  
brief_description | A proposal to simulate 1+1D radial sections of Schwarzschild, Reissner–Nordström, Kerr and Kerr–Newman spacetimes by engineering a spatially- and temporally-dependent effective propagation speed for the electromagnetic field in a dc-SQUID transmission-line array via an external magnetic flux profile; event horizons map to locations where the effective speed vanishes and Hawking-like photon pair emission can be probed.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime (1+1D radial sections of Kerr–Newman family: Schwarzschild, Reissner–Nordström, Kerr, Kerr–Newman)  
black_hole_phenomena_targeted | Event-horizon formation analogues and potential Hawking radiation (photon-pair emission from vacuum), plus study of ergosphere appearance/limitations in rotating cases  
simulation_paradigm | Analog quantum simulation (continuous-variable electromagnetic field in a superconducting transmission line with engineered local wave speed)  
quantum_hardware_platform | Superconducting circuits — dc-SQUID array embedded on an open microwave transmission line (Josephson-junction based metamaterial)  
encoding_and_mapping | The mapping uses the conformal invariance of the 1+1D Klein–Gordon equation to identify the 1+1D section of the black-hole metric with a wave equation having a position-dependent effective light speed c(x,t). The effective local squared speed c^2 is implemented by tuning the SQUID inductance with an external magnetic flux via c^2(phi_ext)=c0^2 |cos(pi phi_ext/phi0)| (Eqs. 4,6–9,22–23). The metric factor dot{c}^2(ξ) for each black-hole family (Eqs. 22,26,30,38,41) is inverted through Eq. (9) to obtain the required spatial flux profile phi_ext(ξ). Degrees of freedom: 1D electromagnetic field modes of the transmission line (linearized regime, cos ψ ≈ 1). Discretization: continuous target profile approximated by a discrete array of SQUIDs of length ε; event horizon ideally localized to a single SQUID to minimize high-impedance regions.  
algorithm_or_protocol | Analog protocol: set a DC bias flux to reduce global effective speed, then apply the spatial (and in general temporal) flux profile phi_ext(ξ,t) (via Eq. 9) to reproduce the target dot{c}^2(ξ). Detection protocol: measure correlated photon pairs emitted from the array endpoints using coincidence detection to identify Hawking-like pair creation (citing DCE and previous proposals). No gate-based algorithmic steps are used; the physics is enacted by continuous control of circuit parameters.  
resource_estimates | No explicit qubit/gate resource counts or circuit-depth estimates are provided. Experimental-resource-level guidance: keep the region near critical flux (pi phi_ext/phi0 = pi/2) as small as possible (ideally a single SQUID) to avoid collective high impedance and phase-fluctuation-driven breakdown; choose large effective black-hole mass M (scales radial compression) to minimize the number of SQUIDs in the critical region. No counts of SQUIDs, detectors, or measurement shots are specified.  
noise_and_error_mitigation | Noise discussion is qualitative: main limitation arises from quantum phase fluctuations (ψ) and large array impedance when many SQUIDs approach the critical flux, breaking the cos ψ ≈ 1 linear approximation and potentially driving the array out of the superconducting regime. Mitigation proposed qualitatively: restrict high-flux region to as few SQUIDs as possible (single SQUID ideal) and operate in weak-signal linear regime. No quantitative noise model, error budgets, or explicit mitigation techniques (ZNE, PEC, postselection) are given.  
key_results_or_demonstrations | This work is a theoretical proposal/analysis (no experimental realization reported). Core findings: explicit analytic expressions to convert 1+1D radial metric sections of Schwarzschild, Reissner–Nordström, Kerr and Kerr–Newman black holes into required external flux profiles (Eqs. 22, 23, 26, 30, 38, 41, 42); demonstration that event-horizon analogues (locations where effective c^2→0) can in principle be produced for non-rotating black holes; identification that Hawking-like photon-pair emission could be observed via coincidence detection if horizons are realized; demonstration that ergospheres (regions where radial-wave propagation is forbidden / effective c^2 would have to be negative/imaginary) cannot be properly simulated with these radial sections because they require flux beyond the allowed linear regime.  
validation_and_benchmarks | Validation is analytical: mapping is constructed by conformal transformation of the 1+1D Klein–Gordon equation and direct algebraic matching of metric coefficients to effective wave-speed profiles; comparison to known analytic positions of horizons and static limits (Eqs. 16–19,17,19) to identify where phi_ext reaches threshold π/2. No numerical simulations, no experimental data, and no explicit comparison to full-wave electromagnetic simulations are presented; experimental validation is proposed via coincidence photon detection to discriminate Hawking-like pairs from thermal noise.  
claimed_feasibility | Feasibility claims are cautious: generating event-horizon analogues and possibly Hawking radiation is, in principle, achievable for non-rotating black holes within this platform, but experimental verification is required. The ergosphere (rotating BH) simulation appears beyond reach for the considered radial sections because it requires flux beyond the linear regime. Practical bottlenecks identified: quantum-phase fluctuations and high impedance near critical flux, nonlinearity breakdown (cos ψ ≈ 1 invalid), and the discrete nature of the array requiring horizons be localized to very few SQUIDs. The paper suggests that experiments should choose large M to compress critical regions and minimize problematic SQUIDs.  
limitations_and_open_problems | Explicit limitations: (1) Linear weak-signal approximation (cos ψ ≈ 1) may fail near critical flux; (2) quantum phase fluctuations/high-impedance of an extended critical region can drive insulating behavior preventing horizon formation; (3) discrete SQUID array cannot perfectly reproduce a continuum metric—event horizon is at best one or a few SQUIDs; (4) ergospheres (frame-dragging regions) require regions where the simulated radial c^2 becomes negative/imaginary or flux beyond π/2, which is outside allowed operating regime, so ergosphere physics cannot be captured with the considered radial sections; (5) charged black holes produce regions not simulable for small r (flux undefined or discontinuous depending on A); (6) no assessment of spectral shape/temperature of Hawking radiation beyond qualitative expectation; (7) no resource quantification (numbers of devices/detectors) or full noise modeling.  
complexity_or_hardness_arguments | No complexity-theoretic claims are made (no statements about BQP/QMA hardness or classical intractability).  
theory_context_keywords | quantum field theory in curved spacetime, analogue gravity, event horizon analogue, Hawking radiation, dynamical Casimir effect, conformal invariance of Klein–Gordon, SQUID metamaterial, frame dragging, ergosphere  
citations_to_prior_work | Key prior works cited and used as basis: Sabín 'One-dimensional sections of exotic spacetimes with superconducting circuits' (New J. Phys. 2018) [15] (procedure followed); Nation et al. 'Analogue Hawking Radiation in a dc-SQUID Array Transmission Line' (Phys. Rev. Lett. 2009) [18] (prior theoretical proposal); Nation et al. 'Stimulating uncertainty: Amplifying the quantum vacuum with superconducting circuits' (Rev. Mod. Phys. 2012) [17] (review of related effects and photon-pair generation); Lähteenmäki et al. 'Dynamical Casimir effect in a Josephson metamaterial' (PNAS 2013) [19] (experimental DCE in Josephson metamaterial); Steinhauer 'Observation of quantum Hawking radiation and its entanglement in an analogue black hole' (Nat. Phys. 2016) [16] (BEC experiment detecting Hawking radiation); and foundational JJ/SQUID works and studies of phase fluctuations and insulator transition [20–22,24–26].  
  
### Analogue Hawking Radiation in a dc-SQUID Array Transmission Line (Nation, Blencowe, Rimberg, Buks, 2009)

Field | Value  
---|---  
name_short | Nation et al. PRL 2009  
name_full | Analogue Hawking Radiation in a dc-SQUID Array Transmission Line (Nation, Blencowe, Rimberg, Buks, 2009)  
brief_description | A prior theoretical proposal to generate analogue Hawking radiation by engineering horizons in a dc-SQUID transmission-line metamaterial through modulation of the local wave propagation speed using SQUID inductances.  
citation_title | Analogue Hawking Radiation in a dc-SQUID Array Transmission Line  
mention_or_use | mention  
target_system_or_model | Analogue quantum field theory in curved spacetime using SQUID-array transmission line  
black_hole_phenomena_targeted | Analogue event horizons and Hawking radiation (photon pair creation)  
simulation_paradigm | Analog quantum simulation (microwave SQUID metamaterial)  
quantum_hardware_platform | Superconducting circuits (dc-SQUID arrays)  
encoding_and_mapping | Map target effective metric to spatially-dependent propagation speed via SQUID inductance controlled by magnetic flux (c^2(phi_ext) relationship cited in main paper).  
algorithm_or_protocol | Continuous control of external flux to create horizon-like region; detection via emitted photons (DCE-like signatures).  
resource_estimates | Not given in the citing paper (referenced here only as prior proposal).  
noise_and_error_mitigation | Not detailed in this paper's discussion beyond qualitative references; main paper references it as theoretical prior work.  
key_results_or_demonstrations | Cited as foundational theoretical proposal motivating the present work; no experimental realization reported here.  
validation_and_benchmarks | Analytic theoretical derivation in original proposal (not reproduced numerically here).  
claimed_feasibility | Presented as a feasible theoretical approach in prior literature; cited here as motivation/basis.  
limitations_and_open_problems | Original limitations (as referenced): need to control flux precisely, manage phase fluctuations, and address nonlinear regime near critical flux—these are discussed in the present paper.  
complexity_or_hardness_arguments | None stated in the present paper's citation context.  
theory_context_keywords | analogue Hawking radiation, SQUID metamaterial, dynamical Casimir  
citations_to_prior_work |   
  
### One-dimensional sections of exotic spacetimes with superconducting circuits (Sabín, New J. Phys. 2018)

Field | Value  
---|---  
name_short | Sabín 2018 procedure  
name_full | One-dimensional sections of exotic spacetimes with superconducting circuits (Sabín, New J. Phys. 2018)  
brief_description | A methodology to simulate 1+1D sections of exotic spacetimes using superconducting-circuit transmission lines (dc-SQUID arrays) by mapping spacetime metric coefficients to local propagation speeds; the present paper follows this procedure.  
citation_title | One-dimensional sections of exotic spacetimes with superconducting circuits  
mention_or_use | mention  
target_system_or_model | 1+1D sections of curved spacetimes (analogue gravity) implemented in SQUID arrays  
black_hole_phenomena_targeted | General exotic-spacetime features in 1+1D sections (used as methodological basis for BH sections in present work)  
simulation_paradigm | Analog quantum simulation  
quantum_hardware_platform | Superconducting circuits (dc-SQUID arrays)  
encoding_and_mapping | Conformal mapping of 1+1D Klein–Gordon to engineered position-dependent wave speed implemented via flux control of SQUID inductance (approach used here).  
algorithm_or_protocol | Design flux profiles from metric coefficients; implement via DC+AC flux control in transmission line; analyze resulting effective c^2(ξ).  
resource_estimates | Not specified in present paper beyond the same qualitative guidance (minimize SQUIDs near critical flux).  
noise_and_error_mitigation | Original procedure works in linear regime and flags nonlinear breakdowns near critical flux; present paper inherits those cautions.  
key_results_or_demonstrations | Procedure provided analytical mapping for 1+1D spacetime sections; present paper applies it to Kerr–Newman family.  
validation_and_benchmarks | Analytical construction and examples in prior work; present paper builds upon it.  
claimed_feasibility | Proposed as feasible in principle within linear-operating SQUID arrays; practical issues remain (phase fluctuations, impedance).  
limitations_and_open_problems | Same platform limitations: phase fluctuations, limited to sections where mapping yields physically-allowed fluxes inside linear regime.  
complexity_or_hardness_arguments | None.  
theory_context_keywords | conformal mapping, Klein–Gordon, SQUID array, analogue spacetimes  
citations_to_prior_work |   
  
## Citation

Cite this artifact as `\cite{ast-ext-terrones-2026-08-13}`.
[code] 
    @misc{ast-ext-terrones-2026-08-13,
      title        = {Extraction: Towards Quantum Simulation of Black Holes in a dc-SQUID Array},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-towards-quantum-simulation-of-black-holes-in-a-dc-squid-array.md},
      crossref     = {terrones2021towards},
      note         = {Theorizer's extraction from \cite{terrones2021towards}. asta-artifact id: extraction-result-67},
    }
    
    @article{terrones2021towards,
      title     = {Towards Quantum Simulation of Black Holes in a dc-SQUID Array},
      author    = {Adri'an Terrones and C. Sab'in},
      year      = {2021},
      journal   = {Universe},
      url       = {https://www.semanticscholar.org/paper/239616504},
    }
[/code]
