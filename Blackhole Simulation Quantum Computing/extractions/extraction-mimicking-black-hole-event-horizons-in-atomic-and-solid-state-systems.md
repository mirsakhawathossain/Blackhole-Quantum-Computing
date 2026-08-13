[<- All artifacts](<../index.md>)

# Extraction: Mimicking black hole event horizons in atomic and solid-state systems

**Contents:**

  * Sachdev-Ye-Kitaev model
  * Digital quantum simulation algorithm for SYK/cSYK
  * cSYK realization with ultracold gases (Danshita, Hanada, Tezuka)
  * cSYK realization in an irregular graphene flake (Landau-level platform)
  * SYK with semiconductor quantum wires coupled to a disordered quantum dot
  * SYK realization in Fu–Kane superconductor (TI surface proximitized by superconductor with irregular hole trapping vortices)
  * Protocols to measure out-of-time-order correlators (OTOCs) and scrambling



### Sachdev-Ye-Kitaev model

Field | Value  
---|---  
name_short | SYK  
name_full | Sachdev-Ye-Kitaev model  
brief_description | A zero-dimensional quantum many-body model of N Majorana fermions with random all-to-all quartic interactions (or its complex-fermion variant cSYK) that in the large-N, low-energy limit displays emergent conformal symmetry, maximal scrambling, and is holographically dual to nearly-AdS2 black holes.  
citation_title |   
mention_or_use | use  
target_system_or_model | SYK / cSYK quantum mechanical model (dual to nearly-AdS2 black hole)  
black_hole_phenomena_targeted | Fast scrambling / many-body quantum chaos (OTOC and maximal Lyapunov exponent), black-hole thermodynamics as encoded in low-energy Schwarzian action, emergent near-horizon (AdS2) dynamics  
simulation_paradigm | Both analog realizations (engineered condensed-matter / cold-atom systems realizing the Hamiltonian) and digital quantum simulation (gate-based) are discussed; primarily analog/emergent realization proposals are analyzed in detail.  
quantum_hardware_platform | platform-agnostic review but concrete proposals target: ultracold atoms in optical lattices, graphene flakes (2D electrons in Landau level), proximitized semiconductor quantum wires coupled to a disordered quantum dot, Fu–Kane topological-insulator surface with superconducting film (solid-state platforms); digital-algorithm proposals assume gate-based quantum computers (superconducting qubits / generic)  
encoding_and_mapping | Not a qubit mapping per se in the analog proposals; mappings are physical: (i) cSYK from cold atoms by integrating out photo-associated molecular states to generate effective four-fermion J_{ij;kl} (Eq. 4.3 → 4.4); (ii) cSYK in graphene: electrons restricted to the n=0 Landau level (kinetic energy quenched) with disorder-provided random wavefunctions, Coulomb matrix elements supply J_{ij;kl}; (iii) SYK from Majorana platforms: Majorana zero modes delocalized into a disordered dot (wires+dot) or trapped vortices in Fu–Kane hole, interactions produce J_{ijkl}; no Jordan-Wigner/Bravyi-Kitaev qubit encoding is given for digital schemes in this review.  
algorithm_or_protocol | For analog proposals: engineer Hamiltonian directly via interactions (photo-association, Coulomb interactions, proximity-induced superconductivity). For digital mention: a digital quantum simulation algorithm for SYK/cSYK is cited (Ref. [62]) and OTOC-measurement protocols (Ref. [69]) are discussed; backward time evolution by sign flip of effective Hamiltonian is described for cold-atom OTOC protocol (flip detuning of PA lasers).  
resource_estimates | Qualitative / order-of-magnitude statements only: cold-atom proposal notes requirement n_ms (number of molecular states) × N(N-1)/2 PA lasers — becomes very large for sizable N; numerical observation that N ≳ 10 required to see characteristic spectral signatures; requirement K ≪ J (hybridization scale K versus interaction scale J) to have a wide SYK window (crossover energy E_c ≈ K^2 / J). No explicit qubit counts, gate depths, T-gate counts, or measurement-shot budgets for digital algorithms are provided in this review.  
noise_and_error_mitigation | Discussion is qualitative: for analog proposals main error sources are unwanted bilinear hybridization terms H_2 = i Σ K_{ij} χ_i χ_j (must be suppressed), disorder control and reproducibility, and difficulty of implementing backward time evolution for OTOCs; for digital proposals the review only cites existence of algorithms and experimental first steps but does not present explicit noise models or mitigation protocols.  
key_results_or_demonstrations | This is a review/proposal-level work: it (i) summarizes theoretical large-N SYK analytic results (conformal propagator, spectral A(ω) ~ 1/√(J|ω|), maximal Lyapunov exponent λ_L=2π/β, Schwarzian low-energy action), (ii) surveys and analyzes multiple concrete experimental proposals to realize SYK/cSYK (cold atoms, graphene flake, semiconductor wires+dot, Fu–Kane TI surface), (iii) highlights challenges and measurable observables (spectroscopy, tunneling DOS, two-terminal conductance, compressibility, and OTOCs). No new experimental data is presented here.  
validation_and_benchmarks | Validation methods discussed: theoretical comparison to large-N analytic solution and conformal limit predictions (spectral function, OTOC exponential growth and λ_L), numerical simulations cited in specific proposals (e.g., random wavefunction simulations for graphene [72]), and suggested experimental probes (STM spectral function to compare against A(ω) ∝ 1/√|ω| and transport measurements). For OTOC measurement proposals the review points to previously developed measurement protocols and first experimental steps (Refs. [69–71]).  
claimed_feasibility | Authors judge analog realizations promising but challenging: cSYK (complex-fermion) implementations may be easier than Majorana SYK because charged fermions are simpler to probe; they state N ≳ 10 needed to see spectroscopic features, but many proposals face practical bottlenecks (number of PA lasers, controlling hybridization K, fabricating many-wire arrays, reproducibility). Measuring OTOCs is called a 'huge challenge' in atomic setups and unsolved for solid-state realizations; some regimes may be accessible on near-term devices for spectral/transport signatures but full holographic diagnostics (OTOCs, thermofield double state preparation) likely require more advanced control.  
limitations_and_open_problems | Explicit limitations listed: (i) unwanted bilinear hybridization H_2 is a relevant perturbation and tends to destroy SYK low-energy fixed point unless K ≪ J; (ii) ensuring sufficiently random Gaussian-distributed J_{ijkl} is nontrivial and often requires many degrees of freedom (e.g., many molecular states in cold-atom proposals) or engineered disorder; (iii) practical resource challenges (large number of lasers, device fabrication complexity, scalability to large N); (iv) measurement difficulty for OTOCs and time-reversal evolution; (v) finite-N effects and finite temperature/frequency windows limit access to conformal SYK regime; (vi) analog platforms lack dynamical spacetime — they realize matter side of holography, not dynamical gravity.  
complexity_or_hardness_arguments | No explicit computational complexity-theoretic hardness proofs are provided in this review. The paper emphasizes physical/thermodynamic universality (fast scrambling bound λ_L ≤ 2π/β saturated by SYK) rather than complexity-theoretic statements about simulation hardness.  
theory_context_keywords | AdS/CFT, holographic duality, Sachdev-Ye-Kitaev (SYK), cSYK, Schwarzian action, nearly-AdS2 gravity, fast scrambling, Lyapunov bound, conformal reparametrization symmetry, emergent quantum black hole  
citations_to_prior_work | Key references cited in context: large-N SYK theory and chaos: Kitaev [7], Maldacena & Stanford [8]; digital quantum simulation algorithm: L. García-Álvarez et al., "Digital quantum simulation of minimal AdS/CFT" (Ref. [62]); early experimental quantum-simulator steps: Z. Luo et al., "Observing Fermion Pair Instability of the Sachdev-Ye-Kitaev Model on a Quantum Spin Simulator" (Ref. [63]); OTOC measurement protocol: B. Swingle et al., "Measuring the scrambling of quantum information" (Ref. [69]); cold-atom proposals: I. Danshita, M. Hanada, M. Tezuka, "Creating and probing the sachdevyekitaev model with ultracold gases: Towards experimental studies of quantum gravity" and "How to make a quantum black hole with ultra-cold gases" (Refs. [67,68]); graphene proposal: A. Chen et al., "Quantum holography in a graphene flake with an irregular boundary" (Ref. [72]); Majorana wires proposal: A. Chew, A. Essin, J. Alicea, "Approximating the sachdev-ye-kitaev model with majorana wires" (Ref. [80]); Fu–Kane / TI proposal: D. I. Pikulin and M. Franz, "Black hole on a chip: Proposal for a physical realization of the sachdev-ye-kitaev model in a solid-state system" (Ref. [82]).  
  
