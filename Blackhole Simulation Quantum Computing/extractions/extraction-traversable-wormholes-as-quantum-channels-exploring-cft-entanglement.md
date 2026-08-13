[<- All artifacts](<../index.md>)

# Extraction: Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography

**Contents:**

  * Traversable Wormhole as a Quantum Channel (coarse-grained code-subspace mapping)



### Traversable Wormhole as a Quantum Channel (coarse-grained code-subspace mapping)

Field | Value  
---|---  
name_short | TW-as-QChannel  
name_full | Traversable Wormhole as a Quantum Channel (coarse-grained code-subspace mapping)  
brief_description | This paper formulates a traversable AdS wormhole (two-sided AdS-Schwarzschild/BTZ rendered traversable by a double-trace deformation) as a quantum communication channel between boundary CFT subsystems, and constructs a coarse-grained finite-dimensional encoding/decoding (code-subspace) map that captures signal transmission, entanglement capacity, and entanglement-witness protocols.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Two-sided AdS black hole in AdS/CFT (explicitly BTZ in D=3) with a double-trace deformation producing negative null-energy shock(s) that render the Einstein-Rosen bridge traversable; dual boundary system is two large-N CFTs in the thermofield-double family.  
black_hole_phenomena_targeted | Wormhole traversability induced by double-trace boundary deformation (negative null energy shock), horizon shift and causal window for signal transmission (Δv window), transmission of localized excitations across the wormhole, entanglement structure between the two boundaries, and entanglement capacity of the induced channel.  
simulation_paradigm | The paper develops a theoretical mapping to finite-dimensional quantum channels (coarse-grained code-subspace) rather than proposing a concrete hardware-level quantum simulation; i.e., a platform-agnostic, analytical channel-model construction and protocols (not a gate-level digital or analog experimental implementation).  
quantum_hardware_platform | platform-agnostic (no specific hardware or experimental platform is assumed or used).  
encoding_and_mapping | Coarse-graining: select N left and N right bulk insertion locations x_i^{L/R} (close to boundary) and associate each with a local boundary operator O_{A_i} (left) or O_{B_j} (right) supported on disjoint minimal boundary subregions A_i, B_j. Define a finite-dimensional code Hilbert space ~H = ~H_L ⊗ ~H_R with dimension d^2, d = 2^N. Encoding operator V (Eq. 37) maps basis states |~X_α>_L |~X_β >_R to multi-insertion states (tensor product of chosen O_ is explicitly defined as states reachable by allowed local operators acting on the reduced TFD state on A (Eq. 32). Backreaction is controlled by restricting to at most single insertions per location and working in perturbative regime to keep geometry semiclassical.}, O_{B_j} acting on |TFD(t_i)>), normalized; V is not isometric because encoded states are not orthogonal. Time evolution (including double-trace deformation) implements U = U(t_f,t_w) e^{iħ O_L O_R} U(t_w,t_i). Decoding W projects late-time bulk excitations back onto the code basis via overlaps with strings of boundary operators (Eqs. 40-41). Domain of the boundary-subregion channel N^{A->B  
algorithm_or_protocol | Conceptual protocol: prepare thermofield-double-like state; encode qubits by acting with selected local boundary operators (encoding V) to create localized bulk excitations; evolve under CFT unitary with an intervening double-trace deformation e^{i h O_L O_R} at time t_w producing negative-energy shock(s); receive output at the other boundary at t_f and decode via overlap measurements (W) onto the finite code basis. Information-theoretic protocols include bounding/saturating entanglement capacity (using entanglement-cost/distillable-entanglement framework) and using signal-sending protocols as entanglement witnesses for specific entanglement structure. The analysis uses standard quantum-channel quantities (coherent information, one-shot/asymptotic capacities) and known results for bipartite unitary channels to infer additivity and capacities (Refs. [2.x] in paper).  
resource_estimates | No hardware-level resource estimates (no qubit counts, gate counts, T-gate counts, circuit depths, shot counts, or explicit runtime scalings) are provided. The only explicit finite-dimensional parameter is the coarse-graining dimension d = 2^N (N chosen insertion sites per side), yielding d^2 code states; constraints arise from requiring perturbative backreaction (small number and energy of excitations) so geometry remains semiclassical. No fault-tolerance or FTQC overheads are discussed.  
noise_and_error_mitigation | No quantum-hardware noise model or mitigation techniques are discussed. The paper treats the full boundary evolution as unitary (CFT time evolution) and semiclassical bulk as deterministic; open-system/noisy channel aspects are studied abstractly (quantum channel formalism) but no experimental error mitigation (ZNE, PEC, tomography budgets, etc.) or decoding error rates are given.  
key_results_or_demonstrations | Main achievements are conceptual/theoretical: (1) explicit definition of a quantum channel N^{A->B} mapping initial reduced states on a left boundary subregion A to reduced states on a right subregion B (Eq. 31 and Eq. 32); (2) construction of an explicit finite-dimensional code-subspace encoding V and decoding W to model traversable-wormhole signal transmission as a channel between d-dimensional factors; (3) gravitational estimate of horizon shift α (Eq. 27) and identification of a finite causal window for successful transmission; (4) derivation of bounds on entanglement capacity of the wormhole channel using holographic/geometric data and demonstration of a protocol that saturates that bound in the semiclassical limit; (5) formulation of wormhole traversability as an entanglement witness and explicit protocols to probe entanglement structure between the two CFTs. All are proposals/analytical results; no numerical simulations or hardware experiments are performed.  
validation_and_benchmarks | Validation is conceptual: the channel and code-subspace construction is checked for consistency against semiclassical gravitational analysis (shock-wave horizon-shift computations, AdS-Vaidya matching, and causal-window reasoning), and channel capacity/entanglement statements are connected to established quantum-information theorems (entanglement capacity of bipartite unitaries, coherent information definitions). No numerical benchmarks, exact-diagonalization comparisons, or experimental cross-checks are presented.  
claimed_feasibility | Authors treat the construction as a theoretical framework and do not make claims about near-term experimental feasibility. They emphasize working in the large-N semiclassical holographic regime and small backreaction; preparation of TFD-like states and exact operator reconstructions are acknowledged as nontrivial. No NISQ/timeframe estimates are provided and the implementation-level feasibility (e.g., on NISQ devices) is not discussed.  
limitations_and_open_problems | Explicitly discussed limitations: (1) infinite-dimensional nature of full CFT Hilbert spaces motivates coarse-graining; finite-dimensional code-subspace mapping is a simplification and V is not isometric because basis states are nonorthogonal; (2) it is not rigorously known that the assumed local reconstructions of bulk operators on minimal boundary subregions exist for the TFD background (caveat noted); (3) restrictions to perturbative regime to avoid strong backreaction limit the number/energy of insertions and thus channel throughput; (4) no explicit hardware-level realization, resource estimates, or error budgets are provided; (5) the formalism does not resolve fundamental statements such as entanglement non-observability — it only yields partial entanglement witnesses; (6) verification challenges remain (preparing unknown TFD-family states, distinguishing different t-shifts in Eq. 29).  
complexity_or_hardness_arguments | No formal computational-complexity theorems (e.g., BQP/QMA hardness) are presented for the simulation task. The paper does not claim classical intractability or provide reductions; complexity considerations are framed in terms of channel capacity and entanglement measures rather than algorithmic hardness or resource scaling proofs.  
theory_context_keywords | AdS/CFT, traversable wormhole, double-trace deformation, thermofield double, BTZ black hole, AdS-Vaidya shock, quantum channel, coherent information, entanglement capacity, code subspace, holographic reconstruction, ER/EPR (discussed), entanglement witness, semiclassical gravity, fast-scrambling (background context).  
citations_to_prior_work | Key referenced works and topics mentioned in the paper (by reference number and topic as given in text): Refs. [17,18] — double-trace deformation / traversable wormhole construction; Ref. [19] — finite-dimensional code-subspace approach (used as motivation for encoding); Ref. [24] — entanglement capacity results for bipartite unitary channels; Refs. [29,30] — shock-wave/AdS-Vaidya techniques for horizon shifts; Ref. [14] — earlier discussion linking wormholes and entanglement non-observability; Refs. [36,37] — infinite-dimensional bosonic channels commentary; Refs. [38,39] — operator reconstruction results in AdS and AdS-Schwarzschild. (The paper's reference list should be consulted for the exact bibliographic titles.)  
  
## Citation

Cite this artifact as `\cite{ast-ext-bao-2026-08-13}`.
[code] 
    @misc{ast-ext-bao-2026-08-13,
      title        = {Extraction: Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-traversable-wormholes-as-quantum-channels-exploring-cft-entanglement.md},
      crossref     = {bao2018traversabl},
      note         = {Theorizer's extraction from \cite{bao2018traversabl}. asta-artifact id: extraction-result-30},
    }
    
    @article{bao2018traversabl,
      title     = {Traversable wormholes as quantum channels: exploring CFT entanglement structure and channel capacity in holography},
      author    = {N. Bao and A. Chatwin-Davies and Jason Pollack and Grant N. Remmen},
      year      = {2018},
      journal   = {Journal of High Energy Physics},
      url       = {https://www.semanticscholar.org/paper/53601332},
    }
[/code]
