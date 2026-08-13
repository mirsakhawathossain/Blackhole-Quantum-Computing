[<- All artifacts](<../index.md>)

# Extraction: Quantum simulation of Unruh radiation

**Contents:**

  * Quantum simulation of Hawking-Unruh radiation in a driven Bose-Einstein condensate
  * Quantum circuit model for non-inertial objects: a uniformly accelerated mirror
  * Sonic analog of gravitational black holes in Bose-Einstein condensates
  * Hawking radiation from an acoustic black hole on an ion ring
  * Electromagnetic/optical simulations of gravitational effects (waveguides and Newton–Schrödinger analogues)
  * Observation of quantum Hawking radiation and its entanglement in an analogue black hole



### Quantum simulation of Hawking-Unruh radiation in a driven Bose-Einstein condensate

Field | Value  
---|---  
name_short | BEC Unruh simulator  
name_full | Quantum simulation of Hawking-Unruh radiation in a driven Bose-Einstein condensate  
brief_description | An analog quantum simulation that maps the Rindler (accelerating-frame) transformation to time evolution under a parametrically driven pair-creation Hamiltonian in a Bose-Einstein condensate, producing matter-wave emissions that locally exhibit a thermal (Unruh/Hawking-like) distribution while retaining long-range coherence and partial temporal reversibility.  
citation_title | here  
mention_or_use | use  
target_system_or_model | Quantum field theory in curved spacetime — Rindler/Unruh effect (Hawking-Unruh radiation) simulated via mode-pair production in a driven BEC  
black_hole_phenomena_targeted | Unruh/Hawking-Unruh thermal radiation spectrum and associated per-mode entropy; coherence and unitary origin of Hawking-Unruh-like radiation (spatial phase correlations and time-reversal/reversibility as signatures of quantum origin)  
simulation_paradigm | Analog quantum simulation (laboratory analog using a driven many-body atomic system implementing a bosonic parametric Hamiltonian)  
quantum_hardware_platform | Neutral atoms — Bose-Einstein condensate (ultracold atom platform using Feshbach-modulated interactions)  
encoding_and_mapping | Momentum-mode mapping: field modes a_k of the quantum scalar field correspond to momentum modes of the condensate; the simulated Rindler boost is implemented by evolution under H = iħ Σ_k g_k (a_k^† a_{-k}^† - a_k a_{-k}) with only modes |k| = k_f retained (rotating-wave/Bogoliubov approximations). The lab time τ and coupling g map to the Rindler squeeze parameter via gτ = r_ω/2, and the mean occupation per mode sinh^2(gτ) maps to the thermal occupation with effective temperature T = E_{k_f}/[k_B ln(1+1/ n̄)]. No qubit encoding — continuous-variable bosonic mode encoding (momentum-space modes). Boundary conditions: finite disk condensate → finite angular mode width; truncation to resonant |k|=k_f modes.  
algorithm_or_protocol | Experimental protocol: modulate scattering length a(t) = a_dc + a_ac sin(ω t) near Feshbach resonance to realize parametric pair creation; measure angular/momentum-resolved atom counts by slicing emission pattern into angular bins; extract P(n) per slice, fit to thermal model; probe phase coherence via two-pulse interference (different ω pulses) and perform time reversal by applying a phase jump α to the driving to attempt reversal of parametric amplification.  
resource_estimates | Experimental resource numbers (analog-platform): ~6×10^4 to 1×10^5 atoms in a disk-shaped condensate; observed emission into up to ≈276 angular/momentum modes (typical analysis dividing into 180 slices); mode width ~1.33°; modulation frequencies used e.g. ω/2π = 2.1 kHz, 3 kHz, 5.63 kHz; typical modulation times τ up to ~6 ms. No qubit/gate counts or digital resource estimates (platform-agnostic continuous-variable experiment).  
noise_and_error_mitigation | Detection noise characterized and convolved into probability-distribution fits; rotating-wave and Bogoliubov approximations justify truncation to resonant modes; limits to ideal behavior identified (off-resonant coupling to nearby momentum modes due to finite condensate size, counter-rotating terms, atom motion out of condensate). Numerical Gross–Pitaevskii simulations include these effects; no digital error-correction methods applied.  
key_results_or_demonstrations | Experimental demonstration: (1) Mode population P(n) in angular slices fits a thermal (exponential/Bose) distribution; extracted effective temperature T scales linearly with inferred simulated acceleration A with prefactor κ = 1.17(7) pK·s, consistent with Unruh prediction ħ/(2π k_B) ≈ 1.22 pK·s. (2) Entropy per mode S extracted from distributions agrees qualitatively with theoretical von Neumann entropy and shows logarithmic increase with A. (3) Spatial phase correlations: phase of interference fringes satisfy φ_θ + φ_{θ+π} = constant, indicating phase-locked counter-propagating pairs. (4) Temporal reversibility: phase jump α ≈ π produces maximum suppression η ≈ 0.49 experimentally (51% reduction reported), with ~26% of excitations reversed back to condensate (~2,200 atoms); numerical GP simulations reproduce partial reversal and attribute limits to off-resonant modes. Results are hardware experiments (analog) with analytical mapping and numerical simulation support.  
validation_and_benchmarks | Validation by multiple routes: analytic mapping of Bogoliubov evolution to Rindler Bogoliubov transformation (Eqs. M3–M5/M11–M18) and identification of gτ ↔ r_ω/2; fits of measured P(n) to derived p(n,ξ) distributions including convolution with measured detection noise; extraction of T and S compared to Unruh/Hawking predictions; numerical Gross–Pitaevskii simulations (CUDA solver) reproduce suppression/reversal behavior and quantify off-resonant effects; phase-correlation results compared to analytic formulas (M41–M46).  
claimed_feasibility | Demonstrates feasibility of bench-top analog simulation of Unruh/Hawking-like radiation with current ultracold-atom technology; authors suggest this platform can probe quantum field effects in non-inertial frames and provide insights into Hawking/Unruh physics. No claims that digital quantum computers are required; scalability limited by condensate size, mode resolution, and control of off-resonant couplings.  
limitations_and_open_problems | Analog nature: simulates field quantization in an accelerating frame but not full dynamical spacetime or black-hole backreaction; mapping uses approximations (rotating-wave, Bogoliubov, restriction to |k|=k_f); finite condensate size causes momentum uncertainty and off-resonant mode coupling limiting ideal reversal; partial reversal limited by counter-rotating terms and atoms leaving condensate; measured thermal behavior is local while global state is coherent (distinguishing from true black-hole thermalization); no direct study of information-loss/Page curve, scrambling, or evaporation dynamics.  
complexity_or_hardness_arguments | No complexity-theoretic claims (no statements about BQP/QMA hardness or classical intractability).  
theory_context_keywords | Unruh effect, Hawking radiation, Rindler transformation, Bogoliubov transformation, squeezed states, von Neumann entropy, analogue gravity, parametric pair creation, matter-wave jets, quantum field in curved spacetime  
citations_to_prior_work | Key referenced works include Unruh (1976) and Hawking (1974/1975) for foundational theory; Robert Wald (Quantum Field Theory in Curved Spacetime) for formalism; Ref. [14] (D. Su et al., 'Quantum circuit model for non-inertial objects: a uniformly accelerated mirror') for quantum-circuit mapping ideas; experimental/analogue precedents: Garay et al. 'Sonic analog of gravitational black holes in Bose-Einstein condensates' (Ref. 24), Schützhold & Unruh 'Hawking radiation in an electromagnetic waveguide?' (Ref. 25), Horstmann et al. 'Hawking radiation from an acoustic black hole on an ion ring' (Ref. 26), Bekenstein et al. 'Optical simulations of gravitational effects in the newtonschringer system' (Ref. 27), and Steinhauer 'Observation of quantum hawking radiation and its entanglement in an analogue black hole' (Ref. 28).  
  
