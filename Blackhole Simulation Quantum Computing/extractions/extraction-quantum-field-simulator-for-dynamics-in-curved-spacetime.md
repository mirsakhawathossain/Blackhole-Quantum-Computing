[<- All artifacts](<../index.md>)

# Extraction: Quantum field simulator for dynamics in curved spacetime

**Contents:**

  * FLRW (Friedmann-Lemaître-Robertson-Walker) cosmology simulator in a Bose-Einstein condensate
  * Sonic (acoustic) black hole analogue in fluids/BECs
  * Analogue Hawking-radiation experiments (BECs, fluids, light, ions)



### FLRW (Friedmann-Lemaître-Robertson-Walker) cosmology simulator in a Bose-Einstein condensate

Field | Value  
---|---  
name_short | FLRW-BEC-simulator  
name_full | FLRW (Friedmann-Lemaître-Robertson-Walker) cosmology simulator in a Bose-Einstein condensate  
brief_description | An experimental analogue quantum-field simulator that realises a (2+1)-dimensional FLRW metric for a massless scalar field using phononic excitations in a two-dimensional potassium-39 Bose-Einstein condensate; time-dependent scale factor implemented via controlled s-wave scattering length and spatial curvature via configurable density profiles.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime (massless real scalar field) on a (2+1)-dimensional FLRW metric (Eq. (1) in paper).  
black_hole_phenomena_targeted | Not a direct black-hole simulation; targets cosmological particle (phonon) pair production in expanding spacetime (analogue of cosmological particle creation). The paper situates itself in analogue-gravity context that includes sonic/black-hole analogues, but the experiment focuses on FLRW expansion rather than horizon/Hawking phenomena.  
simulation_paradigm | Analog quantum simulation (phonons in an ultracold-atom BEC implementing an acoustic metric).  
quantum_hardware_platform | Neutral atoms: two-dimensional Bose-Einstein condensate of 39K (ultracold atoms).  
encoding_and_mapping | Phononic field in the condensate is mapped to a massless real relativistic scalar field via the acoustic metric; metric elements set by local speed of sound c_s(t,r) where c_s^2 = λ(t) n_0(r)/m (Eq. (6)). Spatial curvature (κ) is encoded in the radial density profile n_0(r) (e.g. hyperbolic: n_0(r)=¯ n_0 [1 - r^2/R^2]^2; spherical: n_0(r)=¯ n_0 [1 + r^2/R^2]^2). Time-dependent scale factor a(t) is implemented by controlling the 3D s-wave scattering length a_s(t) (via Feshbach resonance) with relation a^2(t) ∝ 1/a_s(t) (Eq. (2)). Coordinates map: laboratory radial coordinate r -> reduced circumference coordinate u(r)=r/(1-r^2/R^2) (Eq. (8)). No qubit encoding, no truncation/discretization in qubit sense; continuum phonon field approximated in experimental finite-size geometry and measured continuously (imaging pixels).  
algorithm_or_protocol | Experimental protocol: shape static spatial density (harmonic trap or DMD-shaped potential) to set spatial curvature; perform controlled power-law ramps of scattering length a_s(t) to effect scale factor a(t) ∝ t^γ (power-law ramps with chosen γ and durations Δt); measure in-situ density and compute density contrast (Eq. (3)); extract two-point correlation function <δ_c δ_c>(L) as function of metric distance L (Eq. (9)); perform zero-order Hankel transform (Eq. (10)) to obtain spectral S_k and monitor time evolution (heterodyne detection via interference with condensate background). This is an analog time-evolution experiment rather than a digital quantum algorithm.  
resource_estimates | Platform experimental parameters reported (not qubit resources): ~23,000 atoms in 2D BEC; tight z-trap ω_z = 2π·1.6 kHz; radial trap frequency dynamically adjustable between 7 Hz and 23 Hz; Thomas-Fermi radius R_TF ~ 25–30 μm; scattering length ramps from ~400 a_B to 50 a_B; imaging resolution ~1 μm. No gate counts, circuit depths, qubit numbers, T-gates, or measurement-shot scaling are applicable/ reported.  
noise_and_error_mitigation | Experimental noise sources and mitigations described qualitatively: finite temperature (initial T measured ~60(10) nK; effective central temperature inferred ~40 nK), atom-number post-selection (realisations post-selected within 10% of mean atom number), pixel averaging (4 pixels) to increase SNR, optical resolution convolution accounted for in theory comparisons (Gaussian σ=0.8 μm). No digital error-correction or QEC methods (not relevant).  
key_results_or_demonstrations | Demonstrated configurable spatial curvature (negative/hyperbolic and positive/spherical) via density shaping and verified by wave-packet propagation along predicted geodesics; implemented time-dependent FLRW expansions via controlled a_s(t) ramps and observed particle (phonon) pair production manifested as enhanced density fluctuations and nontrivial two-point correlations; measured real-space propagation of correlation features at speed v = 2.5(1) μm/ms (consistent with twice central c_s); observed Sakharov oscillations in spectral modes S_k with amplitude and phase evolution matching analytic predictions for Bogoliubov-mode evolution (fits f_k(t_h)=A_k cos(2 ω_k t_h + ϑ_k) + const); quantitative agreement between experiment and analytic theory for amplitude and phase for different expansion exponents γ (0.5, 1.0, 1.5) and two ramp durations. This is a laboratory hardware experiment (analog simulator) with direct experimental measurements.  
validation_and_benchmarks | Validation via multiple methods: analytic theory for free massless scalar field mode evolution in (2+1)-D expanding spacetime (refs [32],[48]) used to predict Bogoliubov coefficients, amplitude and phase of oscillations; comparison between observed wave-packet trajectories and geodesics calculated from acoustic metric (Eq. (9)); speed of sound cross-checked via fits to data and GPE ground-state simulations; spectral data compared to theoretical S_k including thermal initial distributions; convolution with optical resolution included in theoretical curves (Extended Data Figure). Statistical averaging over many realisations; post-selection for atom-number stability.  
claimed_feasibility | Authors claim the platform establishes a new class of quantum-field simulator in curved spacetime and that straightforward upgrades will allow access to new regimes; the experiments are fully feasible on their current analog cold-atom apparatus (NISQ/analogue era). No claims that fault-tolerant quantum computing is required; no projections given in gates/qubits/time for a digital quantum-computing implementation.  
limitations_and_open_problems | Limitations stated explicitly: experiment realises phononic (linearized) scalar-field dynamics (no dynamical metric backreaction from the phonons); finite-size effects (central region approximates the intended metric; deviations occur close to Thomas-Fermi radius ~25 μm); optical resolution (~1 μm) and finite imaging SNR limit spatial fidelity; effective temperature and thermal population differences (thermal excitations are expelled from centre affecting inferred effective temperature); experiment is an analogue model, not a true gravitational system — horizons and full black-hole dynamics are not implemented here. Open problems: entanglement in time-evolving curved space, event-horizon thermodynamics, multispecies/extensions to more exotic spacetime geometries.  
complexity_or_hardness_arguments | No computational complexity claims (BQP/QMA/etc.) or hardness arguments are made — paper is experimental analogue simulation rather than digital quantum algorithm or complexity-theoretic proposal.  
theory_context_keywords | analogue gravity, acoustic metric, FLRW metric, (2+1)-dimensional scalar QFT, cosmological particle production, Bogoliubov coefficients, Sakharov oscillations, Poincaré disc mapping, Hankel transform, phonons.  
citations_to_prior_work | Key prior works cited in the analogue-gravity and BEC/horizon literature: W. G. Unruh, 'Experimental Black-Hole Evaporation?' (1981); L. J. Garay et al., 'Sonic Analog of Gravitational Black Holes in Bose-Einstein Condensates' (2000); P. Jain et al., 'Analog model of a Friedmann-Robertson-Walker universe in Bose-Einstein condensates' (2007); I. Carusotto et al., 'Numerical observation of Hawking radiation from acoustic black holes in atomic Bose-Einstein condensates' (2008); O. Lahav et al., 'Realization of a Sonic Black Hole Analog in a Bose-Einstein Condensate' (2010); J. Steinhauer, 'Observation of self-amplifying Hawking radiation in an analogue black-hole laser' (2014); J. R. Muñoz de Nova et al., 'Observation of thermal Hawking radiation and its temperature in an analogue black hole' (2019); and theoretical method papers and companion theory arXiv:2202.10441, arXiv:2202.10440 cited as [32],[48].  
  
