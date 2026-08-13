[<- All artifacts](<../index.md>)

# Extraction: A bound on chaos

**Contents:**

  * Out-of-time-order correlator (OTOC) and squared commutator C(t)
  * Thermofield double state and two-sided correlators
  * Qubit models and random quantum circuits as models of scrambling
  * Bulk near-horizon scattering in AdS (shockwave/eikonal analysis) and the Rindler scattering bound
  * Bound on chaos: λ_L ≤ 2π/β (λ_L ≤ 2π k_B T / ħ)



### Out-of-time-order correlator (OTOC) and squared commutator C(t)

Field | Value  
---|---  
name_short | OTOC / commutator diagnostics  
name_full | Out-of-time-order correlator (OTOC) and squared commutator C(t)  
brief_description | Thermal quantum diagnostic of chaos defined via F(t)=tr[yVyW(t)yVyW(t)] and C(t) = -⟨[W(t),V(0)]^2⟩; used to quantify scrambling and to define a Lyapunov exponent for operator growth.  
citation_title |   
mention_or_use | use  
target_system_or_model | Generic thermal quantum systems; large-N gauge theories with holographic duals (black holes in AdS), semiclassical billiards, and qubit/lattice models as examples  
black_hole_phenomena_targeted | Scrambling (butterfly effect), operator growth, relation to near-horizon high-energy scattering and Lyapunov exponent  
simulation_paradigm | conceptual / measurement target (measurement of OTOCs); no specific quantum-simulation algorithm is provided in the paper  
quantum_hardware_platform | None  
encoding_and_mapping | Not specified; the paper notes qubit models (Pauli operator bases) and large-N operator bases as contexts where OTOCs are meaningful, but gives no explicit qubit mapping or discretization  
algorithm_or_protocol | Measurement of OTOCs conceptually identified as the observable of interest; no concrete circuit or Hamiltonian-simulation algorithm described  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Analytic argument and bounds on the rate of growth of OTOC-related quantities leading to the universal bound on the Lyapunov exponent λ_L ≤ 2π/β; connects exponential growth of OTOCs in holographic large-N systems to near-horizon scattering with s ∼ exp(2πt/β)  
validation_and_benchmarks | Validated by comparison to known semiclassical examples (billiards), large-N holographic calculations (shockwave scattering in black hole backgrounds), and expected weak-coupling behavior; no experimental or quantum-hardware benchmarks  
claimed_feasibility | Not applicable as a hardware claim; authors discuss regimes (large N, separation of timescales) where OTOC behavior and bounds apply but do not assess feasibility of quantum simulation  
limitations_and_open_problems | Paper does not provide protocols to prepare states or measure OTOCs on quantum hardware; practical preparation of thermofield double states and measurement of such complex correlators is not addressed here  
complexity_or_hardness_arguments | No explicit complexity-theoretic statement about measuring OTOCs on quantum devices is given in the paper  
theory_context_keywords | OTOC, squared commutator, scrambling time, dissipation time, Lyapunov exponent, fast scrambling, large N, holography, AdS black holes, shockwave scattering  
citations_to_prior_work | References discussing operator growth and scrambling: [4] Larkin & Ovchinnikov (1969); quantum-circuit scrambling refs [9–15]; holographic computations [16,17,5,18,19]  
  
### Thermofield double state and two-sided correlators

Field | Value  
---|---  
name_short | Thermofield double (TFD)  
name_full | Thermofield double state and two-sided correlators  
brief_description | TFD state |TFD⟩ = Z^{-1/2} ∑_n e^{-βE_n/2} | n̄ ⟩_L | n ⟩_R used to interpret OTOCs as two-sided correlators and to connect operator growth to destruction of entanglement between the two sides (black hole two-sided geometry).  
citation_title |   
mention_or_use | use  
target_system_or_model | Two-copy thermal systems equivalent to two-sided black hole in holography (two-sided AdS black hole / Rindler wedge interpretation)  
black_hole_phenomena_targeted | Two-sided correlation structure of the eternal black hole, interpretation of operator insertion as perturbations to the TFD, and connection to wormhole-type geometry  
simulation_paradigm | conceptual target state for simulations intending to probe two-sided correlators/ER=EPR analogues; paper does not provide a preparation algorithm  
quantum_hardware_platform | None  
encoding_and_mapping | Not specified; the TFD is discussed abstractly. The paper notes its role in mapping single-trace CFT correlators to two-sided gravity but gives no qubit encoding  
algorithm_or_protocol | No explicit circuit protocol given; the TFD is used analytically to reinterpret F(t) as ⟨Ψ|V_L V_R|Ψ⟩ with |Ψ⟩ a perturbed TFD  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Provides conceptual mapping: decay of F(t) corresponds to destruction of special two-sided correlations in TFD by time-evolved operators; used to motivate connection between OTOC decay and bulk high-energy scattering near the horizon  
validation_and_benchmarks | Cross-checked against holographic shockwave calculations and general thermal-field-theory analytic structure; not validated via quantum simulation  
claimed_feasibility | Paper notes conceptual difficulty (TFD is highly non-generic) but does not discuss concrete feasibility or resource requirements for preparing TFD on quantum devices  
limitations_and_open_problems | Practical state preparation of TFD and operational two-sided measurements on quantum hardware are not addressed; mapping to finite qubit systems left implicit  
complexity_or_hardness_arguments | No explicit complexity claims about preparing TFD  
theory_context_keywords | thermofield double, two-sided black hole, entanglement, ER=EPR (contextual), two-sided correlators  
citations_to_prior_work | Uses standard thermofield formalism; cites holographic works that employ TFD interpretation [16,17,5,18,19]  
  
