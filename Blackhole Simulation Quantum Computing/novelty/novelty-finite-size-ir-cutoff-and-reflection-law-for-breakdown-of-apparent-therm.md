[<- All artifacts](<../index.md>)

# Novelty: Finite-size IR cutoff and reflection law for breakdown of apparent thermality

**Contents:**

  * Dimensions



Assessed theory: [theory-5](<../theories/horizon-encoded-hopping-universality-for-hawking-like-thermality.md>)

### Dimensions

### Phenomenon / Effect — Explicit Peripheral

**What is Known:** Within the horizon-encoded nearest-neighbor hopping-chain analogue-gravity literature, finite-size simulations already explicitly observe that the outgoing spectrum is approximately exponential over a window and that the lowest-energy part deviates first when the outer region is spatially truncated, with an order-of-magnitude IR cutoff estimate and practical guidance to stop evolution before boundary reflections return. Other related analogue-gravity experiments/simulations show low-frequency suppression or late-time contamination, but often attribute it to dispersion/finite duration or simply note reflections without formulating an energy-ordered breakdown rule. At least one superconducting-chain implementation reports reflections and spectral deviations, but its energy-resolved deviations are not consistent with a universal “lowest-energy-first” breakdown in that dataset (low energies look comparatively more thermal than high energies).

**What is Introduced:** The statement elevates finite-size caveats into a specific, operational regularity for hopping-chain horizons: deviations from Boltzmann form appear first at low energies and late times, and can be summarized by an effective IR scale E_IR(L,BC) governed by chain length, boundary conditions, and outer-region box size; it further claims mitigation by increasing L or using absorbing/impedance-matched boundaries to push E_IR down and delay reflection-induced contamination, thereby widening the usable energy/time window for extracting thermality and entanglement growth.

**What is Novel:** The existence of finite-size–induced low-energy deviations and a rough IR cutoff scale is not new at the statement level, because it is already explicitly reported (though not necessarily framed as a general “law”) in a key curved-spacetime-to-hopping-chain simulation paper. What remains more novel is the stronger universality/ordering claim (IR-first and late-time-first as the generic earliest breakdown mode across implementations), the explicit emphasis on boundary-condition dependence as a primary control knob, and the prescription that impedance-matched/absorbing boundaries systematically extend the thermal window; however, the superconducting-chain evidence showing larger high-energy deviations than low-energy deviations weakens the universality of the “IR-first” ordering as stated.

### Explanatory / Mechanistic — Explicit Peripheral

**What is Known:** Across related analogue-gravity and lattice-horizon works, finite size and non-absorbing boundaries are known to cause reflections and late-time contamination, and more generally finite observation regions/times can limit access to long-wavelength (low-energy) modes. One closely aligned curved-spacetime-to-hopping mapping paper explicitly connects finite outer-region size, boundary prescriptions, lattice parameters, and evolution time to an infrared cutoff scale and interprets deviations from thermality using that linkage.

**What is Introduced:** The statement asserts an ordered causal mechanism: in finite horizon-encoded hopping chains, the first deviations from a Boltzmann line occur at low energies and late times because boundary reflections and finite outer-region extent impose an effective IR scale E_IR(L,BC). It further proposes a control law: increasing chain length L or using absorbing/impedance-matched boundaries lowers E_IR and delays reflection-driven contamination, expanding the energy/time windows over which exponential spectra and clean entanglement-growth signals can be extracted.

**What is Novel:** The main non-novelty evidence is that an explicit finite-size/IR-cutoff explanation with dependence on implementation details is already present in the discrete curved-spacetime mapping work (even if not always treated as the headline contribution). Relative to several other lattice-horizon and analogue-Hawking papers that mention reflections or finite regions only qualitatively, the specific 'IR-first' breakdown framing and the explicit mitigation prescription are typically not stated, but appear largely derivable from standard mode-quantization/reflection-time reasoning rather than constituting a wholly new mechanism.

### Unification — Derivable Unstated