### Sonic (acoustic) black hole analogue in fluids/BECs

Field | Value  
---|---  
name_short | Sonic-black-hole-analogue  
name_full | Sonic (acoustic) black hole analogue in fluids/BECs  
brief_description | A class of analogue-gravity proposals/experiments where spatial flow profiles (regions of sub- and supersonic flow) in a fluid or BEC create an effective metric with an event-horizon analogue, enabling study of Hawking-like radiation and horizon-related phenomena in the laboratory.  
citation_title | Experimental Black-Hole Evaporation?  
mention_or_use | mention  
target_system_or_model | Acoustic metric for phonons in flowing fluids/BECs that mimic event-horizon geometries (Unruh's analogy); effectively quantum field theory on a curved background that contains horizon-like features.  
black_hole_phenomena_targeted | Hawking radiation analogues, horizon formation, stimulated/thermal emission from horizons, black-hole-laser instabilities.  
simulation_paradigm | Analog quantum simulation (fluid/condensate flow generates metric).  
quantum_hardware_platform | Neutral atoms (BEC), fluids, light in nonlinear media, ion traps and other analogue platforms (historical papers across platforms cited).  
encoding_and_mapping | Mapping: background flow velocity v(r) and local sound speed c_s(r) produce acoustic metric g_{μν} where horizons occur where |v|=c_s; phononic excitations map to quantum field modes propagating on this metric. The present paper references the general acoustic-metric mapping concept but does not implement a horizon.  
algorithm_or_protocol | Physical engineering of flow profile (e.g., constrictions, moving potentials) to create supersonic/subsonic regions; measurement of correlations, emitted phonon spectra, and thermal signatures. (This paper only cites such approaches historically.)  
resource_estimates | No resource estimates in qubit terms; experimental parameters vary per cited work. The present paper does not provide gate/circuit resources.  
noise_and_error_mitigation | Experimental issues in cited works include thermal backgrounds and finite-size effects; mitigation using careful trap shaping, single-phonon detection, correlation measurements. The present paper does not expand on specific noise models for horizon experiments.  
key_results_or_demonstrations | Mentioned prior demonstrations in literature (cited): experimental realisations of sonic black-hole analogues and observations consistent with Hawking-like emission in BEC and other systems (see refs [21],[22],[23],[25] in the paper). The present paper does not itself perform a black-hole/horizon experiment but places its FLRW simulator in the analogue-gravity context.  
validation_and_benchmarks | Prior horizon experiments validated via correlation measurements, spectral fits to thermal/Hawking predictions, and numerical (GPE) simulations. The present paper references those validation approaches but does not reproduce them here.  
claimed_feasibility | Analog horizon experiments are feasible in current BEC setups (cited), and have been realised; authors reference those works as established.  
limitations_and_open_problems | Known limitations (cited literature): distinguishing genuine quantum Hawking emission from classical/thermal backgrounds, finite-temperature effects, trans-Planckian and dispersion concerns in analogue systems, limited tunability of flows. The present paper notes analogue-gravity is not the same as real gravity and that their setup addresses a different class (FLRW) of curved spacetimes.  
complexity_or_hardness_arguments | No computational complexity statements in the present paper regarding horizon analogues.  
theory_context_keywords | acoustic metric, analogue gravity, Hawking radiation analogue, sonic horizons, Bogoliubov excitations.  
citations_to_prior_work | References in paper: W. G. Unruh (1981), L. J. Garay et al. (2000), I. Carusotto et al. (2008), O. Lahav et al. (2010), J. Steinhauer (2014), J. R. Muñoz de Nova et al. (2019), and reviews on analogue models (e.g. M. Visser et al., M. Novello et al.).  
  
### Analogue Hawking-radiation experiments (BECs, fluids, light, ions)

Field | Value  
---|---  
name_short | Analogue-Hawking-expts  
name_full | Analogue Hawking-radiation experiments (BECs, fluids, light, ions)  
brief_description | A set of experimental and numerical studies that aim to observe Hawking-like radiation and related horizon physics in analogue systems (BECs, fluids, optical fibers, quantum fluids of light, ion traps).  
citation_title |   
mention_or_use | mention  
target_system_or_model | Acoustic/optical analogue metrics with horizon-like regions; phonon or photon quantum fields on effective curved backgrounds.  
black_hole_phenomena_targeted | Hawking radiation spectrum/temperature, stimulated Hawking emission, black-hole-laser instabilities, analogue thermal emission.  
simulation_paradigm | Analog experiments and numerical simulations (Gross-Pitaevskii equation simulations, classical-field methods, quantum-optical heterodyne detection).  
quantum_hardware_platform | BECs (neutral atoms), nonlinear optics/fibers, quantum fluids of light, trapped ions (cited examples across the references).  
encoding_and_mapping | Mapping via acoustic/optical metric; the present paper cites these works to contextualise analogue-gravity but does not implement horizon-specific encodings.  
algorithm_or_protocol | Experimental protocols: generate supersonic flows or inhomogeneous refractive-index profiles; measure two-point correlations, emission spectra, and temperature via correlation and spectral analysis. Numerical protocols: GPE and classical-field simulations.  
resource_estimates | Not applicable in qubit terms; experiments report trap frequencies, atom numbers and imaging resolutions (varies by cited work).  
noise_and_error_mitigation | Common experimental concerns: thermal backgrounds, finite imaging resolution, shot noise; mitigations include averaging many realisations, post-selection, and heterodyne-type detection (cited).  
key_results_or_demonstrations | Cited experimental claims include observations interpreted as Hawking-like emission and measurements of associated temperatures and correlations (e.g. refs [20],[21],[23],[25] in the paper). The current paper references these as precedent but does not present new horizon results.  
validation_and_benchmarks | Prior works validated using correlation analysis, comparison to numerical GPE simulations, and fits to thermal/Hawking predictions; the present paper cites these validation methodologies.  
claimed_feasibility | Cited experiments demonstrate feasibility on current analogue platforms; the paper treats these as established results in the analogue-gravity community.  
limitations_and_open_problems | Ambiguities remain in separating quantum Hawking radiation from classical/stimulated emission and thermal noise; dispersion and trans-Planckian issues in analogues; scaling to other gravitational phenomena remains challenging.  
complexity_or_hardness_arguments | None in this paper.  
theory_context_keywords | Hawking radiation analogue, stimulated emission, black-hole laser, acoustic horizons, GPE simulations.  
citations_to_prior_work | Representative cited experimental/numerical papers: T. G. Philbin et al. (fiber-optical analogue), S. Weinfurtner et al. (stimulated Hawking emission), I. Carusotto et al. (numerical Hawking radiation), O. Lahav et al. (sonic black hole realisation), J. Steinhauer (self-amplifying Hawking radiation), J. R. Muñoz de Nova et al. (observation of thermal Hawking radiation).  
  
## Citation

Cite this artifact as `\cite{ast-ext-viermann-2026-08-13}`.
[code] 
    @misc{ast-ext-viermann-2026-08-13,
      title        = {Extraction: Quantum field simulator for dynamics in curved spacetime},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-field-simulator-for-dynamics-in-curved-spacetime.md},
      crossref     = {viermann2022quantum},
      note         = {Theorizer's extraction from \cite{viermann2022quantum}. asta-artifact id: extraction-result-93},
    }
    
    @article{viermann2022quantum,
      title     = {Quantum field simulator for dynamics in curved spacetime},
      author    = {C. Viermann and Marius Sparn and Nikolas Liebster and Maurus Hans and Elinor Kath and Á. Parra-López and Mireia Tolosa-Simeón and N. S'anchez-Kuntz and Tobias Haas and H. Strobel and S. Floerchinger and M. Oberthaler},
      year      = {2022},
      journal   = {Nature},
      url       = {https://www.semanticscholar.org/paper/247011689},
    }
[/code]