### Qubit models and random quantum circuits as models of scrambling

Field | Value  
---|---  
name_short | Qubit / random-circuit scrambling  
name_full | Qubit models and random quantum circuits as models of scrambling  
brief_description | Discussion of qubit lattice and nonlocal qubit models where operator growth and scrambling occur (W(t) expressed in Pauli bases), and references to literature on random quantum circuits and unitary designs as contexts exhibiting logarithmic or fast scrambling.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Large-N qubit systems, nonlocal quantum circuits, and lattice quantum systems (many qubits N_q)  
black_hole_phenomena_targeted | Analogue of scrambling and operator growth (toy-model mimicry of black-hole fast scrambling behavior)  
simulation_paradigm | Digital quantum circuits / random-circuit paradigms are discussed conceptually (refs [9–14]) but no explicit simulation protocol is given in this paper  
quantum_hardware_platform | platform-agnostic (discussion is abstract about qubit systems)  
encoding_and_mapping | Qualitative: operators built from local Pauli factors; time evolution produces growth in Pauli weight; no explicit Jordan-Wigner or fermion mappings are given  
algorithm_or_protocol | Random quantum circuits and local Hamiltonian evolution are cited as mechanisms producing scrambling; no explicit Trotterization, measurement circuit, or resource breakdown provided  
resource_estimates | Scaling statements: qualitative scaling t__∼ log N_q for nonlocal qubit models and t__ ∼ distance for local models; no concrete qubit counts, gate counts, or depths provided  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Paper uses qubit/random-circuit models as conceptual examples to argue that many-body systems can show parametrically separated dissipation and scrambling times; no experimental/demo results  
validation_and_benchmarks | References to mathematical results (Lieb-Robinson bounds) and literature on random circuits; no hardware benchmarking  
claimed_feasibility | Paper does not claim feasibility for quantum-hardware simulations, only uses qubit models as illustrative toy systems  
limitations_and_open_problems | No circuit constructions or verification strategies are provided; bridging toy qubit models to gravitational duals remains speculative  
complexity_or_hardness_arguments | No explicit complexity-theory statements, but cites works on unitary designs and scrambling convergence rates  
theory_context_keywords | qubit models, random quantum circuits, unitary 2-designs, Lieb-Robinson bounds, fast scrambling, Pauli operator bases  
citations_to_prior_work | Random-circuit and scrambling literature cited: [9] Dankert et al.; [10] Harrow & Low; [11] Arnaud & Braun; [12] Brown & Viola; [14] Brown & Fawzi; [15] Lashkari et al.  
  
### Bulk near-horizon scattering in AdS (shockwave/eikonal analysis) and the Rindler scattering bound

