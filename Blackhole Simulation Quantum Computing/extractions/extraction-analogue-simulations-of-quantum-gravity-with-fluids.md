[<- All artifacts](<../index.md>)

# Extraction: Analogue simulations of quantum gravity with fluids

**Contents:**

  * Bose-Einstein condensate acoustic black hole with measured Hawking-partner entangled phonon pairs
  * Parametrically modulated Bose-Einstein condensate simulation of Unruh radiation
  * Quantum fluid of light simulating rotating (2+1)-D black hole and sonic ergoregion with observed superradiance
  * Planar Anti-de Sitter black-hole analogue realized with a nonrelativistic BEC in (2+1) dimensions
  * Relativistic Bose-Einstein condensate models whose acoustic spacetime obeys Nordström scalar gravitation equations
  * Fluid-system modified dispersion relations as analogues of Planck-scale / Lorentz-violating corrections in quantum gravity
  * Numerical simulations in a fluid of light showing phonon backreaction and excitation of quasi-normal modes



### Bose-Einstein condensate acoustic black hole with measured Hawking-partner entangled phonon pairs

Field | Value  
---|---  
name_short | BEC acoustic BH (Hawking pairs)  
name_full | Bose-Einstein condensate acoustic black hole with measured Hawking-partner entangled phonon pairs  
brief_description | Analogue acoustic black hole implemented in a BEC where phononic excitations experience an effective curved spacetime; experiments measured density-density correlations across the sonic horizon and reported quantum entanglement between Hawking and partner phonons.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Quantum field theory in curved spacetime realized as phonon field on an acoustic metric in a Bose-Einstein condensate (acoustic black hole / sonic horizon)  
black_hole_phenomena_targeted | Hawking radiation (phononic Hawking pairs), entanglement between Hawking and partner modes, Hawking temperature (thermal spectrum), stationary nature of emission  
simulation_paradigm | analog quantum simulation (quantum fluid analog — phonons in a BEC act as quantum field on curved background)  
quantum_hardware_platform | neutral atoms / Bose-Einstein condensate (cold-atom platform)  
encoding_and_mapping | Physical mapping: condensate mean field (ψ0) defines a background flow velocity v(x) and speed of sound c_s(x), which determine an acoustic metric g_{μν} = [[-c_s^2+v^2, -v^T],[-v, I]]; phonon excitations (density/phase fluctuations ψ1) are the quantum field degrees of freedom propagating on this emergent spacetime. Sonic horizon realized where normal component of v crosses c_s (subsonic → supersonic). No qubit encoding or digitization — continuum analogue.  
algorithm_or_protocol | Experimental protocols: create inhomogeneous flow with supersonic region (using potentials/flows), measure density-density correlations across horizon to extract pair correlations and entanglement; spectral analysis to infer temperature. (No digital quantum algorithm.)  
resource_estimates | Not specified; experiment-dependent (atom number, trap geometry, imaging resolution) — paper gives no qubit/gate counts or circuit depths.  
noise_and_error_mitigation | Experimental noise sources discussed qualitatively (finite temperature background, detection noise, non-ideal hydrodynamic limit, dissipation); mitigation via operating in hydrodynamic regime, careful imaging and averaging. No quantum-computing error mitigation protocols discussed.  
key_results_or_demonstrations | Paper reports (by citation) that quantum signatures of Hawking radiation were observed in BECs via direct measurement of density-density correlations and entanglement between outgoing and ingoing phonon pairs; subsequent experiments verified thermal nature and stationarity of the spectrum. In this Perspective the authors summarise these experimental demonstrations (they do not present new data).  
validation_and_benchmarks | Validation reported in cited experiments by comparison to semiclassical Hawking predictions: density correlations consistent with pair production, spectral shape compared with thermal prediction determined by horizon surface gravity; stationarity tests performed in experiments.  
claimed_feasibility | Feasible and already realized in current cold-atom analogue platforms (NISQ-like experimental systems); further experiments suggested to probe backreaction and correlations between condensate atomic states and phonons.  
limitations_and_open_problems | Analogue simulates kinematic aspects only (field propagation) not Einstein dynamics; limited to hydrodynamic (low-energy) regime; background typically treated classically (ψ0), so full unitary evolution including backreaction requires access to higher-order nonlinear terms; finite-size and short-distance (beyond-hydrodynamic) deviations present.  
complexity_or_hardness_arguments | No complexity-theoretic claims made.  
theory_context_keywords | acoustic metric, Hawking radiation, phonons, sonic horizon, backreaction, entanglement, hydrodynamic limit  
citations_to_prior_work | [9] Unruh 1981; experimental references cited in text for BEC results e.g. refs cited as [28],[29],[30]; general analogue gravity reviews [10],[15]  
  
