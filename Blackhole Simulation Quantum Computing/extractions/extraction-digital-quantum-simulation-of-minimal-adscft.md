[<- All artifacts](<../index.md>)

# Extraction: Digital Quantum Simulation of Minimal AdS/CFT.

**Contents:**

  * Digital quantum simulation of the Sachdev-Ye-Kitaev (SYK) model (minimal AdS/CFT)
  * Ancilla-controlled time inversion protocol for reversible evolution
  * Ancilla-based n-time correlation / OTOC measurement protocol



### Digital quantum simulation of the Sachdev-Ye-Kitaev (SYK) model (minimal AdS/CFT)

Field | Value  
---|---  
name_short | SYK digital simulation  
name_full | Digital quantum simulation of the Sachdev-Ye-Kitaev (SYK) model (minimal AdS/CFT)  
brief_description | Proposal to digitally simulate the Sachdev-Ye-Kitaev model — a strongly interacting all-to-all fermion model with a conjectured NAdS2 holographic dual — by encoding fermions onto qubits and Trotterizing time evolution to probe dynamics including scrambling/OTOCs.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model: variants in Majorana fermions (quartic and quadratic terms) and complex spinless fermions (four-fermion interactions, chemical potential), with holographic interpretation as near-AdS2 (NAdS2) gravity in the large-N/strong-coupling limit.  
black_hole_phenomena_targeted | Scrambling of information and out-of-time-order correlators (OTOCs) tied to maximal chaos (Lyapunov exponent saturating the bound λ ≤ 2π/β); more generally non-equilibrium dynamics relevant to minimal holographic (black-hole-like) behaviour.  
simulation_paradigm | Digital gate-based quantum simulation using Trotter–Suzuki decomposition of the spin Hamiltonian after fermion-to-qubit mapping (Jordan–Wigner).  
quantum_hardware_platform | Platform-agnostic proposal with concrete implementation prescriptions for trapped ions (Mølmer–Sørensen multi-qubit gates) and superconducting circuits (decomposition to two-qubit gates and resonator-mediated multiqubit interactions).  
encoding_and_mapping | Jordan–Wigner mapping from spinless complex fermions c_i (n modes) to n qubits: c_i^† = (∏ _{j=1}^{i-1} σ_j^z) σ_i^+; Majorana operators built from complex fermions (χ_) are encoded similarly, so 2n Majoranas ↔ n qubits. Resulting spin terms contain Pauli strings with two disjoint σ^z Jordan–Wigner tails; grouping/symmetrisation of random couplings is used to reduce the number of independent terms.}, χ_{2j  
algorithm_or_protocol | Trotterized time evolution (first- and higher-order Trotter–Suzuki decompositions) of H = Σ_j H_j with H_j being many-body Pauli strings; explicit gate constructions for generic 4-body Pauli-string exponentials via sequences using Mølmer–Sørensen gates (trapped ions) or decomposed two-qubit gates (superconducting circuits). Ancilla-based protocols are given for (i) time inversion (control ancilla implementing H_CS = σ_C^z ⊗ H_S to get U(t) and U(−t)) and (ii) measurement of n-time correlators/OTOCs using a single ancilla with controlled-V operations.  
resource_estimates | Scaling and counts reported analytically: number m of spin-interaction terms ~ O(N^4) (N = number of Majorana fermions, or equivalently 2n), naive worst-case gate count per simulation (to accuracy ε over time t) estimated as m × (m choose 2) × J^2 t^2 / ε → formally O(N^12). Accounting for the actual number of nonzero commutators (~O(N^6)) reduces gate-count scaling to O(N^10). Table V (Supplemental) gives explicit polynomial counts in n for different interaction types; per-Trotter-step gate counts: (i) trapped ions: O(1) physical multiqubit operations per interaction term (using Mølmer–Sørensen patterns); (ii) superconducting decomposition: O(N) two-qubit gates per interaction in worst case but they show constructions reducing to O(n) entangling gates (n = number of qubits) per interaction. Qubit count: equals number of fermionic modes encoded (n qubits for n complex fermions, which equals N/2 for Majorana description). No explicit numeric depths, T-gate counts, or measurement-shot counts are given beyond the polynomial scalings and counts table.  
noise_and_error_mitigation | No detailed hardware noise model or quantitative mitigation is assumed; authors discuss Trotter error scaling (error ∼ J^2 t^2 / s for s Trotter steps) and note higher-order Trotter–Suzuki reduces error. They mention self-averaging over disorder (large-N) can reduce need to sample many disorder realizations. No explicit error-mitigation techniques (ZNE, PEC, symmetry verification, etc.) or fault-tolerance overheads are quantified.  
key_results_or_demonstrations | This work is a theoretical proposal (no experimental data). Key deliverables: (a) explicit mapping of SYK variants onto Pauli strings via Jordan–Wigner and grouping of random couplings, with term counts; (b) Trotterization strategy and worst-case/ refined scaling estimates (m ~ O(N^4); gate complexity O(N^10) after commutator-count improvement); (c) explicit trapped-ion and superconducting-circuit gate sequences to implement generic 4-body Pauli-string exponentials (including circuit-level constructions using Mølmer–Sørensen gates and two-qubit decompositions); (d) ancilla-based protocols for time inversion and measuring OTOCs/n-time correlators; (e) discussion of state preparation options (product fermionic vacua via JW mapping and references to thermal-state-preparation methods). No numerical simulation or benchmarking presented beyond counting and analytic scaling.  
validation_and_benchmarks | Validation is proposed conceptually rather than performed: authors recommend comparing measured OTOCs/scrambling behavior to known analytic large-N SYK results (approximate conformal symmetry, maximal chaos/Lyapunov exponent), finite-size scaling and self-averaging arguments for disorder. No explicit numerical exact-diagonalization cross-checks or experimental benchmarks are provided in the paper.  
claimed_feasibility | Authors claim the proposal is feasible 'with state-of-the-art' trapped-ion and superconducting platforms for small system sizes; they emphasise polynomial (but steep) scaling and identify that regimes relevant for semiclassical gravity require large N and strong coupling (βJ ≫ 1), which are resource-intensive. They note digital-analog hybrids and connectivity (2D layouts) can reduce SWAP overhead; explicit statement: certain regimes (small n) practical on NISQ devices while large-N holographic regime requires more resources (likely beyond NISQ).  
limitations_and_open_problems | Explicitly noted limitations: (i) steep polynomial gate counts (O(N^10)) making large-N simulation demanding; (ii) finite-size deviations from large-N holographic physics (the holographic interpretation strictly holds at large N); (iii) Trotter errors and many non-commuting terms increasing required Trotter steps; (iv) lack of emergent dynamical spacetime in the simulator — this is a minimal/holographic field-theory realization, not a simulation of full spacetime dynamics; (v) no quantitative noise/FTQC analysis; (vi) generating and sampling disorder realizations may be burdensome though self-averaging helps at large N; (vii) preparing thermal states and certain many-body states may be challenging (they cite thermal state-prep methods but do not implement them).  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness proofs (BQP/QMA) are provided. The authors argue digital quantum simulators are exponentially more efficient than classical simulation for general many-body Hamiltonians (following Feynman/standard arguments) and note classical methods face sign problems and inefficacy for real-time Lorentzian dynamics; but no rigorous complexity reductions specific to SYK are given.  
theory_context_keywords | AdS/CFT; holographic duality; Sachdev-Ye-Kitaev (SYK); NAdS2; fast scrambling / scrambling; out-of-time-order correlators (OTOCs); Lyapunov bound (λ ≤ 2π/β); Jordan–Wigner mapping; disorder averaging; digital quantum simulation; Trotter–Suzuki.  
citations_to_prior_work | Key references cited in support of the approach include Kitaev's talks on SYK [14], Sachdev (2015) on related physics [15], Maldacena & Stanford (SYK and gravity) [19], Maldacena–Shenker–Stanford (bound on chaos) [20], references on digital quantum simulation and gate constructions including Lloyd (1996) and Mølmer–Sørensen / trapped-ion implementations [24,32], and works on OTOC measurement protocols and ancilla-based correlator measurement [25,26,27]. The paper also cites experimental platform references for trapped ions and superconducting circuits [8-12,30-37].  
  
### Ancilla-controlled time inversion protocol for reversible evolution

Field | Value  
---|---  
name_short | Ancilla time-inversion control  
name_full | Ancilla-controlled time inversion protocol for reversible evolution  
brief_description | A proposal to implement both forward and backward time evolution U(t) and U(−t) without reengineering Hamiltonian signs by coupling the simulated system Hamiltonian to a control ancilla via H_CS = σ_C^z ⊗ H_S, enabling creation of U(t) and U(−t) conditioned on the ancilla state.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Generic time-independent many-body system (here the SYK spin-mapped Hamiltonian H_S) whose sign-reversed evolution is required for correlator/OTOC protocols.  
black_hole_phenomena_targeted | Enables measurement of scrambling and OTOCs which are central probes of black-hole-like chaotic dynamics.  
simulation_paradigm | Digital gate-based with an additional ancilla qubit that controls the sign of the Hamiltonian in the evolution operator.  
quantum_hardware_platform | Platform-agnostic; implementation details given in the trapped-ion and superconducting contexts insofar as H_S is implemented there.  
encoding_and_mapping | No additional encoding beyond the system's Jordan–Wigner qubit encoding; the ancilla is a single extra qubit coupled via control operations that implement σ_C^z ⊗ H_S (realised by conditional application of the same gate sequences used for H_S with ancilla-controlled phases).  
algorithm_or_protocol | Prepare ancilla in superposition α|e⟩+β|g⟩ and apply evolution under H_CS = σ_C^z H_S: result is α|e⟩U(t)|ψ⟩ + β|g⟩U(−t)|ψ⟩, enabling the construction of sequences that compute scrambling correlators without explicit Hamiltonian sign flips. The authors give an explicit ancilla+system gate sequence to build the scrambling four-point function expectation.  
resource_estimates | Requires a single extra ancilla qubit; otherwise resource overhead equals implementing U(t) with conditional control (i.e., controlled versions of the same gate sequence). No explicit extra-depth estimate is quantified, but controlled versions of many-body exponentials generally increase gate depth and require conditional-control implementations per Trotter step.  
noise_and_error_mitigation | No quantitative noise analysis; implicit caveat that implementing controlled many-body evolutions increases gate depth and susceptibility to decoherence/Trotter error.  
key_results_or_demonstrations | Protocol formulation and explicit sequence to embed U(t) and U(−t) in a single controlled evolution; provides a practical route to measure OTOCs without engineering negative couplings.  
validation_and_benchmarks | No experimental validation; logical correctness follows from algebraic expansion of exp(−i σ_C^z H_S t).  
claimed_feasibility | Presented as experimentally feasible in platforms capable of implementing controlled Hamiltonian terms (trapped ions, superconducting circuits); feasibility limited by ability to implement ancilla-controlled many-body exponentials with acceptable fidelity.  
limitations_and_open_problems | Extra control overhead and deeper circuits; implementing ancilla-controlled many-body interactions precisely is challenging in NISQ devices; increased noise sensitivity for controlled evolutions.  
complexity_or_hardness_arguments | No complexity-theoretic claims beyond noting the controlled-evolution construction doubles accessible evolution directions in a single circuit.  
theory_context_keywords | time inversion; controlled Hamiltonian; ancilla-assisted measurement; OTOC.  
citations_to_prior_work | Construction is presented in this paper and related to prior work using ancillas for correlator protocols (Refs. [25], [26]).  
  
### Ancilla-based n-time correlation / OTOC measurement protocol

Field | Value  
---|---  
name_short | Ancilla correlator measurement  
name_full | Ancilla-based n-time correlation / OTOC measurement protocol  
brief_description | Protocol using a single ancilla qubit and controlled-V operations to encode n-time correlation functions (including OTOCs) into ancilla σ_x and σ_y expectation values, applicable to both analog and digitally synthesized evolutions.  
citation_title | here  
mention_or_use | use  
target_system_or_model | General quantum many-body system (here applied to SYK spin-qubit encoding) for measurement of n-time correlators such as ⟨W^†(t) V^†(0) W(t) V(0)⟩.  
black_hole_phenomena_targeted | Direct measurement of scrambling/OTOCs used to probe black-hole-like maximal chaos in SYK.  
simulation_paradigm | Ancilla-based measurement combined with digital (Trotterized) time evolution; applicable also to analog simulators.  
quantum_hardware_platform | Platform-agnostic; practical on trapped-ion and superconducting platforms capable of implementing controlled unitaries between ancilla and system.  
encoding_and_mapping | Uses the same Jordan–Wigner qubit encoding of fermions; requires ability to implement controlled unitaries of the form |0⟩⟨0|_A ⊗ I + |1⟩⟨1|_A ⊗ V_i for system unitaries V_i.  
algorithm_or_protocol | Prepare ancilla in (|0⟩+|1⟩)/√2, sequentially apply controlled-V_k and system evolutions between times t_k, and read out ancilla σ_x and σ_y at the end. For OTOCs choose the sequence {W^†, V^†, W, V} with appropriate time-ordering and time inversion when needed (using the ancilla time-inversion control protocol).  
resource_estimates | Overhead is one ancilla qubit plus implementing controlled versions of each V_i; measurement yields correlation as (⟨σ_x⟩ + i⟨σ_y⟩)/2. No shot-number estimates are given; cost dominated by repeated runs to accumulate statistics and by the cost of implementing controlled many-body unitaries and required forward/backward evolutions.  
noise_and_error_mitigation | No explicit mitigation strategies; protocol sensitivity to errors is noted implicitly (controlled gates and forward/backward evolution amplify circuit depth).  
key_results_or_demonstrations | Provides an efficient, constructive ancilla protocol to read out n-time correlators and OTOCs in the SYK simulation context; links to similar proposals in the literature (Refs. [26,27]).  
validation_and_benchmarks | No experimental benchmarks provided; correctness rests on standard controlled-unitary circuit identities and the availability of time-reversal capability when needed.  
claimed_feasibility | Authors claim the protocol is practical for current platforms for small systems; ancilla-controlled operations are standard in many platforms (trapped ions, superconducting).  
limitations_and_open_problems | Requires implementing controlled many-body operators and time inversion; measurement of OTOCs with long evolution times is challenging due to decoherence and Trotter errors; no error analysis or sample-complexity quantification given.  
complexity_or_hardness_arguments | No formal complexity arguments; measurement complexity (statistical sampling) is not quantified.  
theory_context_keywords | n-time correlators; out-of-time-order correlators (OTOCs); ancilla-controlled measurement; scrambling.  
citations_to_prior_work | Refers explicitly to an efficient n-time correlator measurement protocol (Ref. [26]) and to related recent discussions of OTOC measurement (Refs. [25], [27]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-garcalvarez-2026-08-13}`.
[code] 
    @misc{ast-ext-garcalvarez-2026-08-13,
      title        = {Extraction: Digital Quantum Simulation of Minimal AdS/CFT.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-digital-quantum-simulation-of-minimal-adscft.md},
      crossref     = {garcalvarez2016digital},
      note         = {Theorizer's extraction from \cite{garcalvarez2016digital}. asta-artifact id: extraction-result-25},
    }
    
    @article{garcalvarez2016digital,
      title     = {Digital Quantum Simulation of Minimal AdS/CFT.},
      author    = {L. García-Álvarez and Í. Egusquiza and L. Lamata and A. Campo and J. Sonner and Enrique Solano and Enrique Solano},
      year      = {2016},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/5144368},
    }
[/code]
