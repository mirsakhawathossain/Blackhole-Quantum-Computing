[<- All artifacts](<../index.md>)

# Extraction: Dirac equation in 2-dimensional curved spacetime, particle creation, and coupled waveguide arrays

**Contents:**

  * Classical optical simulation of the Dirac equation in curved 1+1D spacetime using binary waveguide arrays
  * Single-particle analog of gravitational pair creation via Dirac wavepacket dynamics
  * Simulation of the Dirac equation in curved spacetime with cold atoms on optical lattices (cited work)



### Classical optical simulation of the Dirac equation in curved 1+1D spacetime using binary waveguide arrays

Field | Value  
---|---  
name_short | Waveguide optical analog  
name_full | Classical optical simulation of the Dirac equation in curved 1+1D spacetime using binary waveguide arrays  
brief_description | A proposal and numerical demonstration to simulate the 1+1D Dirac equation in curved spacetime (e.g. FRW, Rindler conformal metrics) by mapping the discretised Dirac spinor to amplitudes in a binary coupled waveguide array, with time evolution represented by propagation along the waveguide (z) and a spacetime-dependent effective mass implemented via modulated on-site refractive indices.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime (Dirac fermion in 1+1D); specific metrics: conformally-flat 1+1D spacetimes including FRW and Rindler  
black_hole_phenomena_targeted | Particle-creation analogs (pair production in time-dependent backgrounds), Unruh/Hawking-style phenomena presented as context (Unruh/Rindler and Hawking effect discussed theoretically); single-particle manifestation of pair production (negative-to-positive energy conversion) and zitterbewegung as indicator  
simulation_paradigm | Analog classical photonic simulation (tight-binding / coupled-mode analog of Dirac equation); not a digital quantum-computing protocol  
quantum_hardware_platform | Photonics (laser-written coupled optical waveguide arrays; classical light propagation), platform-agnostic in the sense of classical analogs  
encoding_and_mapping | Spatial discretisation with lattice spacing d: spinor components mapped to alternating waveguides (psi_1(n) -> even waveguides, psi_2(n) -> odd waveguides). Kinetic term -> evanescent coupling between neighboring guides with coupling k_n = 1/d; mass term -> alternating on-site potential (-1)^n sigma with sigma = m (or time/spacetime-dependent sigma_n(z) = Omega(z)_m for curved spacetime). Time in Dirac equation maps to propagation coordinate z in the array; a time-dependent conformal factor is implemented via z-dependent onsite index modulation producing a time-dependent effective mass m_eff(t)=Omega(t)_ m.  
algorithm_or_protocol | Classical coupled-mode / tight-binding propagation (i d/dz c_n = k_n(c_{n+1}+c_{n-1}) + (-1)^n sigma_n(z) c_n). Numerical integration of the coupled-mode equations for given initial wavepacket; preparation of input field profile to represent chosen spinor wavepacket.  
resource_estimates | Experimental/numerical examples reported: arrays with N = 502 waveguides (k ≈ 6.2 used in simulation) and N = 50 waveguides (k ≈ 0.63) were simulated; effective masses used include m = 1 and time-dependent inverted-Gaussian profiles of Omega(t) producing m_eff excursions. No qubit/gate counts (classical optical device).  
noise_and_error_mitigation | Not applicable for quantum gate noise; practical experimental limitations discussed qualitatively: discretisation (finite N) leads to coarse-graining and small artefacts (e.g., residual zitterbewegung), but simulations show feasibility even for N ~ 50; no quantitative error-budget or error-mitigation protocols for quantum noise presented.  
key_results_or_demonstrations | Numerical demonstrations that (i) the binary waveguide tight-binding model reproduces zitterbewegung and wavepacket evolution of the continuum Dirac equation in flat 1+1D, (ii) a negative-energy Gaussian wavepacket evolves under a time-dependent m_eff(t) (inverted Gaussian profile) into a superposition containing positive-energy components — interpreted as a single-particle analog of particle creation; quantitative examples: agreement between continuum Dirac evolution and coupled-mode simulation for N=502 and acceptable agreement for N=50 waveguides. These are proposal + classical-numerical simulation results (not a quantum-hardware experiment in this paper, although prior experiments on related effects are cited).  
validation_and_benchmarks | Validation by direct comparison to solutions of the discretised and continuum Dirac equation (exact numerical integration of continuum Dirac PDEs); comparisons shown between continuum results (section IV) and coupled-mode simulations (section V; figures showing close match in mode amplitudes and mean position); benchmark metrics include visual agreement of absolute mode amplitudes and average position (showing zitterbewegung signatures) and qualitative matching of negative-to-positive energy conversion.  
claimed_feasibility | Authors claim feasibility on existing photonic experimental platforms: simulations show arrays with as few as ~50 waveguides produce qualitatively correct dynamics, while larger arrays (502) closely approximate continuum dynamics. They state general spacetime dependence (not only FRW time-dependence) can be implemented by appropriate refractive-index and coupling engineering along propagation coordinate. They emphasise that the proposal is a single-particle (classical-field) analog and therefore readily implementable in current waveguide technology.  
limitations_and_open_problems | The approach is a classical single-particle analog and does not implement the full quantum-field-theoretic multi-particle creation process (no second-quantized field, no mode-annihilation/creation operators, vacuum ambiguity subtleties beyond the single-mode analogy). Back-action on gravity and true particle statistics (bosonic commutators or fermionic anti-commutators in a many-body QFT) are absent. Quantitative particle-number creation (i.e., expectation values in Fock space) cannot be captured fully; verification relies on single-particle signatures (conversion & zitterbewegung). Discretisation and finite-size effects introduce coarse-graining artefacts. No quantum-computational resource estimates (qubits/gates) or fault-tolerance analysis are provided because this is a classical analog.  
complexity_or_hardness_arguments | None  
theory_context_keywords | Dirac equation in curved spacetime, conformal factor, FRW metric, Rindler metric, Unruh effect, Hawking effect (context), particle creation, zitterbewegung, Klein paradox, coupled-mode / tight-binding mapping  
citations_to_prior_work | Refs cited in paper relevant to approach include Longhi (Opt. Lett., Phys. Rev. B) proposals and Dreisow et al. experiments for Dirac/zitterbewegung in waveguides [14-17]; fundamental QFT in curved space references: Birrell & Davies 'Quantum Fields in Curved Space' [4], Mukhanov & Winitzki 'Introduction to Quantum Effects in Gravity' [6]; simulation-with-cold-atoms reference: Boada et al., New J. Phys. 13, 035002 (2011) [31].  
  