**What is Known:** Across the assessed set, several works already treat (i) Hawking-like thermality as a near-horizon, surface-gravity/gradient-controlled effect in analogue gravity, and (ii) explicit mappings from static 1+1D curved-spacetime field dynamics to site-dependent nearest-neighbor hopping chains; individual studies then show approximately exponential outgoing/transmitted spectra in specific finite lattice realizations. However, these papers mostly present platform-specific demonstrations or broad continuum “horizon robustness” arguments, rather than an explicit, portable law about how finite size and reflections systematically degrade the apparent thermality window.

**What is Introduced:** The statement elevates finite-length/boundary effects into a general, cross-implementation rule: in horizon-encoded hopping chains with open boundaries and finite exterior region, deviations from a Boltzmann line appear first in the IR and at late times due to an effective IR scale EIR(L,BC) set by chain length, boundary conditions, and outer-region cutoff, and the thermality/entanglement-extraction window can be predictably widened by increasing L or using absorbing/impedance-matched boundaries.

**What is Novel:** Given that the horizon→hopping mapping and near-horizon control of effective temperature are already explicit and central in at least one broad mapping paper, and that specific experiments/simulations already show exponential spectra in finite chains, the proposed “IR-first/late-time breakdown with a tunable EIR(L,BC) and reflection-delay prescription” looks like a synthesized unifying articulation of standard finite-size/reflection physics applied to these mappings. In the provided assessments, this rule is not identified as an explicitly stated, established principle in the cited works; it appears instead to be a natural, largely derivable but previously unstated cross-paper generalization.

### Generalization / Scope Expansion — Derivable Unstated

**What is Known:** Across the assessed literature, (i) Hawking/Unruh-like approximate thermality and sensitivity to cutoffs/finite-volume/reflections are established in continuum gravity/field-theory and continuum analogue-gravity discussions, and (ii) discrete simulations/experiments commonly acknowledge that finite discretization/finite chain length and boundaries affect how well a continuum thermal picture is reproduced. However, an explicit, general, statement-level law for horizon-encoded nearest-neighbour hopping chains that specifies an IR-first breakdown governed by a tunable scale E_IR(L,BC) and a bounded time/energy window of apparent thermality is not consistently presented as established knowledge in these papers.

**What is Introduced:** The statement introduces an operational scope claim tailored to finite, horizon-encoded hopping chains: deviations from P_out(E) ∝ exp(−E/T_eff) arise first at low energies and at late times, with the onset controlled primarily by chain length and boundary conditions via an effective IR scale E_IR(L,BC) and reflection times. It further claims that increasing L or using absorbing/impedance-matched boundaries systematically lowers E_IR and delays reflection contamination, widening the extractable thermal (and entanglement-growth) window in numerics/experiments.

**What is Novel:** Relative to the continuum-focused papers in the set (firewalls/replica wormholes/QES/scrambling/analogue-fluid reviews), the discrete, device-facing scope extension to finite nearest-neighbour hopping chains plus the explicit IR-cutoff/window language is not present and functions as a genuine scope expansion. Relative to the most directly related discrete curved-spacetime and superconducting-chain works, finite-size/boundary effects are discussed but typically not elevated into a generic, ordering-specific (IR-first, late-time-first) law with an explicit controllable E_IR(L,BC); thus the contribution is best characterized as a synthesis/generalization that is plausibly inferable from standard finite-size/reflection physics but not established as a recognized result across the literature.

### Constraint / Limitation — Explicit Peripheral

**What is Known:** In the most directly relevant horizon-encoded hopping/chain literature, finite size, open/reflecting boundaries, and outer-region cutoffs are explicitly recognized to cause late-time reflection contamination and to limit the temporal window and spectral fidelity of an extracted Hawking-like exponential/thermal distribution; practitioners sometimes choose readout times specifically to avoid boundary effects. Several related analogue-gravity and curved-spacetime simulation works also explicitly note low-frequency/long-wavelength fragility and finite-window/finite-size artifacts, though often as caveats rather than as a central, quantified law.

**What is Introduced:** The statement elevates these known finite-size issues into a specific operational constraint: deviations from Boltzmann behavior should emerge first in the infrared (low energies) and at late times, governed by an effective IR scale E_IR(L,BC) controlled by chain length, boundary conditions, and outer-region box size. It also asserts concrete mitigation prescriptions—making L larger and/or using absorbing/impedance-matched boundaries—to lower E_IR and extend the usable energy/time window for thermality and entanglement-growth extraction.

