[<- All artifacts](<../index.md>)

# Extraction: Digital Quantum Simulation of Minimal AdS/CFT.

**Contents:**

  * Digital quantum simulation of the Sachdev–Ye–Kitaev (SYK) model as a minimal AdS/CFT



### Digital quantum simulation of the Sachdev–Ye–Kitaev (SYK) model as a minimal AdS/CFT

Field | Value  
---|---  
name_short | SYK digital simulation  
name_full | Digital quantum simulation of the Sachdev–Ye–Kitaev (SYK) model as a minimal AdS/CFT  
brief_description | Proposal and detailed digital-quantum-algorithm construction to simulate the Sachdev–Ye–Kitaev (SYK) model (Majorana and complex-fermion variants) on qubit hardware as a minimal laboratory realisation of AdS/CFT-like holographic physics; includes encodings, gate-level implementations for trapped ions and superconducting circuits, protocols to measure scrambling (OTOCs), and resource-scaling estimates.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Sachdev–Ye–Kitaev (SYK) model (Majorana and complex spinless fermion variants), viewed as a minimal holographic (NAdS_2 / AdS/CFT-like) model of quantum gravity / black-hole-like dynamics.  
black_hole_phenomena_targeted | Scrambling of information as diagnosed by out-of-time-order correlators (OTOCs) and related non-equilibrium dynamics (four-point OTO four-point functions used to extract Lyapunov exponent and diagnose 'maximal chaos'); more generally reproducing minimal features of holographic black holes (fast scrambling, large-N conformal behaviour in strong coupling).  
simulation_paradigm | Digital gate-based quantum simulation using Trotter–Suzuki decomposition of the spin-mapped SYK Hamiltonian; proposed digital-analog hybrid remarks but main algorithms are digital/Trotterized.  
quantum_hardware_platform | Platform-agnostic proposals with explicit implementation recipes for trapped-ion systems (Mølmer–Sørensen multi-qubit gates + local rotations) and superconducting circuits (decomposition into two-qubit and single-qubit gates mediated by resonators); also discusses linear and 2D qubit layouts and digital-analog possibilities.  
encoding_and_mapping | Fermion-to-qubit Jordan–Wigner encoding: spinless complex fermions c_i <-> strings of Pauli Z and local raising/lowering operators; Majorana fermions constructed from complex fermions and encoded similarly (explicit formulae for χ_{2j-1}, χ_{2j}); nonlocal all-to-all SYK couplings become multi-qubit Pauli-string interactions with Jordan–Wigner Z-strings; models considered: (i) Majorana quartic-only, (ii) Majorana with repeated-index terms (quadratic reductions), (iii) complex fermion quartic with/without real coefficients. No gauge constraints or dynamical spacetime encoding—holography is via model selection (SYK ~ NAdS_2).  
algorithm_or_protocol | Trotter–Suzuki time evolution of decomposed spin Hamiltonian H = ∑_i H_i; ancilla-controlled time-reversal protocol (use ancilla qubit with H_CS = σ_C^z ⊗ H_S to implement both U(t) and U(-t)); ancilla-controlled-unitary protocol to measure n-time correlators and OTOCs (prepare ancilla in (|0›+|1›)/√2, apply controlled-V_i unitaries interleaved with evolution, measure σ_x, σ_y of ancilla); specific gate constructions for a generic 4-body Pauli-string term using Mølmer–Sørensen blocks (trapped ions) or decomposition into O(N) two-qubit gates (superconducting circuits). Also describes thermal-state preparation references and simple initial state encodings via Jordan–Wigner.  
resource_estimates | High-level polynomial scalings reported: number of independent spin interaction terms m ~ O(N^4) (N = number of Majorana fermions); naive Trotter gate-count estimate O(N^{12}) if every commutator contributed; authors refine estimate noting number of nonzero commutators ~ O(N^6), yielding asymptotic gate-count scaling ≈ O(N^{10}) for achieving fixed accuracy ε over time t (with s Trotter steps and Trotter error ~ J^2 t^2 / s). Supplemental table gives explicit counts of Pauli-string interaction types (closed-form polynomials in n or N). Platform-specific per-interaction costs: trapped ions — O(1) multi-qubit gate sequence per interaction (using collective Mølmer–Sørensen style gates); superconducting circuits — decomposition yields O(N) two-qubit gates per interaction (authors state entangling-gate reduction to n per interaction). Trotter error scaling and commutator-count dependence are explicitly given; no explicit qubit-number examples with numerical qubit counts in the small-N regime are provided beyond formulae (qubit count equals number of fermionic modes mapped to qubits: n complex fermions -> n qubits; N = 2n Majoranas -> n qubits).  
noise_and_error_mitigation | No detailed noise model or quantitative error-mitigation study; discussion qualitative: Trotter errors quantified (order J^2 t^2 / s), and platforms considerations mention that phases of gates implement random-coupling strengths; self-averaging over disorder may reduce need for many disorder realisations at large N. No explicit use of error mitigation techniques (ZNE, PEC, symmetry verification) or FTQC overhead accounting is given; comments that higher-order Trotter–Suzuki can improve accuracy and that some schemes may benefit from digital-analog approaches.  
key_results_or_demonstrations | This paper is a theoretical proposal (not an experimental demonstration). Key deliverables: (1) explicit Jordan–Wigner mappings of different SYK variants to Pauli strings, with classification and counts of interaction terms; (2) gate-level constructions to implement a generic 4-body Pauli-string term on trapped-ion and superconducting platforms (Mølmer–Sørensen sequence and decompositions); (3) ancilla-based time-reversal and ancilla-controlled n-time-correlation measurement protocols enabling measurement of OTOCs/scrambling; (4) resource-scaling estimates (m ~ O(N^4), worst-case gate counts ~ O(N^{10}) after improving naive estimate). No numerical simulations or hardware experiments are reported; the work is a concrete, implementable proposal for near-to-mid-term quantum platforms.  
validation_and_benchmarks | Validation is conceptual/proposal-level: mapping correctness justified analytically via Jordan–Wigner and property counting; Trotter error bounded by standard formula (commutator-dependent error terms shown); physical validation suggestions include measuring OTOCs and comparing extracted Lyapunov exponents with known analytic large-N/strong-coupling results of SYK (e.g., maximal chaos bound λ ≤ 2π/β). No explicit small-N numerics or cross-platform benchmarking is presented in the paper; authors point to self-averaging at large N and comparison to known solvable large-N SYK limits as intended validation targets.  
claimed_feasibility | Authors claim feasibility as a near-term experimental target on state-of-the-art trapped-ion and superconducting devices for small to moderate N, and more generally as a realistic laboratory minimal AdS/CFT simulator. They highlight bottlenecks: very large number of interaction terms (m ~ N^4) and consequent gate-depth scaling (leading to O(N^{10}) gates for long-time/high-accuracy simulations), measurement cost for OTOCs, and the need for time-reversal control. They state that large-N semiclassical holographic regime is out of reach for near-term devices; the proposal is positioned as a way to access finite-N, nonperturbative regimes experimentally. No explicit timeframe is given.  
limitations_and_open_problems | Explicitly noted limitations: (a) SYK is a minimal toy model of holography—no dynamical spacetime degrees of freedom are simulated and bulk gravity emerges only in the large-N/strong-coupling limit; (b) finite-N simulations may not fully reproduce semiclassical gravity features; (c) resource scaling is steep (many-body nonlocal interactions -> many Pauli strings) making large-N or long-time simulations challenging; (d) need for disorder averaging unless relying on self-averaging at large N; (e) lack of quantitative noise/error-mitigation analysis; (f) verification beyond OTOCs and finite-size scaling remains to be developed; (g) no explicit protocol for preparing thermofield double / black-hole-like purified thermal states beyond citing known thermal-state-preparation methods.  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness proofs (e.g., BQP-/QMA-hard) are asserted for simulating SYK in this paper. Authors motivate classical difficulty of strongly-coupled real-time dynamics (sign problem, Lorentzian physics) and point to quantum advantage conceptually (Feynman's argument), but do not present formal complexity lower bounds or no-go theorems.  
theory_context_keywords | AdS/CFT, holographic duality, Sachdev–Ye–Kitaev (SYK), NAdS_2, fast scrambling, maximal chaos, Lyapunov exponent, out-of-time-order correlators (OTOCs), Jordan–Wigner transformation, Trotter–Suzuki decomposition, Mølmer–Sørensen gates, digital quantum simulation, self-averaging, minimal quantum gravity model.  
citations_to_prior_work | Key references cited in the proposal: Maldacena (AdS/CFT foundational work), Hawking (information paradox), Kitaev (SYK talks introducing model), Sachdev (SYK-related work), Maldacena & Stanford (SYK holographic connections), Maldacena–Shenker–Stanford (bound on chaos / Lyapunov bound), Lloyd (digital quantum simulation), Jordan & Wigner (fermion–spin mapping), works on trapped-ion Mølmer–Sørensen gates and superconducting circuit quantum processors, and prior protocols for n-time correlation measurements and ancilla-based OTOC measurements (e.g., Pedernales et al. PRL 2014; Swingle et al. arXiv:1602.06271). The paper's bibliography gives full reference list (refs. [1],[2],[14-20],[23-27],[30-38],[42-43]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-garcalvarez-2026-08-13-2}`.
[code] 
    @misc{ast-ext-garcalvarez-2026-08-13-2,
      title        = {Extraction: Digital Quantum Simulation of Minimal AdS/CFT.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-digital-quantum-simulation-of-minimal-adscft-1.md},
      crossref     = {garcalvarez2016digital},
      note         = {Theorizer's extraction from \cite{garcalvarez2016digital}. asta-artifact id: extraction-result-85},
    }
    
    @article{garcalvarez2016digital,
      title     = {Digital Quantum Simulation of Minimal AdS/CFT.},
      author    = {L. García-Álvarez and Í. Egusquiza and L. Lamata and A. Campo and J. Sonner and Enrique Solano and Enrique Solano},
      year      = {2016},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/5144368},
    }
[/code]