### Digital quantum simulation algorithm for SYK/cSYK

Field | Value  
---|---  
name_short | Digital-QS-for-SYK  
name_full | Digital quantum simulation algorithm for SYK/cSYK  
brief_description | A gate-based (digital) quantum simulation algorithm proposed to simulate SYK and cSYK Hamiltonians on a quantum computer; cited as a pathway to simulate minimal AdS/CFT dynamics on quantum hardware.  
citation_title | Digital quantum simulation of minimal AdS/CFT  
mention_or_use | mention  
target_system_or_model | SYK / cSYK Hamiltonians (quantum many-body models dual to nearly-AdS2 black holes)  
black_hole_phenomena_targeted | Access to holographic observables such as dynamics related to AdS2/CFT1 correspondence, scrambling and OTOC behavior  
simulation_paradigm | Digital gate-based quantum simulation (mentioned; actual algorithm details are not given in this review)  
quantum_hardware_platform | assumed gate-based quantum computers (platform-agnostic in the review)  
encoding_and_mapping | Not detailed in the review; reference to an algorithmic proposal is made but mapping specifics (fermion-to-qubit transforms, locality, or truncation) are not described in this paper.  
algorithm_or_protocol | Cited as a digital algorithmic route; review does not provide explicit method steps (Trotterization / LCU / qubitization etc. are not spelled out here).  
resource_estimates | No resource numbers (qubit counts, gate depths, measurement budgets) are provided in the review — only the existence of a digital algorithm is cited.  
noise_and_error_mitigation | Not discussed in this review in the context of the specific digital algorithm.  
key_results_or_demonstrations | This review simply cites the existence of a digital-simulation algorithm (Ref. [62]) and notes first experimental steps reported in Ref. [63]; no digital-simulation results are presented here.  
validation_and_benchmarks | Not provided in this review for the digital algorithm — the paper points readers to the cited algorithm paper and first experimental implementations for details.  
claimed_feasibility | Mentioned as an alternate route (digital) to access SYK physics; feasibility and resource demands are not analyzed here.  
limitations_and_open_problems | Review does not spell out algorithmic limitations; general challenges implicit: requirement of enough qubits and gate fidelity to simulate many-body dynamics and to measure OTOCs.  
complexity_or_hardness_arguments | No explicit complexity claims in the review for the digital algorithm.  
theory_context_keywords | AdS/CFT, minimal AdS/CFT digital simulation, SYK  
citations_to_prior_work | Primary citation given: L. García-Álvarez et al., "Digital quantum simulation of minimal AdS/CFT" (Ref. [62]); experimental steps: Z. Luo et al., "Observing Fermion Pair Instability of the Sachdev-Ye-Kitaev Model on a Quantum Spin Simulator" (Ref. [63]).  
  
