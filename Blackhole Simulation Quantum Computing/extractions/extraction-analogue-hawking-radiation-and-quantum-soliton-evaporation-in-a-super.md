[<- All artifacts](<../index.md>)

# Extraction: Analogue Hawking radiation and quantum soliton evaporation in a superconducting circuit

**Contents:**

  * Waveguide-like SQUID-array superconducting transmission line realizing sine-Gordon solitons (analogue JT black hole)



### Waveguide-like SQUID-array superconducting transmission line realizing sine-Gordon solitons (analogue JT black hole)

Field | Value  
---|---  
name_short | SG-SQUID simulator  
name_full | Waveguide-like SQUID-array superconducting transmission line realizing sine-Gordon solitons (analogue JT black hole)  
brief_description | A proposed analog quantum simulator implemented as a coplanar transmission line whose unit cells each contain a capacitor in parallel with a symmetric dc-SQUID; the superconducting phase field obeys the sine-Gordon equation and 1+1D sine-Gordon solitons map to Jackiw-Teitelboim (JT) black-hole metrics, enabling study of analogue Hawking radiation via quantum perturbations on the soliton background.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Jackiw-Teitelboim (JT) 1+1 dimensional dilaton gravity realized via the mapping between solutions of the sine-Gordon (SG) field theory (in a continuum SQUID-array transmission line) and 1+1D black-hole geometries (1-soliton → JT black hole). Also targets quantum field theory in curved spacetime for a massless scalar perturbation propagating on this soliton (analogue Hawking radiation).  
black_hole_phenomena_targeted | Analogue Hawking radiation (thermal spectrum of particle creation from the soliton horizon), horizon formation as the 1-soliton metric (event horizon r_H = beta_s), quantum soliton evaporation (perturbative radiation φ1), and Doppler-corrected laboratory-frame Hawking temperature.  
simulation_paradigm | Analog quantum simulation (engineered superconducting transmission line implementing a continuous bosonic field whose classical solutions realize black-hole-like metrics); not a digital gate-based algorithm.  
quantum_hardware_platform | Superconducting circuit / circuit QED: coplanar-waveguide-like transmission line with unit cells containing dc-SQUIDs and capacitors (SQUID-array transmission line).  
encoding_and_mapping | No qubit encoding is used; the mapping is field-based: node flux Φ(x,t) (or superconducting phase φ = 2πΦ/Φ0) in the continuum limit satisfies the sine-Gordon equation derived from the circuit Lagrangian. The 1-soliton SG solution φ_s(τ,ξ) maps to a JT black-hole metric via metric ds^2 = -sin^2(φ/2)dτ^2 + cos^2(φ/2)dξ^2 and coordinate transformations to Schwarzschild/Kruskal forms. Degrees of freedom: continuous bosonic field (flux/phase) along the waveguide; continuum approximation (a/λ ≪ 1) and small-amplitude/phase-regime assumptions (E_J ≫ charging energy, Φ/Φ0 ≪ 1). Boundary/coordinate treatments use tortoise and Kruskal coordinates for horizon regularity. There is no fermion-to-qubit mapping or lattice-to-qubit discretization described.  
algorithm_or_protocol | Prepare a classical SG soliton signal φ_s propagating along the transmission line (sets soliton velocity β_s ≤ c), inject/monitor a weak quantum perturbation φ_1 (φ = φ_s + φ_1 with φ_1 ≪ φ_s), then measure emitted microwave photons or voltage quadratures at the line end; theoretical analysis uses Bogoliubov transformations between Kruskal and Boulware modes and linear perturbation equation [ (∂_τ^2 + ∂_ξ^2) - cos(φ_s) ] φ_1 = 0 to predict thermal spectrum. Detection protocols suggested: single-shot microwave photon detectors (superconducting phase qubit) or four-quadrature voltage correlation measurements of sidebands.  
resource_estimates | No qubit/gate resources given (analog device). Experimental component estimates provided: Josephson junction critical current I_c = 2 μA, junction capacitance C_J = 1.2 fF, ground capacitance C_0 = 0.8 fF, unit-cell inductance L_0 = 0.01 nH, cell length a = 6 μm; plasma frequency ω_p ≃ 2.25×10^12 Hz; propagation velocity c ≃ 0.14 c_0. Hawking temperature scale: T_H = β_s / (2π) in comoving frame, Doppler-corrected laboratory-frame T_H = β_s/(2π) sqrt((1-β_s)/(1+β_s)); temperatures can reach 'a few mK' per authors' estimates and are compared to dilution-refrigerator base temperatures. Radiation power estimated by dE/dT = (π/12ħ) (k_B T_H)^2 (Eq. 19). No counts of required measurements/shots, circuit depth, or fault-tolerance overhead apply because this is an analog hardware proposal.  
noise_and_error_mitigation | No detailed noise model or error-correction protocol provided. Authors note ambient (dilution fridge) temperature and background noise and recommend engineering the transmission line to reduce unwanted coupling; suggest using single-shot detectors and quadrature correlation measurements to resolve Hawking signal above thermal background. No quantification of detection noise budgets or mitigation techniques such as ZNE/PEC/etc. is given.  
key_results_or_demonstrations | Theoretical proposal and analysis (not an experimental demonstration). Core results: (i) derivation that the superconducting-phase field in the SQUID-array obeys the sine-Gordon equation (Eq. 3); (ii) mapping of 1-soliton SG solution to a JT black-hole metric with event horizon r_H = β_s and explicit coordinate transforms to Schwarzschild/Kruskal forms (Eqs. 11–15); (iii) prediction of thermal particle spectrum ⟨N_Ω⟩ = [exp(2πΩ/β_s)-1]^{-1} with comoving-frame temperature T_H = β_s/(2π) (Eq. 16) and Doppler-corrected laboratory-frame formula (Eq. 18); (iv) feasibility estimates showing T_H up to a few mK for chosen circuit parameters and that the signal could sit above refrigerator temperature; proposal of detection modalities (photon counting, voltage quadrature correlations).  
validation_and_benchmarks | Validation is analytical: (a) mapping to JT gravity uses established results (Ref. [14]) that SG solutions yield constant-negative-curvature geometries; (b) Hawking spectrum derived via standard QFT in curved spacetime using Bogoliubov transformations between Kruskal and Boulware modes (textbook approach, Eqs. 14–16) and cross-checked by linear perturbation analysis φ = φ_s + φ_1 (Eq. 17) referencing prior SG perturbation work; (c) consistency with earlier related proposals/analyses (e.g., Ref. [44], inverse-scattering literature). No numerical exact-diagonalization, no experimental benchmark data, and no cross-platform verification are presented.  
claimed_feasibility | Authors claim the proposal is feasible in principle with contemporary cQED technology and existing device parameters, citing similar experimental platforms (coplanar waveguides, SQUID-array metamaterials, dynamical Casimir experiments). They state Hawking temperatures of order a few mK should be measurable above dilution-fridge backgrounds, given adequate single-shot microwave photon detection or quadrature-correlation measurements. No claim that fault-tolerant quantum processors are required; apparatus is analog and within near-term experimental reach subject to engineering noise suppression and detector performance.  
limitations_and_open_problems | Explicit limitations include: the analogy is 1+1D and represents JT dilaton gravity rather than full higher-dimensional GR; reliance on continuum and phase-regime approximations (a/λ ≪ 1 and E_J ≫ charging energy, small phase oscillation Φ/Φ0 ≪ 1); neglect of SQUID loop self-inductance and assumption of symmetric SQUIDs; soliton velocity must satisfy β_s < c (propagation velocity); detection limited by background thermal noise and detector efficiency; no claim of probing quantum gravity—this is an analogue model; no resource counts for statistics/measurement overhead; extensions (N-soliton, variable mass m(x,t)) noted as future work. Practical bottlenecks: engineering to reduce unwanted couplings and achieving sufficiently sensitive single-photon microwave detection.  
complexity_or_hardness_arguments |   
theory_context_keywords | sine-Gordon equation, Jackiw-Teitelboim (JT) dilaton gravity, analogue gravity, Hawking radiation, soliton/black-hole duality, quantum field theory in curved spacetime, Bogoliubov transformation, Kruskal coordinates, dynamical Casimir effect  
citations_to_prior_work | Notable cited works used as foundation or context include: "Solitons and black holes" (J. Gegenberg and G. Kunstatter, Phys. Lett. B) [Ref. 14]; "Analog cosmological particle generation in a superconducting circuit" (Z. Tian et al., Phys. Rev. D) [Ref. 31]; "Analogue hawking radiation in a dc-squid array transmission line" (P. D. Nation et al., Phys. Rev. Lett.) [Ref. 50]; experimental and theoretical cQED/dynamical-Casimir works: "Observation of the dynamical Casimir effect in a superconducting circuit" (C. M. Wilson et al., Nature) [Ref. 28], "Dynamical Casimir effect in a superconducting coplanar waveguide" (J. R. Johansson et al., Phys. Rev. Lett.) [Ref. 25], "Dynamical Casimir effect in superconducting microwave circuits" (J. R. Johansson et al., Phys. Rev. A) [Ref. 24]; and theoretical analyses of SG perturbations and soliton Hawking analogs: "Sine-Gordon soliton as a model for hawking radiation of moving black holes and quantum soliton evaporation" (L. Di Mauro Villari et al., J. Phys. Commun.) [Ref. 44].  
  
## Citation

Cite this artifact as `\cite{ast-ext-tian-2026-08-13}`.
[code] 
    @misc{ast-ext-tian-2026-08-13,
      title        = {Extraction: Analogue Hawking radiation and quantum soliton evaporation in a superconducting circuit},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-analogue-hawking-radiation-and-quantum-soliton-evaporation-in-a-super.md},
      crossref     = {tian2018analogue},
      note         = {Theorizer's extraction from \cite{tian2018analogue}. asta-artifact id: extraction-result-40},
    }
    
    @article{tian2018analogue,
      title     = {Analogue Hawking radiation and quantum soliton evaporation in a superconducting circuit},
      author    = {Zehua Tian and Jiangfeng Du},
      year      = {2018},
      journal   = {The European Physical Journal C},
      url       = {https://www.semanticscholar.org/paper/119227492},
    }
[/code]
