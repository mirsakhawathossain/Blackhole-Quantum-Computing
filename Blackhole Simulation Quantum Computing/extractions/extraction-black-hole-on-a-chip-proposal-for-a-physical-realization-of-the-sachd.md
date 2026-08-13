[<- All artifacts](<../index.md>)

# Extraction: Black Hole on a Chip: Proposal for a Physical Realization of the Sachdev-Ye-Kitaev model in a Solid-State System

**Contents:**

  * Solid-state realization of the Sachdev-Ye-Kitaev (SYK) model via Majorana zero modes at a TI/SC interface
  * Mentioned digital quantum simulation proposals for the SYK model
  * Mentioned ultracold-gas realization proposals for the Sachdev-Ye model
  * Related solid-state SYK proposal using semiconductor quantum wires coupled to a disordered quantum dot



### Solid-state realization of the Sachdev-Ye-Kitaev (SYK) model via Majorana zero modes at a TI/SC interface

Field | Value  
---|---  
name_short | SYK on a chip  
name_full | Solid-state realization of the Sachdev-Ye-Kitaev (SYK) model via Majorana zero modes at a TI/SC interface  
brief_description | Proposal and numeric demonstration that N Majorana zero modes bound to a nanoscale irregular hole in a superconductor proximitizing a 3D topological insulator realize an effective Majorana SYK Hamiltonian (all-to-all random four-fermion couplings) whose low-energy physics is holographically dual to AdS2 extremal black hole horizons.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model (Majorana fermion version: infinite-range, random four-fermion interactions), believed to be holographically dual to extremal black hole horizons in AdS2 / dilaton gravity.  
black_hole_phenomena_targeted | Black-hole-like holographic features associated with the SYK model: AdS2 holographic duality to extremal horizons, fast scrambling / quantum chaos (OTOCs/Lyapunov behavior), non-Fermi-liquid conformal low-energy physics, thermodynamics resembling black hole entropy scaling and thermalization.  
simulation_paradigm | Analog quantum simulation (physical solid-state device implementing SYK Hamiltonian via engineered Majorana zero modes) combined with classical numerical simulation (exact diagonalization up to N=32) for benchmarking.  
quantum_hardware_platform | Solid-state TI/SC heterostructure: Majorana zero modes on the surface of a three-dimensional topological insulator proximitized by an s-wave superconductor (Fu–Kane platform).  
encoding_and_mapping | Low-energy projection (BdG eigenmode expansion) maps the N exact Majorana zero modes χ_j (localized at an irregular hole threaded by N flux quanta) to the SYK operators. Two-fermion terms K_{ij} arise from Σ-breaking perturbations (notably chemical potential μ ≠ 0) and are suppressed at μ=0 due to an extra chiral symmetry; screened Coulomb interactions projected onto the zero-mode subspace produce four-fermion couplings ​J_{ijkl} given by integrals of zero-mode charge densities. Randomness/independence of J_{ijkl} arises from irregular hole shape and mesoscopic disorder; coarse-graining with length ζ (≈ ξ) and M_s grid sites yields a central-limit Gaussian ensemble in M_s ≫ N limit.  
algorithm_or_protocol | Experimental protocols: tunneling spectroscopy / scanning tunneling spectroscopy (STS) to measure averaged spectral function A(ω) (distinguish conformal 1/√|ω| vs semicircle); measurement of level statistics via spectroscopy; OTOC F(t) proposed as diagnostic of scrambling (no concrete experimental protocol for F(t) in this solid-state device given). Numerical protocols: diagonalize BdG to obtain zero-mode wavefunctions, compute K_{ij} and J_{ijkl} from projection formulas (Eqs. 2.11 and 2.12), exact diagonalization of many-body Majorana Hamiltonian (2.15) up to N=32; compute thermodynamics, Green's functions, level statistics, OTOCs.  
resource_estimates | Numerical: exact diagonalization performed up to N=32 (many-body matrix size ~2^{15} × 2^{15} per parity sector for N=32). Experimental (estimates): hole radius scaling R_N ≈ π ξ √(2N) to host N vortices; coupling scale J estimated from screened Coulomb parameters: J estimated ~ (a0 λ_{TF}/(ε ξ^2))×const×E_0; for Pb-like superconductors with ξ ~ tens of nm and ε~50, estimated J on order of tens of μeV (paper gives tens of μeV as example). No qubit counts / gate counts (not a digital protocol).  
noise_and_error_mitigation | Not applicable as a gate-based quantum computation proposal; experimental error sources discussed qualitatively: residual Σ-breaking (e.g., from lattice regularization M_k) and deviations of μ from neutrality produce finite two-fermion couplings K_{ij} that cut off SYK conformal behavior; disorder and finite-sample realizations cause sample-to-sample fluctuations. No quantum-error-correction or noise-mitigation algorithms are proposed.  
key_results_or_demonstrations | Proposal plus extensive numerical evidence: (1) BdG simulations show N exact (up to small lattice-induced splitting) zero modes localized in same region for a stadium-shaped hole threaded by N flux quanta; (2) computed J_{ijkl} ensemble follows expected statistics (central-limit Gaussian for large M_s) and K_{ij} ∝ μ; (3) exact diagonalization of the many-body Hamiltonian (N≤32) yields thermodynamic observables (entropy, heat capacity) qualitatively consistent with SYK large-N behavior; (4) many-body level statistics show Wigner-Dyson ensembles cycling with N mod 8 as predicted for SYK; (5) spectral functions approach conformal 1/√|ω| behavior over an intermediate frequency window when K≪J; (6) OTOCs computed for N≤22 show fast decay consistent with scrambling but N too small to extract temperature-controlled Lyapunov exponent. Overall: a concrete, physically realistic analog realization of SYK with experimentally measurable diagnostics (STS, level statistics).  
validation_and_benchmarks | Validation against analytic large-N SYK theory and limiting cases: (a) compare numerically solved large-N Schwinger-Dyson (Eqs. 3.2,3.3) conformal solutions and free-fermion limit to numerically obtained Green's functions; (b) match thermodynamic quantities (entropy per particle, heat capacity) to SYK expectations; (c) level statistics compared to Wigner-Dyson ensembles (GOE/GUE/GSE) with predicted Z_8 pattern; (d) compare spectral functions to conformal 1/√|ω| and to semicircle law in noninteracting limit; (e) sample averaging over disorder realizations to assess universality. Exact diagonalization provides numerically exact benchmarks for finite N.  
claimed_feasibility | Authors claim experimental feasibility with presently available materials and nanofabrication (TI proximitized by conventional SC, focused ion milling to pattern irregular hole, ability to gate TI to neutrality point), and STS is adequate to detect spectral signatures; energy scales (J) estimated within STS resolution for suitable materials. They note numerics limited to N ≲ 32 but physical realization is not limited by exponential Hilbert space growth; measuring OTOCs remains an open experimental challenge (no protocol provided). Bottlenecks: precise tuning of chemical potential to Dirac point (μ=0) to suppress K_{ij}, controlling screening length and dielectric environment to enhance J, fabricating and stabilizing multi-quantum vortex in hole, and devising a method to measure OTOCs in solid-state device.  
limitations_and_open_problems | Finite-N effects limit observation of asymptotic conformal/SYK scaling; residual two-fermion terms K_{ij} (if μ or disorder breaks Σ) cut off low-frequency SYK behavior; assumptions used in mapping include short-range screened interaction (V(r) approximated as short-ranged) and wavefunction randomness/coarse-graining (M_s ≫ N) for Gaussianity of J's; numerically accessible N too small to extract universal Lyapunov exponent or full 1/√|ω| divergence at lowest ω; no experimental protocol for measuring OTOCs provided; requirement of tuning to global neutrality point may be challenging; energy scales (J) can be small (μeV—meV range) depending on materials and screening.  
complexity_or_hardness_arguments | No complexity-theoretic claims (BQP/QMA/etc.) are made in this paper.  
theory_context_keywords | SYK model, AdS2 holographic duality, extremal black hole horizon, dilaton gravity, fast scrambling, out-of-time-order correlator (OTOC), conformal limit, Jackiw–Rossi index theorem, Majorana zero modes, random-matrix level statistics (Wigner–Dyson), non-Fermi liquid.  
citations_to_prior_work | References and concepts cited as motivation or methods: Kitaev's SYK lectures and subsequent SYK literature (Kitaev [6,7], Maldacena & Stanford [7,9], Sachdev-Ye [4]); proposals to realize SYK with ultracold gases [20] and a protocol for digital quantum simulation of the complex and Majorana SYK models [21]; related solid-state proposal using semiconductor wires + disordered quantum dot [41]; Fu–Kane model for TI/SC interface [36]; Jackiw–Rossi/Weinberg index theorem for zero modes [43,44]; prior numerical/experimental works on Majorana modes in TI/SC heterostructures [34,35]; references on quantum chaos and billiards [39,40].  
  
