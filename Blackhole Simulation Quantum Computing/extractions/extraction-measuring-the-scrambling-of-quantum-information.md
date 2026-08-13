[<- All artifacts](<../index.md>)

# Extraction: Measuring the scrambling of quantum information

**Contents:**

  * Interferometric protocol for measuring out-of-time-order correlators (OTOCs)
  * Distinguishability (projection) protocol to measure |F(t)|^2
  * Cavity quantum electrodynamics implementation of nonlocal spin models for probing scrambling
  * Kicked top as a paradigmatic chaotic many-body model for probing scrambling
  * Kitaev's model (SYK-like random fermion model) and cold-atom realizations



### Interferometric protocol for measuring out-of-time-order correlators (OTOCs)

Field | Value  
---|---  
name_short | OTOC interferometric protocol  
name_full | Interferometric protocol for measuring out-of-time-order correlators (OTOCs)  
brief_description | A gate-sequence protocol using a control qubit to prepare two interferometer branches whose interference (measurement of control X and Y) yields the complex OTO correlator F(t)=⟨W_t^† V^† W_t V⟩; requires the ability to implement V conditioned on the control and to reverse the sign of the system Hamiltonian for an echo.  
citation_title | here  
mention_or_use | use  
target_system_or_model | generic many-body quantum system (spin ensemble) evolving under a many-body Hamiltonian H; used to probe scrambling rather than to simulate a specific gravitational model  
black_hole_phenomena_targeted | scrambling / OTOC growth and Lyapunov/chaos diagnostics (black-hole-related: diagnosing fast scrambling and comparing Lyapunov exponents to the chaos bound)  
simulation_paradigm | analog quantum simulation / quantum many-body interferometry (experimentally implemented as an interferometric sequence rather than a digital algorithm)  
quantum_hardware_platform | neutral atoms in optical cavity (cavity QED) as the primary proposal; protocol also discussed as translatable to trapped ions, Rydberg atoms, optical lattices (platform-agnostic in principle)  
encoding_and_mapping | system degrees of freedom encoded as two-level atoms (pseudo-spins) |↑⟩,|↓⟩; operators V and W are simple unitaries (global or local spin rotations); time evolution U(t)=e^{-iHt} under engineered spin Hamiltonians (e.g., one-axis twisting S_x^2 or kicked-top stroboscopic map); permutation-symmetric states exploited for uniform-coupling cases (Dicke subspace) to reduce Hilbert space  
algorithm_or_protocol | apply controlled-V (control qubit implements V on one arm), then U(t), W, U(-t) (time reversal of sign of H), then controlled-V on the other arm to prepare (VW_t|ψ⟩)|0⟩ + (W_tV|ψ⟩)|1⟩; measure control Pauli-X and Y to obtain Re(F) and Im(F).  
resource_estimates | No fault-tolerant resource counts; experimental resource estimates: controlled collective phase rotation magnitude limited by φ_max ≲ sqrt(η/(8N)); cavity cooperativity η ~ 10–100 gives usable regimes; atom numbers N ≲ 10^2 give small dissipation; with η≈100 and k=3 chaotic timescales observable up to N ~ 10^3. No qubit/gate counts provided.  
noise_and_error_mitigation | Explicit dissipation sources modeled: cavity photon leakage rate κ and atomic excited-state spontaneous emission Γ. Effective Lindblad operators: L_κ = √γ S_x with γ = 2χ/d, and per-atom spontaneous-emission jumps L_i^{±}, L_i^{↑,↓} with rate μ≈χ d/(4η). Partial time-reversal (Hamiltonian sign reversed but dissipation not) is used; mitigation by choosing detuning d to balance channels, optimizing detuning z for controlled-phase, keeping evolution times short (before many spontaneous events), and post-calibrating/renormalizing contrast. Simulations use quantum-trajectory methods and post-selection strategies in hermitian-operator extensions.  
key_results_or_demonstrations | Proposal and detailed protocol; numerically demonstrated (simulation-only) for collective spin models (one-axis twisting and kicked top) including dissipative quantum-trajectory simulations showing early-time dissipative evolution closely follows unitary evolution and that OTOC (F) decays on a longer timescale than time-ordered correlator (G) with scaling consistent with log(N) scrambling time; no full hardware experiment reported in this paper.  
validation_and_benchmarks | Validation against unitary dynamics and semiclassical expectations: comparisons of OTOC vs time-ordered correlator decay times for various N, demonstration of log(N) scaling consistent with semi-classical Ehrenfest/fast-scrambling arguments, and dissipative quantum-trajectory simulations (hundreds of trajectories) to benchmark realistic cavity parameters (η, δ, κ, Γ).  
claimed_feasibility | Authors claim feasibility of early-time OTOC measurements on state-of-the-art cavity-QED platforms (η ~ 10–100) for N up to O(10^2) (small dissipation) and possibly up to ∼10^3 for observing onset of chaos with optimized parameters; identify controlled-phase contrast and dissipation as primary bottlenecks but assert present technology can perform meaningful experiments.  
limitations_and_open_problems | Protocol depends on reversing Hamiltonian sign while dissipation is not reversed (partial time reversal); controlled-phase angle limited (φ_max ~ √(η/8N)), limiting rotation magnitude as N grows; finite-size effects and dissipation limit access to late-time dynamics and full scrambling; paper does not realize a genuine gravitational black hole dual system—mapping to true holographic models (e.g., SYK/Kitaev) is suggested but remains challenging experimentally; verification of black-hole-like universal Lyapunov exponent is contingent on realizing appropriate fast-scrambling Hamiltonians.  
complexity_or_hardness_arguments | No formal complexity-theoretic hardness claims for simulation; conceptual statements: fast-scrambling conjecture and chaos bound discussed (Lyapunov exponent bound), and random-circuit models are argued to be optimal scramblers; no BQP/QMA claims.  
theory_context_keywords | scrambling, out-of-time-order correlators (OTOC), butterfly effect, fast scrambling, chaos bound (Maldacena–Shenker–Stanford), Ehrenfest time, holographic duality / AdS/CFT (mentioned as motivation), semiclassical limit, Lyapunov exponent  
citations_to_prior_work | Shenker & Stanford (black hole chaos), Maldacena–Shenker–Stanford (chaos bound), Lashkari et al. (random-circuit fast-scrambler), Kitaev (SYK model talk), experimental cavity-QED and collective-spin references (Sørensen & Mølmer; Leroux, Schleier-Smith & Vuletić; multimode cavity proposals: Gopalakrishnan et al.; Strack & Sachdev).  
  