### Quantum circuit model for non-inertial objects: a uniformly accelerated mirror

Field | Value  
---|---  
name_short | Quantum circuit model (Ref.14)  
name_full | Quantum circuit model for non-inertial objects: a uniformly accelerated mirror  
brief_description | A theoretical model proposing a quantum-circuit description of non-inertial objects (uniformly accelerated mirrors) that maps non-inertial transformations to circuit elements — cited here as a theoretical foundation for mapping Rindler transformations to unitary evolutions.  
citation_title | Quantum circuit model for non-inertial objects: a uniformly accelerated mirror  
mention_or_use | mention  
target_system_or_model | Rindler/accelerating mirror model (quantum circuit mapping of non-inertial transformations)  
black_hole_phenomena_targeted | Unruh/Hawking-like particle creation from acceleration (analogue of horizon-induced particle production)  
simulation_paradigm | Theoretical quantum-circuit model (proposal for digital mapping rather than implemented hardware here)  
quantum_hardware_platform | platform-agnostic (theoretical circuit model)  
encoding_and_mapping | Maps field-mode Bogoliubov transformations from acceleration into equivalent circuit/squeezing operations (cited as conceptual basis for mapping evolution to Rindler boost).  
algorithm_or_protocol | Not implemented in paper; cited as conceptual mapping between circuit evolution and Rindler transform.  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Mentioned as prior theoretical work motivating mapping used in present experiment; no experimental usage in this paper.  
validation_and_benchmarks | Not detailed in present paper (cited as reference).  
claimed_feasibility | Mention used to justify equivalence of unitary evolution to Rindler transformation; no feasibility claims reproduced here.  
limitations_and_open_problems | Cited as conceptual; specifics not discussed in detail in this paper.  
complexity_or_hardness_arguments | None  
theory_context_keywords | quantum circuit, non-inertial transformation, accelerated mirror, Rindler  
citations_to_prior_work |   
  