### Mentioned digital quantum simulation proposals for the SYK model

Field | Value  
---|---  
name_short | Digital QS proposals (ref)  
name_full | Mentioned digital quantum simulation proposals for the SYK model  
brief_description | Paper cites prior work that discussed digital (gate-based) quantum simulation protocols for both complex and Majorana versions of the Sachdev-Ye(-Kitaev) model but does not detail mapping, resources, or algorithms in this manuscript.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model (complex and Majorana fermion versions) — referenced as target of prior digital simulation proposals.  
black_hole_phenomena_targeted | Implied: SYK-related holographic features such as fast scrambling and black-hole-like thermalization (mentioned as motivation), but no specifics in this paper.  
simulation_paradigm | Digital gate-based quantum simulation (referenced work), details not given in this paper.  
quantum_hardware_platform | Platform-agnostic (referenced as digital quantum simulation — no platform specified here).  
encoding_and_mapping | Not specified in this paper; the paper refers to earlier work [21] for a 'protocol for digital quantum simulation' but does not reproduce the mapping/encoding.  
algorithm_or_protocol | Not specified here (the paper only cites the prior digital-simulation protocol).  
resource_estimates |   
noise_and_error_mitigation |   
key_results_or_demonstrations | Only cited as existing work proposing digital quantum simulation; this manuscript does not implement or numerically simulate gate-based protocols.  
validation_and_benchmarks |   
claimed_feasibility | Not discussed beyond citation of the prior proposal.  
limitations_and_open_problems | Not discussed here; the manuscript notes such digital-simulation proposals exist but focuses on a solid-state analog instead.  
complexity_or_hardness_arguments |   
theory_context_keywords | SYK, quantum simulation, Majorana fermions, digital quantum simulation  
citations_to_prior_work | Referenced generically as prior digital simulation proposals (citation [21] in text).  
  