### Distinguishability (projection) protocol to measure |F(t)|^2

Field | Value  
---|---  
name_short | Distinguishability protocol  
name_full | Distinguishability (projection) protocol to measure |F(t)|^2  
brief_description | An alternative protocol that prepares the many-body state |ψ_f⟩ = W_t^† V^† W_t V |ψ⟩ and measures the projector Π = |ψ⟩⟨ψ| to obtain |F|^2 = ⟨ψ_f|Π|ψ_f⟩, avoiding the need for a control qubit at the cost of requiring projective measurement onto a many-body state or careful choice of initial states.  
citation_title | here  
mention_or_use | use  
target_system_or_model | generic many-body system (spin ensemble) under engineered Hamiltonian evolution; applied in context of cavity-QED spin models and other cold-atom platforms  
black_hole_phenomena_targeted | scrambling diagnostics (magnitude of OTOC) as a measure of the indistinguishability growth between two evolution orders  
simulation_paradigm | analog quantum simulation / measurement protocol (non-digital)  
quantum_hardware_platform | cavity QED with cold atoms; also translatable to optical lattices, trapped ions, Rydberg atoms (platform-agnostic)  
encoding_and_mapping | as above: two-level atoms as pseudo-spins; uses the same time-evolution U(t) and operator actions (V, W); requires the ability to prepare and project onto chosen many-body initial states (e.g., coherent states, superfluid or Mott states) or use local probes/time-of-flight  
algorithm_or_protocol | Apply sequence to prepare W_t^† V^† W_t V |ψ⟩, then measure overlap with |ψ⟩ (projector Π) to get |F|^2; practical implementation requires states where projector is accessible (special initial states) or indirect measurement techniques.  
resource_estimates | No explicit circuit counts; practicality limited by ability to implement many-body projective measurement; resource scaling similar to interferometric protocol but without control-qubit operations; measurement shot counts not quantified.  
noise_and_error_mitigation | Same dissipative noise channels as interferometric protocol (cavity decay κ and spontaneous emission Γ); advantage: no controlled-phase fidelity requirement for control qubit conversion to cavity photon, but relies on accurate many-body state projection which is experimentally challenging and noise-sensitive; mitigation via choice of measurable initial states and short evolution times.  
key_results_or_demonstrations | Presented as a viable simpler-to-implement alternative for accessing |F|^2; not demonstrated in hardware; argued to contain similar timescale information as full complex F(t).  
validation_and_benchmarks | The paper argues theoretically that |F|^2 contains similar timescales as F; no explicit numerical benchmarks separate from interferometric results.  
claimed_feasibility | Claimed as feasible in systems where projection onto the chosen initial state is experimentally possible (e.g., certain optical-lattice states measured by time-of-flight or in-situ imaging); less demanding in control-qubit hardware but more demanding in measurement capabilities.  
limitations_and_open_problems | Requires ability to project onto arbitrary many-body states (often impractical); provides only magnitude |F| not phase information (loses sign/imaginary parts); sensitivity to state-preparation and measurement errors.  
complexity_or_hardness_arguments | No complexity claims.  
theory_context_keywords | OTOC magnitude, Loschmidt echo analog, state distinguishability, projective measurement  
citations_to_prior_work | Refs to prior many-body interferometry and projection techniques (Abanin & Demler; Jiang et al.; Knap et al.), and to experimental platforms where projection may be easier (optical-lattice measurement literature).  
  