### Single-particle analog of gravitational pair creation via Dirac wavepacket dynamics

Field | Value  
---|---  
name_short | Single-particle particle-creation analog  
name_full | Single-particle analog of gravitational pair creation via Dirac wavepacket dynamics  
brief_description | Using wavepacket evolution of the Dirac equation in time-dependent metrics (FRW conformal factor), conversion of negative-energy localized wavepackets into mixtures with positive-energy components is proposed and used as a single-particle signature of pair creation; zitterbewegung (interference of positive and negative energy components) is used as an experimentally accessible indicator.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Dirac fermion in 1+1D curved spacetime (time-dependent conformal factor / effective mass m_eff(t) = Omega(t) m).  
black_hole_phenomena_targeted | Analog of gravitational particle creation (expanding-universe pair production); connection to Unruh/Hawking effects discussed but not directly simulated as Hawking radiation spectrum.  
simulation_paradigm | Theoretical/numerical wavepacket evolution (continuum PDE numerical integration) and analog classical simulation via photonic waveguides (see Waveguide optical analog entity).  
quantum_hardware_platform | None  
encoding_and_mapping | No qubit encoding — analysis in momentum and position space of Dirac spinors; single-particle negative-energy spinor packets are prepared and evolved under time-dependent mass in continuum or discretised lattice.  
algorithm_or_protocol | Time integration of Dirac PDEs for chosen Omega(t); projective checks: projection onto positive-energy subspace and observation of mean position/zitterbewegung as diagnostics.  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Numerical demonstration that an inverted-Gaussian excursion of the conformal factor (m_eff(t) inverted Gaussian) induces ZB in an initially negative-energy wavepacket, interpreted as creation of positive-energy components (single-particle analog of pair creation). Figures show mean-position dynamics and mode amplitudes illustrating the effect.  
validation_and_benchmarks | Validation by comparing continuum Dirac numerical evolution with discretised coupled-mode array simulations; use of zitterbewegung-free positive-energy-only wavepackets as control cases.  
claimed_feasibility | Authors argue the single-particle analog is experimentally observable in waveguide arrays (classical optics) and that ZB provides an easily measurable signature bypassing full multi-particle checks.  
limitations_and_open_problems | Explicitly noted: single-particle description cannot capture full QFT particle creation; anticommutation/commutation differences (fermions vs bosons) affect mode expansion and occupation-number interpretation; quantitative particle-number production and true vacuum ambiguities require full quantum-field simulation (e.g., cold-atom many-body proposals) which is beyond the classical-waveguide setup.  
complexity_or_hardness_arguments | None  
theory_context_keywords | Dirac sea picture, Bogolyubov transformation, mode expansion, positive/negative energy projection, zitterbewegung  
citations_to_prior_work | Parker (particle creation in expanding universe) [11]; discussions of Schwinger effect and Klein paradox as single-particle hints of pair production [8-10,32]; references to experiments/proposals for Dirac analogues in waveguides [14-17].  
  