Field | Value  
---|---  
name_short | Holographic black hole scattering (Rindler/high-energy)  
name_full | Bulk near-horizon scattering in AdS (shockwave/eikonal analysis) and the Rindler scattering bound  
brief_description | Relates late-time exponential growth of OTOCs to high-energy scattering near the black hole horizon with center-of-mass energy s ∼ β^{-2} exp(2πt/β); for Einstein gravity this yields F(t) ≈ f0 - f1 N^{-2} e^{2πt/β} and motivates the universal bound λ_L ≤ 2π/β.  
citation_title |   
mention_or_use | use  
target_system_or_model | Holographic large-N CFTs dual to black holes in Einstein gravity (AdS black branes/black holes) and Rindler wedge CFT interpretation  
black_hole_phenomena_targeted | Scrambling rate (Lyapunov exponent), shockwave backreaction, eikonal phase δ(s), connection to causality/analyticity (scattering bound)  
simulation_paradigm | Analytic holographic calculation / semiclassical gravity; not a quantum-computational simulation  
quantum_hardware_platform | None  
encoding_and_mapping | Not applicable; mapping is between boundary OTOCs and bulk scattering amplitudes via AdS/CFT rather than a qubit encoding  
algorithm_or_protocol | Shockwave/eikonal gravitational scattering calculations and use of large-N factorization; no quantum algorithms specified  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Derives the characteristic exponential growth rate of OTOC contributions in Einstein gravity and shows higher-derivative corrections do not change the spin-two dominance that sets the exponent; relates growth to bulk scattering phase δ(s) and bounds its growth (p ≤ 1 where δ ∝ G_N s^p)  
validation_and_benchmarks | Comparison across Einstein gravity, higher-derivative corrections, and stringy corrections (cite [19]); consistency with semiclassical examples and scattering analyticity/causality arguments (cite [32])  
claimed_feasibility | Paper does not propose quantum-hardware simulation; rather it identifies black holes in Einstein gravity as reference systems with maximal allowed Lyapunov exponent  
limitations_and_open_problems | Translation of these bulk scattering calculations to explicit quantum-simulation protocols is not provided; stringy corrections and weak-coupling field-theory behavior show deviations from the Einstein result  
complexity_or_hardness_arguments | Discusses physical constraints (unitarity, analyticity, causality) rather than computational complexity; no BQP/QMA statements  
theory_context_keywords | AdS/CFT, shockwave scattering, eikonal phase, Rindler horizon, large N, Einstein gravity, scattering bound, string corrections  
citations_to_prior_work | Holographic and scattering references: [16] Shenker & Stanford 'Black holes and the butterfly effect'; [17] 'Multiple Shocks'; [19] 'Stringy effects in scrambling'; scattering bound citation [32]  
  
### Bound on chaos: λ_L ≤ 2π/β (λ_L ≤ 2π k_B T / ħ)

Field | Value  
---|---  
name_short | Chaos bound (Lyapunov bound)  
name_full | Bound on chaos: λ_L ≤ 2π/β (λ_L ≤ 2π k_B T / ħ)  
brief_description | Main conjecture/result of the paper: in thermal quantum systems with many degrees of freedom and a separation between dissipation and scrambling times, the Lyapunov exponent controlling early exponential growth of OTOCs obeys λ_L ≤ 2π/β.  
citation_title | here  
mention_or_use | use  
target_system_or_model | General thermal quantum systems satisfying analyticity and approximate factorization (includes large-N CFTs holographically dual to Einstein gravity and semiclassical chaotic systems)  
black_hole_phenomena_targeted | Rate of scrambling in black holes (characterizes how fast perturbations grow near horizons); sets a reference for 'fastest' chaos realized by black holes  
simulation_paradigm | The bound is a theoretical constraint on OTOC growth rather than a simulation protocol; it constrains expectations for any simulator attempting to reproduce black-hole-like scrambling  
quantum_hardware_platform | None  
encoding_and_mapping | None  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Provides a rigorous argument (under stated physical assumptions) for the bound and connects saturation to Einstein-gravity holographic systems; shows how the bound emerges from analyticity and Schwarz-Pick type argument on the complex time plane  
validation_and_benchmarks | Supported by holographic calculations (Einstein gravity gives saturation), higher-derivative and string corrections (give ≤ value), semiclassical billiards (classical limit consistent when ħ→0)  
claimed_feasibility | Not a feasibility claim for quantum simulation; rather a universal theoretical bound that any simulation of chaotic thermal systems should respect  
limitations_and_open_problems | Argument depends on factorization assumptions and a separation of timescales; fails or is not applicable in systems without these properties (e.g., random-matrix-type Hamiltonians, certain 2D CFT light-cone singularities)  
complexity_or_hardness_arguments | No computational complexity classification, but the bound is linked to physical analyticity/unitarity/causality constraints  
theory_context_keywords | chaos bound, Lyapunov exponent, analyticity in complex time, Schwarz-Pick theorem, factorization, fast scrambling, large N, holography  
citations_to_prior_work | Motivated by holographic computations [16,17,5,18,19], and earlier discussions of scrambling [2,3] and semiclassical diagnostics [4]  
  
## Citation

Cite this artifact as `\cite{ast-ext-maldacena-2026-08-13-2}`.
[code] 
    @misc{ast-ext-maldacena-2026-08-13-2,
      title        = {Extraction: A bound on chaos},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-a-bound-on-chaos.md},
      crossref     = {maldacena2015bound},
      note         = {Theorizer's extraction from \cite{maldacena2015bound}. asta-artifact id: extraction-result-86},
    }
    
    @article{maldacena2015bound,
      title     = {A bound on chaos},
      author    = {J. Maldacena and S. Shenker and D. Stanford},
      year      = {2015},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/84832638},
    }
[/code]