### Parametrically modulated Bose-Einstein condensate simulation of Unruh radiation

Field | Value  
---|---  
name_short | Parametric-BEC Unruh simulation  
name_full | Parametrically modulated Bose-Einstein condensate simulation of Unruh radiation  
brief_description | Quantum simulation of Unruh radiation achieved by parametrically modulating a BEC trap so that modulation plays the role of boosting to an accelerating reference frame; collective excitations display thermal-like populations analogous to Unruh effect.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Unruh effect / Rindler acceleration radiation simulated by phonon excitations in a parametrically driven BEC  
black_hole_phenomena_targeted | Unruh radiation (thermal response seen by accelerated observers), analogue of acceleration-induced particle production  
simulation_paradigm | analog quantum simulation (time-dependent modulation of quantum fluid parameters to emulate non-inertial frame effects)  
quantum_hardware_platform | Bose-Einstein condensate (neutral-atom platform) with trap modulation  
encoding_and_mapping | Mapping: temporal parametric modulation of system parameters reproduces the effect of a time-dependent Bogoliubov transformation analogous to an accelerated observer seeing a thermal bath; excitations in lab frame correspond to Rindler modes in analogue mapping.  
algorithm_or_protocol | Protocol: parametric modulation of trapping potential (drive), measure excitation populations and correlations to infer Unruh-like thermal spectra; no digital quantum algorithm used.  
resource_estimates | Not provided (experiment-specific: modulation amplitude/frequency, atom number, detection sensitivity); no qubit resources.  
noise_and_error_mitigation | Experimental limitations from heating, finite temperature and decoherence; mitigation via low-temperature operation and controlled modulation; no quantum-error-correction discussed.  
key_results_or_demonstrations | Cited experiments reported observation of Unruh-like signatures in parametrically modulated BECs (thermal-like excitation spectra correlated with modulation parameters). The Perspective summarizes these as proof-of-principle quantum simulations.  
validation_and_benchmarks | Compared experimentally to theoretical predictions for parametric excitation and to expected Unruh temperature scaling with modulation parameters; evidence consistent with analogue-Unruh expectations.  
claimed_feasibility | Already demonstrated in table-top cold-atom experiments; accessible with present analogue quantum fluid technology.  
limitations_and_open_problems | Analogy limited to kinematic aspects (mode populations) and to regimes where mapping to acceleration is valid; distinction between true observer-dependent particle notion and lab-frame excitations needs care.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | Unruh effect, parametric modulation, Bogoliubov transformation, analogue accelerated observer  
citations_to_prior_work | Reference to experiment reported in text as [31]; general analogue gravity references [9],[10]  
  
### Quantum fluid of light simulating rotating (2+1)-D black hole and sonic ergoregion with observed superradiance

Field | Value  
---|---  
name_short | Photon-fluid rotating BH (superradiance)  
name_full | Quantum fluid of light simulating rotating (2+1)-D black hole and sonic ergoregion with observed superradiance  
brief_description | Rotating effective spacetime created in photon superfluids (quantum fluids of light) or in water tank vortices to simulate (2+1)-D rotating black holes and ergoregions; experiments observed Penrose-like superradiant amplification and mode amplification in the sonic ergoregion.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Rotating black hole analogue in (2+1) dimensions (ergosphere and superradiance) implemented as vortex flows in photon superfluids or water tanks  
black_hole_phenomena_targeted | Penrose superradiance, ergoregion amplification, horizon-less superradiant scattering, black-hole bomb instability conditions and scalar-cloud analogues when massive modes present  
simulation_paradigm | analog quantum simulation (photon superfluid or classical fluid vortices providing rotating background metric)  
quantum_hardware_platform | quantum fluids of light (photonic condensates / microcavity polaritons) and classical water tank experiments; for quantum aspects photon superfluid platform is relevant  
encoding_and_mapping | Mapping: vortex flow velocity field v(θ) creates frame-dragging in acoustic metric for phonon-like (polaritonic) excitations; angular velocity of flow maps to black hole rotational parameter; massless vs massive excitations depend on medium interactions (photon fluids typically massless, some engineered condensates support massive phonons).  
algorithm_or_protocol | Experimental scattering experiments: excite waves/modes and measure amplification or scattering spectra; in photon fluids, measure mode occupations and correlations; no digital algorithm used.  
resource_estimates | Not specified; platform resource demands are experimental (optical pump power, cavity quality, detection bandwidth).  
noise_and_error_mitigation | Dissipation and absorption in optical systems discussed qualitatively (e.g., absorbing object experiments); experiments tune parameters to observe amplification above losses. No quantum-computing error mitigation applied.  
key_results_or_demonstrations | Reported observations (cited) of Penrose superradiance in water and photon-fluid experiments and evidence of modes amplified in a sonic ergoregion in photon-fluid setups; demonstration that superradiance does not require an event horizon.  
validation_and_benchmarks | Comparison of observed amplification with theoretical superradiance conditions (frequency relative to rotational frequency); experimental checks of dispersion-regime dependence (dispersive vs nondispersive).  
claimed_feasibility | Demonstrated experimentally in laboratory platforms (classical and quantum fluids); feasible with current photonics/condensate technology.  
limitations_and_open_problems | Most fluctuations are massless in many platforms, limiting study of massive-field bound states; nonlinear backreaction and full gravitational dynamics not simulated; finite dissipation modifies ideal predictions.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | ergosphere, superradiance, Penrose process, vortex flow, photon superfluid, acoustic metric  
citations_to_prior_work | Experiments and theory cited in text, e.g. refs [32],[33],[34],[35],[37],[38] (as mentioned in Perspective)  
  
