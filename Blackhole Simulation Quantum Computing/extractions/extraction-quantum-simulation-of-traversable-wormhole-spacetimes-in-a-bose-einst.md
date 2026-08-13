[<- All artifacts](<../index.md>)

# Extraction: Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate

**Contents:**

  * Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate
  * dc-SQUID array proposal for 1+1D Ellis wormhole simulation
  * Analogue black-hole simulations in Bose-Einstein condensates (prior literature)



### Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate

Field | Value  
---|---  
name_short | BEC-wormhole-analog  
name_full | Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate  
brief_description | Proposed analog-quantum-simulation recipe to reproduce traversable-wormhole spacetimes (1+1D family with shape b(r) and 3+1D Ellis wormhole) using phonons in a weakly interacting Bose-Einstein condensate by engineering the local speed of sound and flow via spatially dependent scattering length and magnetic field (Feshbach resonance) and by using generalized Gullstrand–Painlevé coordinates for 3+1D.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Traversable wormhole spacetimes (metric with shape function b(r); 1+1D family with b(r)=b0^{1-q} r^q and 3+1D Ellis wormhole with b(r)=b0^2/r), i.e. acoustic analogue of wormhole geometry  
black_hole_phenomena_targeted | Simulation of spacetime geometry associated with traversable wormholes (metric structure, throat, two asymptotically flat branches), i.e. black-hole-like/compact-object spacetime geometry (not direct Hawking radiation or horizon thermodynamics).  
simulation_paradigm | Analog quantum simulation (analogue gravity using phonons in a Bose-Einstein condensate); proposal/analytical+numerical design rather than digital-gate algorithms.  
quantum_hardware_platform | Neutral-atom Bose-Einstein condensate (weakly interacting BEC), platform-agnostic beyond BEC specifics but explicitly assumes cold-atom BEC (e.g., Cs, Rb, K, Na, Li) with tunable scattering length via Feshbach resonance.  
encoding_and_mapping | Metric-matching (continuous-field mapping): match the effective acoustic metric G_{μν} of phonons in a BEC to the target wormhole metric by engineering spatial dependence of the phonon speed c_s(r) and flow 4-velocity v^μ. In 1+1D: exploit conformal invariance to equate c_s^2(r) = c^2[1 - b(r)/r] and realize c_s via a(r) through g = 4πħ^2 a/m and Feshbach-controlled a(B). In 3+1D: use generalized Gullstrand–Painlevé (GP-like) coordinates so the wormhole metric becomes nondiagonal and can be matched to the BEC acoustic metric by choosing constant radial flow v^r = v_∞ and a radial profile c_{s0}(r) ∝ r/b0 (linear in r) (see Eqs. (42),(43)). No qubit mapping or discretization is used (continuum field analogue). Boundary conditions: two branches represented by mapping laboratory coordinate x with |x−R|=r−b0 to embed both branches into a single condensate.  
algorithm_or_protocol | Experimental control protocol rather than quantum algorithm: (1) choose wormhole shape b(r) (family parameter q, throat b0), (2) compute required spatial profile of scattering length a(r) and magnetic field B(r) using relations a(B) near Feshbach resonance and c_s(a) from Bogoliubov speed of sound, (3) implement B(x) spatial profile across the condensate, (4) optionally set background flow v^r (constant) to realize GP-like coordinates; theoretical/numerical solution of matching equations (Eqs. (40a),(40b)). No Trotterization/phase estimation/etc.  
resource_estimates | Experimental parameter estimates (not qubit counts): target phonon speeds c_s ~ 10^{-3}–10^{-2} m/s, background flow v_∞ ≈ 0.009–0.01 m/s, throat radii b0 in μm (examples: b0=0.1–3 μm, plotted values b0=0.1,1,3), condensate density ρ≈10^{15} cm^{-3} used for estimates. Spatial resolution must exceed healing length ξ = ħ/(√2 m c_s); computed ξ values (Table I) range from ≈0.034 μm (Cs) to ≈0.648 μm (Li) for given c_s values; spatial step choices for numerical plots were O(0.4–1.5 μm). No gate/circuit resource estimates since this is an analog experiment.  
noise_and_error_mitigation | Experimental limitations and approximations discussed rather than noise models: approximations include v^r/c ≪ 1 and c_{s0}/c ≪ 1; validity requires condensate length scales larger than healing length ξ so Bogoliubov/Gross-Pitaevskii picture holds. No discussion of quantum-computational noise mitigation; experimental errors would come from imperfect B-field spatial control, scattering-length inhomogeneities, finite-temperature excitations, and deviations from weakly interacting regime.  
key_results_or_demonstrations | Analytical derivation and numerical solutions demonstrating feasibility: (a) 1+1D case: derived B(r) and a(r) profiles (Eqs. (12),(14),(15)) for family b(r)=b0^{1-q} r^q; identified range 0<q<1 as compatible with state-of-the-art spatial variation of scattering length (comparison to Clark et al. [19]); (b) 3+1D case: introduced GP-like coordinates, derived matching conditions and zero-order solution v^r = v_∞, c_{s0}(r)= (v_∞/b0) r (Eqs. (42),(43)), numerically solved full matching (Eqs. (40a),(40b)) and plotted results (Fig.4); derived B(x) and a(x) in lab coordinate (Eqs. (50),(51)) and plotted for Cs (Fig.5), concluding 3+1D requirements likely beyond present capabilities. Overall result: a concrete, experimentally parameterized proposal (theoretical + feasibility analysis) — 1+1D family feasible with current tech, full 3+1D Ellis-wormhole challenging.  
validation_and_benchmarks | Validation by (i) analytical consistency checks (matching acoustic metric components to wormhole metric), (ii) comparison of predicted a(x) spatial variation to experimental measurements/ability from Clark et al. [19] (rate of change of scattering length per μm), (iii) numerical solution of full matching equations and comparison to zero-order analytic solutions (Eqs. (42),(43)) to check approximations, and (iv) consistency with condensate healing length (ξ) to ensure validity of continuum theory. No direct experimental demonstration was performed — validation is theoretical+comparison to experimental control capabilities.  
claimed_feasibility | 1+1D: Claimed feasible with current state-of-the-art (spatial Feshbach control as in Clark et al. [19]) for wormhole shape parameter range 0<q<1 and appropriate b0 scales. 3+1D: Proposed in principle (Ellis wormhole in GP-like coordinates) but experimental requirements (magnetic-field profiles, scattering-length ranges and asymptotes) appear to exceed current capabilities for Cs BEC; identified bottlenecks include required spatial variation/amplitude of scattering length and controlling profiles without hitting resonant asymptotes.  
limitations_and_open_problems | Limitations explicitly stated: (a) analog simulation reproduces acoustic spacetime for phonons, not a dynamical gravitational field (no backreaction or real spacetime curvature), (b) 1+1D lacks true throat topology (only a 1D section), (c) approximations used (v≪c and c_s≪c) and use of weakly interacting BEC/Bogoliubov theory require length scales >ξ, (d) 3+1D details (for Ellis wormhole) produce magnetic-field profiles with asymptotes and high a-values making experimental implementation difficult, (e) no discussion of simulating horizon thermodynamics/Hawking radiation or quantum information aspects like teleportation, and (f) verification in experiment would be indirect (probe phonon propagation) and limited by experimental control.  
complexity_or_hardness_arguments | None provided — no complexity-theoretic claims (BQP/QMA etc.) are made because this is an analog condensed-matter based simulator rather than a computational algorithmic simulation.  
theory_context_keywords | analogue gravity, traversable wormhole, Ellis wormhole, shape function b(r), Gullstrand–Painlevé coordinates, acoustic metric, Feshbach resonance, scattering length spatial control, phonon speed of sound c_s, Bogoliubov theory, healing length ξ  
citations_to_prior_work | References and comparisons: prior dc-SQUID proposal for wormhole simulation by one author [14]; BEC analogue-gravity literature for black holes and gravitational waves [2,16,17,18,21]; experimental spatial control of scattering length via Feshbach resonance [19]; foundational traversable wormhole literature [8,9]; use of GP coordinates references [24,25,26]; embedding/metric references [22,23].  
  
