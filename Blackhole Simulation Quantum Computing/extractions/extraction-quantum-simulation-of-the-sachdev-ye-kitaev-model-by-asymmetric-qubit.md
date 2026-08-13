[<- All artifacts](<../index.md>)

# Extraction: Quantum simulation of the Sachdev-Ye-Kitaev model by asymmetric qubitization

**Contents:**

  * Quantum simulation of the Sachdev-Ye-Kitaev (SYK) model via asymmetric qubitization



### Quantum simulation of the Sachdev-Ye-Kitaev (SYK) model via asymmetric qubitization

Field | Value  
---|---  
name_short | SYK-qsim  
name_full | Quantum simulation of the Sachdev-Ye-Kitaev (SYK) model via asymmetric qubitization  
brief_description | Proposal and resource analysis to digitally simulate the SYK model (N Majorana modes) using an asymmetric extension of qubitization (LCU) with quantum signal processing and randomized state preparation, targeting SYK observables relevant to black-hole holography such as OTOCs and density-of-states.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model (N Majorana modes; Hamiltonian H = (1/(4·4!)) sum_{p,q,r,s} J_{pqrs} γ_p γ_q γ_r γ_s). The SYK model is discussed as a many-body system believed to have a holographic dual (AdS2 / Einstein gravity-like behaviour) in the large-N, strong-coupling limit.  
black_hole_phenomena_targeted | Scrambling and chaos (out-of-time-order correlators, Lyapunov exponent), thermal properties / density of states of SYK (relevant to black-hole thermodynamics via AdS/CFT-like duality); paper explicitly cites OTOCs and density-of-states as motivating observables.  
simulation_paradigm | Digital, gate-based quantum simulation designed for fault-tolerant / error-corrected quantum computers (algorithm compiled to Clifford+T and discussed in context of surface-code logical qubits); uses LCU/asymmetric qubitization + quantum signal processing (QSP). Quantum phase estimation is mentioned as a method to sample density-of-states.  
quantum_hardware_platform | Platform-agnostic digital qubits; analysis assumes fault-tolerant logical qubits (surface-code assumptions discussed qualitatively, with emphasis that T gates are expensive); no NISQ implementation or specific native hardware demonstrated.  
encoding_and_mapping | SYK Majorana modes mapped to qubits via Jordan–Wigner representation: each Majorana operator represented by Pauli strings (X on target site times Z-string on lower-index sites). Hamiltonian terms indexed by ℓ corresponding to 4-tuples (p,q,r,s) with L = N^4; index register of size log L = 4 log N used. The Hamiltonian is encoded as H = sum_ℓ w_ℓ H_ℓ with H_ℓ self-inverse controlled via a unitary V = sum_ℓ |ℓ><ℓ| ⊗ H_ℓ. State-preparation oracle A produces Gaussian-distributed amplitudes (random orthogonal circuit) proportional to J_{pqrs}; B is equal superposition via Hadamards. Implementation uses an ancilla qubit to build a self-inverse U as in Eq. (3).  
algorithm_or_protocol | Asymmetric qubitization (an LCU variant) combined with quantum signal processing (QSP) to implement e^{-iHt}; prepare two ancilla states A|0>→|A>, B|0>→|B> and a block-encoded, self-inverse U so that  = H/λ; generate polynomial approximation to time-evolution via QSP (Chebyshev/Jacobi–Anger expansion) of order O(λ t + log(1/ε)/log log(1/ε)). Also discusses quantum phase estimation as an application for sampling density-of-states.  
resource_estimates | Asymptotic gate complexity: O(N^{7/2} t + N^{5/2} t · polylog(N/ε)). Signal normalization λ ≈ const · N^{5/2} J (explicit expression given: λ ≈ N^{5/2} J · sqrt(3!)/(4·4!) up to approximations). Leading-order T-count reported: (2/√6) N^{7/2} J t. Concrete estimates: for N=100, leading-order T-count < 10^7 · (Jt); for N=200, < 10^8 · (Jt). Costs of primitives: C_A = O(polylog(N/ε)) (random circuit state prep), C_B = O(log N) (Hadamards), C_U = O(N) (application of Majorana strings); explicit T-count for the Majorana-operator primitive (single γ application) = 4N-4 T gates, four such primitives needed per H_ℓ yielding 16N-16 T gates to implement U, and uses ≈ log N extra ancilla qubits. Index/register qubits: index size log L = 4 log N; system qubits = N (one qubit per Majorana mode when mapped), plus reported ancillary qubits (log N, one ancilla qubit for asymmetric construction). Polynomial order required: O(λ t + log(1/ε)/log log(1/ε)), with refined cutoff K ≈ λ t + (3^{2/3}/2)(λ t)^{1/3} log^{2/3}(1/ε) (Appendix B).  
noise_and_error_mitigation | Assumes fault-tolerant quantum computation (surface-code-style) and compiles to Clifford+T; no explicit NISQ noise model or noise-mitigation protocols are applied. Discussion highlights that T gates dominate cost in surface-code architectures and that the approach is intended for error-corrected machines; no error-mitigation (ZNE/PEC/etc.) is used or numerically modeled. Precision parameter ε appears in algorithmic error bounds.  
key_results_or_demonstrations | Main deliverable is an algorithm and resource analysis (no hardware experiment). Core results: development of 'asymmetric qubitization' encoding H =  with random-circuit A and Hadamard B; asymptotic complexity O(N^{7/2} t + N^{5/2} t polylog(N/ε)), an exponential improvement in 1/ε and large polynomial improvements over prior Trotter-based proposals claimed as O(N^{10} t^2 / ε). Concrete Clifford+T compilation of bottleneck primitives and T-count leading coefficient (2/√6) N^{7/2} J t and numerical T-count estimates for N=100 and 200. Proposal-level demonstration: recommendation of random orthogonal circuits for state-prep A to yield Gaussian amplitudes, and a concrete circuit (from [21]) for controlled Majorana application (T-count 4N-4).  
validation_and_benchmarks | Validation is analytic/theoretical: (i) formal derivation using LCU/qubitization and QSP (relating powers of the walk operator W to Chebyshev polynomials and Jacobi–Anger expansion), (ii) complexity comparison to prior Trotter-based SYK simulation schemes (cites [8]), (iii) use of prior results on random-circuit convergence to Porter-Thomas/2-design behavior (cites [15] and design-convergence results [17-20]) to argue state-prep A feasibility, and (iv) use of prior circuit constructions for Majorana operators ([21]) for gate counts. No numerical simulation of the full algorithm or experiment is presented; correctness is argued via analytic bounds (Appendix B for truncation errors in Jacobi–Anger expansion).  
claimed_feasibility | Authors claim the approach makes 'interesting' SYK simulations plausible on early surface-code quantum computers, arguing that T counts (e.g., <10^7 Jt for N=100) are modest compared to other chemically/condensed-matter problems; they identify the method as targeted for error-corrected machines rather than NISQ. Bottlenecks identified: cost and latency of T gates under common 2D error-correcting codes, and the required size of random circuits to reach Gaussian amplitudes (they conservatively assume polylog(N/ε) depth).  
limitations_and_open_problems | Explicit limitations: (i) SYK is a toy model whose holographic dual is conjectural and emerges in large-N strong-coupling limit — finite-N simulations may not capture full gravitational dynamics; (ii) outstanding question on how large / deep the random orthogonal circuit A must be to converge amplitudes to Gaussian within error ε (only conservative polylog assumption is given); (iii) no direct simulation of dynamical spacetime or explicit gravitational degrees of freedom — only the quantum many-body SYK side is simulated; (iv) validation/verification at large N remains challenging; (v) the algorithm presumes fault-tolerance and does not address NISQ noise mitigation; (vi) the asymptotic prefactors and constants (e.g., in λ) involve approximations and averaging assumptions about J_{pqrs}.  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness class claims (e.g., BQP-hard, QMA-hard) for SYK simulation are made; argumentation is practical: prior Trotter-based algorithms had scaling O(N^{10} t^2 / ε) making them intractable for large N, while asymmetric qubitization yields polynomial improvements placing simulations within reach of early FT machines. The paper uses established QSP/qubitization complexity results to derive gate-count scaling and truncation error bounds.  
theory_context_keywords | AdS/CFT; holographic duality; Sachdev-Ye-Kitaev (SYK) model; AdS2; maximal chaos; Lyapunov exponent; out-of-time-order correlators (OTOCs); random quantum circuits; Porter–Thomas distribution; linear combinations of unitaries (LCU); qubitization; quantum signal processing (QSP); Chebyshev polynomials; Jacobi–Anger expansion.  
citations_to_prior_work | Key references cited and used in the approach include: A. Kitaev, 'A Simple Model of Quantum Holography' [SYK origin and holographic motivation]; S. Sachdev and J. Ye (original SY model); J. Maldacena and D. Stanford (SYK and gravity connections); G. H. Low and I. L. Chuang (qubitization and quantum signal processing framework); A. M. Childs and N. Wiebe (LCU framework); L. García-Álvarez et al. (prior proposal for SYK quantum simulation using Trotter methods cited as [8]); S. Boixo et al. (random-circuit convergence / Porter–Thomas behavior cited as [15]); R. Babbush et al. (Majorana operator circuits and Clifford+T compilations cited as [21]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-babbush-2026-08-13}`.
[code] 
    @misc{ast-ext-babbush-2026-08-13,
      title        = {Extraction: Quantum simulation of the Sachdev-Ye-Kitaev model by asymmetric qubitization},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-the-sachdev-ye-kitaev-model-by-asymmetric-qubit.md},
      crossref     = {babbush2018quantum},
      note         = {Theorizer's extraction from \cite{babbush2018quantum}. asta-artifact id: extraction-result-22},
    }
    
    @article{babbush2018quantum,
      title     = {Quantum simulation of the Sachdev-Ye-Kitaev model by asymmetric qubitization},
      author    = {R. Babbush and D. Berry and H. Neven},
      year      = {2018},
      journal   = {Physical Review A},
      url       = {https://www.semanticscholar.org/paper/51682134},
    }
[/code]
