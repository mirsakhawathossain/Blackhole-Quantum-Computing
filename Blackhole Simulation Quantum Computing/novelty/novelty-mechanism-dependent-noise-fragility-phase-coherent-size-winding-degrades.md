[<- All artifacts](<../index.md>)

# Novelty: Mechanism-dependent noise fragility: phase-coherent size-winding degrades faster under dephasing than peaked-size teleportation

**Contents:**

  * Dimensions



Assessed theory: [theory-6](<../theories/operator-size-phase-coherence-as-the-mechanism-for-wormhole-teleportation-signal.md>)

### Dimensions

### Phenomenon / Effect — Genuinely New

**What is Known:** Across the assessed wormhole-teleportation/scrambling literature, the size-winding vs peaked-size (thermal-correlator-controlled) distinction is already articulated as two regimes that can both yield teleportation-like signatures, and some experimental/simulation works note that generic noise/Trotterization suppresses absolute fidelity/MI. However, none of the assessed papers explicitly isolate phase-randomization between operator-size sectors as the key noise knob, nor do they compare winding-based vs peaked-size teleportation under matched, controlled dephasing.

**What is Introduced:** The statement introduces a specific, mechanism-discriminating empirical prediction for NISQ implementations: phase-randomizing noise between size sectors (dephasing/phase diffusion/control-phase errors, including Trotter-like phase diffusion) should disproportionately suppress (i) sign-of-μ asymmetry and (ii) MI/fidelity peaks when teleportation relies on coherent size-winding (R(l)≈1 with linear arg q(l)), compared to regimes where teleportation is dominated by peaked-size/thermalization mechanisms without such coherence.

**What is Novel:** In the aggregated evidence, the closest papers establish the two mechanisms and report noise sensitivity in a general sense, but they do not formulate or demonstrate the differential fragility claim as an operational diagnostic (e.g., injected dephasing that selectively kills the winding-mediated signal while leaving peaked-size teleportation comparatively intact). Thus, relative to this set of papers, the mechanism-dependent dephasing fragility is not established and remains a novel, testable effect-level prediction.

### Explanatory / Mechanistic — Derivable Unstated

**What is Known:** Across the most directly relevant SYK/teleportation analyses, traversable-wormhole-style teleportation is already explained as an interference effect that depends on organized operator-size phases (“size winding”) and quantified with size-resolved complex amplitudes (e.g., q(l)/Q_n) and coherence ratios (R(l)/r_n), while alternative teleportation-like signatures can arise from peaked-size/thermalization mechanisms without requiring cross-size phase alignment. These works generally do not propagate explicit, experimentally realistic phase-randomizing noise channels (dephasing/phase diffusion/control or Trotter-like phase errors) through the size-resolved formalism to predict selective degradation of winding-based signals versus peaked-size signals.

**What is Introduced:** The statement makes an explicit causal/mechanistic prediction: because size-winding teleportation relies on phase coherence across size sectors, noise that randomizes relative phases between size sectors should disproportionately suppress the sign-of-μ asymmetry and mutual-information/fidelity peaks in the coherent-winding regime (diagnosed by near-linear arg q(l) and R(l)≈1), compared to regimes where teleportation is dominated by peaked-size/thermalization magnitudes. It operationalizes a mechanism-discriminating test via injected/controlled dephasing (or identifiable phase-diffusion-like errors) and contrasts the expected fragility between the two mechanisms.

**What is Novel:** The underlying intuition that dephasing destroys interference is not new; given the already-articulated role of phase alignment in size-winding, the differential fragility claim is largely a consequence that could be derived from those formalisms but is not typically stated as a named, mechanism-separating prediction. The novelty is therefore mainly in elevating this consequence into a clear, testable, mechanism-dependent noise diagnostic (selective loss of sign-of-μ asymmetry and fidelity peaks under size-sector phase scrambling), rather than proposing a fundamentally new teleportation mechanism.

### Unification — Derivable Unstated

**What is Known:** At least one assessed paper already explicitly and centrally distinguishes two microscopic mechanisms that can generate similar traversable-wormhole/teleportation signatures—(i) phase-coherent operator-size winding and (ii) noncoherent peaked-size/thermalization—and provides size-resolved diagnostics demonstrating both regimes. Other assessed works connect wormhole-teleportation protocols to broader scrambling/decoding language and (in reviews) also discuss the winding vs peak-size distinction, but typically without elevating noise response as the key cross-platform discriminator.