### Simulation of the Dirac equation in curved spacetime with cold atoms on optical lattices (cited work)

Field | Value  
---|---  
name_short | Cold-atom mention  
name_full | Simulation of the Dirac equation in curved spacetime with cold atoms on optical lattices (cited work)  
brief_description | The paper cites earlier work proposing simulation of Dirac equation in curved spacetime using cold atoms in optical lattices as an example of (many-body) quantum simulation of curved-space Dirac physics; the cited work is not developed in this paper but pointed to as an example where full quantum-field aspects might be addressed.  
citation_title |   
mention_or_use | mention  
target_system_or_model | Dirac equation in curved spacetime (proposal to realise with cold atoms in optical lattices)  
black_hole_phenomena_targeted | Implicitly: particle creation in curved backgrounds (full quantum-field aspects), potential many-body quantum simulation of QFT in curved space (not detailed here)  
simulation_paradigm | Analog quantum simulation (cold atoms in optical lattices) — mentioned but not elaborated in this paper  
quantum_hardware_platform | Neutral atoms in optical lattices (cold-atom quantum simulator) — mentioned in passing  
encoding_and_mapping | Not provided in this paper (reference only). The paper points readers to ref. [31] for detailed mapping.  
algorithm_or_protocol | None  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | No results in this paper — the citation is used to point to an external quantum-simulation proposal; no demonstration or resource claims are reproduced here.  
validation_and_benchmarks | None  
claimed_feasibility | None  
limitations_and_open_problems | Not discussed here; the citation is noted as an example that goes beyond single-particle classical analogs and toward quantum many-body simulation of curved-space Dirac fields.  
complexity_or_hardness_arguments | None  
theory_context_keywords | quantum simulation, optical lattices, Dirac equation in curved spacetime  
citations_to_prior_work | Reference [31] in the paper: O. Boada, A. Celi, J. I. Latorre, and M. Lewenstein, New J. Phys. 13, 035002 (2011) (cited as an example of quantum simulation with cold atoms).  
  
## Citation

Cite this artifact as `\cite{ast-ext-koke-2026-08-13}`.
[code] 
    @misc{ast-ext-koke-2026-08-13,
      title        = {Extraction: Dirac equation in 2-dimensional curved spacetime, particle creation, and coupled waveguide arrays},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-dirac-equation-in-2-dimensional-curved-spacetime-particle-creation-an.md},
      crossref     = {koke2016dirac},
      note         = {Theorizer's extraction from \cite{koke2016dirac}. asta-artifact id: extraction-result-88},
    }
    
    @article{koke2016dirac,
      title     = {Dirac equation in 2-dimensional curved spacetime, particle creation, and coupled waveguide arrays},
      author    = {Christian Koke and C. Noh and D. Angelakis and D. Angelakis},
      year      = {2016},
      url       = {https://www.semanticscholar.org/paper/119234857},
    }
[/code]