### Planar Anti-de Sitter black-hole analogue realized with a nonrelativistic BEC in (2+1) dimensions

Field | Value  
---|---  
name_short | Analogue Planar-AdS in BEC  
name_full | Planar Anti-de Sitter black-hole analogue realized with a nonrelativistic BEC in (2+1) dimensions  
brief_description | Proposal/realization that planar AdS black-hole solutions can be exactly mimicked using nonrelativistic Bose-Einstein condensates in (2+1) dimensions, enabling analogue tests of holographic ideas relating boundary dynamics and bulk emergent geometry.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Planar AdS black-hole geometry (holographic toy model) mapped to condensate flow in (2+1) dimensions  
black_hole_phenomena_targeted | Holographic correspondence tests: relation between boundary fluid dynamics and bulk effective metric, excitations propagation in volume vs correlated dynamics at boundary  
simulation_paradigm | analog quantum simulation (BEC as platform to emulate both bulk and boundary dynamics in an emergent-gravity/holography analogue)  
quantum_hardware_platform | Bose-Einstein condensate (neutral-atom platform), platform-agnostic conceptual mapping  
encoding_and_mapping | Mapping: engineered condensate background provides effective metric reproducing asymptotic AdS geometry; boundary fluid dynamics can be implemented in another coupled fluid or engineered degrees of freedom, producing an analogue of bulk-boundary correspondence. No qubit encoding or discrete holographic tensor network used in the paper's proposals.  
algorithm_or_protocol | Experimental/theoretical protocol proposals: engineer condensate density/flow profiles to match AdS black-hole metric, measure excitations in volume and correlated observables at the effective boundary; study backreaction to probe emergent gravitational dynamics.  
resource_estimates | Not provided (conceptual proposal); no digital computational resources given.  
noise_and_error_mitigation | Not discussed beyond usual experimental considerations for cold-atom systems.  
key_results_or_demonstrations | Perspective reports that planar AdS black-hole solutions can be exactly mimicked in nonrelativistic BECs (citing prior work), enabling potential experimental tests of bulk-boundary relationships; no new experimental data presented here.  
validation_and_benchmarks | Proposals validated by theoretical mapping in cited works; ultimate validation would require measuring bulk excitations and boundary correlations and comparing to AdS/CFT predictions.  
claimed_feasibility | Authors view this as promising and potentially realizable in analogue experiments; further work required to study backreaction and emergent gravitational phonon dynamics.  
limitations_and_open_problems | Analogue models may reproduce only kinematic or restricted dynamical aspects; real AdS/CFT gravitational dynamics (Einstein equations) not generically emergent from nonrelativistic BECs without further structure; need to demonstrate backreaction yields gravitational-like equations.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | AdS/CFT, holography, emergent gravity, bulk-boundary correspondence, analogue AdS black hole  
citations_to_prior_work | Cited works in text given as [124],[125],[126],[127] (specific references in Perspective)  
  
### Relativistic Bose-Einstein condensate models whose acoustic spacetime obeys Nordström scalar gravitation equations

