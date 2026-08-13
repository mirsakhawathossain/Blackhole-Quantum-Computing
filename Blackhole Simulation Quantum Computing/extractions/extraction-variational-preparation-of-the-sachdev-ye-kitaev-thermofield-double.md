[<- All artifacts](<../index.md>)

# Extraction: Variational Preparation of the Sachdev-Ye-Kitaev Thermofield Double

**Contents:**

  * Variational preparation of the Sachdev-Ye-Kitaev thermofield double via VQE



### Variational preparation of the Sachdev-Ye-Kitaev thermofield double via VQE

Field | Value  
---|---  
name_short | SYK-TFD VQE  
name_full | Variational preparation of the Sachdev-Ye-Kitaev thermofield double via VQE  
brief_description | A hybrid variational quantum algorithm that prepares the thermofield-double (TFD) state of two coupled q=4 SYK systems by finding the ground state of H_TFD = H_L + H_R + H_int using parameterized quantum circuits and gradient-based optimization (parameter-shift rule). Demonstrated in classical simulation (Yao.jl) up to N=12 qubits and tested under finite-shot measurement noise.  
citation_title | Variational Preparation of the Sachdev-Ye-Kitaev Thermofield Double  
mention_or_use | use  
target_system_or_model | Sachdev-Ye-Kitaev (SYK) model (q = 4) on two coupled copies; the thermofield double state which is dual to an eternal two-sided black hole / traversable wormhole in AdS2-like holography.  
black_hole_phenomena_targeted | Preparation of the thermofield double (TFD) state which is the CFT dual of an eternal two-sided black hole and is the starting state for traversable-wormhole protocols; probes relevant to scrambling, teleportation/teleportation-through-wormhole, and holographic dynamics (TFD/entanglement structure), with parity (H_L - H_R) and thermal correlators suggested as diagnostics.  
simulation_paradigm | Hybrid variational (VQE-style) circuit ansatz with measurement-based analytic gradients (parameter-shift rule); classical optimizer (Adam) for parameter updates.  
quantum_hardware_platform | platform-agnostic / NISQ-focused (discussion targets NISQ devices generically; no hardware experiment performed).  
encoding_and_mapping | Majorana fermions mapped to qubits via the Jordan-Wigner transformation (Majorana operator -> nonlocal Pauli strings). Two copies (L/R) of SYK yield 2N Majoranas which are encoded into N physical qubits (convention used in paper); OpenFermion was used to automate conversion; Bravyi-Kitaev mentioned as alternative.  
algorithm_or_protocol | 1) Form H_TFD = H_L,SYK + H_R,SYK + i μ Σ_j ψ_L^j ψ_R^j; 2) map to Pauli-sum qubit Hamiltonian; 3) prepare parameterized quantum circuit (layers of single-qubit rotations + cyclic CNOT/Ising R_XX entanglers); 4) evaluate energy and gradients using parameter-shift rule; 5) update parameters with classical optimizer (Adam) to minimize variational energy (VQE). Shot-noise experiments performed by sampling expectation values with finite measurements. Suggestion to combine with qubitization for time evolution (cited externally).  
resource_estimates | Reported/simulated system sizes: up to N=12 qubits (numerical comparison via exact diagonalization); N=8 circuits reached ground state with depth d=2–3 layers (d=3 typical), N=12 reached within ~0.2% of exact ground energy with moderate depth; N=16 not attempted due to classical simulation limits. No explicit gate counts, T-gate counts, or full asymptotic runtime formulas provided. Optimization iterations: typically <500 gradient update steps reported for N=8. Measurement/shot budgets: shot-noise was studied qualitatively (performance varied non-monotonically with shot number) but no fixed required shot counts or scaling laws given.  
noise_and_error_mitigation | Simulated only finite-sampling (shot) noise in expectation values; found procedure still succeeds if circuit depth increased (example: had to go from d=3 to d=4 under shot noise). No explicit gate-level noise model (depolarizing, coherent errors) or error-correction implemented. Authors note the parameter-shift gradients report the gradient of the actually implemented (noisy) gate and so mitigate need for precise gate-model calibration. Proposed mitigations: add penalty terms (e.g., (H_L - H_R)^2) or parity post-selection to enforce diagnostics; did not apply ZNE/PEC or fault-tolerance overheads in this work.  
key_results_or_demonstrations | Simulation-only demonstration (classical state-vector simulation and finite-shot sampling): (a) For N=8, q=4 SYK: variational circuit (d=2–3) found states with energy below the first excited state and matched exact ground state energy for several disorder instances. (b) For N=12: variational procedure reached energies within ≈0.2% of exact ground-state energy; spectral near-degeneracy observed near ground state. (c) Shot-noise tests: algorithm remained effective but required slightly deeper circuits and showed non-monotonic dependence on shot number. Authors produced explicit parameterized circuits (ansatz) as outputs that could be executed on hardware.  
validation_and_benchmarks | Primary validation by direct comparison to exact diagonalization spectra for system sizes up to N=12 (Hilbert dimension 2^12). Secondary diagnostic: expectation value of H_L - H_R tracked (should vanish for ideal TFD) as a parity diagnostic; suggestion to compare thermal correlators or imaginary-time-evolved states for temperature checks. Also referenced large-N theoretical limit (Ref. [7]) that justifies H_TFD ground-state ≈ TFD in classical/large-N regime.  
claimed_feasibility | Authors argue approach is feasible on near-term NISQ devices (platform-agnostic), at least for small N (demonstrated up to 12 in simulation); learning gradients on device scales better than classical optimization on the full Hilbert space and naturally incorporates device noise. Bottlenecks identified: circuit depth vs gate noise tradeoff, classical verification beyond exact diagonalization for larger N, and requirement of larger N and large λ for genuine semiclassical holographic regimes.  
limitations_and_open_problems | Small system sizes (far from semiclassical large-N limit) limit direct gravity interpretation; approximation that ground state of H_TFD equals TFD is exact only in large-N, large-λ limit and for small μ/J; classical simulation limited beyond N≈12 (N=16 not tractable in this work); no modeling of hardware coherent/stochastic gate errors (only shot noise studied); near-degeneracy in spectrum complicates optimization and verification; temperature dependence and 1/N corrections not analyzed here and left for future work; verification strategies for larger N (thermal correlators, parity penalties) remain to be developed.  
complexity_or_hardness_arguments | No formal complexity-theory theorems presented. Authors note practical classical intractability of storing and optimizing in the full Hilbert space (exponential memory growth) and motivate hybrid quantum-classical approach for scalable gradient evaluation; no BQP/QMA hardness claims made.  
theory_context_keywords | AdS/CFT, holographic duality, thermofield double (TFD), traversable wormhole, SYK model, large-N limit, Schwarzian action, scrambling, teleportation-through-wormhole, semiclassical limit, parity diagnostics (H_L - H_R).  
citations_to_prior_work | Central prior works cited and used as context: Ref. [7] (coupled-SYK approaches showing ground-state ≈ TFD / traversable-wormhole connection), Ref. [9] (general TFD-as-ground-state strategies), Ref. [10],[11] (TFD preparation for Ising models and small-scale ion-trap implementation), Refs. [3],[2] (Gao-Jafferis-Wall traversable wormholes and Maldacena eternal black holes), Ref. [43] (qubitization approach for SYK time evolution suggested as promising for dynamics), Refs. [40],[41] (experimental proposals / reviews for realizing SYK-like models), parameter-shift foundations [22],[23], Jordan-Wigner/OpenFermion mapping tools [25],[27], and simulation tools Yao.jl [12].  
  
## Citation

Cite this artifact as `\cite{ast-ext-su-2026-08-13}`.
[code] 
    @misc{ast-ext-su-2026-08-13,
      title        = {Extraction: Variational Preparation of the Sachdev-Ye-Kitaev Thermofield Double},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-variational-preparation-of-the-sachdev-ye-kitaev-thermofield-double.md},
      crossref     = {su2020variationa},
      note         = {Theorizer's extraction from \cite{su2020variationa}. asta-artifact id: extraction-result-49},
    }
    
    @article{su2020variationa,
      title     = {Variational Preparation of the Sachdev-Ye-Kitaev Thermofield Double},
      author    = {V. P. Su},
      year      = {2020},
      journal   = {Physical Review A},
      url       = {https://www.semanticscholar.org/paper/243143608},
    }
[/code]