### cSYK realization with ultracold gases (Danshita, Hanada, Tezuka)

Field | Value  
---|---  
name_short | Cold-atom cSYK  
name_full | cSYK realization with ultracold gases (Danshita, Hanada, Tezuka)  
brief_description | Proposal to realize the complex SYK model using ultracold fermionic atoms in deep optical-lattice wells with photo-association to molecular states; integrating out molecular states generates effective four-fermion couplings J_{ij;kl}.  
citation_title | Creating and probing the sachdevyekitaev model with ultracold gases: Towards experimental studies of quantum gravity  
mention_or_use | use  
target_system_or_model | cSYK (complex-fermion Sachdev-Ye-Kitaev model)  
black_hole_phenomena_targeted | Scrambling / OTOC dynamics (protocol for measuring OTOC described), spectroscopic signatures related to SYK non-Fermi-liquid spectral function  
simulation_paradigm | Analog quantum simulation (engineer effective Hamiltonian via controlled atom–molecule coupling and detunings); with an added prescription to implement backward time evolution by flipping sign of molecular detunings.  
quantum_hardware_platform | Ultracold fermionic atoms in optical-lattice wells with photo-association lasers (platform: neutral atoms)  
encoding_and_mapping | Physical mapping: N localized atomic single-particle states per well, Q atoms filling; molecular states m_s coupled via PA lasers to atomic pairs with amplitudes g_{s,ij}; integrating out molecules perturbatively yields effective J_{ij;kl} = Σ_s g_{s,ij} g_{s,kl} / ν_s (Eq. 4.4). No qubit encoding; degrees of freedom are physical fermionic atomic modes.  
algorithm_or_protocol | Prepare atomic ensemble in deep wells; use PA lasers to mediate pairwise interactions; measure spectral and transport observables; OTOC protocol involves coupling to a control qubit, conditionally annihilating atoms, and enacting forward/backward evolution by detuning flips to change sign of Hamiltonian.  
resource_estimates | Quantitative warning: number of required PA lasers scales as n_{ms} × N(N-1)/2 (potentially very large); authors note N ≳ 10 required to see spectroscopic SYK signatures; no specific runtimes or shot counts provided.  
noise_and_error_mitigation | Practical challenges discussed: need for precise control of PA laser frequencies/intensities, difficulty of implementing many distinct laser drives, and errors in implementing time-reversal via detuning flips; no explicit error-mitigation protocols quantified.  
key_results_or_demonstrations | Proposal-level: derivation of effective cSYK Hamiltonian via integrating out molecular states (Eq. 4.3 → 4.4); proposed protocol to measure OTOCs using a control qubit and sign-flip of detunings; assessment that experimental resources (laser count) may be a bottleneck. No experimental realization presented in this review.  
validation_and_benchmarks | Validation argument: central limit theorem leads to approximately Gaussian-distributed J_{ij;kl} if the number of molecular states n_{ms} ≫ 1 and g_{s,ij}, ν_s treated as random; spectroscopic signatures compared to theoretical SYK predictions (need N ≳ 10).  
claimed_feasibility | Authors consider the approach viable in principle but highlight significant experimental bottlenecks (very large number of PA lasers, precise detuning control); measuring OTOCs is challenging but protocols exist in the literature.  
limitations_and_open_problems | Large experimental overhead for many molecular states, difficulty achieving Gaussian Js for small n_{ms}, precise laser control and detuning flips for time reversal, and experimental difficulty measuring OTOCs in analog cold-atom settings.  
complexity_or_hardness_arguments | No complexity-theoretic claims are made in the review for this analog proposal.  
theory_context_keywords | cSYK, photo-association, central limit for random couplings, OTOC measurement protocol  
citations_to_prior_work | Primary citations: I. Danshita, M. Hanada, M. Tezuka (Refs. [67,68]) for the cold-atom cSYK proposals; OTOC measurement protocol: B. Swingle et al., "Measuring the scrambling of quantum information" (Ref. [69]).  
  
