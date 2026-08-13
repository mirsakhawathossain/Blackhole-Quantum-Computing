[<- All artifacts](<../index.md>)

# Extraction: Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer

**Contents:**

  * Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer



### Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer

Field | Value  
---|---  
name_short | VQE-Hawking-IBMQ  
name_full | Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer  
brief_description | Implements a hybrid variational quantum simulation of Hawking-radiation-related observables for a non-rotating (Schwarzschild), uncharged black hole by discretizing the continuum Hamiltonian into a small finite grid, mapping it to qubits (Pauli basis), and finding the ground-state energy with VQE on IBM Quantum Experience. The ground-state energies are used to extract temperature and power scalings vs mass and radius and compared with exact solver and theoretical expectations.  
citation_title | Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer  
mention_or_use | use  
target_system_or_model | Non-rotating, uncharged Schwarzschild black hole; Hamiltonian derived from the Schwarzschild metric (Jacobi principle) leading to a particle Hamiltonian H^d ∝ (1 + GM/2r)^{1/4} Σ p_i^2 terms.  
black_hole_phenomena_targeted | Hawking radiation thermodynamic observables: ground-state energy used to extract effective temperature (T ∝ 1/M) and Bekenstein–Hawking luminosity / radiated power scaling (P ∝ 1/M^2); energy vs radius dependence near horizon.  
simulation_paradigm | Hybrid/variational (VQE) — gate-based digital quantum circuits prepared by parametrized ansätze and classical optimization (SPSA).  
quantum_hardware_platform | IBM Quantum Experience (superconducting qubits) — experiments/implementations performed using Qiskit/Aqua on IBMQ backends (platform acknowledged).  
encoding_and_mapping | Continuum-to-discrete spatial discretization: 2D (x,y) grid with each coordinate discretized to N=4 points (mesh of N^2 spatial points). Position operator is diagonal (N×N), momentum obtained by discrete Fourier transform p^d = (F^d)^{-1} x^d F^d. Two qubits per spatial dimension were used (stated), leading to a 4-qubit representation for their implementation; multi-dimensional kinetic term assembled via tensor products. The discrete Hamiltonian is decomposed into a Pauli basis (σ_x, σ_y, σ_z, I) for circuit implementation (explicit Pauli-sum provided, Eq. 12). Boundary/gauge choices: simple finite discrete mesh centered at origin; no gauge fields or fermion mappings needed (bosonic/particle position-momentum discretization).  
algorithm_or_protocol | Variational Quantum Eigensolver (VQE) with three tested custom ansätze (combinations of U3, Ry, CNOT and controlled-U3 gates) and SPSA (simultaneous perturbation stochastic approximation) classical optimizer; exact eigensolver from Qiskit Aqua used for comparison/benchmarking.  
resource_estimates | Reported/used resources: N=4 per coordinate (discrete basis), two qubits per spatial dimension → implemented with 4 qubits total in the reported experiments; explicit circuit gate-level counts or depths not provided. No T-counts, logical-layer FTQC overheads, or detailed scaling formulas given beyond statements that larger N requires more qubits and more ansatz parameters (hence higher circuit depth). Number of VQE iterations and measurement shots are not specified in the paper.  
noise_and_error_mitigation | No explicit noise model or formal error mitigation protocol is described. The experiments used IBMQ (no detailed readout-depolarizing model, no zero-noise extrapolation, probabilistic error cancellation, or symmetry verification reported). Authors discuss ansatz-induced errors (overfitting, control-gate effects) and attribute some deviations to circuit/ansatz structure rather than applying explicit mitigation.  
key_results_or_demonstrations | Demonstration: VQE computed ground-state energies for varied black-hole mass (M) and radius (r) for the discretized Schwarzschild Hamiltonian; extracted relations E(M) ≈ a(b + c M)^{1/4} and E(r) ≈ a(b + c/r)^{1/4}. From energy they derived temperature scaling (T ∝ 1/M) and power scaling (P ∝ 1/M^2). Three ansätze tested: Ansatz 3 produced results closest to theory; Ansatz 2 matched the exact eigensolver closely in many cases; Ansatz 1 showed larger deviation/variance (likely due to many parameters/control gates). The work is an actual hardware/software experiment on IBMQ (not only a purely theoretical proposal). Quantitative fidelity/error numbers are not provided; agreement is described qualitatively via plotted curves and energy gaps vs exact solver.  
validation_and_benchmarks | Validation: direct comparison to an exact eigensolver available in Qiskit Aqua (used as ground truth for the discrete Hamiltonian); qualitative comparison of extracted temperature and power scalings with semiclassical Hawking theory (T ∝ 1/M, P ∝ 1/M^2) and with prior literature on Hawking radiation. No extensive finite-size scaling study or statistical error bars are reported, but plots show VQE vs exact curves and discussion of deviations per ansatz.  
claimed_feasibility | Authors claim NISQ-era quantum computers can be used to study cosmological phenomena in toy limits (small discretizations); small-N experiments feasible on IBMQ now (demonstrated). They note scaling: higher N (finer discretization) requires more qubits and more ansatz parameters increasing circuit depth and difficulty, implying practical limits on NISQ and a need for larger/noiseless devices for more accurate simulations. No explicit timeframe or threshold for fault-tolerance is given.  
limitations_and_open_problems | Explicit limitations: toy-model (non-rotating, uncharged Schwarzschild only), small discretization (N=4) and hence coarse approximation of continuum, limited qubit count (4 qubits used), lack of explicit noise mitigation, ansatz-dependent errors (overfitting, control-gate induced energy shifts), absence of dynamical spacetime evolution (only stationary Hamiltonian), omission of charged/rotating black holes and full field-theory treatment, and no quantitative error budgets or scalability estimates. Open problems suggested: extend to rotating/charged black holes, increase discretization (N) and qubit counts, improve ansätze and mitigation, and simulate richer gravitational models.  
complexity_or_hardness_arguments | No formal complexity-theoretic claims (e.g., BQP/QMA hardness) are made in the paper; no rigorous statements about classical intractability or verification complexity are presented.  
theory_context_keywords | Schwarzschild metric, Hawking radiation, Bekenstein–Hawking luminosity, Jacobi principle (least action), discrete spatial lattice, variational quantum eigensolver (VQE), quantum cosmology, minisuperspace-style toy model.  
citations_to_prior_work | Key cited works used as basis or context: Peruzzo et al., 'A variational eigenvalue solver on a photonic quantum processor' (VQE algorithm); S. Hawking, 'Black hole explosions?' (1974) and 'Particle creation by black holes' (1975); J. Steinhauer, 'Observation of Quantum Hawking Radiation and its Entanglement in an Analogue Black Hole' (2016) (analogue experiments); R. D. Somma, 'Quantum simulations of one dimensional quantum systems' (methods for discretized operator construction); I. S. Kohli, 'Quantum wave function in a Schwarzschild spacetime' (arXiv:1110.6204) (spacetime wavefunction context); IBM Quantum Experience and Qiskit/Aqua references used for implementation and exact eigensolver. The paper's reference list (Refs. [2],[3],[24],[26],[33],[35],[36]) contains these and other background sources.  
  
## Citation

Cite this artifact as `\cite{ast-ext-dhaulakhandi-2026-08-13}`.
[code] 
    @misc{ast-ext-dhaulakhandi-2026-08-13,
      title        = {Extraction: Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-hawking-radiation-using-vqe-algorithm-on-ibm-qu.md},
      crossref     = {dhaulakhandi2021quantum},
      note         = {Theorizer's extraction from \cite{dhaulakhandi2021quantum}. asta-artifact id: extraction-result-16},
    }
    
    @article{dhaulakhandi2021quantum,
      title     = {Quantum Simulation of Hawking Radiation Using VQE Algorithm on IBM Quantum Computer},
      author    = {Ritu Dhaulakhandi and B. K. Behera},
      year      = {2021},
      url       = {https://www.semanticscholar.org/paper/245634244},
    }
[/code]