### Cavity quantum electrodynamics implementation of nonlocal spin models for probing scrambling

Field | Value  
---|---  
name_short | Cavity-QED spin simulator  
name_full | Cavity quantum electrodynamics implementation of nonlocal spin models for probing scrambling  
brief_description | A concrete experimental proposal using an ensemble of two-level atoms coupled to one or more cavity modes and driven by lasers to realize controllable nonlocal spin-spin couplings J_ij (including one-axis twisting S_x^2 and variants), with sign-control via two-photon detuning and ability to switch interactions on/off to implement time reversal.  
citation_title | here  
mention_or_use | use  
target_system_or_model | nonlocal spin models realized by cavity-mediated interactions; special cases: one-axis twisting H_twist = χ S_x^2 and periodically kicked-top stroboscopic map U = e^{-ikS_x^2/(2S)} e^{-ipS_z}  
black_hole_phenomena_targeted | fast scrambling-like dynamics and chaotic growth of commutators (OTOCs) as an analog diagnostic of black-hole-like information spreading  
simulation_paradigm | analog quantum simulation (engineer Hamiltonian H via cavity-mediated interactions and drives), with echo sign reversal implemented by changing two-photon detuning δ (sign of J_ij)  
quantum_hardware_platform | neutral atoms in optical cavities (cavity QED) with possibility to adapt to multimode cavities; proposals also discuss translation to trapped ions, Rydberg atoms, and optical lattices  
encoding_and_mapping | each atom encodes a spin-1/2 (pseudo-spin s_i); cavity modes produce effective pairwise couplings J_{ij} = Σ_α (Ω_↑^_(r_i) Ω_↓(r_j) / (Δ_↑ Δ_↓)) (g_α(r_i) g_α^_(r_j) / δ); uniform single-mode coupling reduces to collective spin operators S_x^2 and dynamics in permutation-symmetric Dicke subspace (dimension N+1).  
algorithm_or_protocol | Implement drive lasers and cavity couplings to realize desired H (turn interactions on/off and change sign via two-photon detuning δ); produce controlled phase gate by converting control qubit to cavity photon to enact Z_φ^C = I⊗|0⟩⟨0| + e^{-iφ S_z}⊗|1⟩⟨1|; perform echo U(t) and U(-t) by flipping sign of χ (via δ) to measure OTOCs.  
resource_estimates | Analytic experimental estimates: controlled rotation limited by φ_max ≲ √(η/(8N)); detuning optimality yields z_opt and d_opt formulas; minimum cooperativity to observe chaotic timescales η ≳ (k/2 ln N)^2; example numbers: η≈10–100 achievable in strong-coupling cavities, permitting N ≲ 10^2 with small dissipation and up to N∼10^3 for onset-of-chaos observation with η≈100 and k=3; no gate-counts or qubit numbers beyond atom count N given.  
noise_and_error_mitigation | Dissipation explicitly modeled: cavity decay κ → collective Lindblad L_κ = √γ S_x with γ = 2χ/d; spontaneous emission Γ → per-atom jumps with rate μ ≈ χ d/(4η). Control-phase errors from photon loss reduce interferometric contrast; mitigation via optimizing detuning parameters (d, z), keeping evolution times short (fewer than O(1) spontaneous events), quantum-trajectory averaging, and rescaling F(0)=1 to correct contrast loss.  
key_results_or_demonstrations | Detailed proposal and quantitative modeling (master-equation/quantum-trajectory simulations) of OTOC measurement in one-axis twisting and kicked-top models including dissipation; numerics show early-time dissipative dynamics track unitary predictions and that OTOC decay times separate from time-ordered correlators, consistent with scrambling behavior; no experimental demonstration in this work.  
validation_and_benchmarks | Benchmarking via comparison of unitary vs dissipative simulations (quantum trajectories), semi-classical expectation for kicked top (log(N) scaling of scrambling time), statistical error estimates from trajectory sampling, and limits set by cooperativity-derived formulas validated by physical-parameter estimates.  
claimed_feasibility | Authors claim current cavity-QED experiments (η∼10–100) can observe early-time OTOC physics and distinguish scrambling vs relaxation timescales for N ≲ 10^2; observing classical-chaos timescales up to N∼10^3 may be possible with optimally chosen parameters (η≈100, k=3). Bottlenecks: cooperativity, photon loss during controlled-phase, and spontaneous emission.  
limitations_and_open_problems | Model realizes nonlocal spin dynamics but is not equivalent to a gravitational black hole; realizing models that are dual to black holes (e.g., SYK/Kitaev) in cavity settings is challenging; controlled-phase magnitude and dissipation scale poorly with N; approximations in adiabatic elimination and truncation of spontaneous-emission events in simulations (limiting trajectory depth) introduce errors; partial time reversal (dissipation not reversed) may limit access to late-time physics.  
complexity_or_hardness_arguments | No explicit computational complexity statements; conceptual mapping to random nonlocal spin models and SYK-like models (which have been argued to be maximally chaotic) is discussed but not formalized into complexity claims.  
theory_context_keywords | cavity QED, one-axis twisting, Dicke subspace, collective spin, kicked top, random nonlocal spin models, fast scrambling, cooperativity, Lindblad dissipation  
citations_to_prior_work | References given to cavity-mediated spin models and experiments (Sørensen & Mølmer; Leroux et al.; Schleier-Smith et al.), multimode cavity spin-glass proposals (Gopalakrishnan et al.; Strack & Sachdev), controlled-phase and dissipation modeling (Davis, Bentsen & Schleier-Smith), and implementation references (Colombe et al.; Klinder et al.).  
  