Field | Value  
---|---  
name_short | Relativistic BEC → Nordström gravity  
name_full | Relativistic Bose-Einstein condensate models whose acoustic spacetime obeys Nordström scalar gravitation equations  
brief_description | Relativistic BEC models where the acoustic spacetime dynamics take the form of a geometric theory equivalent to Nordström scalar gravity: curvature determined by stress-energy expectation of quasiparticles, with Newton and cosmological constants set by microscopic scales.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Emergent semiclassical scalar-gravity (Nordström theory) from relativistic BEC microscopic dynamics  
black_hole_phenomena_targeted | Emergence of gravitational dynamics, potentially allowing analogue study of backreaction and semiclassical gravity effects (not a direct black-hole solution necessarily but relevant to gravitational dynamics)  
simulation_paradigm | analog quantum simulation of emergent gravitational dynamics (relativistic quantum fluid degrees of freedom produce geometric field equations)  
quantum_hardware_platform | Relativistic condensate models (theoretical); not an implemented hardware experiment in the Perspective  
encoding_and_mapping | Mapping: expectation value of phonon stress-energy in relativistic BEC provides source for emergent scalar curvature; condensate microscopic scales set effective gravitational coupling constants. No qubit encoding.  
algorithm_or_protocol | Theoretical derivation and modelling; proposed experimental implications include measuring quasiparticle distributions and backreaction signatures in relativistic-like condensates.  
resource_estimates | Not applicable / not provided.  
noise_and_error_mitigation | Not discussed.  
key_results_or_demonstrations | Authors highlight prior theoretical work showing Nordström gravity equations can emerge in relativistic BECs, representing a geometric semiclassical gravity analogue; Perspective suggests this as a route to closer analogues of gravitational dynamics.  
validation_and_benchmarks | Validation in cited theoretical work via derivation of field equations from microscopic model and mapping of coupling constants to microscopic scales. Experimental validation remains an open direction.  
claimed_feasibility | Conceptually feasible as a theoretical mapping; realization would require engineered relativistic-condensate setups—viewed as promising but not yet standard laboratory practice.  
limitations_and_open_problems | Scalar (Nordström) gravity is not full tensorial general relativity; equivalence limited to scalar gravity features. Need to generalize to tensorial Einstein-like dynamics for more faithful analogues.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | emergent gravity, Nordström theory, semiclassical gravity, backreaction, relativistic BEC  
citations_to_prior_work | Cited as result in text with reference [122]  
  
### Fluid-system modified dispersion relations as analogues of Planck-scale / Lorentz-violating corrections in quantum gravity

Field | Value  
---|---  
name_short | Modified-dispersion analogue (planckian effects)  
name_full | Fluid-system modified dispersion relations as analogues of Planck-scale / Lorentz-violating corrections in quantum gravity  
brief_description | Analogue study of high-energy/short-distance corrections to field propagation via phonon dispersion relations in fluids (Bogoliubov, surface-wave, viscous corrections, roton minima), used to explore robustness of Hawking radiation and deviations from thermality.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Modified-dispersion quantum field theory on curved spacetime analogues — phonon dispersion relations in fluids model Planck-scale Lorentz-violating corrections  
black_hole_phenomena_targeted | Effects of short-distance/Planck-scale physics on Hawking radiation spectrum (deviations from thermality), modified greybody factors, influence of roton minima on emission  
simulation_paradigm | analog quantum / classical simulation (engineering microscopic fluid parameters to introduce Lorentz-breaking dispersion in phonon modes)  
quantum_hardware_platform | Various fluids: water tanks (surface waves), atomic BECs (Bogoliubov dispersion), dipolar BECs (roton features), viscous classical fluids — platform-agnostic comparative study  
encoding_and_mapping | Mapping: higher-order momentum-dependent terms in phonon dispersion (e.g., Bogoliubov relation with p^4 corrections, roton minima) correspond to Lorentz-violating dispersion relations studied in quantum gravity phenomenology; analogue Planck momentum p_c = M c_s sets scale.  
algorithm_or_protocol | Experimental protocol: operate analogue black holes in regimes where short-distance physics is relevant (shallow channels, surface tension effects, dipolar interactions), measure emitted spectra and correlations to detect deviations from thermal Hawking emission; theoretical/numerical analysis of dispersion effects on mode conversion and spectrum.  
resource_estimates | Not provided; experimental requirements depend on achieving length/momentum scales where dispersion matters (coherence length, channel depth, interaction strength). No quantum computational resource estimates.  
noise_and_error_mitigation | Discussed qualitatively: dissipative terms (viscosity), nonlinearities, and finite-size effects can mask dispersion-induced signatures; experiments operate to minimise these but full mitigation strategies are experimental in nature.  
key_results_or_demonstrations | Perspective summarises theoretical and experimental evidence that Hawking radiation is robust to many high-energy modifications but that specific dispersion features (e.g., roton minima, surface-tension-induced microscale) can produce measurable deviations from thermality, greybody factors, and mode-conversion effects; cites experiments reporting deviations [25] and theoretical work [107–114].  
validation_and_benchmarks | Validation via comparison between measured spectra/correlations and predictions from models with modified dispersion; numerical simulations support robustness of low-energy Hawking radiation and predict specific high-energy deviations.  
claimed_feasibility | Authors argue experiments can be engineered to probe dispersion-induced Planckian effects using current/controlable fluid platforms (e.g., dipolar BECs, surface-wave channels).  
limitations_and_open_problems | Analogue mapping is limited to kinematic aspects and to the particular microscopic physics of the chosen fluid; universality of conclusions for quantum gravity remains interpretationally limited; isolating genuine quantum-gravity analogues from fluid-specific effects is challenging.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | modified dispersion relations, Lorentz violation, analogue Planck scale, Bogoliubov dispersion, roton minimum, greybody factors  
citations_to_prior_work | References in text include [72–75] for quantum-gravity modified dispersion literature and fluid examples [100–105],[113–114] for Bogoliubov and dispersion-specific studies  
  