**What is Novel:** The generic limitation (finite size and reflections spoil late-time signals) is not novel relative to key hopping-chain Hawking experiments and some simulation-focused papers where these constraints are already explicit. The more specific packaging as an IR-first breakdown with an explicit, tunable scale E_IR(L,BC) and boundary-engineering prescriptions appears only sporadically: at least one curved-spacetime many-body simulation paper already discusses an effective IR scale tied to L/d and recommends increasing L/engineering boundaries (making this formulation largely prefigured), while many other papers lack this quantified, IR-first framing (where it is better viewed as a synthesis/standardization of scattered caveats).

### Conceptual Reframing / Abstraction — Derivable Unstated

**What is Known:** In the most directly relevant lattice analogue-gravity line (superconducting/XY or fermionic hopping chains implementing 1+1D curved-spacetime Dirac/field dynamics), the metric-function-to-site-dependent-nearest-neighbor-hopping encoding and the interpretation of Hawking-like thermality via a horizon and a local gradient/surface-gravity analogue are already explicit and treated as core conceptual machinery. This establishes that the broader “horizon-encoded hopping” lens itself is not novel with respect to that subliterature.

**What is Introduced:** The statement adds an operational finite-size organizing rule: in finite open chains, breakdown of apparent Boltzmann spectra is expected to onset first in the IR (low energies) and at late times due to an effective IR scale E_IR(L,BC) controlled by chain length, boundary conditions, and outer-region cutoff, with mitigation via increasing L or using absorbing/impedance-matched boundaries to suppress reflections. It also ties this IR-first deviation pattern to practical extraction windows for exponential spectra and inside/outside entanglement growth in experiments/numerics.

**What is Novel:** Across the aggregated assessments, the closest prior lattice papers already supply the metric↔hopping/horizon framework (so that part is established), but they do not appear to have elevated a named, general “IR-first breakdown via finite-size reflections/cutoffs” rule with an explicit E_IR(L,BC) control-parameter summary as a standalone organizing principle. The most supported novelty is therefore a higher-level articulation/packaging of finite-size deviation phenomenology that is plausible to derive from existing finite-chain physics and the established mapping, rather than a clearly documented, previously established claim in the core lattice papers.

### Empirical Synthesis / Meta-Regularity — Derivable Unstated

**What is Known:** Across the assessed corpus, individual studies report approximately exponential/thermal-like outgoing populations over a finite window and sometimes observe finite-size or mode-structure limitations within a single platform (e.g., discrete Dirac-lattice numerics; trapped/BEC experiments). A review-level synthesis in analogue fluids discusses robustness of Hawking-like thermality and attributes deviations to dispersion/greybody/nonlinear/dissipative effects, but it does not articulate a discrete hopping-chain-specific law that the first systematic breakdown is IR-first and reflection/outer-box controlled.

**What is Introduced:** The statement introduces an across-implementation meta-regularity for finite horizon-encoded hopping chains: departures from Boltzmann behavior should emerge first at low energies and late times due to a finite-size IR scale EIR(L,BC) set by outer-region length and boundary reflectivity. It further claims a controllability/mitigation rule (increase L or use absorbing/impedance-matched boundaries) that predictably lowers EIR and delays reflection contamination, widening the energy/time window over which apparent thermality and entanglement-growth diagnostics are reliable.

**What is Novel:** Relative to the assessed papers, the novel element is elevating scattered single-platform observations into an explicit, portable cross-study scaling/diagnostic claim: an IR-first deviation pattern parameterizable by EIR(L,BC) and systematically improvable by boundary engineering. The least-novel evidence comes from papers that already contain pieces of the story (finite-size/mode limitations and exponential windows within one system), making the overall claim plausibly synthesizable from prior results even though no assessed paper is identified as explicitly stating this specific EIR(L,BC) reflection/IR-first law as established knowledge.

* * *

**Related Artifacts:**

  * [Horizon-Encoded Hopping Universality for Hawking-like Thermality](<../theories/horizon-encoded-hopping-universality-for-hawking-like-thermality.md>)