### Sonic analog of gravitational black holes in Bose-Einstein condensates

Field | Value  
---|---  
name_short | Sonic black hole BEC (Ref.24)  
name_full | Sonic analog of gravitational black holes in Bose-Einstein condensates  
brief_description | A prominent analogue-gravity proposal mapping black-hole horizons to sonic horizons in BECs, enabling laboratory study of Hawking-like emission of phonons.  
citation_title | Sonic analog of gravitational black holes in bose-einstein condensates  
mention_or_use | mention  
target_system_or_model | Acoustic (sonic) analog black hole in Bose-Einstein condensate  
black_hole_phenomena_targeted | Analogue Hawking radiation at sonic horizons (phonon emission), horizon physics  
simulation_paradigm | Analog quantum simulation (condensed-matter/optical analogue)  
quantum_hardware_platform | Bose-Einstein condensates (neutral atoms)  
encoding_and_mapping | Field-to-phonon mapping: density/phase fluctuations in BEC mimic scalar field in curved spacetime with effective metric determined by flow profile  
algorithm_or_protocol | Experimental/proposal-based: engineering flow profiles with horizons and measuring phonon emission and correlations  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Cited as background motivating analogue experiments; not used directly in present experiment.  
validation_and_benchmarks | None  
claimed_feasibility | None  
limitations_and_open_problems | General caveats of analogue models (effective metric, limited correspondence to full gravity) discussed in literature but not detailed here.  
complexity_or_hardness_arguments | None  
theory_context_keywords | analogue gravity, sonic horizon, phonon Hawking radiation  
citations_to_prior_work |   
  
### Hawking radiation from an acoustic black hole on an ion ring

Field | Value  
---|---  
name_short | Ion-ring acoustic BH (Ref.26)  
name_full | Hawking radiation from an acoustic black hole on an ion ring  
brief_description | A theoretical proposal to realize acoustic black-hole analogues and Hawking radiation using phonon/ion excitations in a trapped-ion ring geometry.  
citation_title | Hawking radiation from an acoustic black hole on an ion ring  
mention_or_use | mention  
target_system_or_model | Acoustic black hole analogue on an ion-trap ring  
black_hole_phenomena_targeted | Analogue Hawking radiation (phonon emission) and horizon physics  
simulation_paradigm | Analogue quantum simulation proposal (ion-trap platform)  
quantum_hardware_platform | Trapped ions (ion ring)  
encoding_and_mapping | Mapping collective vibrational modes/phonons to scalar-field modes in curved effective metric (as cited conceptually)  
algorithm_or_protocol | Proposal-level: engineer effective flow/horizon in ion ring and detect emitted excitations/correlations  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Cited among analogue proposals; not used experimentally in this paper.  
validation_and_benchmarks | None  
claimed_feasibility | None  
limitations_and_open_problems | None  
complexity_or_hardness_arguments | None  
theory_context_keywords | acoustic black hole, trapped-ion analogue  
citations_to_prior_work |   
  