### Numerical simulations in a fluid of light showing phonon backreaction and excitation of quasi-normal modes

Field | Value  
---|---  
name_short | Fluid-of-light backreaction numerics  
name_full | Numerical simulations in a fluid of light showing phonon backreaction and excitation of quasi-normal modes  
brief_description | Numerical studies (with realistic experimental parameters) in photon-fluid platforms demonstrating that phonon quantum fluctuations near a sonic horizon produce correlated Hawking emission and excite quasi-normal modes of the acoustic black hole (a form of quantum backreaction).  
citation_title |   
mention_or_use | mention  
target_system_or_model | Phonon field on an acoustic metric in photon superfluids (fluid of light); semiclassical/numerical simulation including backreaction effects  
black_hole_phenomena_targeted | Quantum backreaction, quasi-normal mode excitation, signatures in density correlations and Hawking spectrum  
simulation_paradigm | numerical simulation of quantum/fluid-field dynamics (classical field simulations including quantum fluctuations or semiclassical approximations) — not gate-based quantum computation  
quantum_hardware_platform | Photon superfluid (fluid of light) as experimental platform for the parameters used in numerics  
encoding_and_mapping | Mapping: numerical field variables correspond to condensate order parameter and phonon modes; background flow determines acoustic metric; quantum fluctuations included perturbatively to model phonon emission and backreaction.  
algorithm_or_protocol | Numerical protocols: integrate nonlinear wave/mean-field equations with stochastic/quantum-noise seeds to capture spontaneous emission and backreaction; extract density-density correlations and spectral features. Not a quantum algorithm.  
resource_estimates | Not specified (computational cost not given in Perspective).  
noise_and_error_mitigation | Numerical considerations: include realistic experimental dissipation and parameter noise; no QC error mitigation discussed.  
key_results_or_demonstrations | Cited numerical results show coupled behaviour: correlated Hawking emission and excitation of quasi-normal modes in the acoustic black hole, with signatures visible in density correlations and spectrum — demonstrating an instance of quantum backreaction in an analogue system.  
validation_and_benchmarks | Comparison of numerical outputs with theoretical predictions for Hawking correlations and quasi-normal mode frequencies; parameter choices motivated by experimentally realistic regimes.  
claimed_feasibility | Numerical studies indicate that experiments in photon superfluids could observe such backreaction signatures with current or near-term technology.  
limitations_and_open_problems | Numerical models depend on approximations (mean-field + perturbations); fully quantum backreaction beyond perturbative regime remains challenging; translation to gravitational backreaction in full GR is analogical and limited.  
complexity_or_hardness_arguments | None given.  
theory_context_keywords | backreaction, quasi-normal modes, photon superfluid, density correlations, semiclassical numerics  
citations_to_prior_work | Cited within text as recent numerical simulations (ref. given in Perspective as [48])  
  
## Citation

Cite this artifact as `\cite{ast-ext-braunstein-2026-08-13}`.
[code] 
    @misc{ast-ext-braunstein-2026-08-13,
      title        = {Extraction: Analogue simulations of quantum gravity with fluids},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-analogue-simulations-of-quantum-gravity-with-fluids.md},
      crossref     = {braunstein2023analogue},
      note         = {Theorizer's extraction from \cite{braunstein2023analogue}. asta-artifact id: extraction-result-63},
    }
    
    @article{braunstein2023analogue,
      title     = {Analogue simulations of quantum gravity with fluids},
      author    = {S. Braunstein and M. Faizal and L. Krauss and F. Marino and N. Shah},
      year      = {2023},
      journal   = {Nature Reviews Physics},
      url       = {https://www.semanticscholar.org/paper/261139644},
    }
[/code]