### Kicked top as a paradigmatic chaotic many-body model for probing scrambling

Field | Value  
---|---  
name_short | Kicked top simulator  
name_full | Kicked top as a paradigmatic chaotic many-body model for probing scrambling  
brief_description | Use of the periodically-kicked collective-spin (kicked top) model U = e^{-ik S_x^2/(2S)} e^{-ip S_z} (with p=π/2) to generate dynamics ranging from regular (small k) to chaotic (large k); used as an experimentally accessible testbed whose OTOC behavior (decay times, log(N) scaling) models scrambling phenomena.  
citation_title | here  
mention_or_use | use  
target_system_or_model | kicked top (collective spin) model implemented via cavity-mediated S_x^2 interactions plus global S_z kicks  
black_hole_phenomena_targeted | scrambling / exponential growth of operator complexity and separation of relaxation vs scrambling timescales (analog of butterfly effect and Ehrenfest-time scaling relevant to black-hole scrambling bounds)  
simulation_paradigm | analog quantum simulation (stroboscopic evolution) and numerical quantum-trajectory simulation for dissipative dynamics  
quantum_hardware_platform | cavity-QED ensemble of neutral atoms (collective spin), optionally scalable to other platforms that realize collective spin couplings  
encoding_and_mapping | collective spin S = Σ_i s_i in permutation-symmetric (Dicke) subspace; semiclassical limit S→∞ (N→∞) maps to classical motion on Bloch sphere with Lyapunov exponent λ; V and W are chosen as small-angle S_z rotations (φ∼1/√S) to separate time-ordered vs OTOC timescales  
algorithm_or_protocol | Stroboscopic application of interaction and kick unitaries to implement U; measurement of OTOC via interferometric protocol (control qubit) or distinguishability; sign-reversal of H realized by switching sign of interaction (via two-photon detuning) to perform echo U(-t).  
resource_estimates | Simulated atom numbers N = 50–500 in numerical results; to observe log(N) scaling and onset of chaos authors discuss requirements η ≳ (k/2 ln N)^2 with example k=3 giving feasibility up to N≈10^3 for η≈100; no digital-gate resource counts.  
noise_and_error_mitigation | Dissipation modeled as above (L_κ and per-atom jumps); quantum-trajectory simulations show early-time fidelity of OTOC vs unitary; mitigation via limiting number of kicks (log N), optimizing detuning to balance decay channels d_opt ≈ √(8η), and choosing evolution times before many spontaneous events.  
key_results_or_demonstrations | Numerical demonstration (unitary and dissipative trajectories) that OTOC |F(t)| decays on a timescale growing ≈log(N) while time-ordered correlator |G(t)| decays on an N-independent timescale; dissipative simulations (η=100, δ=10κ) show early-time agreement with unitary dynamics and resolvable separation of timescales.  
validation_and_benchmarks | Comparison of numerical unitary results to semiclassical expectations (Ehrenfest time and Lyapunov scaling), and to dissipative quantum-trajectory simulations; demonstration of finite-N scaling consistent with classical chaos theory and prior theory of scrambling.  
claimed_feasibility | Authors claim this model is an ideal experimental testbed where N can be scaled from small quantum regime (small S) to semi-classical, and that present cavity-QED setups can probe early-time OTOC behavior for moderate N.  
limitations_and_open_problems | Kicked-top is a toy chaotic model with collective (nonlocal) interactions and not equivalent to bona fide holographic quantum field theories or gravitational black holes; extrapolation of observed Lyapunov-like behavior to holographic universality requires realizing true fast-scrambling many-body Hamiltonians (e.g., SYK).  
complexity_or_hardness_arguments | No formal complexity-theoretic claims; used as an illustrative model for semiclassical chaos and scrambling.  
theory_context_keywords | kicked top, Lyapunov exponent, Ehrenfest time, semiclassical limit, collective spin chaos, log(N) scrambling time  
citations_to_prior_work | Haake et al. (kicked-top theory), Chaudhury et al. (experimental kicked top), Wang et al. (kicked-top studies).  
  
