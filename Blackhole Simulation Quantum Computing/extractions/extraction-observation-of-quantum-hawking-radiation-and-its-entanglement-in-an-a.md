[<- All artifacts](<../index.md>)

# Extraction: Observation of quantum Hawking radiation and its entanglement in an analogue black hole

**Contents:**

  * Analogue black hole formed in a one-dimensional Bose–Einstein condensate
  * Density–density correlation (G^(2)) Fourier-transform protocol for extracting Bogoliubov pair correlations and entanglement
  * One-dimensional Gross–Pitaevskii numerical simulation with short-pulse Bragg-fluctuation injection



### Analogue black hole formed in a one-dimensional Bose–Einstein condensate

Field | Value  
---|---  
name_short | BEC analogue black hole  
name_full | Analogue black hole formed in a one-dimensional Bose–Einstein condensate  
brief_description | An experimental analogue of a black-hole horizon realized by creating a sharp potential step in a 1D 87Rb Bose–Einstein condensate so that the flow is subsonic outside and supersonic inside; phonons (Bogoliubov excitations) play the role of quantum fields and spontaneously produce Hawking/partner pairs.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime realized as acoustic (sonic) black hole / analogue gravity (Unruh analogue) using phonons in a BEC  
black_hole_phenomena_targeted | Hawking radiation spectrum (thermal population), Hawking-partner pair correlations, and entanglement between Hawking and partner modes  
simulation_paradigm | analog quantum simulation (laboratory analogue using neutral-atom BEC phonons)  
quantum_hardware_platform | neutral atoms (Bose–Einstein condensate of 87Rb)  
encoding_and_mapping | Analogue mapping: local flow velocity v(x) and local sound speed c(x) define an effective spacetime metric for phonons; field degrees of freedom are continuous phonon (Bogoliubov) modes. Key physical parameters used: healing lengths ξ_out and ξ_in (ξ = sqrt(ξ_out ξ_in), ξ ≈ 2.0 μm), Bogoliubov coefficients U_k and V_k (entirely determined by ξ_i k_i), horizon produced by a potential step narrower than ξ (step width 0.442 μm). There is no discretization into qubits, fermion mappings, or holographic encoding — simulation is continuous analogue.  
algorithm_or_protocol | Experimental protocol: prepare stationary flowing BEC with sharp step (horizon), perform repeated phase-contrast imaging to measure 1D density n(x) over many runs; compute two-body density correlation G^(2)(x,x') normalized by √(n_out n_in ξ_out ξ_in); extract k-space pair correlation ⟨b_{k_HR} b_{k_P}⟩ via 2D Fourier transform of cross-horizon quadrant (equations (1) and (2)); measure static structure factor S(k) to obtain populations ⟨b_k^† b_k⟩; evaluate nonseparability measure Δ = ⟨n_H⟩⟨n_P⟩ - |⟨b_H b_P⟩|^2 (Peres–Horodecki criterion) to detect entanglement. Also: oscillating-horizon (driven) experiment as a stimulated-probe for dispersion and calibration.  
resource_estimates | Experimental ensemble and time: main spontaneous-Hawking dataset: 4600 repetitions (≈6 days continuous measurement); oscillating-horizon runs: 200–1200 repeats per frequency. Spatial scales: ξ ≈ 2.0 μm; imaging resolution set by NA=0.5 optics; step sweep speed 0.18 mm/s; measured flow speeds v_out = 0.24 mm/s, v_in = 1.02 mm/s; sound speeds c_out = 0.57 mm/s, c_in = 0.25 mm/s. No qubit/gate counts or circuit-depth style resource estimates (not a gate-based quantum computation).  
noise_and_error_mitigation | Experimental noise handling: ensemble averaging over thousands of shots; filtering of imaging shot noise and imaging fringes; smoothing of diagonal region contaminated by technical noise; application of an overall multiplicative calibration factor (≈2.2) to account for reduced imaging sensitivity (likely optical aberrations). The analysis assumes negligible correlations between phonons of different frequencies (neglecting negative-k correlation terms); this assumption functions as both a simplification and an implicit systematic approximation.  
key_results_or_demonstrations | Observation of spontaneous Hawking radiation and entanglement in an analogue black hole: measured Hawking/partner correlation band in G^(2)(x,x') emanating from horizon; extracted k-space pair correlation S_0^2 |⟨b_{k_HR} b_{k_P}⟩|^2 and population ⟨b_k^† b_k⟩ consistent with a thermal distribution with fitted Hawking temperature k_B T_H = 0.36 m c_out^2 (≈1.2 nK). Entanglement (Δ<0) observed for a broad range of higher k (high-energy) modes; low-k (long-wavelength) pairs found not entangled (suppressed correlations). Agreement with driven-oscillation experiment and 1D Gross–Pitaevskii numerical simulation.  
validation_and_benchmarks | Validated by multiple comparisons: fits of measured dispersion relations to Doppler-shifted Bogoliubov dispersion; comparison of measured S(k) to theoretical Planck distributions (Planck brought to zero at observed ω_peak) giving T_H fit; oscillating-horizon (driven) experiments used to check response and β^2 scaling; numerical 1D Gross–Pitaevskii simulations (with short-pulse Bragg injection of fluctuations) reproduce correlation features and k-distributions; checks of Heisenberg-limit (maximal entanglement) consistency in hydrodynamic limit and comparison to theoretical predictions (Refs. cited).  
claimed_feasibility | Demonstrated feasible in current cold-atom laboratory hardware (NISQ-like experimental platform): spontaneous quantum Hawking radiation and entanglement observed with current imaging and control, but required long averaging (thousands of runs) and careful imaging calibration. No discussion of mapping to gate-based quantum hardware nor claims that gate-model quantum computers are needed; quantum-gravity regimes beyond analogue phonon QFT are not accessed.  
limitations_and_open_problems | Limitations explicitly stated: analogue nature (phonon field ≠ dynamical spacetime; not full quantum gravity); assumption of negligible cross-frequency (negative-k) correlations to evaluate non-commuting terms; observed suppression of low-k (long-wavelength) Hawking pairs (possible insufficient formation time or other dynamical/finite-size effects); finite duration and finite spatial regions limit k-resolution; imaging sensitivity reduced by optical aberrations (calibration factor ≈2.2) and necessitates heavy averaging; horizon steepness (few ξ) produces dispersion departures from hydrodynamic limit at low k. Open problems: origin of low-k suppression, finite-time formation dynamics, and extension to other analogue platforms.  
complexity_or_hardness_arguments | None presented — no computational complexity claims (paper is experimental/analogue, not gate-model quantum algorithm research).  
theory_context_keywords | analogue gravity, Hawking radiation, Bogoliubov modes, Unruh analogy, Peres–Horodecki criterion (nonseparability), Heisenberg entanglement limit, hydrodynamic limit, dispersion, gray soliton, quantum vacuum fluctuations  
citations_to_prior_work | References cited as relevant foundations: Unruh (1981) 'Experimental black-hole evaporation?', Balbinot et al. (2008) 'Nonlocal density correlations as a signature of Hawking radiation', Carusotto et al. (2008) 'Numerical observation of Hawking radiation...', Macher & Parentani (2009) 'Black-hole radiation in Bose-Einstein condensates', Larré et al. (2012), Recati et al. (2009), Busch & Parentani (2014) on entanglement, and other analogue-gravity proposals (Barceló et al. 2001, Horstmann et al. 2010).  
  
### Density–density correlation (G^(2)) Fourier-transform protocol for extracting Bogoliubov pair correlations and entanglement

Field | Value  
---|---  
name_short | G^(2) Fourier entanglement protocol  
name_full | Density–density correlation (G^(2)) Fourier-transform protocol for extracting Bogoliubov pair correlations and entanglement  
brief_description | A measurement and data-analysis protocol that uses ensemble-averaged two-point density correlations across the horizon, Fourier transformed over the cross-horizon quadrant, to extract k-space pair correlations ⟨b_{k_HR} b_{k_P}⟩ and populations ⟨b_k^† b_k⟩, enabling evaluation of nonseparability Δ (Peres–Horodecki) to detect entanglement.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Phononic quantum field (Bogoliubov theory) in an inhomogeneous flowing BEC (analogue curved spacetime); effectively quantum field theory in curved spacetime for phonons  
black_hole_phenomena_targeted | Hawking/partner pair correlations, thermal spectrum, and entanglement detection  
simulation_paradigm | experimental measurement protocol within analog quantum simulation  
quantum_hardware_platform | neutral atoms (BEC); platform-specific imaging and ensemble averaging  
encoding_and_mapping | Mapping is analytic: the cross-horizon G^(2)(x,x') when Fourier-transformed in the appropriate perpendicular coordinate x'' yields S_0 ⟨b_{k_HR} b_{k_P}⟩ (equations (1) and (2)); S_0=(U_k+V_k)(U_{k'}+V_{k'}) accounts for Bogoliubov normalization. Coordinates are limited to finite intervals [-L_out,0] and [0,L_in]. Neglected terms involving negative k are explicitly justified by Doppler-shifted frequency separation.  
algorithm_or_protocol | Compute ensemble-average G^(2)(x,x'); isolate quadrant connecting outside and inside regions; average along correlation band's length to get profile in x''; perform 1D Fourier transform of that profile to obtain S_0^2 |⟨b_{k_HR} b_{k_P}⟩|^2; measure static structure factor S(k) to get populations; compute Δ = ⟨n_H⟩⟨n_P⟩ - |⟨b_H b_P⟩|^2 and compare to zero and Heisenberg limit to determine entanglement.  
resource_estimates | Requires large ensemble statistics to suppress shot noise: demonstrated with 4600 repetitions for spontaneous measurement (6 days). Spatial windows of order tens/hundreds of μm and k resolutions limited by finite window size and imaging resolution (NA=0.5); no qubit/resources reported.  
noise_and_error_mitigation | Mitigation via heavy ensemble averaging; filtering in spatial frequencies to remove imaging shot noise and fringes; smoothing of diagonal region; convolution of theory curves with measured outgoing-mode k-distribution to compare to data; assumption-based neglect of cross-frequency correlations as an analysis simplification.  
key_results_or_demonstrations | Protocol yields direct extraction of pair-correlation spectrum and populations enabling observation of thermal behavior at high k and demonstration of entanglement (negative Δ) for a range of k. The method also allowed demonstration that driven oscillating-horizon produces correlations consistent with stimulated Hawking processes and calibration of β^2 factors.  
validation_and_benchmarks | Protocol validated by (i) hydrodynamic-limit analytic expectations (linear dispersion → |⟨b b⟩|^2 = |α|^2|β|^2 and maximal entanglement); (ii) driven-oscillation experiments whose correlations scale consistent with theory; (iii) reproduction in numerical GP simulations.  
claimed_feasibility | Feasible for analogue BEC experiments where high-quality, high-repetition imaging is available; requires stationarity over ensemble and ability to isolate cross-horizon quadrant. Not presented as a gate-model quantum algorithm.  
limitations_and_open_problems | Relies on assumption that cross-frequency (negative-k) correlations are negligible to infer non-commuting operator correlations from density measurements; finite imaging resolution and windowing limit k-space fidelity; low-frequency suppression may complicate entanglement inference at long wavelengths.  
complexity_or_hardness_arguments | None.  
theory_context_keywords | G^(2) correlations, Fourier analysis of correlation bands, Bogoliubov coefficients U,V, Peres–Horodecki nonseparability criterion, Heisenberg entanglement limit  
citations_to_prior_work | Protocol development references: Balbinot et al. (2008), Carusotto et al. (2008), earlier theoretical work on correlation signatures and entanglement (Refs. 9,10,22,24 in paper).  
  
### One-dimensional Gross–Pitaevskii numerical simulation with short-pulse Bragg-fluctuation injection

Field | Value  
---|---  
name_short | 1D Gross–Pitaevskii simulation  
name_full | One-dimensional Gross–Pitaevskii numerical simulation with short-pulse Bragg-fluctuation injection  
brief_description | Numerical simulations of the 1D Gross–Pitaevskii equation, with injected fluctuations created by a short-pulse, filtered random potential (designed to mimic zero-temperature quantum fluctuations), used to reproduce observed G^(2) correlation features and dispersion behavior of the analogue black hole.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Mean-field Gross–Pitaevskii description of a flowing 1D BEC (classical-field simulation approximating quantum fluctuations via injected noise) — used to simulate analogue Hawking radiation features  
black_hole_phenomena_targeted | Hawking/partner correlation band shape, dispersion relation inside/outside horizon, and k-space features including k_peak and k_max  
simulation_paradigm | classical numerical simulation (Gross–Pitaevskii), used as a complement/validation to analogue quantum experiment  
quantum_hardware_platform | classical computation (numerical solver); not quantum hardware  
encoding_and_mapping | Continuum classical-field representation (ψ(x,t)) evolving under 1D Gross–Pitaevskii equation; fluctuations introduced by applying a random potential filtered by (U_k+V_k)^{-1} and turned on for a short time to create an approximately correct zero-temperature fluctuation spectrum.  
algorithm_or_protocol | Integrate 1D Gross–Pitaevskii equation with experimental-like potential step and flow parameters; inject randomized short-pulse Bragg-like perturbations; compute density correlations and 2D Fourier transforms in the same spatial windows as experiment; extract dispersion branches, k-distributions, and Fourier profiles for direct comparison.  
resource_estimates | Not specified in paper (standard classical simulation cost dependent on grid size, time steps); used to model parameter regime similar to experiment and to produce Figures showing qualitative and quantitative agreement.  
noise_and_error_mitigation | Simulation mitigates finite-sampling noise by ensemble averaging over many realizations of random potentials; no quantum noise beyond mean-field approximations included except via engineered stochastic initial conditions.  
key_results_or_demonstrations | Simulation reproduces the observed correlation band, dispersion relations (including k_peak and multiple branches inside black hole), and narrowing of correlation features due to components above k_peak. Qualitative agreement supports interpretation that observed correlations are Hawking-like and that suppression of low-k correlations can arise under experimental conditions.  
validation_and_benchmarks | Benchmarked against experimental measurements (G^(2) profiles, dispersion, k- distributions) and against theoretical Bogoliubov-dispersion fits; used to explain features such as presence of components above k_peak and finite-k broadening.  
claimed_feasibility | Used as a practical classical validation tool; does not claim to simulate genuine quantum entanglement beyond mean-field plus engineered fluctuations, but reproduces many experimental observables.  
limitations_and_open_problems | Gross–Pitaevskii is a mean-field classical-field approximation and does not fully capture genuine quantum many-body entanglement; the injected-fluctuation method is engineered to mimic zero-temperature quantum fluctuations but remains an approximation. Hence simulation cannot replace full quantum description of entanglement but is adequate for validating classical-field features.  
complexity_or_hardness_arguments | None.  
theory_context_keywords | Gross–Pitaevskii equation, classical-field simulation, Bragg injection of fluctuations, Bogoliubov dispersion  
citations_to_prior_work | References motivating numerical approaches: Carusotto et al. (2008) 'Numerical observation of Hawking radiation...', and other theoretical works on quantum fluctuations around horizons (Refs. 10,11,12).  
  
## Citation

Cite this artifact as `\cite{ast-ext-steinhauer-2026-08-13}`.
[code] 
    @misc{ast-ext-steinhauer-2026-08-13,
      title        = {Extraction: Observation of quantum Hawking radiation and its entanglement in an analogue black hole},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-observation-of-quantum-hawking-radiation-and-its-entanglement-in-an-a.md},
      crossref     = {steinhauer2015observatio},
      note         = {Theorizer's extraction from \cite{steinhauer2015observatio}. asta-artifact id: extraction-result-92},
    }
    
    @article{steinhauer2015observatio,
      title     = {Observation of quantum Hawking radiation and its entanglement in an analogue black hole},
      author    = {J. Steinhauer},
      year      = {2015},
      journal   = {Nature Physics},
      url       = {https://www.semanticscholar.org/paper/119197166},
    }
[/code]
