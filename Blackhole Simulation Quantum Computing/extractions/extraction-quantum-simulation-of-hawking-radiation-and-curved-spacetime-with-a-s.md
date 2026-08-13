[<- All artifacts](<../index.md>)

# Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole

**Contents:**

  * Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole



### Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole

Field | Value  
---|---  
name_short | On‑chip lattice black hole  
name_full | Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole  
brief_description | Experimental analogue 'lattice black hole' implemented on a 1D chain of 10 superconducting transmon qubits (with 9 tunable couplers) that realizes a site-dependent hopping XY model mapped from a (1+1)-D massless Dirac field in Eddington–Finkelstein coordinates and demonstrates stimulated Hawking radiation and entanglement dynamics across an analogue horizon.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in (1+1)-D curved spacetime (massless Dirac field) discretized to a lattice XY / spinless fermion model (lattice black hole, Jacobson-type lattice)  
black_hole_phenomena_targeted | Hawking radiation (thermal spectrum / tunneling rate and effective Hawking temperature), horizon trapping/particle transmission, dynamics of entanglement (entanglement entropy and concurrence evolution) in presence of an analogue event horizon  
simulation_paradigm | Analog quantum simulation realized on a gate-capable superconducting processor with programmable Hamiltonian (quench dynamics / quantum walks); experiment is effectively an analog/quench simulation rather than digital trotterized circuit decomposition (hybrid control: pulses + static engineered couplings)  
quantum_hardware_platform | Superconducting transmon qubits with flux-tunable transmon-type couplers (10 qubits + 9 tunable couplers)  
encoding_and_mapping | Continuum (1+1)-D massless Dirac field in advanced Eddington–Finkelstein coordinates → discretized on a spatial lattice x_j with lattice spacing d; metric enters via site-dependent nearest-neighbour hopping κ_j related to metric function f(x) by κ_j ≈ f((j - j_h + 1/2)d)/(4 d) (authors use κ_j ≈ (f(x_{j+1})+f(x_j))/(8d) ≈ f(x_j + d/2)/(4d)); spin-1/2 XY model (σ_j^+σ_{j+1}^- + h.c.) is implemented, mapped to spinless fermions by Jordan–Wigner; horizon defined at site j_h where f(x_h)=0 (in experiment j_h=3); on-site potentials μ_j correspond to local chemical potential / frequency offsets; open boundary conditions used (finite chain).  
algorithm_or_protocol | Prepare localized single-particle or two-particle initial states (or Bell pair inside horizon), quench into resonant frequencies and engineered static coupling profile κ_j, then allow unitary evolution e^{-iHt} (quantum walk) for variable t; measure site occupations (single-shot readout averaged) and perform multi-qubit quantum state tomography (QST) on the exterior subsystem (Q4–Q10) to extract energy-resolved radiation probabilities P_n = ⟨E_n|ρ_out|E_n⟩ and entanglement measures (von Neumann entropy, concurrence); fit P(E) to exponential Boltzmann form P_out(E) ∝ e^{-E/T_H} (tunneling/detailed-balance picture).  
resource_estimates | Implemented on N=10 physical qubits and 9 tunable couplers; engineered coupling distribution κ_j using couplers with parameters β/(2π) ≈ 4.39 MHz and η d = 0.35 (they also implemented a uniform κ/(2π) ≈ 2.94 MHz for flat spacetime). Experiment times: evolution times up to 1000 ns; occupation measurements: 5000 single-shot repetitions for each occupation snapshot; QST: 7-qubit tomography on Q4–Q10 (density matrix reconstructed at t=0 and t=1000 ns); error bars/calibration statistics reported from 50 repetitive runs for some datasets and 10 repetitive runs for entanglement tomography. No explicit large-scale resource scaling estimate (gate counts, T‑count, fault-tolerant overhead) or asymptotic circuit-depth scaling for large lattices is provided.  
noise_and_error_mitigation | Noise sources and calibration: decoherence (T1, T2), XY crosstalk, thermal excitation, leakage, pulse distortion and Z-control crosstalk; authors employed extensive device calibration (automatic calibration of qubit/coupler spectra, pulse-shape pre-distortion, Z-crosstalk compensation) and optimized coupler-biasing to realize target κ_j. No error-mitigation protocols like zero-noise extrapolation (ZNE) or probabilistic error cancellation (PEC) are reported; validation relies on high-fidelity calibration, comparing experiment to noise-aware numerical simulations (including imperfect initial state) and quoting fidelities (see key results).  
key_results_or_demonstrations | Hardware experiment demonstrating: (i) quantum-walk dynamics differ for engineered curved κ_j vs uniform κ_j; particles initialized inside horizon show suppressed escape but nonzero P_out(t) (stimulated tunneling analogous to Hawking radiation); (ii) extracted radiation probabilities versus energy fit an exponential spectrum P(E) ∝ e^{-E/T_H}; theoretical T_H/(2π)=β/(8π^2) → numerical value T_H ≈ 1.7×10^{-5} K (simulation), experimental fitted T_H ≈ 7.7×10^{-5} K (same order of magnitude); (iii) fidelity between measured and theoretical site occupancy distributions >97% within 400 ns for quantum-walk comparisons; (iv) 7-qubit QST fidelity at t=0: 99.2% (initial), t=1000 ns: 88.1%; (v) dynamics of an entangled Bell pair inside the analogue horizon: entanglement entropy increases in curved case, concurrence decays slower than in flat case; observed stimulated Hawking radiation (since an excitation was injected). This is an experimental analog demonstration (not a full QFT continuum simulation) performed on real superconducting hardware.  
validation_and_benchmarks | Validation by: (1) direct comparison of measured site-occupations to exact numerical simulation of the engineered finite lattice Hamiltonian (fidelity F(t)=∑_j sqrt(p_j q_j) >97% for 400 ns), (2) comparing extracted energy-resolved radiation probabilities from QST to theoretical exponential dependence from tunneling/detailed-balance (fit to P(E) ∝ e^{-E/T_H}), (3) using numerical simulations seeded with experimentally measured imperfect initial state to explain deviations, (4) discussion of finite-size effects via larger-chain numerical simulations (e.g., 300-site numerics) and disorder sensitivity studies in Supplementary Information, and (5) citing continuum tunneling derivation (analytic) for the temperature T_H = g_h/(2π) with g_h = f'(x_h)/2.  
claimed_feasibility | Authors claim the analogue-curved-spacetime mapping is feasible on near-term superconducting processors with tunable couplers; current demonstration is a first step requiring more qubits, better control accuracy and extended Hamiltonian classes to study more phenomena. They highlight that the experiment is NISQ-feasible for (1+1)-D lattice analogues but that fuller quantum-field-theory-in-curved-spacetime simulations (higher dimensions, dynamical spacetime, backreaction) will need larger scale devices and/or hybrid digital-analog approaches; no explicit threshold or fault-tolerance timeline is given.  
limitations_and_open_problems | Explicit limitations noted: finite-size lattice and boundary reflections (finite chain length causes reflections and affects long-time P_out), experiment observes stimulated rather than spontaneous Hawking radiation (initial excitation inserted), coordinate choice (advanced Eddington–Finkelstein) selects outgoing modes only, mapping restricted to (1+1)-D massless Dirac (or scalar) fields and to static spacetime backgrounds encoded in κ_j (no dynamical metric/backreaction), practical limitations from decoherence and control imperfections, lack of complexity-theoretic analysis for large-scale simulation, and the need to generalize mapping theory for different gravitational fields / higher dimensions.  
complexity_or_hardness_arguments | No formal complexity-theoretic claims (BQP/QMA hardness etc.) are made in the paper; the authors do not present hardness proofs or scaling lower bounds for simulating these analogue black-hole models on classical hardware versus quantum hardware.  
theory_context_keywords | quantum field theory in curved spacetime, (1+1)-D Dirac field, Eddington–Finkelstein coordinates, lattice black hole, Hawking radiation, tunneling picture, surface gravity, quantum walks, Jordan–Wigner mapping, analogue gravity  
citations_to_prior_work | Key prior works cited in context include: Unruh 1981 'Experimental Black-Hole Evaporation?' and follow-ups on sonic/analogue black holes; Corley & Jacobson 'Lattice black holes' (Phys. Rev. D 57, 6269 (1998)) and Jacobson & Mattingly 'Hawking radiation on a falling lattice' (Phys. Rev. D 61, 024017 (1999)); Parikh & Wilczek 'Hawking Radiation As Tunneling' (Phys. Rev. Lett. 85, 5042 (2000)); R.-Q. Yang et al., 'Simulating quantum field theory in curved spacetime with quantum many-body systems' (Phys. Rev. Research 2, 023107 (2020)) which provides theoretical mapping; experimental analogue Hawking works in BEC (Steinhauer 2016, Munoz de Nova 2019/2021) and optical/flow analogues (Weinfurtner et al., Philbin et al.); and works on tunable couplers and superconducting processors enabling multi-qubit interactions (Yan et al. PR Applied 2018; Sung et al. PRX 2021; Arute et al. Nature 2019).  
  
## Citation

Cite this artifact as `\cite{ast-ext-shi-2026-08-13}`.
[code] 
    @misc{ast-ext-shi-2026-08-13,
      title        = {Extraction: Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-hawking-radiation-and-curved-spacetime-with-a-s.md},
      crossref     = {shi2021quantum},
      note         = {Theorizer's extraction from \cite{shi2021quantum}. asta-artifact id: extraction-result-15},
    }
    
    @article{shi2021quantum,
      title     = {Quantum simulation of Hawking radiation and curved spacetime with a superconducting on-chip black hole},
      author    = {Yun-hao Shi and Run-Qiu Yang and Zhongcheng Xiang and Zi-Yong Ge and Hao Li and Yong-Yi Wang and Kaixuan Huang and Ye Tian and Xiaohui Song and D. Zheng and Kai Xu and R. Cai and Heng Fan},
      year      = {2021},
      journal   = {Nature Communications},
      url       = {https://www.semanticscholar.org/paper/259075712},
    }
[/code]