**What is Introduced:** The statement ties the mechanism taxonomy to a specific operational discriminator based on _phase-randomizing_ noise: controlled dephasing/phase diffusion between size sectors should disproportionately erase sign-of-μ asymmetry and mutual-information/fidelity peaks when the signal relies on coherent size-winding (R(l)≈1 and linear arg q(l)), compared to peaked-size/thermalization-dominated teleportation.

**What is Novel:** The unification of mechanisms itself (winding vs peaked-size/thermalization) is not novel given explicit-established prior articulation. What appears novel in aggregate is the elevation of _mechanism-dependent dephasing fragility_ (and associated suppression of sign-of-μ asymmetry) as a general, experimentally actionable diagnostic principle for distinguishing the two mechanisms across NISQ implementations; this is largely a synthesis/extension built on existing mechanism separation rather than a new taxonomy.

### Generalization / Scope Expansion — Derivable Unstated

**What is Known:** Across the provided holography/SYK/teleportation and quantum-simulation papers, NISQ relevance is frequently discussed (finite-N effects, Trotterization, calibration noise, platform feasibility), but typically without a general, mechanism-discriminating prescription that uses tunable phase-randomizing noise to test for operator-size phase coherence or “size-winding.” Some sources (especially the review and NISQ-motivated SYK-teleportation simulations) contain enough ingredients that one could plausibly anticipate that dephasing/phase-diffusion harms interference-based signatures, but they do not elevate this to a standard diagnostic contrasting size-winding vs peaked-size/thermalization mechanisms.

**What is Introduced:** The statement introduces a cross-platform, operational scope expansion: deliberately vary or inject noise that randomizes relative phases between operator-size sectors (dephasing, coherent control phase errors, Trotter-induced phase diffusion) and predict a differential effect—disproportionately suppressing sign-of-μ asymmetry and MI/fidelity peaks when those signatures rely on phase-coherent size-winding (R(l)≈1 and linear arg q(l)) compared to regimes where teleportation-like signals are dominated by peaked-size/thermalization mechanisms without such coherence.

**What is Novel:** In the aggregated evidence, essentially none of the papers explicitly establish this as a general principle or widely recognized experimental diagnostic for mechanism identification in two-sided wormhole-teleportation implementations. The closest countervailing evidence is that it appears inferable from the combination of (i) qualitative NISQ noise/Trotter discussions and (ii) the general understanding that dephasing destroys phase-sensitive interference, making the claim largely derivable rather than wholly unprecedented; however, as a concrete, mechanism-contrastive, experimentally actionable prescription centered on size-sector phase coherence and sign-of-μ asymmetry, it is not stated as such in these works.

### Constraint / Limitation — Derivable Unstated

**What is Known:** Across the assessed SYK/teleportation-facing literature (and reviews), it is already explicitly recognized that teleportation-like signatures (including sign-of-μ asymmetry and mutual-information/fidelity peaks) are not, by themselves, a sufficient certificate of holographic/traversable-wormhole dynamics, because non-holographic dynamics (e.g., commuting/integrable models, peaked-size distributions, or simple thermalization, especially at finite N and with postselection) can mimic these signals. Separately, many papers in adjacent analog-gravity/scrambling-measurement contexts discuss generic coherence fragility under experimental imperfections, but not framed as an operator-size-sector-specific discriminator for wormhole-teleportation mechanisms.

**What is Introduced:** The statement adds a specific, experimentally actionable limitation/diagnostic: when the mechanism is phase-coherent size-winding (R(l)≈1 over dominant support and approximately linear arg q(l)), then phase-randomizing noise between size sectors (dephasing, coherent-control phase noise, and Trotter-like phase diffusion) should disproportionately suppress hallmark observables (loss of sign-of-μ asymmetry and reduction/flattening of mutual-information/teleportation-fidelity peaks) compared to regimes where teleportation is dominated by peaked-size/thermalization mechanisms. It thereby proposes controlled injection or systematic variation/characterization of dephasing as a mechanism-discriminating test, not merely the generic claim that “noise reduces performance.”

