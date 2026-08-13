[<- All artifacts](<../index.md>)

# Extraction: Simulation of the massless Dirac field in 1+1D curved spacetime

**Contents:**

  * Mapping of the 1+1D massless Dirac field in curved spacetime (Simpson metric) onto a site-dependent isotropic XY / Hubbard model
  * Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole (as cited)



### Mapping of the 1+1D massless Dirac field in curved spacetime (Simpson metric) onto a site-dependent isotropic XY / Hubbard model

Field | Value  
---|---  
name_short | Dirac->XY mapping (Simpson spacetime)  
name_full | Mapping of the 1+1D massless Dirac field in curved spacetime (Simpson metric) onto a site-dependent isotropic XY / Hubbard model  
brief_description | A construction that transforms the massless Dirac equation in 1+1D static curved spacetimes (written in arbitrary observer coordinates such as Schwarzschild or Painlevé) into a discretized fermionic tight-binding Hamiltonian with site-dependent hoppings, which is then mapped to an isotropic XY spin model (or Hubbard model) via Jordan-Wigner for implementation on quantum simulation platforms.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Massless Dirac field in 1+1D curved spacetime (Simpson spacetime; Schwarzschild and Painlevé coordinate forms) mapped to a site-dependent fermionic tight-binding model (hopping Hamiltonian) and then to an isotropic XY spin model or Hubbard model.  
black_hole_phenomena_targeted | Hawking radiation tunneling spectrum (tunneling rates compared to blackbody spectrum), infinite redshift near horizon (observed as slowing of wavepacket in Schwarzschild coordinates), particle crossing-horizon dynamics (Painlevé coordinates), and wormhole traversal for Simpson spacetime with a > r_s.  
simulation_paradigm | Analog quantum simulation / Hamiltonian simulation on quantum many-body platforms (XY / Hubbard dynamics); the paper performs classical numerical time-evolution of the mapped lattice model (i.e., simulation-only numerics) but proposes implementation on quantum simulators (superconducting circuits, ion traps).  
quantum_hardware_platform | superconducting circuits (explicitly mentioned), trapped-ion platforms (mentioned), platform-agnostic (waveguide arrays, ultracold atoms mentioned in introduction as viable platforms).  
encoding_and_mapping | Continuous PDE transformed by variable substitution φ = Q(r) ω where Q(r)=√c(r) e^{∫V(r)/c(r) dr}; spatial discretization with lattice spacing d producing site-dependent hopping κ_n ≈ c(n-1/2)d/(2d). Resulting lattice fermionic Hamiltonian H = Σ_n[-κ_n(a_n^† a_{n-1}+h.c.) - μ a_n^† a_n]. Fermion-to-qubit mapping is via Jordan-Wigner to obtain an isotropic XY spin model; Dirichlet boundary conditions used in numerical simulations. The mapping reduces to known forms in special limits (V(r)=0 or constant c(r)).  
algorithm_or_protocol | No explicit gate-based algorithm specified; protocol is: derive site-dependent XY/Hubbard Hamiltonian from continuum Dirac equation, then simulate real-time dynamics of that lattice Hamiltonian (classical numerics in paper). Intended quantum implementation would realize the XY/Hubbard Hamiltonian dynamics on analog quantum simulators or digital hardware (no explicit Trotterization/phase-estimation/VQE described).  
resource_estimates | Not provided — the paper gives no quantitative resource counts (no qubit number, gate depth, shot counts, or FT assumptions).  
noise_and_error_mitigation | Not discussed — the manuscript does not present a noise model or error mitigation strategies for experimental implementations.  
key_results_or_demonstrations | Numerical (classical) simulations of the mapped lattice dynamics showing: (i) in Schwarzschild coordinates, the outgoing-wave tunneling rate matches a blackbody spectrum with an effective temperature 2T_b (numerical points align with theoretical curve); (ii) in Painlevé coordinates, tunneling rates match a blackbody at T_b and full wavepacket crossing of the horizon is observed (incoming waves complete); (iii) wavepacket dynamics show infinite-redshift-like slowing near the horizon in Schwarzschild coordinates and smooth horizon crossing in Painlevé coordinates; (iv) by varying Simpson parameter a, transition from regular black hole (0r_s) is simulated, with successful wormhole traversal dynamics for a>r_s. These are simulation-only demonstrations (no quantum hardware experiment).  
validation_and_benchmarks | Validation by comparison to semiclassical/general-relativistic expectations and analytic Hawking-radiation results: tunneling spectra compared with blackbody predictions (appendix reproduces traditional derivation steps and shows agreement), qualitative matches to GR behaviors (redshift, horizon crossing), and consistency checks to previous mapping limits (reduces to Yang et al. [27] when V=0 and to Sabín et al. [25,26] when c(r) constant). No hardware benchmarks or finite-size scaling error-bars provided beyond plotted numerical agreement.  
claimed_feasibility | Authors claim the mapped XY/Hubbard models can be implemented on present quantum-simulation platforms (superconducting circuits, ion traps, optical waveguides, ultracold atoms) and thus that the approach is experimentally realizable in principle; no quantitative feasibility timeline or NISQ vs fault-tolerant separation is provided.  
limitations_and_open_problems | Limited to 1+1D massless Dirac fields (no massive fields considered); mapping yields effective single-particle tight-binding Hamiltonians — the work does not address backreaction or dynamical spacetime; all results are classical numerical simulations of the mapped lattice (no quantum hardware demonstration); no resource estimates, noise analysis, or error mitigation protocols; Schwarzschild coordinates suffer coordinate-singularity issues for incoming waves (authors switch to Painlevé to avoid this); boundary reflections (Dirichlet BC) are present in numerics; entanglement/Hawking-pair correlations or thermofield-double state preparation not addressed; extension to higher-dimensions and interacting fields left to future work.  
complexity_or_hardness_arguments | None provided — no statements about computational complexity (BQP/QMA hardness) or classical intractability are made in the paper.  
theory_context_keywords | massless Dirac equation, 1+1D curved spacetime, Simpson spacetime, Schwarzschild coordinates, Painlevé coordinates, Hawking radiation, infinite redshift, traversable wormhole, regular black hole, Jordan-Wigner, isotropic XY model, Hubbard model, analog quantum simulation, lattice discretization, tunneling rate.  
citations_to_prior_work | Key referenced prior works include: R.-Q. Yang et al., 'Simulating quantum field theory in curved spacetime with quantum many-body systems' [27]; Y.-H. Shi et al., 'Quantum simulation of hawking radiation and curved spacetime with a superconducting on-chip black hole' [24]; C. Sabín, 'Mapping curved spacetimes into dirac spinors' [25]; C. Koke, C. Noh, and D. G. Angelakis, 'Dirac equation in 2-dimensional curved spacetime, particle creation, and coupled waveguide arrays' [19]; Z. Tian and J. Du, 'Analogue hawking radiation and quantum soliton evaporation in a superconducting circuit' [23]; C. Sabín et al., 'Encoding relativistic potential dynamics into free evolution' [26]; plus broader experimental-analogue literature (Bose-Einstein condensates, optical waveguides, superconducting circuits, ultracold atoms) cited in the introduction.  
additional_notes | The mapping procedure is explicit: start from metric ds^2 = -e^{A(r)} dt^2 + e^{B(r)} dr^2, choose an explicit vielbein, derive first-order PDE ∂_t φ = -c(r) ∂_r φ + V(r) φ, perform φ=Q(r) ω substitution to eliminate first-order potential term, discretize space, and obtain site-dependent hopping Hamiltonian. The Simpson spacetime f(r)=1 - r_s/√(r^2+a^2) is used as the demonstrator metric.  
  
### Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole (as cited)

Field | Value  
---|---  
name_short | On-chip superconducting black hole (Shi et al.)  
name_full | Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole (as cited)  
brief_description | A previously reported quantum-simulation proposal/experiment (cited) using superconducting circuitry to simulate Hawking-radiation-like physics and curved-spacetime effects on-chip; cited here as related experimental progress in superconducting platforms.  
citation_title | Quantum simulation of hawking radiation and curved spacetime with a superconducting on-chip black hole  
mention_or_use | mention  
target_system_or_model | Superconducting-circuit implementation of effective black-hole analog (cited; details not expanded in this paper).  
black_hole_phenomena_targeted | Hawking radiation / black-hole analog effects (cited).  
simulation_paradigm | Quantum simulation on superconducting qubits / on-chip analog (cited by authors as prior art).  
quantum_hardware_platform | superconducting circuits (explicit in citation).  
encoding_and_mapping | Not detailed in this paper; referenced as an example where curved-spacetime/black-hole physics was simulated using superconducting platforms.  
algorithm_or_protocol | Not detailed in this paper.  
resource_estimates | Not provided in this manuscript (citation only).  
noise_and_error_mitigation | Not discussed here (citation only).  
key_results_or_demonstrations | Referred-to as earlier work that simulates black-hole radiation on superconducting chips; this paper cites it as motivation/related work but does not reproduce its experimental details.  
validation_and_benchmarks | Not discussed in this manuscript (citation only).  
claimed_feasibility | Cited as an example of feasible experimental realization on superconducting platforms.  
limitations_and_open_problems | Not discussed here; the present paper only cites this work in related-work context.  
complexity_or_hardness_arguments | None in this manuscript.  
theory_context_keywords | Hawking radiation, superconducting circuit analogs, on-chip black hole (as cited).  
citations_to_prior_work | This entity is itself a cited prior work in the present paper (Y.-H. Shi et al., Nature Communications 2023).  
  
## Citation

Cite this artifact as `\cite{ast-ext-liu-2026-08-13-2}`.
[code] 
    @misc{ast-ext-liu-2026-08-13-2,
      title        = {Extraction: Simulation of the massless Dirac field in 1+1D curved spacetime},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-simulation-of-the-massless-dirac-field-in-11d-curved-spacetime.md},
      crossref     = {liu2024simulation},
      note         = {Theorizer's extraction from \cite{liu2024simulation}. asta-artifact id: extraction-result-20},
    }
    
    @article{liu2024simulation,
      title     = {Simulation of the massless Dirac field in 1+1D curved spacetime},
      author    = {Zhilong Liu and Run-Qiu Yang and Heng Fan and Jieci Wang},
      year      = {2024},
      journal   = {Science China Physics Mechanics and Astronomy},
      url       = {https://www.semanticscholar.org/paper/274233763},
    }
[/code]