### Mentioned ultracold-gas realization proposals for the Sachdev-Ye model

Field | Value  
---|---  
name_short | Ultracold-gases SYK mention  
name_full | Mentioned ultracold-gas realization proposals for the Sachdev-Ye model  
brief_description | The paper cites prior proposals that realize variants of the Sachdev–Ye model (complex fermion SY) using ultracold atomic systems as a contrasting platform to the solid-state proposal presented here.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Sachdev-Ye (complex-fermion) model closely related to SYK (cited as prior experimental-implementation proposal).  
black_hole_phenomena_targeted | Motivation: SYK family models' connection to holographic duality and black-hole-like quantum chaotic behavior; specific gravitational observables not discussed in this manuscript's mention.  
simulation_paradigm | Analog quantum simulation in ultracold atoms (referenced work), details not provided here.  
quantum_hardware_platform | Ultracold atomic gases (mentioned in references), not used in this paper.  
encoding_and_mapping | Not specified in this manuscript (see referenced work).  
algorithm_or_protocol |   
resource_estimates |   
noise_and_error_mitigation |   
key_results_or_demonstrations | Only cited as prior proposal; no implementation or numerics in this manuscript.  
validation_and_benchmarks |   
claimed_feasibility |   
limitations_and_open_problems |   
complexity_or_hardness_arguments |   
theory_context_keywords | Sachdev–Ye model, ultracold atoms, analog quantum simulation, SYK-related physics  
citations_to_prior_work | Referenced as prior work proposing realization of Sachdev–Ye (complex fermion) model with ultracold gases (citation [20] in text).  
  
### Related solid-state SYK proposal using semiconductor quantum wires coupled to a disordered quantum dot

Field | Value  
---|---  
name_short | Wire+dot SYK proposal (ref)  
name_full | Related solid-state SYK proposal using semiconductor quantum wires coupled to a disordered quantum dot  
brief_description | Paper cites a contemporaneous proposal to realize SYK-like physics in a different solid-state architecture (semiconductor wires + disordered quantum dot) as a related approach, but does not analyze it in detail.  
citation_title |   
mention_or_use | mention  
target_system_or_model | SYK-like model (Majorana or complex fermion variants) realized in semiconductor quantum wires coupled to a disordered dot (referenced work).  
black_hole_phenomena_targeted | Implied: SYK holographic features and scrambling, mentioned as alternative realization route; no details provided here.  
simulation_paradigm | Analog solid-state realization (referenced), not implemented here.  
quantum_hardware_platform | Semiconductor nanowires and quantum dot (referenced).  
encoding_and_mapping | Not specified in this manuscript (see referenced work [41]).  
algorithm_or_protocol |   
resource_estimates |   
noise_and_error_mitigation |   
key_results_or_demonstrations | Mentioned for context; no data or analysis in this manuscript.  
validation_and_benchmarks |   
claimed_feasibility |   
limitations_and_open_problems |   
complexity_or_hardness_arguments |   
theory_context_keywords | SYK realization, semiconductor wires, disordered quantum dot  
citations_to_prior_work | Referenced as a related proposal (citation [41] in text).  
  
## Citation

Cite this artifact as `\cite{ast-ext-pikulin-2026-08-13}`.
[code] 
    @misc{ast-ext-pikulin-2026-08-13,
      title        = {Extraction: Black Hole on a Chip: Proposal for a Physical Realization of the Sachdev-Ye-Kitaev model in a Solid-State System},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-black-hole-on-a-chip-proposal-for-a-physical-realization-of-the-sachd.md},
      crossref     = {pikulin2017black},
      note         = {Theorizer's extraction from \cite{pikulin2017black}. asta-artifact id: extraction-result-26},
    }
    
    @article{pikulin2017black,
      title     = {Black Hole on a Chip: Proposal for a Physical Realization of the Sachdev-Ye-Kitaev model in a Solid-State System},
      author    = {D. Pikulin and M. Franz},
      year      = {2017},
      url       = {https://www.semanticscholar.org/paper/119099352},
    }
[/code]