### Electromagnetic/optical simulations of gravitational effects (waveguides and Newton–Schrödinger analogues)

Field | Value  
---|---  
name_short | Optical analogue (Ref.25/27)  
name_full | Electromagnetic/optical simulations of gravitational effects (waveguides and Newton–Schrödinger analogues)  
brief_description | Works proposing electromagnetic and optical systems (e.g., waveguides, Newton–Schrödinger analogues) as platforms to study Hawking-like effects and gravitational analogues in photonics.  
citation_title | Hawking radiation in an electromagnetic waveguide?  
mention_or_use | mention  
target_system_or_model | Electromagnetic/optical analogues of gravitational phenomena (waveguides, optical setups)  
black_hole_phenomena_targeted | Analogue Hawking radiation and gravitational effects simulated in photonic systems  
simulation_paradigm | Analogue quantum simulation / classical wave analogue  
quantum_hardware_platform | Photonics / electromagnetic waveguides / optics  
encoding_and_mapping | Mapping of electromagnetic mode propagation in engineered media to field propagation in curved spacetime (conceptual mention only)  
algorithm_or_protocol | Design and measurement of wave-propagation in structured optical media to emulate horizon-like behavior  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Cited as part of the broader analogue-gravity literature; not implemented in the present experiment.  
validation_and_benchmarks | None  
claimed_feasibility | None  
limitations_and_open_problems | None  
complexity_or_hardness_arguments | None  
theory_context_keywords | optical analogue, electromagnetic waveguide, analogue Hawking radiation  
citations_to_prior_work |   
  
### Observation of quantum Hawking radiation and its entanglement in an analogue black hole

Field | Value  
---|---  
name_short | Steinhauer analogue BH (Ref.28)  
name_full | Observation of quantum Hawking radiation and its entanglement in an analogue black hole  
brief_description | An experimental report of Hawking-like radiation and entanglement observed in an analogue black hole created in a Bose-Einstein condensate flow, cited as a closely related experimental demonstration of analogue Hawking radiation.  
citation_title | Observation of quantum hawking radiation and its entanglement in an analogue black hole  
mention_or_use | mention  
target_system_or_model | Analogue black hole in flowing Bose-Einstein condensate (sonic horizon)  
black_hole_phenomena_targeted | Hawking radiation spectrum and entanglement between Hawking pairs  
simulation_paradigm | Analog quantum simulation (BEC flow with horizon)  
quantum_hardware_platform | Bose-Einstein condensate (neutral atoms)  
encoding_and_mapping | Phononic excitations mapped to field quanta near sonic horizon; measurements of correlations used to infer entanglement  
algorithm_or_protocol | Experimental creation of horizon in flow and measurement of density-density correlations and entanglement witnesses  
resource_estimates | None  
noise_and_error_mitigation | None  
key_results_or_demonstrations | Cited as experimental precedent demonstrating Hawking-like emission and entanglement in analogue gravity; not reproduced here but conceptually connected.  
validation_and_benchmarks | None  
claimed_feasibility | None  
limitations_and_open_problems | None  
complexity_or_hardness_arguments | None  
theory_context_keywords | analogue Hawking radiation, entanglement, sonic horizon  
citations_to_prior_work |   
  
## Citation

Cite this artifact as `\cite{ast-ext-hu-2026-08-13}`.
[code] 
    @misc{ast-ext-hu-2026-08-13,
      title        = {Extraction: Quantum simulation of Unruh radiation},
      author       = {{Asta Theorizer}},
      year         = {2026},
      howpublished = {Asta Theorizer evidence extraction},
      url          = {extractions/extraction-quantum-simulation-of-unruh-radiation.md},
      crossref     = {hu2018quantum},
      note         = {Theorizer's extraction from \cite{hu2018quantum}. asta-artifact id: extraction-result-87},
    }
    
    @article{hu2018quantum,
      title     = {Quantum simulation of Unruh radiation},
      author    = {Jiazhong Hu and Lei Feng and Zhendong Zhang and C. Chin},
      year      = {2018},
      journal   = {Nature Physics},
      url       = {https://www.semanticscholar.org/paper/182221423},
    }
[/code]