### cSYK realization in an irregular graphene flake (Landau-level platform)

Field | Value  
---|---  
name_short | Graphene cSYK  
name_full | cSYK realization in an irregular graphene flake (Landau-level platform)  
brief_description | Proposal to realize cSYK physics using electrons confined to the n=0 Landau level (LL0) of a graphene flake with an irregular boundary; chiral-symmetry-protected degeneracy produces quenching of kinetic energy and Coulomb interactions between spatially random LL0 wavefunctions produce random all-to-all J_{ij;kl}.  
citation_title | Quantum holography in a graphene flake with an irregular boundary  
mention_or_use | use  
target_system_or_model | cSYK realized by interacting electrons projected to LL0 in graphene  
black_hole_phenomena_targeted | Spectroscopic/transport signatures of SYK non-Fermi-liquid physics (spectral function A(ω) ~ 1/√(J|ω|)), potential connections to holographic entropy and scrambling behavior though OTOC measurement is not solved in this solid-state context  
simulation_paradigm | Analog condensed-matter realization by engineering disorder and strong magnetic field to produce degenerate LL0 and random interactions  
quantum_hardware_platform | Solid-state graphene flake in strong magnetic field, irregular boundary to produce chiral-symmetric disorder (platform: 2D electron system)  
encoding_and_mapping | Physical mapping: project electron degrees of freedom onto LL0 manifold; disorder-respecting chiral symmetry preserves exact degeneracy while producing random spatial wavefunctions Φ_j(r); screened Coulomb matrix elements between these LL0 orbitals produce J_{ij;kl}. No qubit encoding discussed.  
algorithm_or_protocol | Device fabrication: make an irregular-shaped graphene flake, apply strong magnetic field to isolate LL0, probe with scanning tunneling spectroscopy (STM), transport (two-terminal conductance), and compressibility measurements to detect SYK signatures. No OTOC measurement protocol for solid-state variant is provided.  
resource_estimates | No explicit resource counts; practicality depends on fabricating suitably irregular flakes and achieving strong magnetic fields; the review emphasizes that LL0 degeneracy protection helps avoid reintroduction of H_2 kinetic terms.  
noise_and_error_mitigation | Main challenges are disorder control and reproducibility; the proposal relies on chiral-symmetric disorder to preserve LL0 degeneracy, but experimental realization must ensure disorder respects that symmetry; no quantum error mitigation protocols are discussed.  
key_results_or_demonstrations | Proposal-level plus numerical simulations cited showing wavefunctions of LL0 have random spatial structure and that Coulomb matrix elements can produce effectively random J; predicted measurable signatures: inverse-square-root divergence in spectral function and non-Fermi-liquid transport signatures.  
validation_and_benchmarks | Validation arguments provided via Aharonov-Casher protection of LL0 degeneracy and numerical simulations (cited) that compute random-like LL0 wavefunctions and the resulting interaction matrix elements; comparison of predicted spectral function to SYK conformal result is proposed as experimental benchmark.  
claimed_feasibility | Authors view this as promising for spectroscopic probes (STM) and transport, but note inability (so far) to measure OTOCs in this setting; practical feasibility depends on fabrication and achieving chiral-symmetric disorder without LL broadening.  
limitations_and_open_problems | Open problems: how to measure OTOCs in solid-state SYK realizations; ensuring disorder both randomizing wavefunctions and preserving LL0 degeneracy; finite-size and edge effects; proving effective Js are Gaussian at relevant N.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | Landau level projection, Aharonov–Casher protection, cSYK, scanning tunneling spectroscopy signature A(ω)∝1/√|ω|  
citations_to_prior_work | Primary citation: A. Chen et al., "Quantum holography in a graphene flake with an irregular boundary" (Ref. [72]); foundational Landau/quantum-Hall refs: Aharonov & Casher (Ref. [77]).  
  
