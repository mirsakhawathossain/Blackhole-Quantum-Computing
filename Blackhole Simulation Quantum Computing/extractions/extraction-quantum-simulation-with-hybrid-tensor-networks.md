[<- All artifacts](<../index.md>)

# Extraction: Quantum Simulation with Hybrid Tensor Networks.

**Contents:**

  * Hybrid tensor networks suggested for quantum-gravity thought experiments and high-energy toy models (e.g., SYK/AdS-related models, Hayden–Preskill style thought experiments)



### Hybrid tensor networks suggested for quantum-gravity thought experiments and high-energy toy models (e.g., SYK/AdS-related models, Hayden–Preskill style thought experiments)

Field | Value  
---|---  
name_short | Hybrid-TN → QG mentions  
name_full | Hybrid tensor networks suggested for quantum-gravity thought experiments and high-energy toy models (e.g., SYK/AdS-related models, Hayden–Preskill style thought experiments)  
brief_description | The paper proposes a general hybrid tensor-network (classical+quantum tensors) framework and explicitly lists potential applications including toy models in high-energy physics and quantum-gravity thought experiments (references to SYK/AdS-like literature and black-hole information thought experiments), but it does not implement any black-hole simulation — these are offered as suggested future applications.  
citation_title | here  
mention_or_use | mention  
target_system_or_model | Not simulated in this work; the paper cites toy models for high-energy physics and quantum-gravity thought experiments (references [45-51, 84-89] in the manuscript) — examples implied by those citations include Sachdev–Ye–Kitaev (SYK)-type models and AdS/CFT-inspired toy models and black-hole information thought experiments (Hayden–Preskill, traversable-wormhole / coupled-SYK scenarios).  
black_hole_phenomena_targeted | Not explicitly targeted or simulated in this paper; the cited literature relates to phenomena such as scrambling and out-of-time-order correlators (OTOCs), information recovery/decoding (Hayden–Preskill), traversable-wormhole teleportation, entanglement and horizon-related entropy questions (Page-curve/entanglement dynamics), but the hybrid-TN paper itself only suggests these as potential future applications without specifying particular observables for a concrete gravitational simulation.  
simulation_paradigm | Hybrid classical-quantum tensor-network-assisted variational quantum simulation (hybrid TTN ansatz), i.e., tensor-network-assisted variational algorithms / variational imaginary-time evolution (VQE-like) applied to many-body problems; the authors propose this paradigm could be applied to toy-model quantum-gravity problems but do not present a concrete BH-specific simulation.  
quantum_hardware_platform | Platform-agnostic (no particular hardware is assumed); numerical experiments in the paper are classical simulations of the hybrid ansatz (emulating circuits that would run on a small quantum processor).  
encoding_and_mapping | No concrete black-hole model mapping is provided. The general hybrid-TTN mapping idea described in the paper: partition the large target system into subsystems (each represented as a quantum tensor prepared by a small quantum circuit or different initial states) and represent inter-subsystem correlations with classical low-rank tensors (MPS/other TN); this allows encoding an N-qubit target into operations on substantially fewer qubits (e.g., subsystems of size n represented by n-qubit quantum tensors, with classical indices of limited bond dimension representing correlations). The paper does not provide discretization, fermion mappings, or holographic encodings specific to black-hole models.  
algorithm_or_protocol | Variational imaginary-time evolution applied to the hybrid TTN ansatz (variational optimization of parameters in both quantum-circuit tensors and classical tensors); measurement procedures for contracting hybrid tensors are described (constructing M^{i',i} matrices via circuits explained in Appendix A3), but no black-hole-specific algorithms (e.g., thermofield-double preparation, traversable-wormhole teleportation protocols, or direct OTOC measurement protocols) are implemented in this work.  
resource_estimates | Paper gives generic resource scalings for hybrid TTNs: quantum-circuit count ~ O(N kappa^2 / epsilon^2) and classical contraction cost ~ O(N g kappa^4) (Proposition 2); specific numerical experiments demonstrated ground-state searches for spin lattices of up to 8x8 and 9x8 qubits using circuits acting only on 8+1 and 9+1 qubits respectively (i.e., they emulated problems of 64 and 72 qubits while needing quantum circuits for 9 and 10 qubits). The paper does not present resource estimates specialized to any black-hole model (no gate counts, T-counts, or fault-tolerance overheads for BH simulations).  
noise_and_error_mitigation | No explicit physical noise model or error-mitigation protocol tailored to black-hole simulations is provided. The paper discusses shot-noise/sample-count scaling for measurement (1/epsilon^2 dependence) and references general error-mitigation and subspace-expansion literature, but does not present concrete mitigation experiments for BH-like simulations.  
key_results_or_demonstrations | This paper demonstrates the hybrid-TTN approach on many-body spin Hamiltonians (1D and 2D nearest-neighbor spin models) via classical numerics: variational imaginary-time evolution using hybrid TTN ansatz reproduces ground-state energies for systems up to 8x8 and 9x4 (main text) / 9x8 (supplement) with relative errors ~10^{-3} compared to MPS/PEPS baselines; it shows the hybrid TTN can represent large systems using circuits on substantially fewer qubits (examples: simulating 64-qubit system using an 8+1 qubit device). No gravitational/black-hole simulations were performed — the gravitational applications are proposed future directions only.  
validation_and_benchmarks | Validation in this paper is against classical tensor-network algorithms for condensed-matter Hamiltonians: open-boundary MPS (DMRG) for 1D problems and PEPS imaginary-time evolution for 2D problems; achieved relative energy errors below ~10^{-3}. There is no validation against any gravitational or holographic analytic results because no BH model was simulated here.  
claimed_feasibility | Authors claim hybrid-TTN can reduce required quantum resources (qubits and circuit depth) for many practical problems and could enable certain large-scale simulations on near-term (NISQ) devices; they suggest potential applicability to quantum field theory and quantum-gravity thought experiments but do not claim immediate practicality for concrete black-hole simulations — specific feasibility statements for BH problems are not provided and would require further problem-specific mapping and resource analysis.  
limitations_and_open_problems | The paper explicitly notes limitations: (i) hybrid TNs are not universal for all states — contraction of arbitrary hybrid TN is #P-hard, (ii) some network topologies (loops, PEPS-like structures) increase contraction complexity substantially, (iii) only a constant number of quantum–quantum index contractions are practical (otherwise success probability may drop exponentially), (iv) measurement/shot cost and classical contraction cost can be high (scaling with bond dimension kappa and inverse target precision), and (v) the paper does not supply concrete encodings or protocols for black-hole/JT/SYK models — mapping and verification for BH problems remain open tasks.  
complexity_or_hardness_arguments | The paper states contracting an arbitrary hybrid tensor network is #P-hard. It does not provide complexity-theoretic claims (BQP/QMA hardness etc.) specific to black-hole models; it only highlights classical contraction hardness and the potential representational advantages of quantum tensors vs classical TNs (i.e., quantum tensors may express correlations that would require much larger classical bond dimensions).  
theory_context_keywords | hybrid tensor networks, tree tensor networks (TTN), MPS, PEPS, MERA, variational imaginary-time evolution, tensor-network-assisted quantum simulation, SYK (implied via citations), AdS/CFT (implied), Hayden–Preskill (black-hole information thought experiment, cited), traversable wormhole / coupled-SYK (cited literature), scrambling/OTOC (context from cited works).  
citations_to_prior_work | The paper cites a number of works in high-energy/quantum-gravity context as potential related applications (references in the manuscript): Y. Gu, X.-L. Qi, and D. Stanford (JHEP 05, 125 (2017), arXiv:1609.07832) [45]; P. Hayden and J. Preskill (JHEP 09, 120 (2007), arXiv:0708.4025) [46]; J. Maldacena, D. Stanford, and Z. Yang (Fortsch. Phys. 65, 1700034 (2017), arXiv:1704.05333) [47]; J. Maldacena and X.-L. Qi (arXiv:1804.00491) [48]; B. Yoshida and A. Kitaev (arXiv:1710.03363) [49]; J. Maldacena and D. Stanford (Phys. Rev. D 94, 106002 (2016), arXiv:1604.07818) [50]; J. Maldacena (Int. J. Theor. Phys. 38, 1113 (1999), arXiv:hep-th/9711200) [51]; and later-cited works relevant to traversable wormholes, ER=EPR, and scrambling such as P. Gao, D. L. Jafferis, and A. C. Wall (JHEP 12, 151 (2017), arXiv:1608.05687) [84], V. Balasubramanian et al. (Class. Quant. Grav. 31, 185015 (2014)) [85], J. Maldacena and L. Susskind (Fortsch. Phys. 61, 781 (2013), arXiv:1306.0533) [86], and S. H. Shenker and D. Stanford (JHEP 03, 067 (2014), arXiv:1306.0622) [87]. These are referenced as potential target literature to which the hybrid-TN framework could be applied; the hybrid-TN paper itself does not implement or adapt the methods of those references to gravitational simulations.  
  
## Citation

Cite this artifact as `\cite{ast-ext-yuan-2026-08-13}`.
[code] 
    @misc{ast-ext-yuan-2026-08-13,
      title        = {Extraction: Quantum Simulation with Hybrid Tensor Networks.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-with-hybrid-tensor-networks.md},
      crossref     = {yuan2020quantum},
      note         = {Theorizer's extraction from \cite{yuan2020quantum}. asta-artifact id: extraction-result-62},
    }
    
    @article{yuan2020quantum,
      title     = {Quantum Simulation with Hybrid Tensor Networks.},
      author    = {Xiao Yuan and Jinzhao Sun and Junyu Liu and Qi Zhao and You Zhou},
      year      = {2020},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/220301699},
    }
[/code]
