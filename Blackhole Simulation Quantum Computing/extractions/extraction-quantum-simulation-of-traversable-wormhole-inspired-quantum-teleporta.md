[<- All artifacts](<../index.md>)

# Extraction: Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model

**Contents:**

  * Quantum-hardware implementation of traversable-wormhole-inspired teleportation using a binary sparse SYK model
  * Binary-coupling sparse Sachdev–Ye–Kitaev (SYK) model
  * Traversable wormhole teleportation protocol (SYK boundary realization)
  * Operator size-winding diagnostics (winding size distribution q(l) and coherence ratio R(l))



### Quantum-hardware implementation of traversable-wormhole-inspired teleportation using a binary sparse SYK model

Field | Value  
---|---  
name_short | TW_HW_SYK  
name_full | Quantum-hardware implementation of traversable-wormhole-inspired teleportation using a binary sparse SYK model  
brief_description | Experimental realization on superconducting qubits of a traversable-wormhole (TW) teleportation protocol driven by a chaotic binary sparse Sachdev–Ye–Kitaev (SYK) Hamiltonian (N=8, K=10), demonstrating the sign-dependent mutual-information asymmetry and size-winding diagnostics expected from holographic duality.  
citation_title | Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model  
mention_or_use | use  
target_system_or_model | Finite-N Sachdev–Ye–Kitaev (SYK) model (q=4), binary sparse variant with N=8 and K=10 nonzero 4-body Majorana terms  
black_hole_phenomena_targeted | Traversable-wormhole teleportation (wormhole-like information transfer), ANEC-violation shockwave analogue (sign-dependent teleportation), size-winding (operator-size-phase alignment) as a gravitational-like diagnostic  
simulation_paradigm | Digital gate-based quantum simulation with a hybrid element: variational preparation of Thermofield Double (VQA) + Trotterized real-time evolution (single-step first-order Lie–Trotter); full gate-based execution on NISQ hardware  
quantum_hardware_platform | Superconducting qubits (IBM device ibm_marrakesh); experimental implementation used a 10-qubit circuit  
encoding_and_mapping | Majorana-to-qubit mapping via Jordan–Wigner transformation mapping each Majorana to Pauli strings (explicit mapping given in Supplemental Sec. S1); two-sided SYK represented on qubit register, TFD preparation approximated variationally; SWAP injection/readout implemented via Dirac operator formed from first two Majoranas.  
algorithm_or_protocol | Traversable-wormhole teleportation protocol: prepare |Bell>_{PQ} ⊗ |TFD >_ with V=(1/qN) H_int at t=0 (double-trace kick), read out at t=t1 via SWAP (or direct measurement); time evolution implemented with single-step first-order Lie–Trotter; Thermofield Double prepared with a hardware-efficient variational quantum algorithm (VQA); final two-qubit state reconstructed by two-qubit tomography.} ⊗ |0>_T, inject message qubit via fermionic SWAP at t=-t0, evolve under H_L+H_R, apply instantaneous two-sided interaction e^{i μ V  
resource_estimates | Experimental instance used 10 physical qubits total; chosen SYK N=8, K=10; compiled full circuit: depth ≈ 765, ~369 two-qubit gates and ~926 single-qubit gates for full protocol (per μ, t1 setting); TFD variational circuit before transpilation: 35 two-qubit gates, 96 single-qubit rotation layers (96 params); compiled TFD depth 56 with 35 two-qubit and 167 single-qubit gates; measurements: 9 Pauli-basis circuits per (μ,t1), 12 t1 values, 2 μ signs → 216 distinct circuits per repetition, each measured with 10,000 shots and repeated 10 times (total QPU time ≈ 1 h 48 min cited); model parameters: β=3, |μ|=12 (hardware implementation), J = 1/√5 for chosen instance; Trotterization: single-step first-order (no multi-step or higher-order used in hardware).  
noise_and_error_mitigation | No explicit advanced error mitigation applied to reported hardware raw results (authors focus on unmitigated raw data); characterization includes repeating runs (10 independent runs) and reporting run-to-run sample standard deviation; discussion acknowledges large suppression of mutual information due to device noise and the vulnerability of later-time signals to noise; Trotter error analysis performed in simulation to choose working point t0=1.8; no post-selection, zero-noise extrapolation, probabilistic error cancellation, or symmetry verification reported for the main hardware data (they emphasize raw unmitigated data).  
key_results_or_demonstrations | Hardware demonstration (IBM superconducting device) of the TW protocol driven by an explicitly chaotic binary sparse SYK Hamiltonian: (i) observed a clear sign-dependent asymmetry in mutual information I_{PT} between μ<0 and μ>0 near the teleportation time, despite strong noise suppression of absolute signal; (ii) VQA-prepared approximate TFD achieved fidelity ≈ 0.927 with exact TFD and reproduces mutual-information dynamics well in simulation; (iii) size-winding diagnostics computed in numerics show approximately linear phase vs operator size and reversal of slope after μ<0 kick, consistent with gravitational-like teleportation; (iv) single-instance spectral diagnostics (time-averaged SFF showing dip–ramp–plateau) and gap-ratio values in parity sectors near GOE indicate spectral chaos for chosen instance; overall: experiment qualitatively reproduces hallmark signatures (sign asymmetry, size-winding) though quantitative agreement with noiseless numerics is limited by hardware noise.  
validation_and_benchmarks | Extensive cross-checks against classical numerics and noiseless emulation: (a) exact statevector time evolution compared to single-step Trotter emulation to determine acceptable t0 (t0=1.8) and Trotter error; (b) disorder-ensemble studies (100 samples) comparing dense (K=70) and sparse (K=10) ensembles to show ensemble robustness of mutual-information asymmetry; (c) spectral diagnostics (Gaussian-filtered spectral form factor and gap-ratio statistic) compared to random-matrix-theory GOE predictions; (d) size-winding diagnostics computed from classical numerics to verify operator-phase structure; (e) hardware tomography reconstructs ρ_{PT} and mutual information and is compared qualitatively to exact curves.  
claimed_feasibility | Authors claim practical feasibility of holographically motivated TW protocols on present-day NISQ devices for small, hardware-tailored sparse SYK instances (N=8, K=10), enabled by aggressive sparsification and VQA TFD prep; identify scaling bottlenecks (circuit depth, Trotter error, noise) for larger N and point to need for improved error mitigation and hardware or alternative architectures (trapped ions) to scale; they frame their instance as a scalable framework but note that larger sizes will need advanced mitigation or fault-tolerance.  
limitations_and_open_problems | Finite-size toy-model limitation (N=8) — small-N caveats for holographic duality; deep circuit depth (≈765) leads to strong noise suppression of later-time signals; first-order Trotterization introduces approximation errors (11 anticommuting term pairs remain); TFD only approximated variationally (F≈92.7%); ambiguity whether extremely sparse models retain full gravitational features at small N (debate cited); verification beyond qualitative signatures is limited by noise; scaling to larger N requires either better error mitigation, more hardware-efficient chaotic Hamiltonians, or fault-tolerance; lack of dynamical bulk geometry — simulation probes boundary quantum dynamics only.  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness claims (no BQP/QMA statements); implicit argument that classical exact simulation becomes costly as N grows and that random-matrix spectral signatures and operator growth justify quantum experiments; discussion references classical intractability of large SYK and importance of spectral chaos but provides no quantitative complexity lower bounds.  
theory_context_keywords | SYK model, holographic duality / AdS2 gravity, traversable wormhole, double-trace deformation, thermal field double (TFD), Schwarzian action, spectral form factor (SFF), random matrix theory (GOE), scrambling, size winding, operator growth, ANEC violation, teleportation-by-size  
citations_to_prior_work | Key cited works used as context and validation: D. Jafferis et al., 'Traversable wormhole dynamics on a quantum processor' (Nature 2022) [experimental TW on quantum processor]; P. Gao, D.L. Jafferis & A.C. Wall, 'Traversable wormholes via a double trace deformation' (JHEP 2017) [protocol foundation]; Maldacena & Stanford, 'Diving into traversable wormholes' (2017) & related SYK holography refs; M. Tezuka et al., 'Binary-coupling sparse Sachdev–Ye–Kitaev model: An improved model of quantum chaos and holography' (Phys. Rev. B 2023) [binary sparse SYK]; works on sparse SYK and spectral diagnostics (Xu et al., García-García et al., Cáceres et al.); size-winding and teleportation-by-size analyses (A.R. Brown et al., S. Nezami et al., PRX Quantum 2023).  
  
### Binary-coupling sparse Sachdev–Ye–Kitaev (SYK) model

Field | Value  
---|---  
name_short | binary_sparse_SYK  
name_full | Binary-coupling sparse Sachdev–Ye–Kitaev (SYK) model  
brief_description | A sparsified SYK variant in which a small number K of q-body interaction terms are retained and each retained coupling takes value ±J/√K (binary signs), designed to preserve spectral signatures of quantum chaos while drastically reducing term count for hardware efficiency.  
citation_title | Binary-coupling sparse sachdev-ye-kitaev model: An improved model of quantum chaos and holography  
mention_or_use | use  
target_system_or_model | SYK model (q=4) with binary ± couplings, finite-N instances; specific hardware instance: N=8, K=10 (p≈0.14), J scaled so nonzero coefficient magnitude = J/√K  
black_hole_phenomena_targeted | Used to emulate boundary quantum dynamics associated with holographic nearly-AdS2 gravity and traversable-wormhole teleportation signatures (spectral chaos, operator scrambling, size winding)  
simulation_paradigm | Classical spectral diagnostics + digital quantum simulation (gate-based) for time evolution of finite-N instance  
quantum_hardware_platform | Platform-agnostic model chosen for gate-based compilation; implemented on superconducting IBM device in this work  
encoding_and_mapping | Same Jordan–Wigner mapping of Majorana operators to Pauli strings; retained K terms chosen by random pruning with ± sign assignment; regular sparsification (r,s-regular hypergraph) discussed in literature but this work uses random pruning for binary model  
algorithm_or_protocol | Generate binary sparse Hamiltonian instance classically, validate spectral chaos via Gaussian-filtered spectral form factor and gap-ratio statistics, compile to Pauli-string exponentials for Trotterized evolution in quantum circuit; choose instance with many commuting pairs to enable term grouping in Trotterization.  
resource_estimates | Sparsification target: K=10 (vs dense K=70 for N=8 q=4); reduces number of Pauli-string exponentials and circuit depth substantially (chosen instance has 34 commuting vs 11 anticommuting term pairs); no formal asymptotic resource scaling provided beyond finite-N examples.  
noise_and_error_mitigation | Not a noise mitigation technique itself; enables shallower circuits reducing noise sensitivity; authors still observe noise-limited measured signals and did not apply additional error mitigation to primary hardware data.  
key_results_or_demonstrations | Classical spectral diagnostics show that binary sparse SYK at N=8, K≈10 retains GOE-like SFF and level-spacing distribution; authors select a particular K=10 instance (explicit 10-term Hamiltonian) that displays dip–ramp–plateau SFF and gap-ratio values near GOE and use it in hardware experiment.  
validation_and_benchmarks | Gaussian-filtered spectral form factor (SFF) with α=3 averaged over samples, gap-ratio statistic ⟨r⟩ computed for unfolded bulk spectrum in parity sectors compared to GOE expectation (⟨r⟩≈0.530); single-instance time-averaged SFF compared to dense model reference (K=70).  
claimed_feasibility | Authors claim binary sparsification enables practical near-term hardware realizations of holographically motivated protocols by reducing circuit depth while preserving spectral signatures of chaos for small N; show K≈10 suffices for N=8 in their diagnostics.  
limitations_and_open_problems | Open question whether extreme sparsification preserves full gravitational features at larger N or for different observables; small-N finite-size effects; need for systematic search for hardware-efficient chaos-preserving Hamiltonians for larger systems.  
complexity_or_hardness_arguments | No formal complexity statements; motivation is pragmatic: retained O(N) terms suffice to preserve chaotic spectral features while lowering experimental cost.  
theory_context_keywords | sparse SYK, binary couplings, spectral form factor, random-matrix theory, GOE, sparsification, hypergraph regularity  
citations_to_prior_work | M. Tezuka et al., 'Binary-coupling sparse Sachdev–Ye–Kitaev model...' (Phys. Rev. B 2023) [origin of binary sparse SYK]; earlier sparse SYK literature: S. Xu et al., 'A sparse model of quantum holography' (2020); A.M. García-García et al., 'Sparse SYK...' (2021); E. Cáceres et al., 'Sparse SYK and traversable wormholes' (2021).  
  
### Traversable wormhole teleportation protocol (SYK boundary realization)

Field | Value  
---|---  
name_short | TW_protocol  
name_full | Traversable wormhole teleportation protocol (SYK boundary realization)  
brief_description | Protocol that maps a bulk process of traversability (ANEC-violating negative-energy shockwave) to a boundary quantum teleportation operation between two entangled many-body systems by application of a weak two-sided coupling (double-trace deformation), enabling information injected on one side to re-emerge on the other.  
citation_title | A traversable wormhole teleportation protocol in the syk model  
mention_or_use | use  
target_system_or_model | Two-sided SYK boundary systems prepared in a thermofield double (TFD) state, evolved under H_L+H_R with an instantaneous two-sided interaction V ∝ H_int = i ∑_j ψ_L^j ψ_R^j at t=0  
black_hole_phenomena_targeted | Traversability induced by negative-energy shockwave analogue (ANEC violation), signal transmission across an eternal Einstein–Rosen bridge, causal time ordering of signals, teleportation-by-size  
simulation_paradigm | Gate-based digital simulation of the TW protocol including state preparation (TFD via VQA), injection/readout SWAPs, Trotterized evolution, and instantaneous interaction kick  
quantum_hardware_platform | Implemented on superconducting qubits (IBM), but protocol is platform-agnostic for gate-based devices  
encoding_and_mapping | Fermionic SWAP injection/readout constructed from first two Majorana operators (Dirac operator) after Jordan–Wigner mapping; interaction V implemented as fermionic bilinear expressed as Pauli strings and exponentiated within Trotter step  
algorithm_or_protocol | Protocol sequence: prepare Bell_{PQ} ⊗ TFD_{LR} ⊗ |0>_T, SWAP_Q_L at t=-t0, evolve U(t0), apply e^{i μ V} at t=0, evolve U(t1), SWAP_R_T (or direct measurement) to obtain ρ_ asymmetry between μ<0 and μ>0 and by size-winding behaviour.} and compute mutual information; teleportation signal identified by I_{PT  
resource_estimates | In this work employed single-step first-order Trotterization (chosen for minimal depth), working injection time t0=1.8 selected to balance Trotter error and signal strength; interaction strengths used |μ|=12 (instantaneous) and Trotterized three-kick variants for causal ordering diagnostics with μ' tuned to match signal amplitude.  
noise_and_error_mitigation | Authors emphasize sensitivity to scrambling/unscrambling dynamics and vulnerability of later-time signals to noise; use of single-step Trotter kept to limit depth; no explicit mitigation beyond repeated runs and reporting unmitigated raw data.  
key_results_or_demonstrations | Demonstrated sign-dependent mutual-information asymmetry (ΔI_PT >0 near teleportation time for μ<0) in both exact numerics and noisy hardware; established causal time-ordering window for chosen Hamiltonian; showed size-winding interpretation via q(l) phase linearity and reversal under μ<0.  
validation_and_benchmarks | Compared exact time evolution, single-step Trotter emulation (noiseless) and hardware data; used SFF and gap-ratio for spectral chaos validation; performed ensemble disorder-sample studies and time-ordering diagnostics (instantaneous vs Trotterized multi-kick) to verify wormhole-like behavior.  
claimed_feasibility | Authors argue TW protocol is experimentally accessible at small N on NISQ devices with hardware-optimized sparse chaotic Hamiltonians and VQA TFD preparation; larger scales require mitigation or fault tolerance.  
limitations_and_open_problems | Requires highly entangled initial TFD and deep circuits as N grows; first-order Trotter may not be sufficient for longer times or less commuting Hamiltonians; debate exists whether small commuting/sparse instances fully capture gravitational features — authors explicitly cite this debate.  
complexity_or_hardness_arguments | No formal complexity statements; implicit scaling bottlenecks in circuit depth and measurement cost discussed.  
theory_context_keywords | double-trace deformation, ANEC violation, TFD, teleportation-by-size, causal time ordering, operator scrambling  
citations_to_prior_work | Foundational references include P. Gao, D.L. Jafferis & A.C. Wall 'Traversable wormholes via a double trace deformation' (JHEP 2017), J. Maldacena, D. Stanford & Z. Yang 'Diving into traversable wormholes' (2017), and experimental precedent D. Jafferis et al., 'Traversable wormhole dynamics on a quantum processor' (Nature 2022).  
  
### Operator size-winding diagnostics (winding size distribution q(l) and coherence ratio R(l))

Field | Value  
---|---  
name_short | size_winding  
name_full | Operator size-winding diagnostics (winding size distribution q(l) and coherence ratio R(l))  
brief_description | Phase-sensitive operator-size decomposition diagnostic: expand thermalized operator ρ_β^{1/2} ψ(t) into Majorana strings, form q(l)=∑_{|P|=l} c_P^2 whose phase θ(l)=arg q(l) should be approximately linear in l (size winding) and coherence ratio R(l)=|q(l)|/P(l) near unity indicates phase alignment; reversal of slope under appropriate two-sided interaction signals wormhole-like teleportation.  
citation_title | Quantum gravity in the lab. i. teleportation by size and traversable wormholes  
mention_or_use | use  
target_system_or_model | Thermalized operator dynamics in the SYK model (one-sided Hamiltonian H) for finite-N instances; applied to binary sparse SYK chosen Hamiltonian  
black_hole_phenomena_targeted | Diagnostic for gravitational-like teleportation: winding encodes size→momentum map and phase alignment enabling constructive interference when μ has appropriate sign (μ<0 to cancel winding and produce teleportation), giving operator-level evidence for traversability  
simulation_paradigm | Classical postprocessing of exact or Trotterized quantum-evolved statevectors; not directly measured on hardware in this work (size-winding results are from numerics), but used to interpret teleportation physics  
quantum_hardware_platform | Computed classically for the chosen instance; informs interpretation of hardware results but size-winding measurement on hardware not demonstrated here.  
encoding_and_mapping | Majorana-string basis obtained via Jordan–Wigner mapping; coefficients c_P computed as Frobenius inner products c_P = 2^{-N} Tr(ρ_β^{1/2} ψ^j(t) ψ^{P†}); size sectors l=|P| grouped to compute q(l) and R(l).  
algorithm_or_protocol | Compute time-evolved thermalized operator coefficients from exact diagonalization / statevector evolution, compute q(l) and R(l) before and after e^{i μ V} kick; inspect linearity of arg q(l) and slope reversal for μ<0 as signature of size-winding teleportation.  
resource_estimates | Classical computation for N=8 feasible; no scaling resource claims for measuring q(l) on hardware given (measuring coefficients requires exponential tomography in general).  
noise_and_error_mitigation | Numerical analysis not subject to hardware noise; authors note that hardware noise suppresses teleportation signal amplitude making direct experimental size-winding reconstruction challenging at present.  
key_results_or_demonstrations | For the chosen binary sparse SYK instance, numerically find arg q(l) approximately linear in l near mutual-information peak, and the interaction with μ=-12 reverses slope; R(l) remains close to unity in relevant size sectors, indicating near-perfect size winding — supports gravitational-like teleportation interpretation.  
validation_and_benchmarks | Benchmarked size-winding behavior across all single-Majorana insertions ψ_L^i (i=1..8) and across disorder ensemble; results consistent across insertions and consistent with earlier theoretical works on teleportation-by-size.  
claimed_feasibility | Authors treat size-winding as a useful classical diagnostic and suggest it as an operator-level probe for gravitational-like dynamics; measuring it directly on larger hardware would be challenging due to tomographic cost.  
limitations_and_open_problems | Direct experimental reconstruction of c_P coefficients is exponentially expensive in system size; size-winding observed here only in numerics for small N; establishing direct measurement protocols or proxies on hardware remains an open problem.  
complexity_or_hardness_arguments | Implicit exponential measurement complexity to reconstruct full operator coefficients; no formal complexity-theory claims made beyond that.  
theory_context_keywords | operator size, size distribution P(l), winding size distribution q(l), teleportation-by-size, operator growth, scrambling, size→momentum correspondence  
citations_to_prior_work | A.R. Brown et al., 'Quantum gravity in the lab. i. teleportation by size and traversable wormholes' (PRX Quantum 2023); S. Nezami et al., 'Quantum gravity in the lab. ii.' (PRX Quantum 2023); X.-L. Qi & A. Streicher 'Quantum epidemiology: operator growth...' (JHEP 2019).  
  
## Citation

Cite this artifact as `\cite{ast-ext-byun-2026-08-13}`.
[code] 
    @misc{ast-ext-byun-2026-08-13,
      title        = {Extraction: Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-traversable-wormhole-inspired-quantum-teleporta.md},
      crossref     = {byun2026quantum},
      note         = {Theorizer's extraction from \cite{byun2026quantum}. asta-artifact id: extraction-result-59},
    }
    
    @article{byun2026quantum,
      title     = {Quantum simulation of traversable-wormhole-inspired quantum teleportation in a chaotic binary sparse SYK model},
      author    = {Moongul Byun and Keun-Young Kim and Hyeonsoo Lee},
      year      = {2026},
      url       = {https://www.semanticscholar.org/paper/287425539},
    }
[/code]