### dc-SQUID array proposal for 1+1D Ellis wormhole simulation

Field | Value  
---|---  
name_short | dcSQUID-wormhole-proposal  
name_full | dc-SQUID array proposal for 1+1D Ellis wormhole simulation  
brief_description | Prior proposal (by one of the authors) to simulate a 1+1D Ellis wormhole using a superconducting dc-SQUID array; cited as earlier work limited to 1+1D and to the Ellis wormhole case.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Ellis wormhole (1+1D section) — simulated via superconducting circuit analog (dc-SQUID array).  
black_hole_phenomena_targeted | Wormhole spacetime geometry (Ellis wormhole) as a black-hole-mimicker-like object; again focused on metric/propagation rather than Hawking radiation.  
simulation_paradigm | Analog quantum simulation implemented in superconducting circuits (dc-SQUID array) — mentioned as prior work.  
quantum_hardware_platform | Superconducting circuits (dc-SQUID array).  
encoding_and_mapping | Not detailed in this paper beyond citation; mapping presumably uses circuit-engineered effective propagation speed for microwave excitations to emulate 1+1D metric (as typical in circuit analogues).  
algorithm_or_protocol | Not applicable in this paper (prior proposal referenced); described as alternative platform for 1+1D wormhole analog.  
resource_estimates | Not provided in this paper (prior work cited without resource details here).  
noise_and_error_mitigation | Not discussed in this paper in context of the cited proposal.  
key_results_or_demonstrations | Mention that the dc-SQUID-based simulation was previously proposed and restricted to 1+1D Ellis wormhole; no experimental realization reported in current paper.  
validation_and_benchmarks | Not given here; prior paper likely contains its own validation but this paper only cites it.  
claimed_feasibility | Mentioned as a prior proposal — no feasibility assessment presented in this paper beyond referencing the earlier work.  
limitations_and_open_problems | Cited limitation: previous SQUID-based proposal was restricted to 1+1D and to the Ellis wormhole only; current paper extends to more general 1+1D family and to 3+1D BEC approach.  
complexity_or_hardness_arguments | None discussed.  
theory_context_keywords | Ellis wormhole, superconducting circuit analogues, 1+1D wormhole simulation  
citations_to_prior_work | Reference [14] (C. Sabín, Phys. Rev. D 94, 081501(R), 2016) is cited as the dc-SQUID wormhole-simulation proposal.  
  