### Kitaev's model (SYK-like random fermion model) and cold-atom realizations

Field | Value  
---|---  
name_short | Kitaev / SYK mention  
name_full | Kitaev's model (SYK-like random fermion model) and cold-atom realizations  
brief_description | The paper mentions Kitaev's model (random all-to-all four-fermion interactions, 'SYK' family) as a model designed to display maximal chaos and to be a close relative of random nonlocal spin models which could be implemented in multimode cavities; suggests periodically modulated fields or multispin couplings may help realize such dynamics and references recent cold-atom realization proposals.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Kitaev's SYK-like model (random four-fermion interactions) and related random nonlocal spin models (Sachdev–Ye type)  
black_hole_phenomena_targeted | fast scrambling and maximal Lyapunov exponent characteristic of black holes (candidate holographic dual behavior)  
simulation_paradigm | analog quantum simulation target (proposed future realization) and conceptual mapping to multimode cavity or cold-atom architectures rather than implemented here  
quantum_hardware_platform | proposed platforms mentioned: multimode optical cavities (random nonlocal spin models), cold-atom proposals (cited Danshita et al.), possibly trapped ions/other platforms for multispin couplings  
encoding_and_mapping | Not detailed in this paper; suggested that random four-fermion interactions are relatives of random nonlocal spin models in multimode cavities and that periodic modulation could simulate multispin couplings or melt glass order to promote scrambling.  
algorithm_or_protocol | Not implemented here; paper suggests periodically modulating external fields or interactions, or engineering multimode couplings, to emulate SYK-like randomness and multispin interactions; does not specify explicit quantum algorithms.  
resource_estimates | No quantitative resource estimates provided for realizing SYK / Kitaev models in hardware in this work; authors state realizing such a model is 'highly nontrivial' and present it as an outlook item.  
noise_and_error_mitigation | Not discussed in detail for SYK realization in this paper; general experimental noise considerations (cavity decay, spontaneous emission) would apply in any proposed implementation.  
key_results_or_demonstrations | Only a conceptual mention and motivation: that Kitaev's model is a target because it is known to have black-hole-like scrambling; the paper does not demonstrate or simulate SYK dynamically.  
validation_and_benchmarks | No direct validation in this paper; authors point to other works (Kitaev's talk, recent cold-atom proposals) as directions to pursue.  
claimed_feasibility | Authors state realizing a model known to have the scrambling properties of a black hole remains highly nontrivial; indicate possible routes (multimode cavities, periodic modulation) but no concrete near-term feasibility claim.  
limitations_and_open_problems | Major open problem: experimental realization of SYK/Kitaev-type Hamiltonians (random four-body interactions) with controlled randomness and coupling strengths; difficulty in mapping fermionic four-body couplings to accessible atomic/cavity interactions; verification of holographic duality remains open.  
complexity_or_hardness_arguments | No explicit complexity-theoretic discussion here; connection to strong chaos and conjectured universality (maximal Lyapunov exponent) is emphasized.  
theory_context_keywords | Kitaev model, SYK, random four-fermion interactions, fast scrambling, holographic duality, multimode cavity spin glasses, Sachdev–Ye  
citations_to_prior_work | References cited: Kitaev (talk) [58]; Sachdev & Ye (random spin/fermion models) [50]; multimode cavity spin-glass proposals (Gopalakrishnan et al. [20], Strack & Sachdev [21]); cold-atom realization proposal (Danshita, Hanada & Tezuka [60]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-swingle-2026-08-13}`.
[code] 
    @misc{ast-ext-swingle-2026-08-13,
      title        = {Extraction: Measuring the scrambling of quantum information},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-measuring-the-scrambling-of-quantum-information.md},
      crossref     = {swingle2016measuring},
      note         = {Theorizer's extraction from \cite{swingle2016measuring}. asta-artifact id: extraction-result-94},
    }
    
    @article{swingle2016measuring,
      title     = {Measuring the scrambling of quantum information},
      author    = {Brian Swingle and Gregory S. Bentsen and M. Schleier-Smith and P. Hayden},
      year      = {2016},
      url       = {https://www.semanticscholar.org/paper/34365945},
    }
[/code]
