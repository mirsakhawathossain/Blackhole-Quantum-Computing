[<- All artifacts](<../index.md>)

# Extraction: Quantum Holography in a Graphene Flake with an Irregular Boundary.

**Contents:**

  * Mesoscopic graphene flake realization of the complex-fermion Sachdev-Ye-Kitaev (SY) model
  * Sachdev-Ye-Kitaev (complex-fermion) model / Sachdev-Ye model
  * Holographic duality between SYK and two-dimensional (1+1D) dilaton gravity in AdS2 — extremal black hole



### Mesoscopic graphene flake realization of the complex-fermion Sachdev-Ye-Kitaev (SY) model

Field | Value  
---|---  
name_short | Graphene-flake SYK realization  
name_full | Mesoscopic graphene flake realization of the complex-fermion Sachdev-Ye-Kitaev (SY) model  
brief_description | Proposal and numerical study showing that electrons confined to the n=0 Landau level (LL_0) of a small, irregular graphene flake in a strong perpendicular magnetic field realize a complex-fermion SYK (Sachdev-Ye) Hamiltonian via Coulomb-projected random all-to-all four-fermion interactions; this many-body state is argued to be holographically dual to an extremal AdS2 black hole.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Complex-fermion Sachdev-Ye-Kitaev (SYK/SY) model realized by projecting Coulomb interactions onto degenerate LL_0 zero modes in an irregular graphene flake (N fermionic zero modes).  
black_hole_phenomena_targeted | Black-hole-like holographic properties of the SYK model: extensive ground-state entropy (in large-N limit), emergent conformal symmetry at low energy, and maximal chaos / fast scrambling (Lyapunov exponent saturating the bound) — i.e., properties characteristic of an extremal AdS2 black hole.  
simulation_paradigm | Analog condensed-matter quantum simulation (solid-state realization of the SY model); the paper is a materials/experimental proposal and numerical many-body simulation, not a gate-based quantum-computation protocol.  
quantum_hardware_platform | Solid-state electrons in a mesoscopic graphene flake (platform-agnostic with respect to quantum-computing hardware; specifically a graphene device under strong perpendicular magnetic field).  
encoding_and_mapping | Mapping occurs physically: the single-particle zero modes of LL_0 (protected by chiral symmetry / Aharonov–Casher index theorem, N ≃ N_Φ = SB/Φ_0) provide N fermionic orbitals; projecting the screened Coulomb interaction onto these zero-mode orbitals yields random antisymmetrized four-fermion couplings J_{ij;kl} (Eq. (4)); small chiral-symmetry-breaking perturbations produce bilinear terms H_2 = ∑ _{ij} K_ c_i^† c_j which must be suppressed (K ≪ J). Boundary irregularity provides random spatial structure of LL_0 wavefunctions that produces random all-to-all J couplings. Charge sectors (total Q) and particle-number sectors are used in level-statistics analysis.  
algorithm_or_protocol | Experimental protocol and theoretical/numerical procedures: (1) fabricate an irregular-shaped graphene flake, apply strong B field to create degenerate LL_0, (2) partially fill spin-polarized LL_0 (exchange-enhanced Zeeman splitting), (3) project Coulomb interactions to LL_0 to obtain J_{ij;kl}, (4) numerically diagonalize the resultant many-body Hamiltonian for finite N to compute thermal entropy and many-body level statistics, (5) experimentally probe signatures by tunneling spectroscopy (dI/dV) expecting g(V) ∼ |V|^{-1/2} in SY regime. No gate-based quantum algorithms are used or proposed.  
resource_estimates | Device and physics parameter estimates provided: required LL_0 degeneracy N ≳ 10 to begin seeing SY spectral signatures; desirable N ≃ 100 for clear SY regime (classically intractable). Example: at B = 20 T, target N ≃ 100 corresponds to flake linear size L ≃ 150 nm (S = N Φ_0 / B). Estimated interaction scale J from coarse-grained analysis: J ≃ 25–34 meV (for B ≃ 20 T and plausible screening); exchange splitting estimate ΔE_C ≃ 8.8 meV/T (order tens of meV at high fields) helps spin polarize LL_0; disorder broadening parameter K estimated from second-neighbor hopping and on-site potential with numerical values K ~ few meV (numerically K ≃ 0.022 t' for t' second-neighbor hopping), condition for visible SY window: K ≪ J and frequency window 16√π K^2 / J < ω ≪ J. The paper notes N ≃ 100 is 'well beyond what one can conceivably simulate on a computer'.  
noise_and_error_mitigation | Not a gate-based QIP noise discussion; experimental 'error' sources are chiral-symmetry-breaking perturbations (second-neighbor hopping t', random on-site potential) that produce bilinear terms H_2 with strength K. Mitigation strategies: (i) preserve chiral symmetry as much as possible via clean interior and irregular boundary design, (ii) limit disorder density n_I and disorder strength w such that n_I w ≪ O(10 meV) (example bound n_I w ≪ 9 meV for parameters discussed), (iii) exploit exchange-enhanced spin splitting to work in a single spin sector. No standard quantum-error-correction techniques are discussed because this is an analog solid-state realization.  
key_results_or_demonstrations | This work is a concrete condensed-matter proposal supported by numerical simulations (tight-binding + projection + exact diagonalization) rather than a quantum-computing experiment. Key demonstrations: (1) tight-binding numerics show LL_0 remains sharp under irregular boundary and produces random zero-mode wavefunctions; (2) evaluation of Coulomb matrix elements J_{ij;kl} (Eq. (4)) yields zero-mean random complex couplings with variance matching SY scaling (Eq. (5)); (3) exact diagonalization for N up to 18 with computed J_{ij;kl} reproduces thermal entropy S(T) comparable to that of Gaussian-random-J SY model; (4) many-body level spacing statistics follow random-matrix theory predictions (GOE/GUE/GSE) depending on N (mod 4) and charge sector q, matching SY model expectations; (5) experimental signature predicted: tunneling differential conductance g(V)=dI/dV ∼ |V|^{-1/2} in SY regime. The work is therefore a proposal validated by numerics (simulation-only / theory + materials proposal).  
validation_and_benchmarks | Validation against known SY model behavior: (i) comparison of computed thermal entropy S(T) with that of a SY model with independent Gaussian J couplings, (ii) many-body level statistics r_n distributions compared to analytic random-matrix formula P(r) for GOE/GUE/GSE (Table I and Fig. 4), (iii) statistical analysis of computed J_{ij;kl} showing zero-mean and variance consistent with SY scaling, (iv) sensitivity studies of chiral-symmetry-breaking perturbations (t', random on-site potential) with numerical estimates of induced K broadening and shifts (Supplementary Figures S1, S2).  
claimed_feasibility | Authors claim experimental feasibility with existing fabrication techniques: device assembly is 'relatively straightforward' (no superconductivity required), and a regime with N ≳ 10 (signatures) to N ≃ 100 (clear SY regime) is achievable with small flakes (~100–200 nm) and high magnetic fields (~20 T), low temperatures, and careful suppression of disorder. No statements about NISQ vs fault-tolerant quantum computing are needed; the bottlenecks are material cleanliness, maintaining chiral symmetry to keep K ≪ J, and reaching sufficiently large N and low T.  
limitations_and_open_problems | Explicit limitations and open issues in the paper: (1) H_2 bilinear perturbations that break chiral symmetry are relevant and ultimately drive the ground state to a disordered Fermi liquid at T→0; only a finite-frequency/temperature SY crossover window exists if K ≪ J. (2) Finite-N effects: true extensive ground-state entropy appears only in large-N limit; for finite N entropy vanishes as T→0. (3) Crossover to bulk behavior in large flakes when boundary irregularity becomes unimportant is not addressed. (4) Proposal does not simulate dynamical spacetime or gravity directly—only the many-body SY system which is holographically dual to an AdS2 black hole. (5) Experimental requirements: high B, low T, clean flakes; measuring OTOCs (explicit scrambling diagnostics) is not demonstrated and would require additional protocols. (6) Verification beyond modest N may be hard because classical exact diagonalization becomes intractable for N ≳ O(30–40).  
complexity_or_hardness_arguments | The paper notes that N ≃ 100 is 'well beyond what one can conceivably simulate on a computer', implying classical intractability of the large-N many-body problem; however no formal complexity-theoretic classification (e.g., BQP/QMA-hard) is provided. The large-N SYK model is solvable in the analytic limit, but finite large-N many-body spectra require exponentially costly exact diagonalization.  
theory_context_keywords | SYK, Sachdev-Ye model, holographic duality, AdS2/dilaton gravity, extremal black hole, fast scrambling, maximal chaos, emergent conformal symmetry, random-matrix theory, level statistics (GOE/GUE/GSE), Aharonov–Casher zero modes, chiral symmetry, projected Coulomb interactions.  
citations_to_prior_work | Key references cited as foundations or closely related proposals: S. Sachdev and J. Ye (1993) original SY model; A. Kitaev (2015) SYK development/lectures; J. Maldacena and D. Stanford, Phys. Rev. D 94, 106002 (2016) (SYK–AdS2 gravity connections); Y.-Z. You, A. W. W. Ludwig, and C. Xu, Phys. Rev. B 95, 115150 (2017); D. I. Pikulin and M. Franz, Phys. Rev. X 7, 031006 (2017) and A. Chew, A. Essin, and J. Alicea, Phys. Rev. B 96, 121119 (2017) (earlier solid-state proposals targeting Majorana SYK); and other theoretical works on SYK properties and spectral statistics cited in the paper (refs. [2,3,4,5,6,19,20] in the manuscript).  
  
### Sachdev-Ye-Kitaev (complex-fermion) model / Sachdev-Ye model

Field | Value  
---|---  
name_short | SYK model (complex fermion)  
name_full | Sachdev-Ye-Kitaev (complex-fermion) model / Sachdev-Ye model  
brief_description | 0+1D model of N fermions with random all-to-all four-fermion interactions J_{ij;kl}, exhibiting emergent conformal symmetry at low energy, maximal chaos (saturating the Lyapunov bound), and a holographic dual to AdS2 dilaton gravity (extremal black hole).  
citation_title |   
mention_or_use | use  
target_system_or_model | SYK (complex fermion) many-body model used as the target holographic many-body system.  
black_hole_phenomena_targeted | Fast scrambling / maximal chaos, large ground-state entropy per fermion in large-N limit, low-energy conformal dynamics analogous to AdS2 black hole physics.  
simulation_paradigm | Target of an analog condensed-matter realization (graphene LL_0) rather than a digital quantum algorithm in this paper.  
quantum_hardware_platform | Not a gate-based platform in this paper; realized by electrons in graphene LL_0.  
encoding_and_mapping | Model parameters realized by projecting Coulomb interactions to random LL_0 orbitals → J_{ij;kl} matrix elements; antisymmetrization ensures correct fermionic exchange structure.  
algorithm_or_protocol | Analytic large-N solution of SYK commonly referenced; in this paper SYK properties are assessed numerically by exact diagonalization of the many-body Hamiltonian constructed from computed J_{ij;kl}.  
resource_estimates | Model scale: N (number of zero modes) is the main resource; paper identifies N ≳ 10 as minimal to see signatures and N ~100 as desirable (classical simulation infeasible).  
noise_and_error_mitigation | N/A for gate-model noise; physical requirement is to keep bilinear symmetry-breaking K ≪ J so SYK physics dominates at finite frequency/temperature.  
key_results_or_demonstrations | Used as the theoretical target: numerically reproduced SYK thermodynamics and level statistics for finite N using J_{ij;kl} obtained from graphene flake wavefunctions.  
validation_and_benchmarks | Comparison between graphene-derived J couplings and independent Gaussian-random-J SY model; level-statistics and thermal entropy benchmarks.  
claimed_feasibility | Paper claims SYK physics can be realized in mesoscopic graphene flakes with current materials technology and high magnetic fields.  
limitations_and_open_problems | Requires suppression of chiral-symmetry-breaking bilinear perturbations; finite-N and finite-temperature window only; no direct simulation of gravity degrees of freedom.  
complexity_or_hardness_arguments | Large finite-N many-body SYK spectra become classically intractable for N ≳ O(100) (practical classical hardness statement in manuscript).  
theory_context_keywords | SY/SYK, random all-to-all interactions, large-N limit, conformal regime, chaos/OTOC, AdS2 duality.  
citations_to_prior_work | Primary theory sources cited: S. Sachdev & J. Ye (1993), A. Kitaev (2015), J. Maldacena & D. Stanford (2016), and many subsequent SYK analyses (refs. in paper).  
  
### Holographic duality between SYK and two-dimensional (1+1D) dilaton gravity in AdS2 — extremal black hole

Field | Value  
---|---  
name_short | AdS2 / extremal black hole duality  
name_full | Holographic duality between SYK and two-dimensional (1+1D) dilaton gravity in AdS2 — extremal black hole  
brief_description | The low-energy large-N limit of the SYK model is argued to be dual to dilaton gravity in AdS2, with the SYK non-Fermi-liquid/chaotic behavior corresponding to properties of an extremal AdS2 black hole (e.g., entropy and maximal scrambling).  
citation_title |   
mention_or_use | mention  
target_system_or_model | AdS2 dilaton gravity / extremal black hole (the gravitational system to which the SYK model is holographically dual).  
black_hole_phenomena_targeted | Horizon thermodynamics (entropy), maximal Lyapunov exponent (fast scrambling), emergent conformal symmetry in near-horizon AdS2 region.  
simulation_paradigm | Not directly simulated; gravitational physics is accessed indirectly via realization/measurement of the dual SYK many-body state in graphene.  
quantum_hardware_platform | N/A (the gravitational model is not implemented on quantum hardware in this work).  
encoding_and_mapping | Holographic correspondence: SYK many-body dynamics ↔ AdS2 dilaton gravity; the paper relies on this duality conceptually to interpret SYK behavior as 'black-hole-like'.  
algorithm_or_protocol | No quantum algorithm — conceptual mapping via AdS/CFT-style duality (SYK ↔ AdS2 gravity).  
resource_estimates | N/A for gravitational system; realization requires achieving SYK regime in graphene (see graphene-flake SYK realization entry).  
noise_and_error_mitigation | N/A; limitations map to the fidelity of realizing the SYK Hamiltonian (control over J, suppression of K).  
key_results_or_demonstrations | Paper argues that observing SYK signatures in graphene corresponds to observing physical properties analogous to those of an extremal AdS2 black hole; no direct gravitational observables simulated.  
validation_and_benchmarks | Validation performed on the SYK side (entropy, level statistics); the AdS2 dual interpretation is invoked from literature (Maldacena & Stanford and others).  
claimed_feasibility | Feasibility claims apply to realizing the SYK side experimentally; interpretation as 'black-hole-like' follows if SYK behavior is observed. No claim of directly simulating dynamical spacetime.  
limitations_and_open_problems | The proposal does not simulate dynamical gravity or spacetime geometry; the duality is used as interpretive context only. Open theoretical questions include the nature of the crossover to bulk behavior in larger flakes and how to access genuine gravitational observables experimentally.  
complexity_or_hardness_arguments | N/A (no explicit complexity claims about simulating gravity are made).  
theory_context_keywords | Holographic duality, AdS2/dilaton gravity, extremal black hole, SYK/AdS2 correspondence, holographic interpretation.  
  
## Citation

Cite this artifact as `\cite{ast-ext-chen-2026-08-13}`.
[code] 
    @misc{ast-ext-chen-2026-08-13,
      title        = {Extraction: Quantum Holography in a Graphene Flake with an Irregular Boundary.},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-holography-in-a-graphene-flake-with-an-irregular-boundary.md},
      crossref     = {chen2018quantum},
      note         = {Theorizer's extraction from \cite{chen2018quantum}. asta-artifact id: extraction-result-96},
    }
    
    @article{chen2018quantum,
      title     = {Quantum Holography in a Graphene Flake with an Irregular Boundary.},
      author    = {Anffany Chen and R. Ilan and F. D. Juan and D. Pikulin and M. Franz},
      year      = {2018},
      journal   = {Physical Review Letters},
      url       = {https://www.semanticscholar.org/paper/51940526},
    }
[/code]