### Analogue black-hole simulations in Bose-Einstein condensates (prior literature)

Field | Value  
---|---  
name_short | BEC-black-hole-analogs  
name_full | Analogue black-hole simulations in Bose-Einstein condensates (prior literature)  
brief_description | Prior established body of work using Bose-Einstein condensates to create sonic/analogue black holes and to study horizon-related phenomena for phonons; cited to place the present wormhole simulation in context of analogue-gravity experiments.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Sonic/analogue black holes in BECs (e.g., configurations creating horizons for phonons), and analogue gravitational-wave simulations.  
black_hole_phenomena_targeted | Horizon physics for phonons (sonic horizons), analog Hawking radiation, and other analogue-gravity phenomena in BECs (cited literature includes Garay et al. and others).  
simulation_paradigm | Analog quantum simulation using continuous BEC field (experimental and theoretical prior work).  
quantum_hardware_platform | Neutral-atom BEC experiments.  
encoding_and_mapping | Acoustic metric mapping of phonon excitations to effective curved spacetime; typically engineer local flow and c_s profiles to create horizons.  
algorithm_or_protocol | Experimental protocols to produce supersonic/subsonic regions and measure phonon correlations; not detailed here but referenced.  
resource_estimates | Not provided here; prior experimental works provide their own experimental parameter regimes.  
noise_and_error_mitigation | Not discussed in detail here; typical experimental noise sources include temperature, finite-size effects, and technical noise in B-field control.  
key_results_or_demonstrations | Cited as existing demonstrations/theory that BECs have been widely used to simulate black holes and gravitational waves; provides context and technological basis for current wormhole-simulation proposal.  
validation_and_benchmarks | Prior literature includes comparisons of analogue predictions to semiclassical expectations and correlation measurements; this paper references them as background but does not reproduce those validations.  
claimed_feasibility | Cited to support feasibility of analogue-gravity experiments in BECs; specific claims delegated to referenced works.  
limitations_and_open_problems | Analogue systems do not reproduce dynamical gravity; limitations apply to backreaction and full quantum-gravity phenomena.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | analogue gravity, sonic black hole, acoustic metric, phonon horizon, Bogoliubov theory  
citations_to_prior_work | References cited in text include Garay et al. (e.g., Phys. Rev. A 2001, Phys. Rev. Lett. 2000) and other analogue-gravity reviews [16,17,18,21].  
  
## Citation

Cite this artifact as `\cite{ast-ext-mateos-2026-08-13}`.
[code] 
    @misc{ast-ext-mateos-2026-08-13,
      title        = {Extraction: Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-traversable-wormhole-spacetimes-in-a-bose-einst.md},
      crossref     = {mateos2017quantum},
      note         = {Theorizer's extraction from \cite{mateos2017quantum}. asta-artifact id: extraction-result-68},
    }
    
    @article{mateos2017quantum,
      title     = {Quantum simulation of traversable wormhole spacetimes in a Bose-Einstein condensate},
      author    = {Jesús Mateos and C. Sab'in},
      year      = {2017},
      url       = {https://www.semanticscholar.org/paper/119200812},
    }
[/code]