### SYK with semiconductor quantum wires coupled to a disordered quantum dot

Field | Value  
---|---  
name_short | Wires+Dot SYK  
name_full | SYK with semiconductor quantum wires coupled to a disordered quantum dot  
brief_description | Proposal to engineer the SYK Hamiltonian by coupling many proximitized semiconductor nanowires (each hosting a Majorana zero mode) to a common disordered quantum dot so Majorana modes delocalize into the dot and interactions generate random all-to-all J_{ijkl}.  
citation_title | Approximating the sachdev-ye-kitaev model with majorana wires  
mention_or_use | use  
target_system_or_model | SYK model realized from Majorana zero modes hybridized into a disordered quantum dot  
black_hole_phenomena_targeted | SYK low-energy non-Fermi-liquid behavior and scrambling (OTOC) characteristic of holographic dual black hole; spectral/thermodynamic probes envisaged  
simulation_paradigm | Analog solid-state engineering of effective SYK Hamiltonian via delocalization and Coulomb interactions  
quantum_hardware_platform | Proximitized semiconductor nanowires (e.g., InSb with Al superconductor) arrayed and coupled to a disordered 2D quantum dot (solid-state Majorana platform)  
encoding_and_mapping | Physical mapping: each wire contributes a Majorana zero mode whose wavefunction penetrates the dot; overlaps and local interactions in the dot produce effective random four-Majorana interaction matrix elements J_{ijkl}; approximate artificial time-reversal symmetry ̃T suppresses bilinear hybridization K_{ab}.  
algorithm_or_protocol | Device fabrication: assemble many Majorana wires coupled to a common disordered dot; tune parameters to preserve approximate ̃T symmetry and to keep hybridization K small; measure spectral and transport properties to infer SYK signatures.  
resource_estimates | No explicit counts; practical requirements include assembling a large number of wires (N large) and ensuring the dot level spacing and coupling produce a protected zero-mode manifold separated from other levels (ε ≈ N δε_typ/π). No gate/circuit-resource estimates (analog platform).  
noise_and_error_mitigation | Practical issues discussed: approximate symmetry ̃T may reduce bilinear terms but is not exact (thus K nonzero); protection via level repulsion in random-matrix sense helps isolate zero-mode manifold; no dedicated quantum error mitigation schemes as this is analog hardware.  
key_results_or_demonstrations | Proposal-level analysis showing (i) delocalization into dot yields all-to-all interactions, (ii) approximate symmetry suppresses bilinears, (iii) random-matrix arguments indicate zero-mode manifold separation from dot levels; no experimental realization presented in this review.  
validation_and_benchmarks | Validation arguments are theoretical: random-matrix theory, model calculations showing level separation and suppression of bilinears, and connection to SYK effective action; suggested benchmarking via spectroscopy and thermodynamics compared to SYK predictions.  
claimed_feasibility | Authors view this as attractive because Majorana zero modes are routinely observed in wires, but assembling many wires and controlling couplings remains a substantial engineering challenge; practical feasibility uncertain but plausible with community progress.  
limitations_and_open_problems | Limitations: approximate symmetry only (bilinears suppressed but not eliminated), need to assemble many wires and control couplings, hybridization with dot levels, finite-N effects, and difficulty measuring OTOCs in solid-state systems.  
complexity_or_hardness_arguments | None provided in the review.  
theory_context_keywords | Majorana zero modes, proximitized nanowires, random-matrix protection, SYK  
citations_to_prior_work | Primary citation: A. Chew, A. Essin, J. Alicea, "Approximating the sachdev-ye-kitaev model with majorana wires" (Ref. [80]); Majorana experimental refs [24–29] are cited as background.  
  