**What is Novel:** No assessed paper explicitly formulates or tests this mechanism-dependent, size-sector-phase-specific dephasing fragility as an operational constraint/diagnostic for interpreting NISQ wormhole-teleportation experiments. The closest in-scope antecedents make the non-uniqueness/insufficiency point explicit and contain size-based or interference-based formalisms from which such fragility can plausibly be inferred, but they do not elevate the selective dephasing prediction (and its asymmetric impact on sign-of-μ effects) to an explicit result; thus the aggregate evidence supports the claim as largely derivable in hindsight rather than established.

### Conceptual Reframing / Abstraction — Derivable Unstated

**What is Known:** Within the operator-size/teleportation subliterature, the core abstraction separating “peaked-size” (magnitude-dominated) teleportation-like signals from “size-winding/phase-coherent” mechanisms is already explicit, including size-resolved complex diagnostics that track both magnitudes and phases. Some review-style treatments already discuss size-winding conceptually, though not always with a single prescriptive operational checklist or a noise-fragility discriminator as the main experimental lever.

**What is Introduced:** The statement elevates “mechanism-dependent fragility to phase-randomizing noise” into a primary operational diagnostic: if teleportation relies on phase-coherent size-winding (linear arg q(l) and high R(l)), then injected dephasing/phase diffusion should disproportionately suppress sign-of-μ asymmetry and MI/fidelity peaks compared to regimes where teleportation arises from peaked-size/thermalization. It also packages this into an experimentally actionable probe (vary/characterize dephasing-like noise and compare responses across mechanisms).

**What is Novel:** Against papers that already build the size-basis magnitude/phase framework and explicitly distinguish peaked-size vs size-winding, the added content is mainly an operational emphasis (using dephasing fragility as a discriminant) rather than a new conceptual basis; this looks like a natural consequence of treating winding as an interference resource. Relative to the broader gravity/QI and simulation papers that do not use operator-size phase-coherence as a central lens, the reframing is new, but the strongest prior-art constraint in this set comes from work where the size-winding vs peaked-size distinction is already established.

### Empirical Synthesis / Meta-Regularity — Derivable Unstated

**What is Known:** Across the assessed literature, wormhole-inspired teleportation/scrambling diagnostics (e.g., mutual information/fidelity signatures, OTOC-based probes) are discussed and sometimes demonstrated on small-N simulations and hardware, and some works connect teleportation phenomenology to scrambling/size-distribution behavior. However, these papers generally do not articulate or document a cross-study regularity that _mechanism-dependent_ teleportation signatures (phase-coherent size-winding vs peaked-size/thermalization) exhibit _differential fragility specifically to phase-randomizing noise_ (dephasing/phase diffusion/control-phase errors), nor do they present controlled cross-mechanism noise-injection comparisons establishing such a pattern as “known.”

**What is Introduced:** The statement introduces a testable meta-regularity/diagnostic: teleportation signatures that depend on phase-coherent size-winding should be disproportionately suppressed by noise that randomizes relative phases between operator-size sectors, with an operational marker being the preferential loss of sign-of-μ asymmetry and MI/fidelity peaks under injected dephasing/phase diffusion. It further proposes that varying/engineering dephasing (or depth-induced phase diffusion) can discriminate winding-mediated (holographic/SYK-like) behavior from peaked-size/thermalization-driven teleportation that does not rely on such coherence.

**What is Novel:** Relative to the assessed papers, the specific _cross-mechanism, cross-implementation_ noise-response rule (winding-based signatures being selectively more fragile to phase-randomizing noise than peaked-size/thermalization signatures, with suppression of sign-of-μ asymmetry as a key readout) is not presented as an established empirical synthesis and is not directly supported by an explicit multi-mechanism, controlled dephasing comparison. The strongest “least-novel” evidence is that the general intuition (coherent-interference effects are dephasing-sensitive) makes the claim plausibly derivable from background principles and review-level expectations, but it still appears unstated as a recognized meta-regularity linking _operator-size phase coherence_ to _diagnostic noise fragility_ of wormhole-teleportation signals.

* * *

**Related Artifacts:**

  * [Operator-Size Phase Coherence as the Mechanism for Wormhole Teleportation Signals (refined)](<../theories/operator-size-phase-coherence-as-the-mechanism-for-wormhole-teleportation-signal.md>)
