[<- All artifacts](<../index.md>)

# Extraction: Mapping curved spacetimes into Dirac spinors

**Contents:**

  * Local phase mapping of 1+1D curved-spacetime Dirac equation to flat-spacetime Dirac spinor
  * Family of 1+1-dimensional traversable-wormhole spacetimes with shape function b(r) = b0^2 / r



### Local phase mapping of 1+1D curved-spacetime Dirac equation to flat-spacetime Dirac spinor

Field | Value  
---|---  
name_short | Phase-encoding mapping  
name_full | Local phase mapping of 1+1D curved-spacetime Dirac equation to flat-spacetime Dirac spinor  
brief_description | A technique that maps solutions of the massless Dirac equation in a static 1+1D curved spacetime into solutions of the free massless Dirac equation in flat spacetime via a local multiplicative phase psi = Omega^{-1/2} phi, thereby encoding the metric in that phase and producing an effective non-Hermitian potential V(x) = -i Omega'/2Omega.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime: massless Dirac fermion in 1+1 dimensions with conformal metric ds^2 = Omega^2(x)(dt^2 - dx^2) (static case, dot{Omega}=0).  
black_hole_phenomena_targeted | Black-hole-like curved-spacetime propagation phenomena — specifically traversable-wormhole traversal and associated distortions/focusing of a Dirac particle's probability density near the wormhole throat (i.e. horizon/throat-like behavior in 1+1 toy model).  
simulation_paradigm | Analog quantum simulation / platform-agnostic proposal: use existing quantum simulators of the free 1+1 massless Dirac equation (analog implementations) and apply a post-processing or pre/post multiplicative local phase to incorporate curved-spacetime effects.  
quantum_hardware_platform | platform-agnostic (explicitly mentions trapped ions, optical waveguide arrays, cold atoms, and theoretical superconducting-circuit proposals as capable platforms).  
encoding_and_mapping | The mapping is psi(x,t) = exp(-i ∫ V(x) dx) phi(x,t) = Omega^{-1/2}(x) phi(x,t). Here phi evolves under the free massless 1+1D Dirac Hamiltonian i∂_t phi = - i sigma_x ∂_x phi; the curved metric produces an effective (imaginary) potential V(x) = - i (Omega'/2Omega). Degrees of freedom: two-component Dirac spinor in continuous 1+1D. No fermion-to-qubit mapping, lattice discretization, or gauge constraints are specified in the paper — the proposal assumes existing continuous or discretized simulator implementations of the free Dirac dynamics and applies the multiplicative phase to their solutions or measured data.  
algorithm_or_protocol | 1) Prepare initial wavepacket phi(x,0) for the free massless Dirac equation on the simulator; 2) evolve under the free Dirac dynamics to obtain phi(x,t) (by the platform's native analog dynamics); 3) obtain curved-spacetime spinor psi(x,t) = Omega^{-1/2}(x) phi(x,t) (apply multiplicative spatially dependent real factor); 4) compute/measure observables (e.g., probability density |psi|^2 = Omega^{-1}|phi|^2). No bespoke quantum circuit, Trotterization, or VQE protocol is specified — the method is a mapping/post-processing technique for analog Dirac simulations.  
resource_estimates | No quantitative resource estimates are provided (no qubit counts, gate counts, circuit depths, number of measurements, or fault-tolerance overheads are given). The claim is qualitative: existing Dirac simulators are immediately capable of incorporating the mapping.  
noise_and_error_mitigation | Not discussed. The paper does not model noise nor propose mitigation strategies (no error budgets, error-correction, or NISQ mitigation methods are presented).  
key_results_or_demonstrations | Analytical demonstration that any solution of the free massless 1+1 Dirac equation can be converted into a solution in a static curved 1+1 spacetime by the local phase; application to a family of traversable-wormhole metrics producing closed-form relations between flat and curved probability densities (|psi|^2 = Omega^{-1}|phi|^2) and plotted example wavepacket dynamics showing focusing/distortion at the wormhole throat. This is a theoretical/analytical proposal and demonstration (no experimental implementation in this paper).  
validation_and_benchmarks | Validation is analytic: substitution of the mapping into the curved Dirac equation shows cancellation of the effective potential and yields the free equation for phi; probability densities are related by an exact formula. The wormhole example uses analytic expressions for Omega and the mapping, and plots of transformed Gaussian wavepackets illustrate expected behavior. No numerical exact-diagonalization, no experimental cross-platform benchmarks, and no finite-size scaling studies are provided.  
claimed_feasibility | Authors assert immediate feasibility on existing quantum simulators of the free 1+1 Dirac equation (trapped ions, waveguides, cold atoms, superconducting-circuit proposals) since no additional Hamiltonian engineering is required — only application of the spatial phase factor to simulated or measured wavefunctions. No timetable or resource thresholds are provided; the claim is qualitative and targeted to current NISQ-era Dirac simulators in 1+1.  
limitations_and_open_problems | Explicit limitations given in the paper: the technique is restricted to static (dot{Omega}=0), massless (m=0) Dirac fields in 1+1 dimensions (where the metric is conformally flat); singular points where Omega=0 (coordinate-dependent singularities, e.g., wormhole throat coordinate) require care and are excluded from direct application; backreaction and pair-creation effects are neglected (single-particle approximation); the mapping produces differences in probability density (the phase is real and non-unitary in that it rescales amplitude), so dynamics are not identical in a unitary-sense; no discussion of extension to m ≠ 0 or higher dimensions is provided in detail.  
complexity_or_hardness_arguments | No complexity-theoretic claims are made (no statements of BQP/QMA hardness or classical intractability are provided).  
theory_context_keywords | quantum field theory in curved spacetime, Dirac equation in curved spacetime, conformal metric, local phase encoding, traversable wormhole, single-particle approximation, analog quantum simulation, non-Hermitian effective potential.  
citations_to_prior_work | Cited representative prior experimental and theoretical works: trapped-ion implementations of Dirac dynamics (R. Gerritsma et al., "Quantum simulation of the Dirac equation", Nature 463 (2010) and related trapped-ion Klein tunneling refs), optical waveguide and cold-atom Dirac simulators (refs. [7],[8]), superconducting-circuit proposals (ref. [9]), a theoretical proposal for Dirac equation curved-spacetime simulation with coupled waveguide arrays (ref. [10], Christian Koke, Changsuk Noh and Dimitris G. Angelakis, arXiv:1607.04821), and the earlier technique for encoding potentials into free evolution (ref. [20], C. Sabín et al., "Encoding relativistic potential dynamics into free evolution", Phys. Rev. A 85, 052301 (2012)). The paper also cites standard wormhole literature (Morris & Thorne) and various analogue-wormhole proposals (refs. [17-19]).  
  
### Family of 1+1-dimensional traversable-wormhole spacetimes with shape function b(r) = b0^2 / r

Field | Value  
---|---  
name_short | 1+1D traversable wormhole (b(r)=b0^2/r)  
name_full | Family of 1+1-dimensional traversable-wormhole spacetimes with shape function b(r) = b0^2 / r  
brief_description | A specific family of static 1+1D traversable-wormhole metrics used as a worked example: after coordinate change the metric is ds^2 = c^2(x)(-dt^2 + dx^2) with c^2(x) = 1 - b0^2/(x^2 + b0^2), and the wormhole throat sits at the coordinate singularity where Omega=0 (x=0 in given coords).  
citation_title |   
mention_or_use | use  
target_system_or_model | Traversable wormhole spacetime in 1+1 dimensions defined by b(r) = b0^2 / r and metric forms ds^2 = -dt^2 + dr^2/(1 - b(r)/r) or, after coordinate change, ds^2 = c^2(x)(-dt^2 + dx^2) with c^2(x)=1 - b0^2/(x^2 + b0^2).  
black_hole_phenomena_targeted | Wormhole throat traversal and the resulting change/distortion of Dirac-particle probability density (analogous to horizon/throat-centered focusing and spatially dependent effective light speed).  
simulation_paradigm | Analog quantum simulation of Dirac dynamics in curved spacetime via the phase-encoding mapping applied to free 1+1D Dirac simulator outputs (platform-agnostic).  
quantum_hardware_platform | platform-agnostic; explicitly suggested platforms are trapped ions, optical waveguides, cold atoms, and superconducting-circuit proposals that already simulate free Dirac dynamics.  
encoding_and_mapping | Coordinate transform x = ± sqrt(r^2 - b0^2) brings metric to conformal form; Omega^2(x) = c^2(x) = 1 - b0^2/(x^2 + b0^2); mapping uses psi = Omega^{-1/2} phi, leading to effective potential V(x) = - i b0^2/(2 x(b0^2 + x^2)). Probability densities obey |psi|^2 = sqrt(b0^2 + x^2)/x * |phi|^2 for this family.  
algorithm_or_protocol | Use an existing free-massless-Dirac wavepacket phi(x,t) (e.g., Gaussian spinor) on simulator, then apply the multiplicative Omega^{-1/2}(x) factor to obtain psi(x,t) representing the wormhole curved-spacetime solution; measure |psi|^2 and observe focusing/distortion near throat. The paper demonstrates this analytically and with plotted examples of transformed Gaussian wavepackets.  
resource_estimates | None provided for implementing this wormhole example on quantum hardware (no qubit counts, gate counts, or measurement budgets).  
noise_and_error_mitigation | Not discussed specifically for the wormhole example.  
key_results_or_demonstrations | Analytical closed-form relation between flat and wormhole probability densities (Eq. (17)) and plotted examples (Fig. 1) showing that wavepackets initialized on one side traverse the throat and exhibit intense focusing at the throat, while wavepackets initialized near the throat on the other side show distortions inversely related to initial distance. The demonstration is theoretical/analytic (no experimental data).  
validation_and_benchmarks | Analytic derivation starting from the wormhole metric and the mapping; references the standard wormhole literature for physical interpretation and coordinate-regularity arguments. No numerical convergence studies or direct experimental benchmarks are provided.  
claimed_feasibility | Authors state that the wormhole dynamics can be obtained directly from free-Dirac simulator data using the mapping and therefore are immediately accessible to current Dirac quantum simulators; no quantitative feasibility thresholds are given.  
limitations_and_open_problems | This specific family exhibits Omega=0 at x=0 (coordinate singularity) so the direct equation is not defined there; the analysis works separately on both sides of the throat and relies on coordinate changes to remove the apparent singularity. The example is 1+1D, massless, static, and neglects backreaction; extension to massive fields or higher dimensions is not treated in the paper.  
complexity_or_hardness_arguments | None provided for the wormhole example.  
theory_context_keywords | traversable wormhole, Morris-Thorne wormhole, conformal coordinate transform, throat, effective light-speed profile c(x), single-particle Dirac propagation in curved background.  
citations_to_prior_work | Wormhole literature and analog proposals cited: Morris, Thorne & Yurtsever ("Wormholes, Time Machines, and the Weak Energy Condition"), Morris & Thorne ("Wormholes in spacetime and their use for interstellar travel"), Ellis ("Ether Flow Through a Drainhole"), and analogue/experimental wormhole proposals (refs. [17-19]). The paper also cites its own related work (ref. [19], C. Sabín, Phys. Rev. D 94, 081501(R) (2016)).  
  
## Citation

Cite this artifact as `\cite{ast-ext-sabn-2026-08-13}`.
[code] 
    @misc{ast-ext-sabn-2026-08-13,
      title        = {Extraction: Mapping curved spacetimes into Dirac spinors},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-mapping-curved-spacetimes-into-dirac-spinors.md},
      crossref     = {sabn2016mapping},
      note         = {Theorizer's extraction from \cite{sabn2016mapping}. asta-artifact id: extraction-result-89},
    }
    
    @article{sabn2016mapping,
      title     = {Mapping curved spacetimes into Dirac spinors},
      author    = {C. Sabín},
      year      = {2016},
      journal   = {Scientific Reports},
      url       = {https://www.semanticscholar.org/paper/9818444},
    }
[/code]