### SYK realization in Fu–Kane superconductor (TI surface proximitized by superconductor with irregular hole trapping vortices)

Field | Value  
---|---  
name_short | Fu-Kane SYK  
name_full | SYK realization in Fu–Kane superconductor (TI surface proximitized by superconductor with irregular hole trapping vortices)  
brief_description | Proposal to create many Majorana zero modes trapped in an irregular nanoscale hole in a superconducting film on the surface of a 3D topological insulator; tuning chemical potential to neutrality forbids bilinears and interactions produce SYK-like four-fermion couplings.  
citation_title | Black hole on a chip: Proposal for a physical realization of the sachdev-ye-kitaev model in a solid-state system  
mention_or_use | use  
target_system_or_model | SYK model built from Majorana vortex zero modes on a Fu–Kane proximitized TI surface  
black_hole_phenomena_targeted | SYK low-energy dynamics and associated holographic signatures (spectral properties, scrambling) as analogs of nearly-AdS2 black hole physics  
simulation_paradigm | Analog solid-state engineering: trap many vortices (hence many Majorana zero modes) in a hole in superconducting film on TI surface; tune chemical potential μ to Dirac point to enforce symmetry forbidding bilinears  
quantum_hardware_platform | Topological insulator surface proximitized by a thin superconducting film (Fu–Kane superconductor); vortices trapped in engineered hole (solid-state Majorana platform)  
encoding_and_mapping | Physical mapping: each vortex binds a Majorana zero mode; when μ tuned to neutrality an extra symmetry eliminates bilinears and screened Coulomb interactions among underlying electrons generate random four-Majorana couplings J_{ijkl}; irregular hole geometry randomizes wavefunctions.  
algorithm_or_protocol | Device fabrication: make a superconducting film on TI, fabricate an irregular hole to pin multiple vortices, tune μ to neutrality point, probe with spectroscopy (e.g., STM) and transport to detect SYK signatures.  
resource_estimates | No explicit numerical resource counts; feasibility depends on ability to produce many vortices in same hole and on material control of TI/superconductor heterostructure; no qubit/gate resource estimates (analog device).  
noise_and_error_mitigation | Main experimental challenges: current limited experimental characterization of Majorana modes in Fu–Kane platforms, reproducibility, and tuning μ precisely to neutrality; no quantum error-correction strategies discussed.  
key_results_or_demonstrations | Proposal-level: combination of analytical and numerical evidence that an irregular hole traps multiple Majorana modes whose wavefunctions become random and Coulomb interactions generate random J_{ijkl}; bilinear terms can be controlled by tuning μ to Dirac point; no experimental realization shown in this review.  
validation_and_benchmarks | Validation arguments: symmetry-based exclusion of bilinears at μ = neutrality, numerical simulations demonstrating random wavefunctions and effective J statistics, and proposed spectroscopic probes to compare to SYK theoretical expectations.  
claimed_feasibility | Authors consider it promising once Fu–Kane Majorana physics is better experimentally established; advantage: bilinears can be suppressed by tuning μ, offering a cleaner knob than approximate symmetry in wire proposal. However, current experimental evidence is limited and reproducibility a concern.  
limitations_and_open_problems | Open issues: experimental replication of Majorana signatures in Fu–Kane systems, control of chemical potential, fabrication of holes that trap many vortices, measuring OTOCs in solid-state setups, finite-N constraints.  
complexity_or_hardness_arguments | None provided.  
theory_context_keywords | Fu–Kane superconductor, Majorana vortices, chemical potential neutrality, SYK  
citations_to_prior_work | Primary citation: D. I. Pikulin and M. Franz, "Black hole on a chip: Proposal for a physical realization of the sachdev-ye-kitaev model in a solid-state system" (Ref. [82]); background on Fu–Kane Majorana vortices: L. Fu & C. L. Kane (Ref. [81]).  
  
### Protocols to measure out-of-time-order correlators (OTOCs) and scrambling

Field | Value  
---|---  
name_short | OTOC-Protocols  
name_full | Protocols to measure out-of-time-order correlators (OTOCs) and scrambling  
brief_description | Measurement protocols for probing scrambling and quantum Lyapunov exponent via out-of-time-order correlators; review cites standard protocols involving coupling to a control qubit, conditional operations, and forward/backward time evolution (time-reversal via sign flip of Hamiltonian).  
citation_title | Measuring the scrambling of quantum information  
mention_or_use | mention  
target_system_or_model | OTOC measurement for SYK/cSYK (general many-body systems exhibiting scrambling)  
black_hole_phenomena_targeted | Scrambling quantified by OTOC C(t) and extraction of quantum Lyapunov exponent λ_L; identification of maximal chaos (λ_L = 2π/β) as black-hole-like behavior  
simulation_paradigm | Experimental measurement protocols applicable to both analog (cold atoms) and digital platforms; involve controlled ancilla qubit, conditional manipulations, and forward/backward Hamiltonian evolution  
quantum_hardware_platform | Platform-agnostic protocols cited; implementations referenced for trapped ions and NMR quantum simulators (Refs. [70,71])  
encoding_and_mapping | Protocols require the ability to perform conditional operations on system degrees of freedom controlled by an ancilla and to enact Hamiltonian sign reversal for backward evolution; mapping specifics depend on platform and are not detailed in the review.  
algorithm_or_protocol | General steps: couple system to control qubit, apply perturbation V(0) conditionally, evolve forward then backward in time (backward via sign flip of Hamiltonian), perform measurements to reconstruct OTOC; for cold atoms backward evolution proposed by flipping detuning of PA lasers.  
resource_estimates | No quantitative resource estimates in the review; practical implementations cited (Refs. [70,71]) give platform-specific experimental costs but are not detailed here.  
noise_and_error_mitigation | Challenges noted: time-reversal fidelity (requiring precise sign flips), decoherence of control qubit and system during long evolutions, and experimental noise in conditional operations; no explicit mitigation recipes given in the review besides pointing to experimental implementations.  
key_results_or_demonstrations | Review points to prior protocols (Ref. [69]) and experimental demonstrations of OTOC measurement in trapped ions and NMR (Refs. [70,71]). In the context of SYK proposals the review describes how the cold-atom proposal could implement such a protocol (flip PA laser detunings for time reversal) but states OTOC measurement in solid-state realizations remains unsolved.  
validation_and_benchmarks | Benchmarking OTOC measurements in prior experiments was done by comparing measured multi-time correlations to theoretical expectations; review suggests similar benchmarking would be required for SYK realizations but provides no new benchmarks.  
claimed_feasibility | OTOC measurement is feasible in atomic quantum-simulator platforms (some experimental progress cited), but remains extremely challenging for analog solid-state SYK proposals according to the authors.  
limitations_and_open_problems | Key limitations: implementing precise backward time evolution, coupling ancilla qubit without disturbing many-body dynamics, scalability to larger N, and decoherence during required evolutions.  
complexity_or_hardness_arguments | None provided in the review beyond noting experimental difficulty.  
theory_context_keywords | OTOC, scrambling, quantum Lyapunov exponent, time-reversal evolution, ancilla-based measurement  
citations_to_prior_work | Primary citations: B. Swingle et al., "Measuring the scrambling of quantum information" (Ref. [69]); experimental implementations: M. Gärttner et al., "Measuring out-of-time-order correlations and multiple quantum spectra in a trapped-ion quantum magnet" (Ref. [70]); J. Li et al., "Measuring out-of-time-order correlators on a nuclear magnetic resonance quantum simulator" (Ref. [71]).  
  
## Citation

Cite this artifact as `\cite{ast-ext-franz-2026-08-13}`.
[code] 
    @misc{ast-ext-franz-2026-08-13,
      title        = {Extraction: Mimicking black hole event horizons in atomic and solid-state systems},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-mimicking-black-hole-event-horizons-in-atomic-and-solid-state-systems.md},
      crossref     = {franz2018mimicking},
      note         = {Theorizer's extraction from \cite{franz2018mimicking}. asta-artifact id: extraction-result-41},
    }
    
    @article{franz2018mimicking,
      title     = {Mimicking black hole event horizons in atomic and solid-state systems},
      author    = {M. Franz and M. Rozali},
      year      = {2018},
      journal   = {Nature Reviews Materials},
      url       = {https://www.semanticscholar.org/paper/119189958},
    }
[/code]
