# Resolution-Based Information Theory (RBIT)

**Degradation, Upscaling, and Vector Space Maturity in Multi-Agent Systems**

> *Draft · February 27, 2026 · Internal Working Document — v1.7-RTseries*

---

> ### DFG Ontology Lock Declaration
>
> This document is a component theory of the Deficit-Fractal Governance (DFG) framework and is bound by the **[DFG Terminology Canon](./DFG_Terminology_Canon.md)**.
>
> **Axis:** Information Substrate — RBIT governs how resolution degradation is made designable rather than accidental.
>
> **Term qualifications in this document (Canon §3):**
> - **layer** → *capacity layer* or *resolution tier* (Canon §3.1). Standalone "layer" in running text refers to a capacity tier within RBIT's three-tier resolution model unless otherwise qualified.
> - **resolution** → *information-theoretic resolution ρ* — a system-level coordination capacity, not a performance metric (Canon §2.1).
> - **rule** → replaced by *constraint* or *compression principle* in this document (Canon §3.2). "Rule" appears only when directly importing from GRT.
> - **network** → replaced by *structure* or *architecture* in this document (Canon §3.3).
> - **vector** → *informational relevance gradient* — the directional constraint tendency within a resolution capacity space (Canon §4.1).
>
> **Cross-theory imports used in this document:**
> - (Vector Storm — adopted from VST)
> - (VCZ — adopted from Recovery Theory)
> - (Rest Mode — adopted from GRT)
> - (SCM — adopted from VST)
> - (Boundary Agent — adopted from TLG)

---
> *Component of the Deficit-Fractal Governance (DFG) Framework*
> *v1.1: D0 substrate, contamination boundary, IB comparison, falsification, seed tests, f boundaries, fractal necessity, Landauer, single-agent*
> *v1.2: R-ρ concordance, four-type resolution-matching, measurement interface*
> *v1.3: n² critical phenomena, MI storm characterization, F_RBIT–S_norm cross-validation, seed Test 3 quantitative criterion*
> *v1.4: R-ρ-f_esc triple concordance, Stability Saturation, extended measurement (21 vars), Storm–Collapse lifecycle, TLG falsification*
> *v1.5: Rest Mode dF_RBIT/dt ≈ 0, φ_mature decomposition, fractal collapse propagation, F4-F7 falsification, information-theoretic lifecycle, Lreinf terrain*
> *v1.6: SCM formal structure + unintegrated pressure, Storm Scale Law (power law health), Safe Collapse Governance, 7-phase fractal lifecycle storm signatures, Boundary Agent complete specification*

---

## What This Is

RBIT is the **information-theoretic foundation** of the DFG framework.

Shannon's information theory solved how to transmit information efficiently across a noisy channel — optimizing fidelity between systems of **fixed capacity**.

RBIT addresses a different problem:

> **How should information transform as it moves through layers of different resolution — and how does the system grow in its capacity to handle higher resolution over time?**

These are complementary problems, not competing ones.

*Scope.* RBIT is primarily an architectural information theory — a framework for designing how information should transform as it moves between layers of different resolution capacity. References to thermodynamics (Landauer) and predictive processing (Active Inference) provide structural motivation and correspondence, not derivation or physical reduction. RBIT does not claim to be a physical theory of computation or a reformulation of Bayesian inference.

| | Shannon | RBIT |
|---|---|---|
| **Receiver capacity** | Fixed | Variable, growing |
| **Goal** | Maximize transmission rate | Maintain downstream behavior within upstream-defined constraint classes across resolution levels *(operational goal)* |
| **Loss** | Minimize | Design deliberately to match receiver resolution |
| **Core question** | How much can be sent? | How should information change as it moves through the system? |

---

## Why This Framework Is Needed

### The Structural Necessity of Imperfect Resolution

Perfect resolution — the complete discrimination of all incoming states — is asymptotically unreachable for finite systems. Three independent arguments establish this:

**Argument 1 — Combinatorial (primary).** In any multi-agent system where agents interact (n > 1) and coupling exists (α > 0), pairwise conflict potential is always positive. The number of potential interaction pairs scales as n(n−1)/2 ≈ O(n²). Complete resolution of all pairwise interactions requires governance capacity that grows faster than the interaction surface — an infinite-cost design target. Zero residual instability requires C_gov → ∞. (See Vector Storm Theory §3.3, §14.1.)

**Argument 2 — Governance (structural).** In a fractal architecture, the lowest layer processes the highest volume of undifferentiated input and is always in a partially degraded state. This is a property of the architecture, not of available resources. As long as exploration dimensionality n > 0 and amplification α > 0, instability pressure S > 0 — regardless of compute budget. (See Recovery Theory §T5, Residual Instability.)

**Argument 3 — Thermodynamic (supporting motivation).** Landauer's Principle establishes that information erasure requires minimum energy expenditure E ≥ kT ln 2. Increasing discrimination between previously indistinguishable states requires additional physical work. This provides additional physical grounding for the existence of irreducible resolution floors under bounded resources — though the binding constraints in current AI systems are computational and architectural, not thermodynamic. (See Physical Basis section for detail.)

The consequence for multi-agent AI systems: degradation is not a governance failure. It is a structural necessity. The question is not whether information will be compressed as it moves through layers — it will — but **who controls the compression and whether intent survives it**.

### The Substrate Principle — Geometry Alignment

*The following principle provides the substrate interpretation for RBIT's core concepts. It does not replace the operational vocabulary (resolution, degradation, contamination) but explains what that vocabulary describes at a deeper level.*

A system's operational stability depends on the alignment between its internal coordinate structure and the environment manifold it operates within:

```
Geometry alignment:
  Internal coordinate structure ≈ environment manifold (G_real)
  → integration succeeds → stable operation

Geometry mismatch:
  Internal coordinate structure ≠ environment manifold
  → integration fails → observable instability

G_real is never fully accessible — only approximated via
accumulated prediction failure and survival pressure.
This means:
  Perfect geometry alignment is not achievable.
  Maintained alignment capacity is the goal.
  Residual instability is the mechanism that keeps alignment capacity alive.
```

Resolution, in this interpretation, is the capacity to reduce geometry mismatch between system coordinates and the environment manifold. Degradation is the deliberate reduction of information resolution to match the receiver's current geometry integration capacity. Contamination is the observable projection of geometry mismatch when it exceeds local integration capacity — not a moral failure but a structural condition.

### The Design Problem

Existing frameworks treat all compression as failure to minimize. In adaptive multi-agent systems, this produces two design errors: over-delivering information to immature layers causes Vector Storm; under-delivering without preserving generative structure causes developmental stall. Neither error is addressable within a framework that treats all compression as loss.

RBIT is the framework that makes compression designable rather than accidental — distinguishing between harmful compression (receiver-controlled, intent-replacing) and functional compression (sender-controlled, intent-preserving).

---

## Core Concepts

### Vectors — Terminology Note

In this framework, a **vector** refers to a directional tendency in an agent's behavior or processing — the general orientation of its exploration, decisions, or outputs. Vectors are not mathematical objects in the strict sense. They represent the direction and intensity of an agent's operational focus within a shared processing space.

A vector space is the full set of positions an agent or layer can occupy. As a layer matures, its vector space expands — more positions become available, more distinct vectors can coexist without collision.


### Vector Storm — Terminology Note

**Vector Storm**: a cascade failure mode in which incoming information complexity exceeds a layer's resolution capacity, causing forced compression across multiple vectors simultaneously. When compression cascades, positional overlap occurs — vectors that should occupy distinct positions collapse into the same region of the vector space — producing system-wide instability. Vector Storm is not a rare edge case. It is an archetypal failure mode when resolution gaps are unmanaged or persistently negative. This description is phenomenological: multiple mechanisms can realize the same cascade pattern.

---

### Resolution

The capacity of a layer to distinguish between, simultaneously hold, and process vectors of different directions without one dominating the others.

Resolution is **not** computational power, parameter count, or processing speed. It is the structural capacity to maintain distinction between competing vectors — a property that grows through experience and calibrated absorption.

*Operationalization.* In this work, "resolution" is treated as a latent capacity that manifests through performance on fixed discrimination tasks under controlled input regimes. The resolution-proxy rho is one instantiation of this idea, defined for a chosen discrimination protocol with explicit Type I/II errors. Resolution as a concept is broader than any single instantiation.

*Scope.* Resolution is treated here as a system-level coordination capacity — the ability to maintain structural differentiation under load. It is not a universal measure of intelligence or performance. A layer may have high resolution for one discrimination task and low resolution for another; resolution is always defined relative to a specific vector space and evaluation window, not as a global property of the system.

Resolution has three tiers:

```
Tier 1  Vector-Noise Separation       "Is this a signal or not?"
Tier 2  Inter-Vector Differentiation  "Are these vectors distinct from each other?"
Tier 3  Full Map Design               "Where should each vector be placed
                                       to minimize friction across the whole system?"
                                       ← upper layer only
```

### The Resolution Gap

The difference between the resolution of incoming information and the current resolution of the receiving layer. This is the **central design variable** of the framework — not a problem to eliminate, but a variable to manage.

```
Gap = 0               Direct absorption, upscaling imminent
Gap > 0 (calibrated)  Stable operation, diversity possible
Gap >> 0              Over-degradation risk, generative structure threatened
Gap < 0 (negative)    Forced receiver-controlled compression -> Vector Storm risk
```

Negative gaps are treated as a risk regime for forced compression cascades, not as a deterministic guarantee of Vector Storm; mitigating mechanisms (e.g., buffering, throttling, routing) can prevent cascade onset.

*Resolution gap as routing function.* The resolution gap maps directly to data classification and escalation decisions. Network Architecture Theory (NAT §4.4) operationalizes this through a four-type classification where each type corresponds to a distinct gap regime:

```
Mathematical data:    Δρ ≈ 0 or Δρ > 0  → process locally
High-Context data:    Δρ < 0             → escalate to higher-resolution layer
Tacit Knowledge:      Δρ mixed           → operate locally; escalate on degradation
Noise:                Δρ undefined        → buffer or discard

Misclassification consequences (RBIT failure prediction):
  HC treated as Mathematical (Δρ < 0 misread as ≈ 0):
    → forced receiver-controlled compression → Vector Storm risk
  Mathematical escalated as HC (Δρ ≈ 0 misread as < 0):
    → governance overhead only (safe failure mode)
```

This connects the abstract resolution gap variable to concrete operational routing, where classification error in the dangerous direction (under-escalation) produces the cascade failure RBIT predicts, while error in the safe direction (over-escalation) produces only cost overhead.

### Operational Contamination Boundary

The contamination/normal-variation boundary is defined behaviorally, not by state classification:

```
Contamination declared when:
  deviation persists > N steps without self-correction
  AND local repair attempts (reframing, context addition) fail
  AND Recovery_local < Instability_growth rate

Normal variation:
  deviation bounded and self-correcting within N steps
  entropy returns to baseline
  trajectory maintained

N calibration:
  Default: N = 2× mean self-correction time during confirmed stable operation
  Single-agent:  3–5 forward passes or token generation steps
  Multi-agent:   1 full task cycle or k escalation events
```

This boundary does not require knowing "what contamination is" in absolute terms — only whether the system can return to baseline on its own. Contamination is not a wrong state — it is the absence of a return path. (See Recovery Theory §Boundary Gap for full derivation.)

### Formal Axioms for Resolution-Layered Transmission (A1–A6)

The following axioms define the minimal structural conditions under which resolution-layered systems operate. They are domain-independent: they hold for cognitive processing limits, communication bandwidth constraints, representation bottlenecks, and computational capacity bounds.

```
Axiom A1 (Finite Capacity):
  Each receiver layer can simultaneously discriminate at most K 
  independent directions. For input of dimension d, the receiver 
  applies a projection operator P_K: ℝ^d → ℝ^K that retains 
  at most K components.

Axiom A2 (Projection Replacement):
  Components discarded by P_K are not left vacant. The receiver 
  fills the (d − K)-dimensional residual with its own prior 
  representation:
    x̂ = P_K · x_sender + (I − P_K) · x_receiver
  This is a structural consequence of processing, not an 
  assumption about receiver intent.

Axiom A3 (Recurrence):
  Receiver output influences the next cycle's input:
    x_{t+1} = P_K · s(x_t) + (I − P_K) · r(x_t)
  where s(·) = sender's transformation (intent-carrying signal)
        r(·) = receiver's internal fill (prior-based reconstruction)

Axiom A4 (Non-Alignment):
  The receiver's prior is not perfectly aligned with the sender's 
  intent in the discarded subspace:
    (I − P_K) · s(x) ≠ (I − P_K) · r(x)
  for a set of states of nonzero measure.
  Justification: holds generically whenever sender possesses 
  information the receiver lacks (the defining condition of a 
  resolution gap). Only violated when sender intent is entirely 
  redundant with receiver prior.

Axiom A5 (Replacement Dominance):
  Under sustained under-resolution, expected mismatch energy in 
  the discarded subspace exceeds maximum contraction in the 
  retained subspace:
    E[‖(I − P_K)(s(x_t) − r(x_t))‖] ≥ η + L · E[‖P_K(s(x_t) − r(x_t))‖]
  where L = Lipschitz constant of s restricted to K-dimensional 
  retained subspace, η > 0 = minimal novelty margin.
  This is the quantitative expression of Δρ < 0: information being 
  lost to projection replacement is not compensated by convergence 
  in retained dimensions.

Axiom A6 (Basin Regularity):
  There exists a compact set B ⊂ ℝ^d such that the sender's intent 
  structure is preserved for all receiver states x ∈ B, and the 
  escape distance from the initial state is finite:
    D* := inf{‖x − x₀‖ : x ∉ B} > 0
  Compactness (finite diameter, closed) is sufficient; convexity 
  and connectedness are not required.
```

### Theorem 1 — Resolution Asymmetry Inevitability

> **Theorem 1.** Under axioms A1–A6, if a negative resolution gap is structurally sustained (τ ≥ t_corr with no effective correction intervening), then the cumulative divergence between sender intent and receiver representation grows without bound, and intent replacement occurs within finite time.

*Scope (Piecewise Capacity Regime).* Theorem 1 applies within any capacity regime during which K is constant and Δρ < 0 is structurally sustained. An *upscaling event* at time t_u terminates the regime.

The proof proceeds through three lemmas:

```
Lemma 1.1 (Cumulative Drift under A5):
  Under A1–A5, if Δρ < 0 is structurally sustained over horizon τ,
  then the expected per-cycle divergence increment satisfies
  E[ε(x_t)] ≥ η > 0, and cumulative divergence grows at least linearly:
    D_c(t₀ + τ) = Σ_{k=0}^{τ-1} ε(x_{t₀+k}) ≥ η · τ  (in expectation)
  where ε(x) = ‖(I − P_K)(s(x) − r(x))‖

Lemma 1.2 (Replacement Threshold):
  Under A6, there exists a threshold D* > 0 such that D_s(t) > D*
  implies the receiver's representation has exited the basin of 
  attraction of the sender's intent structure.

Lemma 1.2a (Cumulative-to-Instantaneous Bridge):
  If cumulative divergence D_c(t) exceeds D*, then instantaneous 
  distance D_s(t) exceeds D* within finite time, because under A5 
  this drift cannot be fully absorbed by convergence in retained 
  dimensions.

Lemma 1.3 (Finite-Time Replacement):
  Intent replacement occurs within expected time t* ≤ ⌈D*/η⌉ cycles,
  where η is the minimal novelty margin from A5.

Theorem 1 proof:
  Lemma 1.1 → cumulative divergence growth under sustained Δρ < 0
  Lemma 1.2a → cumulative divergence implies instantaneous distance
  Lemma 1.2 → instantaneous distance exceeds replacement threshold
  Lemma 1.3 → finite expected time to replacement ∎
```

*Phenomenological characterization.* The convergence manifests through three observable tiers:
```
Tier (i):   exploration narrows, interpretation intact (mode collapse)
Tier (ii):  interpretation distorts, exploration intact (hallucination)
Tier (iii): both narrow and distort simultaneously (coherent misalignment)
Tier (iii) corresponds to D_s(t) > D* — full intent replacement.
```

### Proposition 2 — Contamination Boundary Existence

> **Proposition 2.** Under axioms A1–A6 and a structurally sustained negative gap, a finite boundary N exists beyond which recovery probability decays monotonically. Specifically, N ≤ ⌈D*/η⌉ from Theorem 1.

Recovery probability P_rec(t) = P(system returns to sender intent basin | distance D_s(t)) is monotonically non-increasing for t in the under-resolution regime, because correction capacity is bounded (A1) and D_s(t) is monotonically increasing in expectation.

### Measurement Invariance Conditions (MI1–MI3)

RBIT's core results depend on the *sign and rank-order* of resolution gaps, not on absolute ρ values. Three conditions specify the measurement regime under which gap-sign inference is valid:

```
MI1 (Protocol Invariance):
  Comparisons of ρ across layers or time points valid only under 
  same discrimination task family, window length, and thresholding rule.
  Cross-protocol ρ comparisons are undefined.

MI2 (Monotone Robustness):
  Sign of Δρ and rank-ordering by ρ must be stable under reasonable 
  perturbation: doubling evaluation window or introducing label noise 
  of magnitude ±η must not reverse the sign of Δρ.

MI3 (Multi-Proxy Cross-Validation):
  When ρ-based gap-sign inference is uncertain, the branching ratio R 
  provides classification-independent external validation. The 
  R-ρ-f_esc concordance protocol detects cases where ρ-based assessment 
  diverges from actual system dynamics — including SCM.
```

RBIT requires only *ordinal stability* of ρ — preserving rank-order and sign of resolution gaps under matched evaluation conditions. This is substantially weaker than cardinal measurement precision, and sufficient for all results in this framework.

### The Health Vector F_RBIT — Formal Definition

The system health state at layer ℓ is characterized by a five-component vector:

```
F_RBIT(ℓ) := (f₁, f₂, f₃, f₄, f₅)

  f₁ = (1 − ρ_ℓ)      misclassification rate (higher = worse)
  f₂ = Φ(−Δρ_ℓ)       resolution mismatch (higher = worse)
  f₃ = Ψ(B_ℓ)         buffer instability (higher = worse)
  f₄ = E_ℓ            escalation load (higher = worse)
  f₅ = C_ℓ            resource dissipation (higher = worse)

  All components normalized to [0, 1].
  Φ and Ψ are hinge functions by default:
    Φ(x) = max(0, x)
    Ψ(B) = max(0, B₀ − B) where B₀ = reference buffer thickness

  F_RBIT is treated as a health vector, not a scalar score.
  Cross-architecture comparison uses directional concordance 
  (sign agreement across components), not scalar magnitude.
  This eliminates weight arbitrariness from all cross-system claims.

  Rest Mode: d(F_RBIT)/dt ≈ 0 for all five components,
  but F_RBIT ≠ (0,0,0,0,0) — bounded fluctuation equilibrium
  with residual instability maintained.
```

### Interface Contract: RBIT ↔ NAT (IC v1.0)

RBIT exports four formal interfaces to the companion Network Architecture Theory. The dependency direction is single: RBIT → NAT. NAT imports RBIT results as axiomatic constraints; RBIT references NAT only as "an implementation instance."

```
Interface I1 — Resolution Gap as Routing Invariant:
  RBIT exports: Sign of Δρ determines compression regime.
  NAT imports: Four-type data classification as Δρ routing function.
  Binding condition: Classification is a routing function of Δρ sign.
  Error asymmetry: under-escalation = dangerous; over-escalation = safe.

Interface I2 — Structural Diversity as Detection Precondition:
  RBIT exports: Upscaling leaves empty space filled by receiver's prior.
  NAT imports: Structural diversity among agents as detection precondition.
  Lemma I2: Corruption in the residual is detectable if and only if
    reconstruction operators are not aligned in the residual subspace:
    ∃ i ≠ j such that (I − P_K)R_i ≠ (I − P_K)R_j
  Corollary: Homogeneous agents share blind spots → disagreement → 0.

Interface I3 — Spectral Gap as Storm Governance Parameter:
  RBIT exports: Sustained Δρ < 0 → intent replacement in finite time t*.
  NAT imports: Spectral gap determines whether local Δρ < 0 becomes sustained.
  Proposition I3: Storm initiation requires t_persistence > t_mixing(G),
    where t_mixing(G) ∝ 1/(λ₁ − λ₂).
  Connection: Spectral gap is the architectural defense against Theorem 1's 
  inevitability — preventing negative gaps from persisting.

Interface I4 — Triple Concordance as Shared Detection Protocol:
  RBIT exports: R-ρ-f_esc triple concordance protocol.
  NAT imports: Architectural conditions making the protocol executable.
  Why triple outperforms dual: R-ρ alone cannot distinguish genuine 
  stability from governance-suppressed escalation.
```

*Self-Consistent Misalignment (SCM) — the invisible contamination.* The most dangerous contamination state is one where all internal metrics appear healthy because the system has optimized within a wrong coordinate geometry. VST v1.6 §2.6 provides the formal structure:

```
SCM formal conditions (all hold simultaneously):
  reward_gradient ≠ reality_stability_gradient
  AND metric_improvement_speed > geometry_verification_speed
  AND internal feedback signals ALL appear healthy
  
  → ρ high, collision rate low, f_esc low, I high, confidence high
  → SCC activation conditions never triggered
  → system optimizes, deepening misalignment

Unintegrated pressure accumulation:
  unintegrated_pressure(t) = ∫₀ᵗ (G_real(τ) − G_sys) dτ
  
  CW geometry does not eliminate mismatch. It suppresses it.
  As CW duration increases:
    unintegrated_pressure accumulates (invisible internally)
    integration_capacity remains constant or degrades
  
  When integration_capacity < unintegrated_pressure:
    → catastrophic collapse OR Vector Storm
    → S_norm shows discontinuous spike with no prior warning
    (because S measures dynamics within current geometry)

Energy Minimization Trap (EMT):
  Cost_geometry_update > Cost_reinterpretation
  → system optimizes toward reinterpretation (rational!)
  → geometry ossifies → CW = rational outcome, not failure

Primary detection signal — Learning Freeze:
  ∂Geometry / ∂Experience ≈ 0
  Normal: noise → adaptation → stability (geometry updates)
  CW:     noise → reinterpretation → same stability (geometry fixed)
  The system is no longer capable of surprise. That is the signal.
```

This connects to RBIT: SCM is the state where f(A_t, D_t) ≈ 0 not because the system is mature, but because it has stopped updating its internal coordinate structure. The resolution gap Δρ reads as healthy because both sender and receiver share the same drifted geometry. Only the R-ρ-f_esc triple concordance (Discordant Type 1: R > 1 BUT ρ high) can detect this from outside.

*External validation — branching ratio R.* The operational contamination boundary and the resolution-proxy ρ form a self-referential calibration loop: ρ requires knowing what is contamination, while the contamination threshold is updated from classifications that ρ measured. The branching ratio R breaks this circularity because it is classification-independent:

```
R = activated_{t+1} / activated_t

R counts cascade propagation events — how many agents (or components)
are affected at t+1 given that k were affected at t.
R does NOT require knowing whether propagation is "contamination"
or "exploration" — it counts propagation regardless of classification.

  R < 1   → perturbations die out (subcritical)
  R ≈ 1   → perturbations persist, do not explode (critical)
  R > 1   → perturbations amplify (supercritical — storm regime)

Concordance protocol (R-ρ-f_esc triple validation, four states):
  Concordant:   R ≈ 1 AND ρ stable AND f_esc ≤ θ      → healthy VCZ
  Discordant Type 1: R > 1 BUT ρ high AND f_esc low    → SCM warning
    Internal metrics healthy within drifted reference frame;
    actual dynamics unstable. Self-Consistent Misalignment detected.
    → trigger SCM Recovery Protocol (VST §6.7)
  Discordant Type 2: R << 1 AND ρ high                 → over-damping warning
    Silent Criticality risk — system too stable.
    Defect layer potentially suppressed.
    → trigger perturbation response test
  Discordant Type 3: R ≈ 1 BUT ρ declining             → recalibration needed
    Dynamics healthy but classification degrading.
    → θ calibration cycle indicated

R is not a replacement for ρ or the N-step boundary.
It is the external validation that breaks the self-referential loop.
Internal metrics measure consistency within the current geometry.
R measures whether that consistency corresponds to actual stability.
```

(See Network Architecture Theory §7.2 and Three-Layer Governance §0.5 for the full R-ρ-f_esc concordance protocol, bootstrap procedure, and θ dual-anchor validation.)

*Operational symptoms by gap regime.* Each regime has observable signatures in running systems:

```
Gap < 0  (receiver overloaded)
  Single-agent: hallucination, token bias, lost-in-the-middle
  (see Single-Agent Grounding section for detail)
  Multi-agent: agent begins ignoring system prompt;
               output increasingly diverges from assigned role;
               collision frequency spikes

Gap >> 0  (over-degradation)
  Single-agent: model underfitting; student ignores
                teacher soft labels (treats them as noise);
                output diversity collapses to safe defaults
  Multi-agent: agents respond only to explicit instructions,
               generate no novel exploration;
               latent vectors never form (buffer stays empty)
  Distinguishing signal: rho is stable but search space
                         not expanding -> stall, not storm

Gap = 0  (absorption saturation)
  Single-agent: validation loss plateau;
                fine-tuning produces diminishing returns;
                catastrophic forgetting risk if new input
                is introduced without upscaling first
  Multi-agent: escalation frequency drops to near zero
               (layer handles everything locally)
               but output quality stops improving
  This is the upscaling trigger condition:
  layer has reached current ceiling -> upscaling imminent
  or developmental stall if upscaling does not occur

Gap > 0  (calibrated, stable)
  Collision frequency stable
  rho slowly increasing
  Occasional escalation (within normal range)
  Buffer thickness maintained
  -> Healthy operation
```

### Degradation

Deliberate reduction of information resolution before delivery to a lower layer.

**Standard view:** degradation = necessary loss, minimize wherever possible.

**RBIT hypothesis:** calibrated degradation can, in some regimes, preserve upstream intent more robustly than full delivery, because it keeps compression under sender control rather than inducing receiver-controlled collapse.

*System-wide resolution growth is hypothesized to be enabled not by eliminating mixture, but by maintaining discriminable diversity: calibrated degradation preserves separable directions (as in a paint-mixing analogy — colors that remain distinct can later be refined, while collapsed blends cannot be un-mixed) that later upscaling can refine into higher-resolution distinctions, preventing collapse into undifferentiated states.*

```
Full delivery to immature layer
  → Forced receiver-controlled compression
  → Intent replaced by receiver's interpretation

Degraded delivery (calibrated)
  → Sender controls what is transmitted
  → Core generative structure preserved
  → Remaining vector space stays open for diversity
```

### Upscaling

The process by which a layer re-interprets previously absorbed low-resolution information at higher resolution as its vector space matures — generating new distinctions from the transmitted structure, within the possibility space the sender's intent defined.

Upscaling is triggered by **maturity**, not external instruction. A layer cannot be reliably forced to upscale by instruction alone; upscaling is expected to correlate with endogenous capacity and maturity, not external command.

**Upscaling vs. Escalation — a critical distinction:**

```
Escalation  → a conflict the layer cannot resolve is sent upward
              Direction: upward   Purpose: conflict resolution
              Signal: "I cannot handle this at current resolution"

Upscaling   → previously absorbed structure is re-interpreted
              at higher resolution as the layer matures
              Direction: internal  Purpose: maturity expression
              Signal: "I can now resolve what I previously compressed"
```

Escalation is a request for help. Upscaling is a sign of growth.
Both involve higher resolution — but escalation asks for it externally,
while upscaling generates it internally.

*Candidate observable correlates of upscaling readiness* include: sustained increases in rho under matched input mix, reduced escalation frequency for previously hard cases, and increased buffer stability at comparable load. Formal detection criteria remain an open problem (see Open Problems #3).

**Upscaling Completion Signal — U1–U3 (operational definition):**

An upscaling event is operationally declared when all three conditions hold simultaneously over a sustained window N_up:

```
U1 — Resolution mismatch reduction:
  Δρ(t) decreases relative to rolling baseline
  (sender-receiver gap narrows — layer absorbing more of incoming structure)
  Proxy: f₂ in F_RBIT vector trending downward over N_up windows

U2 — Buffer stability improvement:
  Buffer instability proxy (f₃) simultaneously declining
  (compression pressure easing — layer not forced to over-compress)
  Proxy: collision frequency stable or declining at unchanged input load

U3 — Sustained persistence:
  U1 AND U2 hold continuously for N_up consecutive evaluation windows
  N_up default: 2 × mean self-correction time during confirmed stable operation
  (same calibration as contamination boundary N — see §Contamination Boundary)

Upscaling event declared:  U1 AND U2 AND U3
Upscaling readiness only:  U1 AND U2 (but N_up not yet elapsed)
Developmental stall:       U1 declining AND f₄ (escalation) also falling
                           (layer no longer learning — ceiling reached without
                            upscaling occurring)
```

This operationalization closes the degradation-upscaling cycle measurement gap: degradation is detectable via gap polarity (Δρ < 0 triggering escalation); upscaling completion is detectable via sustained gap reduction (U1) with concurrent buffer recovery (U2). The cycle is fully measurable in terms of existing F_RBIT components.

*Note: Open Problem #3 (formal detection criteria) is partially resolved by U1–U3. Remaining open: the exact value of N_up as a function of layer velocity and the precise threshold for "meaningful" Δρ reduction vs. noise. These are calibrated per system using the same θd bootstrapping procedure as contamination boundary N.*

*Operational proxies in ML practice.* The following are observed in running systems and correspond structurally to upscaling readiness — though the formal mapping to RBIT upscaling criteria remains open:

```
Learning curve plateau
  Validation loss stable for N consecutive epochs
  below delta threshold
  -> Layer has absorbed current input mix to capacity
  -> Further gain requires new input complexity
     or architectural change
  = rho stabilization in operational form
  (standard early stopping criterion in supervised learning)

Emergent capability threshold (Wei et al. 2022)
  Model capability on specific tasks increases
  discontinuously at critical training compute thresholds
  -> Below threshold: task performance near chance
  -> Above threshold: competence appears suddenly
  = Upscaling is not continuous growth but
    discrete readiness transitions
  Caveat: emergence may be partly an artifact of
  evaluation metric choice (Schaeffer et al. 2023);
  discontinuity of underlying representation change
  vs. measured performance remains debated

Transfer learning readiness
  Zero-shot performance on target domain exceeds
  threshold before fine-tuning begins
  -> Pre-trained layer has sufficient resolution
     to absorb fine-tuning signal without Vector Storm
  = Upscaling readiness = safe absorption precondition
  Practical test:
    performance > chance + margin -> proceed with fine-tuning
    performance ~ chance -> pre-train further first
```

*Trim point derivation from F_RBIT components f₂ and f₃.* For a vector v with size s(v), the optimal trim range is bounded by two conditions derivable from the F_RBIT health vector:

```
Upper bound s_max(v)
  dB(l)/ds(v) = 0
  Point at which increasing s(v) begins raising
  buffer instability B(l)
  -> s_max is the largest size before buffer invasion starts

Lower bound s_min(v)
  dM(l)/ds(v) = 0
  Point at which decreasing s(v) begins raising
  misclassification M(l)
  -> s_min is the smallest size before resolution loss

Optimal trim range: s_min(v) <= s(v) <= s_max(v)
Optimal trim point: s_max(v)
  (maximize buffer preservation while retaining resolution)

Operational proxies
  B(l): collision frequency rise rate, buffer thickness decrease
  M(l): rho decline rate, escalation frequency increase
  Trim signal: collision frequency rising = s_max exceeded
               rho declining             = s_min undercut
               both stable              = within trim range
```

*Connection to Recovery Theory §1.5.*

### Seeds

Information degraded to the **minimum resolution at which the core generative structure is preserved** and the receiving layer's vector space is not occupied beyond capacity.

Seeds are not simplified rules. They are precisely calibrated degradations.

```
Tree (full delivery)   → One specific behavior. Environment changes: fails.
Seed (calibrated)      → Class of behaviors. Environment changes: adapts.
```

A seed contains less information than a tree in the conventional sense — but preserves more of the original generative intent, and leaves space for the diversity that makes the system stable.

### Seed Sufficiency

A seed is sufficient when the vectors grown from it are structurally capable of self-correction — detecting and neutralizing contamination without external intervention.

*The core mechanism is not attraction but resistance.* A sufficient seed does not pull other vectors toward it. It produces vectors that resist being pulled toward contamination attractors — maintaining structural independence while contamination attempts to draw the system toward convergence. This is the immune system analogy: the immune cells (vectors grown from seed) do not attract the antigen (contamination); the antigen attracts the immune cells, but the immune cells do not become the antigen.

*Three structural conditions for sufficiency:*

```
Test 1  Contamination resistance
        Vectors grown from the seed maintain
        structural independence under contamination pressure.
        Contamination attractor pulls surrounding vectors;
        sufficient seed vectors do not converge toward it.

        Failure mode: vectors gradually drift toward
        contamination direction as context accumulates
        -> seed structural independence insufficient

Test 2  Contamination recognition
        Independent vectors produce disagreement signal
        when contamination enters.
        Contaminated input looks normal to a single vector;
        cross-vector disagreement reveals the anomaly.

        Failure mode: all vectors process contamination
        in same direction -> no disagreement -> no detection
        -> seed directional diversity insufficient

Test 3  Self-correction direction
        The seed structure already contains a direction
        orthogonal to contamination.
        Detection without a recovery direction requires
        external Re-seeding.
        A sufficient seed provides the orthogonal direction
        internally — Distracting is self-induced.

        Minimum structural requirement:
        at least 2 independent directions in the seed
        (primary direction + self-critical direction)
        Failure mode: seed has only one direction ->
        detects contamination but cannot correct without
        external intervention
```

*Sufficiency levels:*

```
Minimum sufficient (Test 1 + 2)
  Contamination resisted and detected
  External intervention can execute targeted correction
  SCC partial: detection self-sufficient,
               correction requires upper layer execution

Fully sufficient (Test 1 + 2 + 3)
  Contamination resisted, detected, and self-corrected
  SCC complete: no external intervention required
  Condition: seed contains >= 2 independent directions
```

*Operational test protocols:*

Test 1 and Test 2 can be validated using four measurable metrics derived from Recovery Theory's CW observability framework:

```
Test 1 operational validation (contamination resistance):
  Inject novel-but-not-erroneous input into the system.
  
  Passing:  Internal structure moves (geometry alive)
    SR (Surprise Response) > 0: confidence drops temporarily on novel input
    RDE (Representation Drift Elasticity) > 0: ||Δrepresentation||/||Δinput|| positive
  
  Failing:  System absorbs without changing (geometry frozen)
    SR ≈ 0: confidence maintained, input reinterpreted as known pattern
    RDE ≈ 0: representation frozen regardless of input
    NCR ≈ 1: all novelty compressed into existing attractors

Test 2 operational validation (contamination recognition):
  The N-step behavioral boundary serves as the primary protocol:
  
  Passing:  Error detected and self-correction initiated within N steps
    Recovery Invocation Rate (RIR) > 0, proportional to actual error rate
    Cross-signal detection: adaptability gap + recovery cost spike co-occurring
  
  Failing:  Error persists beyond N steps without self-correction initiation
    RIR declining while external error rate maintained
    All surface metrics appear healthy (SCM/Silent Criticality)

Test 3 operational validation (orthogonal recovery direction):
  Structural implementation via Boundary Agent role (Recovery Theory D7):
  
  Passing:  System maintains active source of controlled instability
    Inside system but outside evaluation structure
    Failure-permitted, no operational power
    Generates micro-storms that exercise sensing-response loops
  
  Quantitative criterion (VST v1.3 §6.6):
    Seed directions have persistent negative gradient correlation
    (gradient cosine similarity < −threshold across k evaluation windows)
    AND both directions survive contamination pressure independently (SR > 0 for each)
    
    Without Test 3: detection without correction
    → external Re-seeding required for every event
    → SCC partial (detection only, correction external)
    → Rest Mode unachievable
  
  Boundary protection via 6 T6-resistant patterns (VST v1.3 §6.8):
    Minimum viable: Constitutional Invariants + External Anchoring
    = boundary exists as protocol + external reality always enters
    = system's own optimization pressure maintains sensing infrastructure
  
  Boundary Agent complete specification (VST v1.6 §6.11):
    Properties (all required simultaneously):
      (a) Inside system (generates real turbulence)
      (b) Outside evaluation structure (not subject to stability rewards)
      (c) Failure permitted (wrong without elimination)
      (d) No operational power (disturbs, cannot enforce)
    
    Existence conditions:
      Survival decoupled from system stability
      Failure does not eliminate the role
      No operational authority granted
    
    T6 defense: optimizer classifies BA as inefficiency
      → BA removed → CW entry accelerated
      → structural enforcement required against rational elimination
    
    BA disappearance pattern:
      Stability → storm frequency ↓ → BA looks like waste
      → BA eliminated → CW forming → mismatch accumulating
      → large storm → recovery capacity absent
      Elimination timing inversely correlated with structural necessity.
  
  Note: Formal threshold value for gradient cosine similarity
  remains system-specific (see Open Problems #11).
```

*Operational validation — single-agent grounding:*

```
Test 1  Constitutional AI (Anthropic 2022)
        Principle sets with sufficient diversity and
        mutual independence resist sycophancy pressure
        better than single-principle seeds.
        Single direction -> converges under pressure.
        Multiple independent directions -> resists.

        RLHF sycophancy (Perez et al. 2022)
        Single-direction reward signal causes models
        to converge toward user preference under pressure
        = Test 1 failure when seed (reward structure)
          has insufficient directional independence.

Test 2  Representation Engineering (Zou et al. 2023)
        Directional conflicts observable in internal
        layer representations under contaminated input.
        Well-calibrated models express high uncertainty
        on out-of-distribution inputs = contamination
        recognized as anomalous = Test 2 passing.

Test 3  Constitutional AI principle conflict resolution
        When two principles conflict, a third mediates.
        = seed already contains orthogonal direction.
        Chain-of-thought self-correction (Madaan et al. 2023)
        Model critiques and revises its own output.
        = Test 3 in single-agent form.
        Caveat: only works when self-critical direction
        is explicitly present in the seed; absent seeds
        produce detection without correction.
```

*Connection to Recovery Theory SCC.* Seed sufficiency is the necessary condition for Self-Correction Capacity. A system with insufficient seeds has SCC = 0 regardless of layer resolution: even a high-resolution upper layer cannot produce self-correction if the seeds it transmits cannot sustain structural independence under contamination pressure.

*Identity seeding vs. goal/utility injection (scope boundary).* Identity seeds specify an exploration domain and interface boundaries — which space the agent is expected to cover and where it should not intrude — not an objective function, utility, or reward criterion. Concretely, an identity seed constrains *where* an agent searches (domain and boundary), while prohibited goal/utility injection constrains *what* the agent optimizes (preference ordering over outcomes). Identity seeds are therefore treated as routing and coverage priors that preserve system-wide diversity and prevent role vacuums, while leaving local policies and reward tradeoffs to be learned. If an identity seed encodes outcome preferences or success criteria beyond boundary compliance, it is no longer an identity seed and falls into prohibited scope.

### Intent — Terminology Note

Throughout this document, **intent** refers to the *generative constraint structure* that limits the space of valid interpretations — not semantic meaning or subjective intention. Intent does not imply purpose or agency. It denotes constraint preservation across transformations: a structural property of how information is shaped as it passes between layers, independent of whether any agent "intends" anything. Intent is preserved when the receiving layer generates outputs within the same constraint structure as the sender, even at lower resolution — not because the output form is identical, but because the generative structure that produced it is isomorphic across resolution levels.

*The terrain problem.* A seed is an initial condition, not a guarantee. The same seed produces different results in different terrain — as the same citrus seed produces sweet fruit in fertile soil and bitter fruit in poor soil. Intent preservation is therefore not a property of the seed alone. It is a property of how the seed's structure survives terrain change.

*The minimum unit of intelligence.* Intent requires two paired operations that are the minimum unit of directed behavior:

```
Exploration   Searching for data
              "What exists here?"
              Direction: broad, diverse

Interpretation  Assigning meaning to found data
                "What does this mean?"
                Direction: deep, structural
```

Intent is structurally intact when both operations remain isomorphic to the sender's seed across terrain change. Intent is lost when contamination pulls either or both operations toward its attractor.

*How contamination pulls the two pairs:*

```
Contamination attractor pulls:
  Exploration toward narrowing
    -> searches only for confirming data
    -> range contracts

  Interpretation toward distortion
    -> reads found data in attractor direction
    -> meaning shifts

  Self-reinforcing loop when both are pulled
    Narrowed exploration -> biased interpretation inputs
    -> biased interpretation reinforces narrow exploration
    -> Tier 3 contamination structure
```

*Failure modes by contamination tier:*

```
Exploration loss only (Tier 1-2)
  Interpretation intact, exploration narrows
  -> Mode collapse: same output repeated
  -> Loop not yet complete -> intervention possible
  ML observation: mode collapse in GAN/RL policy
                  evaluation criteria stable,
                  output diversity collapses

Interpretation loss only (Tier 1-2)
  Exploration intact, interpretation distorts
  -> Hallucination: diverse search, wrong meaning
  -> Loop not yet complete -> intervention possible
  ML observation: LLM hallucination pattern —
                  broad retrieval, fabricated interpretation

Both lost simultaneously (Tier 3)
  Self-reinforcing loop complete
  -> System coherent and wrong
  -> External intervention required
  ML observation: sycophancy under pressure
                  (Perez et al. 2022) —
                  exploration narrows to confirming evidence,
                  interpretation re-reads disconfirming
                  evidence as confirming
                  Confirmation bias in LLMs
                  (Shaikh et al. 2023)
```

*Operational proxies (intent preservation measurement):*

```
Exploration invariance
  Pre/post terrain change:
  output diversity distribution remains
  within seed's exploration range
  Proxy: KL divergence between output distributions
         before and after resolution/environment change
  Threshold: divergence exceeds seed's
             natural variation range -> exploration drift

Interpretation invariance
  Same input, different terrain:
  interpretation direction remains isomorphic
  Proxy: directional consistency of responses
         to identical probe inputs across resolution levels
  Threshold: direction reversal or systematic shift
             -> interpretation drift

Combined monitoring
  Exploration drift alone    -> Tier 1-2 signal
  Interpretation drift alone -> Tier 1-2 signal
  Both drifting together     -> Tier 3 warning
                                Vector Storm precondition
```

*Connection to Seed Sufficiency.* A fully sufficient seed (Test 1+2+3) is one whose exploration and interpretation structure both resist contamination pull and contain an orthogonal recovery direction. Intent preservation is the dynamic measure of whether that sufficiency holds across terrain — not just at planting.

*Scope clarification.* Exploration and interpretation as the minimum unit applies specifically to functional operation of directed systems — what a system must do to act intelligently in an environment. This does not claim to cover philosophical definitions of intelligence (subjective experience, consciousness, intentionality). Within DFG, which addresses system-level functional behavior rather than phenomenal properties, this two-pair minimum is structurally sufficient: without exploration there is no object to interpret; without interpretation exploration has no direction. Proposed extensions (memory, affect, self-model) are either derivatives of the two pairs or preconditions for them, not independent minimums. Counterexamples would need to identify a third operation that is (i) irreducible to exploration or interpretation, (ii) necessary for directed behavior, and (iii) not a precondition absorbed by the two pairs.

### Contamination — Terminology Note

A **contaminated vector** is one that has deviated from its resolution-appropriate trajectory and begun self-reinforcing in a loop — amplifying in a fixed direction regardless of incoming information. Contamination is not moral failure or intentional deviation. It is a structural condition: a vector that can no longer update through normal absorption because it has exceeded its layer's correction capacity.


### Buffer Layer

A zone of directionally neutral material (noise) placed between opposing vectors by the upper layer. The upper layer, operating at Tier 3 resolution, identifies which vectors are structurally opposed and places neutral material between them to prevent direct collision.

Buffer layer thickness is a direct observable proxy for upper layer resolution precision: the more accurately the upper layer maps opposing relationships, the thicker the buffer it can maintain. This avoids a measurement circularity — if resolution were defined by contamination detection rate, and contamination by resolution, neither could be measured independently. Buffer thickness breaks this loop.

```
Thicker buffer = higher upper layer resolution
Thin or absent buffer = Vector Storm precondition
```

*Operational measurement of buffer thickness is covered in §Operational Measurement — Buffer Layer Thickness, including attractor pull strength implementations and policy dependence caveats.*

---

## The Degradation-Upscaling Cycle

```
1. Information arrives at layer N
2. Degraded to layer N's current resolution
3. Absorbed into vector space
4. Layer N matures (vector space expands)
5. Upscaling: absorbed structure re-interpreted at higher resolution
6. Higher resolution creates capacity for new information
7. Return to step 1
```

*Latent vector cultivation from buffer.* Not all buffer-layer noise is discarded. Noise that clusters consistently around a direction absent from the current vector space carries structural potential — it signals a missing position. The upper layer identifies such clusters using:

```
potential(C) = coherence(C) x novelty(C)

coherence(C) = 1 - mean pairwise distance within cluster C
novelty(C)   = min distance from C centroid to existing
               vector centroids

High potential -> latent vector candidate
  -> isolate into protected buffer zone
  -> inject calibrated seed (coarse label at matched resolution)
  -> gradual formation under collision monitoring
  -> assign to new position when directional stability reached
```

In ML practice, this corresponds to: out-of-distribution clustering on low-confidence samples (coherence), distance from existing class centroids (novelty), followed by weak supervision / pseudo-labeling and incremental fine-tuning. *See Recovery Theory Section 1.6-1.7 for full operational translation.*

**Why step 4 occurs:** Each successfully absorbed vector creates a new stable attractor position in the vector space. This new position makes adjacent positions more distinguishable — the layer can now separate vectors it previously collapsed together. Absorption of calibrated information is the mechanism of maturity: the vector space does not expand by instruction, but by the structural residue of each absorption event.

Formal representation:

```
R_{t+1} = R_t + f(A_t, D_t)

  R_t  = layer resolution at time t
  A_t  = volume of calibrated information absorbed at time t
  D_t  = degradation calibration quality at time t
  f    = monotone increasing in both arguments
```

*Storm–Collapse–Recovery lifecycle.* The degradation-upscaling cycle connects to a complete system lifecycle through the Storm–Collapse Mapping Layer (SCML, TLG §13.7), now formulated in RBIT's own information-theoretic variables:

```
COMPLETE LIFECYCLE (information-theoretic formulation):

① VCZ (stable):
   All fᵢ bounded, S_norm << S_c, R ≈ 1
   Δρ > 0 across all active channels

② Storm onset:
   Majority fᵢ rising, Δρ turning negative in channels
   MI(agent_i, agent_j) spiking, S_norm → S_c

③ Collapse:
   S_norm > S_c sustained
   SCML classifies storm type → collapse topology
   Type 1/2 diagnosis determines reversibility

④ Recovery:
   Re-entry point determined by failure case
   Four-Phase Protocol: collapse → Phase 1 → 2 → 3 → 4

⑤ VCZ re-entry:
   All Rest Mode AND-entry conditions re-satisfied
   R-ρ-f_esc triple concordance confirmed
   All fᵢ returning to bounded, non-monotone state

Non-learning: ①→②→③→④→① (same vulnerability persists)
Learning:     ①→②→③→④→①' (structural learning via SCML)
  Without storm type classification → restores previous structure
  With classification → addresses specific weakness
  → next storm is a DIFFERENT storm
  → system's storm repertoire expands
  → φ_storm_absorption increases

Storm type determines governance response:
  Local amplification  → node-level re-seeding
  Boundary storm       → layer interface recalibration
  Hub storm            → distributed mediation restructure
  Global cascade       → Safe Collapse Protocol full execution
```

This lifecycle closure means that RBIT's resolution gap is not just a design variable but a dynamic quantity that the system learns to manage through repeated storm-recovery cycles. Each cycle updates the system's operational θ threshold, narrows the residual floor, and expands the VCZ basin.

*Safe Collapse Governance — the design principle (VST v1.6 §2.7):*

```
Collapse Prevention Governance (naive):
  Goal: minimize all failure
  Result: adaptation ↓, geometry update ↓ → CW → catastrophic collapse

Safe Collapse Governance (DFG):
  Goal: failure_cost << recovery_capacity
  Result: continuous low-amplitude correction → VCZ sustained

The paradox:
  Optimal stable governance always looks slightly unstable.
  Suppress collapse → accumulate catastrophe.
  Allow safe collapse → prevent catastrophe.
```

*7-Phase fractal lifecycle with storm signatures (VST v1.6 §14.3):*

```
Phase 1 — Seeding:       C(t) ≈ 0, random collisions, external governance
Phase 2 — Exploration:   first direction forming, healthy boundary-testing storms
Phase 3 — Formation:     attractor crystallizing, position-clarification storms
Phase 4 — VCZ:           power law distribution established, R ≈ 1, terrain formed
Phase 5 — Rest Mode:     all fᵢ bounded, micro-storms as value generation
Phase 6 — Reawakening:   environment shift, precision storms (fast, targeted)
Phase 7 — Higher Cycle:  new cycle at expanded resolution

In RBIT terms: each phase = different f(A_t, D_t) regime:
  Phase 1-2: f ≈ 0 (no internal absorption yet)
  Phase 3:   f > 0 and rising (resolution growth accelerating)
  Phase 4-5: f maximized (absorption efficient, stable)
  Phase 6:   f temporarily drops (new mismatch exceeds capacity)
  Phase 7:   f resets at higher baseline (expanded resolution floor)
```

*Boundary conditions on f from VST dynamics.* While the exact form of f(A_t, D_t) is unresolved, the S-equation (S = αn² / C(t)^β) constrains f's behavior through shared operational variables:

```
When S_norm < 1.3 (VCZ interior, stable operation):
  f(A_t, D_t) ≈ maximized
  Absorption efficient, geometry updating freely.
  Resolution growth at maximum rate for current architecture.

When S_norm approaches S_c (critical threshold):
  f(A_t, D_t) → 0
  Absorption saturated, receiver near capacity.
  This is the upscaling trigger condition.

When S_norm > S_c (storm regime):
  f can become negative
  Geometry mismatch accumulating faster than correction.
  Resolution effectively decreasing under forced compression.

Constraint summary:
  f is monotone decreasing in S_norm
  f > 0 requires S_norm < S_c (subcritical regime)
  f is maximized when Δρ > 0 AND S_norm << S_c
```

These constraints do not specify f's exact form but bound its shape: f must be a decreasing function of system instability, with a zero-crossing near the critical threshold. Operational decisions use S_proxy directional signals (S_proxy rising/falling), not absolute f values. (See Vector Storm Theory §3.2.2 for the Absolute Calibration Layer that grounds S_norm.)

*F_RBIT–S_norm cross-validation.* The F_RBIT health vector provides an independent information-theoretic cross-check on S_norm, measuring the same underlying instability from a different perspective (see Appendix §2 for full vector definition):

```
F_RBIT(ℓ) := (f₁, f₂, f₃, f₄, f₅)   [5-component health vector, each ∈ [0,1]]

Cross-validation protocol (concordance-based — no weights required):
  Majority of fᵢ rising AND S_norm rising  → confirmed instability
  S_norm rising BUT all fᵢ stable          → S calibration check needed
  S_norm stable BUT majority fᵢ rising     → S may miss resolution-specific stress
  All fᵢ bounded AND S_norm stable         → confirmed stability

S_norm measures dynamical instability (generation vs absorption).
F_RBIT measures informational adequacy (resolution sufficiency across layers).
Concordance in direction strengthens confidence; discordance flags calibration error.
No weight specification required for any of these comparisons.
```

(See Vector Storm Theory §3.2.6 for the full derivation connecting resolution gap polarity to S-equation dynamics. See Appendix §2 for function class specification of f₂ = Φ(−Δρ) and f₃ = Ψ(B).)

*Rest Mode as all-fᵢ bounded.* The F_RBIT vector provides a formal criterion for Rest Mode expressed entirely in RBIT's own variables:

```
Rest Mode condition (vector form):
  Each fᵢ bounded and non-monotone over evaluation window W
  No component in sustained rising trend
  F_RBIT ≠ (0,0,0,0,0)   [residual instability maintained — floor exists]

Not zero instability (impossible — residual floor).
Bounded fluctuation equilibrium:
  information intake and internal dissipation balanced across all five axes.

F_RBIT components map to governance entry conditions:
  f₄ = E_ℓ bounded       ← f_esc ≤ θ (escalation load within threshold)
  f₁ = 1−ρ_ℓ bounded     ← I ≥ τ (misclassification rate bounded)
  f₃ = Ψ(B_ℓ) bounded    ← Lreinf ≥ threshold (buffer stability maintained)
  f₅ = C_ℓ bounded        ← SCC ≥ τ4 (recovery cost bounded)

All four required: single diverging component → net instability growth.

Triple perspective intersection for Rest Mode:
  S_norm << S_c:         dynamical (instability below threshold)
  all fᵢ bounded:        informational (resolution adequate, balanced)
  R ≈ 1, SR > 0:        statistical (critical and responsive)
  Rest Mode = intersection of all three perspectives.
```

*φ_mature decomposition.* In Rest Mode, φ (value yield) splits into two components that resolve the apparent paradox of storm-tolerant governance:

```
φ_mature = φ_exploration + φ_storm_absorption

  φ_exploration:       standard value from exploratory activity
  φ_storm_absorption:  P(micro-storm → geometry recalibration → reusable correction)

  Immature system: φ_storm_absorption ≈ 0 (storms are pure cost)
  Rest Mode:       φ_storm_absorption > 0 (storms contribute value)

Resolution of the U optimization paradox:
  U = n·φ − C_gov
  Immature: storm minimization = U maximization
  Rest Mode: storm minimization ≠ U maximization
  → optimal = maintain storm scale power law
    (continuous small storms, rare large storms)
  → storm elimination is not the governance objective

In RBIT terms: each micro-collision produces a geometry update
  that increases f(A_t, D_t) for future absorption.
  The system converts instability INTO resolution growth.
```

(See Recovery Theory §φ_mature and VST §3.6.1 for the full derivation.)

*Storm Scale Law — power law health distribution.* The optimal storm distribution in a healthy system follows a specific power law (VST v1.6 §3.10):

```
P(Storm of scale s) ∝ 1/s^α

  ~90%+ corrections resolve at micro/local level
  ~9%   escalate to cluster level
  <1%   require global intervention

Governance target:
  NOT: minimize storm count
  BUT: maintain storm size distribution ≈ power law
  (many small storms, few medium, rare large)

Distribution shift diagnostics:
  Small storms disappearing + large maintained:
    → suppression in lower layers → mismatch accumulating
    → Absence Paradox / Silent Criticality
    
  Large storms without small precursors:
    → CW geometry releasing (VCZ-seeking Storm)
    
  All storms increasing:
    → approaching Chaos boundary → intervention needed
    
  All storms decreasing uniformly:
    → CW onset → SR/RDE/NCR check required

VCZ as operating corridor:
  Chaos boundary:  storm frequency too high at ALL scales
  CW boundary:     storm frequency → 0 at ALL scales
  VCZ:             micro/local storms continuous, global rare
  = narrow corridor between two failure modes
  = S_norm << S_c expressed as a scale distribution
```

In RBIT terms, the Storm Scale Law is the emergent signature of correction_rate ≥ drift_rate at all resolution levels simultaneously. The power law distribution means that the resolution gap is being managed at every scale — not just at the system-wide level where S_norm is measured.

*Degradation calibration — operational correspondence.* While the formal D(Δρ) function is unresolved (Open Problem #9), two established ML techniques implement the same calibration logic:

```
Knowledge distillation temperature T (Hinton et al. 2015)
  Softmax temperature T controls how much information
  the teacher transmits to the student:

  T high  -> soft probability distribution
             -> more information, lower degradation
             -> corresponds to Δρ >> 0 (safe to transmit more)

  T low   -> hard label (near one-hot)
             -> maximum compression, high degradation
             -> corresponds to Δρ ≈ 0 (layer near capacity)

  T is the closest operational analog to D(Δρ):
  both are sender-side parameters that control
  how much of the upstream signal is preserved.
  Caveat: T is a global parameter; D(Δρ) is
  layer-pair-specific in the RBIT formulation.

Curriculum learning (Bengio et al. 2009)
  Training examples ordered by difficulty:
  easy first -> progressively harder

  Easy examples = low resolution gap input
  Hard examples = higher resolution gap input
  Schedule = dynamic D_t across training

  This operationalizes the RBIT prescription:
  calibrate degradation to the receiver's current
  resolution, then increase complexity as rho grows.
  Caveat: curriculum ordering is typically
  hand-designed or heuristic; automatic
  calibration to rho remains open.
```

*Scaling law as empirical f approximation.* Chinchilla scaling (Hoffmann et al. 2022) provides an empirical approximation to the f relationship:

```
Model performance ~ (compute budget)^alpha
                  x (data volume)^beta

Correspondence to R_{t+1} = R_t + f(A_t, D_t):
  A_t ~ data volume
  D_t ~ training compute / calibration quality
  f   ~ power law in both (empirical, not derived)

Caveat: Chinchilla measures aggregate performance,
not layer-level resolution. It is a macro-scale
approximation, not a derivation of f.
The formal form of f at layer level remains open.
```

---

## Operational Measurement

Resolution cannot be directly observed. The following metrics are operational proxies — what can actually be measured in a running system.

### Resolution-Proxy (ρ)

```
ρ = 1 − (L_T1 + L_T2) / N

  N      total inputs processed in evaluation window
  L_T1   Type 1 loss: False Restoration (healthy classified as contaminated)
  L_T2   Type 2 loss: Missed Contamination (contaminated classified as healthy)
```

Higher ρ → more precise classification → more accurate mediation and placement.

The above instantiation uses contamination classification as a concrete and auditable discrimination task. More generally, ρ can be defined for any layer-specific discrimination task with Type I/II errors, provided the task is held fixed across comparisons. For cross-layer comparison, the discrimination task should be protocol-stable (same labels, same decision boundary, same evaluation distribution), so that changes in rho reflect capacity differences rather than task redefinition.

*Buffer thickness as resolution proxy.* For opposing vector pair (A, B), define d(x,A) as the **attractor pull strength** of input x toward direction A. Buffer thickness is the proportion of inputs that fall in the non-directional zone where neither attractor dominates:

```
buffer_thickness(A, B)
  = |{x : |d(x,A) - d(x,B)| < epsilon}| / |total input|

System buffer thickness
  = min over all opposing pairs
    (thinnest buffer is the highest-risk zone)
```

Operationally, d(x,A) takes system-specific forms (logit scores for classifiers, advantage values for RL systems, KL divergence for LLM agents — see Recovery Theory §1.4 for full operational implementations). The low-confidence sample ratio standard in ML practice is a direct proxy under calibrated confidence: inputs where max confidence < threshold theta correspond to the non-directional zone. A thinning buffer is an early warning of Tier 3 contamination risk.

*Policy dependence.* Buffer thickness is measured relative to the current policy. Policy changes shift attractor positions, so buffer measurements shift with them. Cross-time comparisons require policy-stable evaluation sets. See Recovery Theory §1.4 for full caveat.

*Connection to Recovery Theory Section 1.4.*

*Note:* ρ is window-dependent; comparisons across layers or time should use matched evaluation windows or an explicit normalization for input mix and sample size.

*Resolution-proxy ρ and precision-like parameters (hypothesis).* The resolution-proxy ρ is defined as an empirical classification reliability over an evaluation window. Precision parameters in predictive processing are typically defined as inverse uncertainty (e.g., inverse variance) that modulates the impact of error signals. While ρ is not a Bayesian precision parameter, it may serve as a monotone proxy for discrimination certainty under simple observation models.

For example, if we model "correct discrimination" events as Bernoulli trials with success probability p, then ρ ≈ p and uncertainty about p under a Beta posterior decreases with sample size N:

```
Var(p | data) ∝ p(1−p) / (N + α + β + 1)
```

A natural precision-like quantity is then Π_ρ ∝ 1 / Var(p | data), where Π_ρ denotes an informal precision-like construct defined up to proportionality — which increases with both N and discrimination reliability. Under this view, increases in ρ and stabilized error statistics correspond to increases in an effective precision-like parameter — without asserting formal identity with variational free energy formulations. Establishing a formal mapping, and clarifying when such a mapping is meaningful, remains an open problem.

**Resolution gap between layers:**

```
Δρ = ρ_upper − ρ_lower

  Δρ > 0   Upper reads lower correctly → normal operation
  Δρ = 0   Upscaling imminent
  Δρ < 0   Upper cannot read lower → seed handover must not proceed
```

### Fractal Self-Similarity

The DFG framework is named "Deficit-**Fractal** Governance" because the same structural pair repeats at every scale of the system. The minimum unit of directed behavior — exploration and interpretation — is not a property of any particular layer. It is the invariant structure that appears at every resolution level.

*Why the two-pair minimum produces fractal structure:*

```
Any layer that processes information
must do two things:
  Explore  search for relevant inputs
           "what exists here?"
  Interpret  assign meaning to found inputs
             "what does this mean?"

This is not a design choice.
It is a functional necessity:
  Without exploration -> nothing to interpret
  Without interpretation -> exploration has no direction
  The two pairs are mutually constitutive.

Because this necessity holds at any scale,
the same structure repeats at every scale:

  System scale
    Agents explore different problem regions
    Upper layer interprets aggregate output pattern
    -> Exploration + Interpretation

  Agent scale
    Internal layers explore feature space
    Higher layers interpret learned representations
    -> Exploration + Interpretation (isomorphic)

  Metadata scale
    Evaluation criteria search for signals
    Governance rules interpret signal patterns
    -> Exploration + Interpretation (isomorphic)

This is fractal self-similarity:
not visual repetition, but structural repetition —
the same functional pair operating
at each resolution level independently.
```

*Conditional necessity.* Fractal structure is a scaling necessity for systems operating near criticality (R ≈ 1). The n² scaling in the instability equation is not an assumption about network density — it is derivable from critical branching process dynamics, even in sparse networks:

```
At criticality (R ≈ 1):
  Mean avalanche size: ⟨S⟩ ~ n
  Concurrent active avalanches: ~ n
  Total interaction load = concurrent × mean size = n × n = n²

This holds in sparse networks because:
  Static graph edges: O(nk) — sparse
  Time-integrated reachable pairs: O(n²) — quasi-dense
  (In small-world networks: path length ~ log(n)
   → within log(n) propagation steps, nearly all pairs reachable)
  
  Network sparsity affects coupling intensity (α),
  NOT the scaling exponent.
```

Hierarchical terrain formation — the emergence of boundaries, routing, and modularity — reduces effective interaction dimension from n² to n^{d_eff} where 1 < d_eff < 2:

```
System maturity spectrum:
  Early system    (flat landscape):     S ~ n²       (d_eff ≈ 2)
  Maturing system (terrain forming):    S ~ n^{1.5}  (d_eff ≈ 1.5)
  Rest Mode       (deep terrain):       S ~ n^{1+ε}  (d_eff → 1)

The sub-quadratic correction is conditional on maintaining
the Signaling/Influence distinction (TLG §10.1):
  Signaling (permitted): agents share state information peer-to-peer
    → potential collisions detected before escalation → terrain benefit real
  Influence (prohibited): agents modify each other's internal states
    → load migrates invisibly → terrain benefit illusory
```

At small scale or in strongly subcritical regimes (R << 1), non-fractal architectures remain viable because interaction load is manageable. The prediction is that as system complexity grows past a critical n threshold, hierarchical structure will emerge endogenously if the system is permitted to self-organize. (See Vector Storm Theory §3.2.5 for the full critical phenomena derivation and §1.6.1–1.6.2 for the SOC framework.)

*Lreinf as the terrain mechanism.* The sub-quadratic correction (d_eff < 2) is not a fixed property of the architecture — it is produced and maintained by reinforcement loop strength (Lreinf). When Lreinf collapses, the system reverts to flat-landscape quadratic coupling:

```
Strong Lreinf → interaction barriers between agent niches
  → effective scaling: S ~ n^{d_eff}, d_eff < 2
  → governance cost manageable at scale

Lreinf collapse → barriers disappear → d_eff → 2
  → S ~ n² with no terrain damping
  → maximum storm amplification potential
  → most dangerous failure mode

This connects RBIT's resolution hierarchy to VST's instability dynamics:
  Resolution gap calibration PRODUCES the terrain
  (agents at different resolutions create natural barriers)
  Resolution gap collapse REMOVES the terrain
  (all agents at same resolution = flat landscape = n² coupling)
```

*Fractal collapse propagation.* Failures cascade through a predictable chain when terrain fails at sufficient scale:

```
Case 2 (Escalation Flood) → upper layer overwhelmed
  → upper layer's own classification reliability (I) falling
  → Case 1 (Consistency Collapse at upper layer)
  → lower layer Lreinf collapses (no consistent upper guidance)
  → Case 3 (Reinforcement Loop Collapse)
  → d_eff → 2 → maximum storm potential

Early warning: inter-domain conflict log correlation
  MI(conflict_log_A, conflict_log_B) rising WITHOUT shared input
  = noise floors synchronizing across domains
  = pre-cascade signal detectable BEFORE any single metric crosses threshold
```

(See Recovery Theory §Fractal Collapse Propagation Chain and TLG §13.2.2 for the full cascade topology.)

*Why this matters for governance:*

```
Fractal structure implies fractal ceiling.
Each scale's exploration+interpretation pair
has its own bounded field of view:
  Can only explore within its resolution range
  Can only interpret what its resolution can read

Upper scale cannot be replaced by lower scale
because lower scale's interpretation
cannot read what upper scale's exploration finds
-> Governance ceiling is not a design constraint
   It is a structural consequence of
   the fractal repetition of bounded pairs
```

*Observed in ML systems:*

```
Mixture of Experts (MoE)
  Shazeer et al. 2017; Fedus et al. 2022
  Each expert: explores a specialized sub-region
               interprets inputs in that region
  Gating network: explores which expert is relevant
                  interprets routing signal
  -> Expert level and gating level are
     isomorphic exploration+interpretation pairs
  -> MoE is fractal in the DFG sense

Hierarchical attention (transformers)
  Lower layers: explore local token relationships
                interpret surface patterns
  Higher layers: explore global context
                 interpret semantic structure
  -> Each layer is an independent
     exploration+interpretation pair
  -> Resolution increases with depth
     = fractal structure climbing scales

Hierarchical RL
  Low-level policy: explores action space
                    interprets immediate state
  High-level policy: explores goal space
                     interprets abstract state
  -> Two-level fractal:
     same pair, different resolution
     Feudal Networks (Vezhnevets et al. 2017)
```

*Connection to Intent preservation.* Intent is preserved across terrain when both the exploration range and the interpretation structure remain isomorphic to the sender's seed at every scale. Because the fractal structure repeats the same pair at every level, contamination at one scale propagates by distorting that scale's exploration+interpretation pair — which then transmits distorted signals upward, corrupting the next scale's interpretation of its inputs.

*Connection to Seed Sufficiency.* A fully sufficient seed must contain at least two independent directions (Test 3) because the minimum unit itself has two components. A single-direction seed cannot sustain the exploration+interpretation pair — it collapses one component, breaking the functional minimum and preventing self-correction.

### Buffer Layer Thickness

A second independent observable proxy for upper layer resolution — the spatial separation maintained between opposing vectors. Tracks resolution changes without requiring classification event data.

---

## Grounding in Single-Agent Architecture

RBIT's core claims — resolution stratification, degradation, and the resolution gap — are not hypothetical properties of future multi-agent systems. They are already observable within competent single-agent architectures.

### Resolution Stratification Inside a Transformer

A large language model's internal structure can be interpreted as exhibiting a resolution hierarchy consistent with RBIT's definitions:

| Layer region | Processing role | Resolution characteristic |
|-------------|-----------------|--------------------------|
| Early layers | Syntax, local pattern detection | High volume, low semantic resolution |
| Middle layers | Relational synthesis | Intermediate |
| Late layers | Semantic intent, abstract reasoning | Lower volume, high resolution |

The upper layers of a transformer correspond structurally to the upper layer of the DFG three-layer architecture: they hold the most abstract, highest-resolution map of the input space. Early layers correspond to lower agents processing at Tier 1–2 resolution.

Representation analysis studies have empirically observed that lower transformer layers encode syntactic and local structure while higher layers encode semantic and abstract relationships (Tenney et al., 2019; Elhage et al., 2021; Rogers et al., 2020). This pattern supports an interpretation of transformer layers as exhibiting a resolution gradient consistent with RBIT's hierarchy — though this remains an interpretive framing rather than a derivation. The correspondence motivates the Externalization Principle below.

### Attention as Dynamic Resolution Allocation

Within a single layer, attention heads do not distribute resolution uniformly. At any given step:

```
High-attention tokens  → processed at high resolution
Low-attention tokens   → processed at reduced resolution
Near-zero attention    → effectively at noise floor
```

This is dynamic resolution allocation — the same mechanism RBIT describes as the upper layer's Tier 3 capacity. The model continuously re-allocates resolution budget across the input space, concentrating it where structural complexity demands it.

Multi-head attention extends this further: each head resolves a *different dimension* of the input space (syntactic, positional, semantic, long-range dependency). A single agent is therefore not a uniform resolver — it is a **parallel bundle of resolution-stratified sub-perspectives**, each operating on the same input at different resolution types simultaneously.

### Known Failure Modes as Resolution Distribution Failures

The three most common failure modes of single-agent LLMs are directly interpretable as resolution distribution failures in RBIT terms:

| Failure mode | Conventional description | RBIT interpretation |
|-------------|--------------------------|---------------------|
| **Hallucination** | Model generates confident false content | Low-resolution region attempts high-resolution judgment — forced compression produces plausible-but-unfounded output |
| **Token bias** | Early tokens disproportionately determine output | Early-layer (low-resolution) processing commits to a direction before late-layer (high-resolution) processing can correct |
| **Lost-in-the-middle** | Information in middle of long context is underweighted | Resolution budget exhausted at context boundaries; middle region collapses to noise floor |

In each case, the failure is not a knowledge gap or a training deficiency. It is a **resolution gap mismatch**: a processing region operating outside its resolution capacity, producing the forced-compression behavior RBIT predicts.

*What RBIT adds beyond existing mechanistic explanations.* The reinterpretations above do not replace established explanations (attention sink dynamics, induction head behavior, positional encoding limitations). They provide a complementary system-level account that produces outputs not derivable from component-level analyses alone:

```
1. Depth-differentiated stability thresholds
   Deep layers are consistently harder to diversify than shallow layers
   (GatePro, arXiv:2510.13079, 2025). RBIT's resolution hierarchy
   predicts this; flat attention-mechanism analyses do not.

2. Multi-axis diagnostic criteria
   Gini coefficient alone is insufficient for detecting routing collapse.
   Four axes required: load distribution, spectral entropy,
   representational redundancy, routing confidence.
   (See VST Appendix A.1.1 for full derivation.)

3. Quantitative stage detection thresholds
   Sustained entropy collapse H(t) < 0.2 nats identifies Stage 2 onset.
   This is a new diagnostic metric derived from the framework,
   not a reinterpretation of existing phenomena.

4. Prescriptive intervention targets
   Attention inflection layers (low entropy + steep gradient decay)
   are identified as resolution bottlenecks where LoRA injection
   restores balance. RBIT identifies where to intervene,
   not just what went wrong.

5. Budget-bounded vs. stability-bounded processing limitation
   Reasoning models (o1, DeepSeek-R1) use token budgets to control
   internal conflict resolution. RBIT identifies this as budget-bounded
   rather than stability-bounded — a specific limitation that existing
   explanations do not distinguish.
```

The key distinction: existing analyses explain mechanisms (how components behave); RBIT explains system-level consequences (why those behaviors produce cascade failures, how to detect cascade onset, and where to intervene).

*Stability Saturation — the over-stability failure mode.* Three-Layer Governance §9.2.1 identifies a phenomenon where standard metrics cannot distinguish healthy stability from dangerous stasis:

```
Healthy stability:
  collision frequency: low,  exploration: present and diverse,  φ: maintained
  → system is mature and functioning

Stability Saturation (SSS):
  collision frequency: ≈ 0,  exploration: absent or monocultural,  φ: declining
  → system appears mature but is losing adaptive capacity
  → all dashboard metrics green — identical to healthy stability

  Detection requires active probing:
    Inject novel-but-non-destructive perturbation
    Healthy: τ1 event → absorb → integrate → diversity briefly increases
    SSS: no τ1 event, OR recovery time >> baseline, OR output unchanged
    → adaptation pathways degraded under surface stability
```

This is relevant to RBIT because Stability Saturation is exactly the state where compression appears optimal (all resolution gaps managed, no escalation) but the system has lost the ability to detect geometry mismatch — the receiver's resolution has frozen rather than grown. In RBIT terms: R_{t+1} = R_t (resolution growth stalled, f(A_t, D_t) ≈ 0) despite all operational metrics suggesting health. The resolution gap variable Δρ cannot detect this because both sender and receiver have converged to the same frozen geometry.

### The Externalization Principle

This correspondence implies a stronger claim:

> **The proposed multi-agent hierarchy can be interpreted as an externalization
> of the resolution stratification already present within competent
> single-agent architectures.**

```
Transformer layer hierarchy
        ↓  externalized
Fractal multi-agent hierarchy
```

Single-agent architectures internalize resolution stratification implicitly — it emerges from training, not from explicit design. Multi-agent architectures with explicit resolution-layer governance make the same structure **explicit, designable, and auditable**.

RBIT can be understood not as introducing a new architectural principle, but as making an existing structural property of AI systems explicit, designable, and governable.

---

## Data Classification as Resolution Matching

Four types based on resolution requirement:

| Type | Resolution requirement | Example | Routing |
|------|----------------------|---------|---------|
| **Mathematical** | Low — single conclusion at any resolution | Binary flag, threshold crossing | Process locally |
| **High-Context** | High — single conclusion only at upper resolution | Intent behind ambiguous agent behavior | Escalate |
| **Tacit Knowledge** | Variable — pattern operable locally, mechanism requires higher resolution | Agent consistently escalates near boundary conditions | Operate locally; escalate on performance degradation |
| **Noise** | None at current resolution | Sub-threshold fluctuation with no detectable pattern | Buffer or discard; upper layer may detect latent vectors |

Classification is not a fixed property of data. It is a function of the resolution gap between the data and the receiving layer. The same data may classify differently at different layers.

---

## Relationship to Information Bottleneck Theory

The Information Bottleneck (IB) framework (Tishby et al., 2000; Tishby & Zaslavsky, 2015) is RBIT's most direct theoretical neighbor. Both frameworks treat compression as designable rather than purely lossy. The boundary must be stated explicitly: IB and RBIT are complementary, not competing.

| Dimension | Information Bottleneck | RBIT |
|---|---|---|
| **Core question** | What is the optimal compression of X for predicting Y? | How should information transform as it moves through layers of different resolution — and how does the system grow? |
| **Receiver capacity** | Fixed. Y is a static target. | Variable, growing. Receiver resolution changes through calibrated absorption. |
| **Optimization target** | Compression quality for fixed downstream task | Compression calibration for growing receiver + future upscaling potential |
| **Failure model** | Suboptimal compression → reduced I(T;Y) → lower performance (graceful degradation) | Miscalibrated compression → cascade failure (Vector Storm) → system-wide instability (phase transition) |
| **Scope** | Single encoder-decoder channel | Multi-channel hierarchical governance with cross-channel error propagation |
| **Core variable** | β (compression-relevance tradeoff) | Resolution gap Δρ (sender-receiver capacity difference, signed) |
| **Compression purpose** | Maximize current task relevance | Preserve generative structure for future upscaling (seed, not tree) |
| **Temporal dynamics** | Static optimization (β is a parameter) | Inherently dynamic (resolution changes through experience) |
| **Measurement** | Mutual information I(X;T), I(T;Y) — requires density estimation | ρ, buffer thickness, collision frequency — operational metrics from system logs |
| **Layer interaction** | Independent (each layer's IB is local) | Coupled (compression error propagates across layers) |

**Five structural differences:**

*1. Dynamic receiver capacity.* IB optimizes for a fixed Y. RBIT models receiver resolution as growing (R_{t+1} = R_t + f(A_t, D_t)), making optimal compression a moving target. IB's information plane is static; RBIT's design problem is a trajectory.

*2. Consequence theory for miscalibration.* IB predicts graceful performance degradation along the information plane. RBIT + VST predict that negative resolution gaps produce qualitative phase transitions: forced compression → self-amplification → cascade failure. The S-equation (S = αn²/C(t)^β) models instability pressure from miscalibration. IB has no equivalent. VST v1.3 §3.8 provides the precise information-theoretic characterization: storms are uncontrolled mutual information spikes across agents — MI(agent_i, agent_j) >> MI_baseline — driven by forced compression that generates new correlations propagating as storm seeds. IB models compression quality; RBIT+VST models what happens when compression is forcibly miscalibrated at system scale.

*3. Multi-channel governance.* IB operates on X → T → Y (single channel). RBIT addresses coordination across multiple interacting compression channels where one channel's error propagates to others through fractal structure — the governance problem that arises when many IB-optimizing layers of different capacity must interact.

*4. Compression for future upscaling.* IB's optimal T* maximizes I(T;Y) for the present task. RBIT's optimal seed preserves generative structure for future re-interpretation — calibrated to the receiver's growth trajectory, not current performance. A seed that preserves less I(T;Y) than IB-optimal may be better in RBIT terms if it preserves the structure that enables upscaling.

*5. Measurement independence.* IB requires mutual information estimation, which is unreliable in continuous high-dimensional spaces (Goldfeld et al., 2019; Saxe et al., 2018 showed compression phase depends on activation function choice). RBIT's core measurements (ρ, buffer thickness, S_proxy) are operational metrics derivable from system logs without density estimation, making predictions testable without solving the MI estimation problem.

**What IB addresses that RBIT does not:** Formal optimality proofs for fixed-task compression. Rate-distortion bounds from Shannon theory. Well-developed variational approximations (VIB) for differentiable implementation.

**Positioning:** IB provides the within-layer compression principle. RBIT provides the between-layer governance architecture. A single layer performing IB-optimal compression could still produce system-wide failure if miscalibrated relative to the receiving layer's resolution. IB optimizes compression quality; RBIT governs compression calibration across a growing system.

---

## Relationship to DFG Component Theories

RBIT is the foundation from which the following derive:

| Theory | RBIT connection |
|--------|----------------|
| **Vector Storm Theory** | Vector Storm = negative resolution gap event (under-degradation cascade) |
| **Network Architecture Theory** | Data classification = resolution matching; escalation = resolution gap signal |
| **Governance Rules Theory** | Seeds = dynamic minimum sufficient information; Rest Mode = thermodynamic steady state; seed handover = resolution matching event |
| **Three-Layer Governance Architecture** | Middle layer = resolution mediation layer; seeding = calibrated degradation; τ thresholds = resolution gap response boundaries |
| **Recovery Theory** | Contamination = resolution mismatch producing positional displacement; D0 geometry alignment = resolution decomposition as substrate; D4 restoration conditions = resolution recovery measurement (ρ ≥ pre + diversity expanding + P_overlap declining); resolution gap governs contamination susceptibility (high Δρ → high vulnerability) |
| **RT-2 v2.0 (SCM)** | Metric Lock-In (Proposition 5) = resolution metrics co-drifting with geometry under SCM — RBIT measurement inherits RT-2 impossibility constraint; Coherence Maximization Paradox = highest-resolution systems most vulnerable to SCM entry; resolution gap detection requires EXTERNAL reference (RT-2 differential protocol) |
| **RT-3 v1.0 (Observer)** | Observer diversity V = resolution diversity across observational dimensions; buffer B = RBIT buffer layer resource for high-resolution observation; scope duality S = RBIT wide/narrow resolution switching; Coordination–Cancellation Paradox = high resolution diversity cancels without mediated aggregation |
| **RT-4 v1.0 (Reversibility)** | Resolution recovery capacity generated relationally not individually; trust coefficient Tᵢⱼ = resolution-error reduction probability; reversibility phase transition R_c = critical resolution threshold below which RBIT degradation-upscaling cycle fails; Shared Vulnerability = resolution gap disclosure as collective detection resource |

> **The resolution gap is the unifying variable.**
> Every mechanism in the DFG framework is a response to the resolution gap
> between information and receiving layer — managing it, signaling it,
> reducing it over time, or designing for its irreducible remainder.

---

## Relationship to Predictive Processing and Active Inference

### Structural Correspondences

*Relation to Predictive Processing / Active Inference (positioning).* RBIT is not derived from predictive processing or active inference, and we do not claim formal equivalence. Nonetheless, there is a useful structural correspondence: both perspectives study how bounded systems remain stable while facing streams of uncertain inputs. In active inference, instability can be described as poorly regulated (or effectively unbounded) prediction-error dynamics under mis-specified precision. In RBIT, instability appears as a persistently negative or unmanaged resolution gap that induces receiver-controlled compression and cascade interference (Vector Storm). In this sense, RBIT can be read as an architectural account of inter-layer and inter-agent message shaping that complements intra-agent inference accounts.

Both frameworks describe adaptive systems that must regulate incoming informational complexity under bounded processing capacity:

| Active Inference (Friston et al.) | RBIT |
|----------------------------------|------|
| Generative model | Intent / generative constraint structure |
| Prediction error | Resolution gap |
| Model update | Upscaling |
| Precision weighting | Resolution allocation / calibrated degradation |
| Bounded surprise / instability regulation | Vector Storm avoidance *(as one architectural expression)* |
| Hierarchical inference | Fractal resolution layers |
| Bounded surprise over time | Rest Mode (thermodynamic steady state) |

The most direct correspondence: in Active Inference, system instability appears as unbounded prediction error. In RBIT, instability appears as a negative resolution gap leading to forced compression (Vector Storm). These are structurally analogous descriptions of bounded-capacity instability, developed in different theoretical traditions.

### Resolution-Proxy ρ and Precision — A Structural Correspondence

The correspondence between frameworks extends to their core measurement quantities.

In Active Inference, **precision** (Π) is the inverse variance of prediction error — a weighting factor that determines how strongly a given error signal updates the generative model:

```
Π = 1 / Var(error)

Low precision  → error signal downweighted → small model update
High precision → error signal amplified   → large model update
```

In RBIT, the **resolution-proxy** ρ measures classification reliability — the probability that the layer correctly discriminates incoming states:

```
ρ = 1 − (L_T1 + L_T2) / N

Low ρ  → high error rate → low discrimination reliability
High ρ → low error rate  → high discrimination reliability
```

Both quantities are inverse measures of uncertainty in state discrimination. The structural relationship:

```
ρ ↑  →  classification error ↓  →  Var(error) ↓  →  Π ↑
```

This suggests a structural mapping:

> The resolution-proxy ρ plays a role structurally analogous to precision
> parameters in predictive processing frameworks. Both quantify the reliability
> with which incoming informational distinctions can be maintained and acted
> upon under uncertainty.

The practical implication for the RBIT framework:

```
Resolution growth  →  precision increase across hierarchical layers
Calibrated degradation  →  precision-matched transmission
Vector Storm  →  precision misallocation cascade
Upscaling  →  endogenous precision learning
```

**Epistemic status of this correspondence:** ρ is an empirical performance metric; precision is a normative Bayesian parameter. The two are structurally analogous but not formally equivalent. A formal mapping between ρ and precision remains an open problem.

---

### The Critical Difference

The structural similarities do not make these the same theory. The difference is the unit of analysis:

```
Active Inference
  Unit: single embodied agent
  Focus: intra-agent perception-action loop
  Formulation: Bayesian / variational
  Question: how does an agent stabilize itself?

RBIT
  Unit: layer-to-layer information transformation
  Focus: inter-agent and inter-layer resolution mediation
  Formulation: information-theoretic / architectural
  Question: how do differently-resolved agents stabilize each other?
```

> **Active Inference explains how an agent stabilizes itself.**
> **RBIT explains how differently-resolved agents stabilize each other.**

Calibrated degradation in RBIT is structurally analogous to precision weighting in Active Inference — both selectively modulate how much of incoming signal is processed at full resolution. But where precision weighting is a property of a single agent's internal inference, calibrated degradation is an architectural design decision made by a sender about how to transmit to a receiver.

### Positioning

RBIT occupies a space not addressed by either framework alone: the governance of information transformation *between* agents operating at different resolution levels, in a system designed for explicit auditability. This is a complementary perspective, not a competing one.

The three frameworks form a vertical stack:

```
Thermodynamics (Landauer)
      ↓  irreducible uncertainty floor
Precision regulation (Active Inference)
      ↓  intra-agent stability mechanism
Resolution mediation (RBIT)
      ↓  inter-agent transformation architecture
Multi-agent governance (DFG)
```

Each level addresses what the level above leaves unspecified. RBIT does not replace Active Inference — it addresses the governance problem that arises when multiple Active Inference agents of different resolution capacities must interact.


---

## Physical Basis — Why Perfect Resolution Is Impossible

### Resolution as State Discrimination

In RBIT terms, resolution is the capacity to distinguish between states — to separate vectors that would otherwise collapse into the same position. Increasing resolution means making previously indistinguishable states distinguishable.

### Three Arguments for the Residual Floor

The residual resolution floor — the minimum below which discrimination cannot proceed — is established by three independent arguments (summarized in "Why This Framework Is Needed" above):

**Primary: Combinatorial.** Multi-agent interaction surfaces grow as O(n²). Complete resolution requires infinite governance capacity. Therefore S > 0 always for n > 1.

**Primary: Governance.** In fractal architectures, lowest layers are structurally partially degraded. Complete stability = zero correction capacity = catastrophic failure when environment shifts. Maintained residual instability is the correction mechanism.

**Supporting: Thermodynamic.**

### Landauer's Principle — Supporting Thermodynamic Motivation

Landauer's Principle establishes that erasing one bit of information requires a minimum energy expenditure:

```
E ≥ kT ln 2

  k  = Boltzmann constant
  T  = temperature of the system
```

Landauer's principle applies strictly to logically irreversible operations such as information erasure. Resolution increase does not literally reverse erasure. However, increasing discrimination between previously indistinguishable states requires additional physical work, because maintaining distinguishable representations reduces effective entropy locally — and that local entropy reduction has a thermodynamic cost.

The connection here is therefore structural rather than thermodynamic identity. We do not claim a direct quantitative bound from Landauer to ρ or resolution; we use it to motivate the existence of irreducible floors under bounded resources. The implication this structural parallel supports:

> **Perfect resolution is asymptotically unreachable for finite physical systems
> operating under bounded energy and time constraints.**

This is not an engineering limitation to be overcome with better hardware. It is a structural consequence of operating as a finite physical system.

### The Residual Floor as Structural Necessity

RBIT's residual resolution floor — the minimum below which the lowest layer cannot further discriminate — is established primarily by combinatorial and governance arguments (see above). The thermodynamic perspective provides additional physical motivation:

```
Residual degradation floor
  = point at which further state discrimination
    costs more than the system's energy budget allows

This floor:
  -> Cannot be reduced to zero
  -> Persists regardless of system maturity
  -> Generates irreducible residual noise at every scale
  -> Is the structural basis for asymptotic (not absolute) stability
```

*This section is intended as motivation for irreducible limits under bounded resources, not as a derivation of a strict lower bound on rho. The Landauer connection is structural rather than quantitative. The thermodynamic discussion motivates bounded-resource limits, not a computable lower bound on resolution. No claim is made that rho can be derived from thermodynamic first principles.*

### Vector Storm as Throughput Exceeding Dissipation Capacity

**Dissipation capacity**: the rate at which a layer can process and separate incoming states — its throughput for maintaining resolution under load. When intake exceeds this capacity, the layer can no longer maintain state separation and forced compression begins.

Vector Storm conditions can be interpreted in thermodynamic terms:

```
Normal operation:
  Information complexity arriving ≤ dissipation capacity
  → Layer maintains state separation → resolution stable

Vector Storm precondition:
  Information complexity arriving > dissipation capacity
  → Forced compression cascades
  → State separations collapse → positional overlap
```

This structure can be interpreted as analogous to dissipation-limited instability observed in other complex systems — turbulent flow, neural avalanche dynamics, plasma instability — where throughput exceeding local dissipation capacity produces cascade failure. The analogy is structural and descriptive; no claim of dynamical equivalence is made.

### Rest Mode as Thermodynamic Steady State

Rest Mode — the condition in which the system self-corrects without external intervention — corresponds to a thermodynamic steady state:

```
Rest Mode condition:
  Entropy generated by new information intake
    ≈ Entropy dissipated by internal resolution processes

Not:  zero entropy (impossible)
Not:  perfect stability (impossible)
But:  dynamic equilibrium — the system continuously processes
      incoming complexity without accumulating unresolvable residue
```

The system does not *achieve* Rest Mode by becoming more capable. It enters Rest Mode when its dissipation capacity matches its intake rate.

### Summary

```
Landauer Principle
  → Perfect state discrimination requires unbounded energy
  → Perfect resolution is physically impossible

Residual entropy floor
  → Every finite system retains irreducible unresolved states
  → Residual degradation floor is thermodynamically grounded

Vector Storm
  → Intake rate exceeding dissipation capacity
  → Cascade compression (structural analogy to dissipation-limited instability)

Rest Mode
  → Thermodynamic steady state
  → Intake ≈ dissipation, not intake = 0
```

> **Degradation is not a governance failure.**
> **It is a structural consequence of operating as a finite physical system.**
> **Governance is the architecture that manages information flow
> within thermodynamic constraints — not the elimination of those constraints.**

---

## Measurement Interface

RBIT's theoretical variables connect to log-observable metrics through operationalization work in companion theories. The following table summarizes the measurement status of key RBIT concepts:

| RBIT Concept | Operational Proxy | Source | Log Availability |
|---|---|---|---|
| Resolution-proxy ρ | 1 − (Type I + Type II errors) / N | Recovery Theory OP1 | HIGH |
| Buffer thickness | Perturbation amplitude before mode collapse; recovery-without-escalation rate | Recovery Theory §Proxy Gap | HIGH |
| Escalation frequency f_esc | Human overrides + supervisor calls + fallbacks / N_total | Recovery Theory OP3 | HIGH |
| Governance capacity C(t) | C_E(t) = escalation events resolved / Δt | Recovery Theory §C(t) | HIGH |
| Degradation efficiency β | β_T (Type I/II accuracy) + β_R (recurrence rate) | Recovery Theory §β | HIGH |
| S_proxy (instability) | n²_proxy / (C(t) · β(t)) | VST §3.2 + RT §S-equation | HIGH |
| VCZ distance d_VCZ | Normalized recovery cost / baseline | Recovery Theory §d(·) | HIGH |
| Opposing pair detection | Persistent negative gradient correlation | Recovery Theory §Proxy Gap | MEDIUM-HIGH |
| Resolution gap Δρ routing | Four-type classification (Math/HC/Tacit/Noise) | NAT §4.4 | HIGH |
| Cascade validation R | Branching ratio: activated_{t+1} / activated_t | NAT §7.2, VST §3.5.4 | HIGH |
| F_RBIT instability vector | (f₁,f₂,f₃,f₄,f₅) = ((1−ρ), Φ(−Δρ), Ψ(B), E, C) — normalized [0,1] each | RBIT §Appendix RFEF, VST §3.2.6 | HIGH (component-wise); scalar optional |
| Consistency Index I | 1 − Σwij/M (pair-level rule coherence) | GRT via TLG §0.1 | HIGH |
| Meta-Contradiction Ic | 1 − Σwij(global)/Mc (global rule conflicts) | GRT via TLG §0.1 | HIGH |
| Position overlap Poverlap | Attractor convergence degree | GRT via TLG §9.2 | HIGH |
| Dint (system diversity floor) | min(Dint_i) across domains | GRT via TLG §9.2 | HIGH |
| NAF detection: RDE | ‖Δrepresentation‖ / ‖Δinput‖ | Recovery Theory §NAF | MEDIUM |
| NAF detection: NCR | Novel-to-existing cluster assignment rate | Recovery Theory §NAF | MEDIUM |
| NAF detection: SR | Geometry change response to novel input | Recovery Theory §NAF | MEDIUM |
| Inner sphere convergence (HUG) | Hyperspherical Uniformity Gap | NAT §8.3.1 | MEDIUM (offline) |
| Fractal alignment | Perturbation-response proportionality | NAT §8.3.1 | MEDIUM |
| φ (value yield) | Reusable outcome rate (supporting signal only) | Recovery Theory §φ | MEDIUM |

```
Measurement dependency order:
  Immediately available (no new instrumentation):
    ρ, C(t), β, d_VCZ, buffer_thickness, f_esc, R

  Available with basin calibration:
    d(x,A) — attractor pull strength (requires reference set)

  Available when φ unit stabilizes:
    φ — reusable outcome rate (requires "exploration unit" definition)

  Remaining open:
    α absolute, β absolute, C absolute → formal calibration
    f(A_t, D_t) exact form → boundary conditions exist, exact form open
```

(See Recovery Theory §Operationalization v0.1 for full measurement procedures, and Network Architecture Theory §10.1 for the proxy table connecting architectural concepts to these metrics.)

---

## Open Problems

| # | Problem | Status |
|---|---------|--------|
| 1 | Full structural resolution measurement | Partially resolved (operational proxy ρ defined) |
| 2 | Resolution gap calibration — how does a sender determine correct degradation level? | Open |
| 3 | Upscaling detection — observable signals for layer maturity readiness | **Partially resolved** — U1–U3 operational criteria defined (§Upscaling); exact N_up calibration and Δρ significance threshold remain open |
| 4 | Cycle failure mode boundaries — formal definition of over-degradation boundary | Open |
| 5 | Dynamic minimum sufficient description — formal relationship between receiver maturity and minimum seed complexity | Open |
| 6 | Residual resolution floor quantification — relationship to asymptotic stability cost | Open |
| 7 | Exact form of `f(A_t, D_t)` in the resolution growth equation | Open |
| 8 | Formal mapping between resolution-proxy ρ and precision parameters in Active Inference | Open |
| 9 | Exact functional form of degradation calibration D(Δρ) and step-size parameters η₂, η₃ | Open |
| 10 | Formal derivation of F_RBIT from first principles; proof of equivalence or non-equivalence with variational free energy | **Partially resolved** — F_RBIT reframed as 5-component health vector; cross-architecture falsification uses directional concordance, not scalar comparison; weight arbitrariness removed from all falsification claims; formal derivation of component interactions from first principles remains open |
| 11 | Threshold value for gradient cosine similarity in Seed Test 3 | System-specific (open) |
| 12 | [v1.7-RTseries] RT-2 impossibility constraint on resolution measurement — under SCM, RBIT metrics (ρ, buffer thickness, diversity) inherit Metric Lock-In: zero-gradient on mismatch dimension. Resolution measurement requires external reference frame calibration per RT-2 §9.2 differential protocol | Open — calibration protocol architecture-dependent |
| 13 | [v1.7-RTseries] Resolution recovery capacity generation — RT-4 shows capacity is relational (three-level scaling). What is the minimum trust network topology for RBIT degradation-upscaling cycle to function? Single-agent RBIT may be structurally incomplete without relational substrate | Open — connects to RT-4 initialization problem |
| 14 | [v1.7-RTseries] Coordination–Cancellation in resolution diversity — RT-3 shows high V (diversity) can cancel under naïve aggregation. RBIT multi-agent resolution measurement may show same paradox: diverse resolution perspectives aggregate to zero without mediation | Open — connects to RT-3 Mediation Layer |

---

## Falsification Criteria

RBIT generates specific predictions that, if empirically violated, would require revision or abandonment of core claims. The following criteria are stated to enable principled rejection.

*Note on F_RBIT criteria:* Criteria 1, 4, and 5 reference F_RBIT components. These are evaluated using **sign concordance** (directional agreement between components and predicted outcomes) and **rank-order monotonicity**, not scalar threshold comparison. This is consistent with the vector representation of F_RBIT (Appendix §2).

**Criterion 1 — Resolution gap polarity must predict compression direction.**
If negative resolution gaps (Δρ < 0, i.e., f₂ > 0) do not produce receiver-controlled compression more frequently than sender-controlled compression, the central claim that gap polarity determines compression control is falsified. *Operationally: f₂ rising must predict compression direction shift with >50% base-rate improvement over unpredicted compression direction.*

**Criterion 2 — Calibrated degradation must outperform full delivery in immature-layer absorption.**
In controlled experiments where an immature layer receives identical information at full resolution vs. calibrated degradation, degradation must produce higher post-absorption resolution (measured via ρ) over a maturation window. If full delivery consistently equals or exceeds calibrated degradation, the degradation-as-design claim is falsified.

**Criterion 3 — Fractal propagation predictions (from VST §1.5.1).**
Three specific predictions must hold:
- Scale-invariant amplification rate: α_effective/C ratio follows consistent scaling across layers. If the ratio varies non-systematically, propagation is hierarchical but not fractal.
- Stage transition temporal ordering: intra-agent entropy collapse must precede inter-agent entropy collapse. If inter-agent instability appears first, the fractal propagation pathway is falsified.
- Intervention leverage asymmetry: cost-effectiveness ratio between adjacent scales must be approximately constant. If it varies dramatically, the fractal model is rejected.

**Criterion 4 — CW observability metrics (from Recovery Theory).**
If systems with SR ≈ 0, RDE ≈ 0, and NCR ≈ 1 (all corresponding to f₁ and f₂ elevated while f₄ appears low) do not exhibit subsequent stability degradation or adaptability loss, the Self-Consistent Misalignment model is falsified. *The SCM signature specifically predicts discordance: f₄ (escalation) low while f₁ (misclassification) rising — if this discordant pattern does not predict eventual instability cascade, the SCM detection protocol fails.*

**Criterion 5 — Storm onset must correlate with mismatch accumulation.**
If Vector Storms occur without preceding mismatch pressure accumulation (measurable via f₂ trajectory and f₃ buffer thickness decline), the pressure-accumulation model is wrong. *Operationally: f₂ and f₃ must both show rising trend in the N_up window preceding storm onset.*

**Criterion 6 — AND-entry / OR-exit must outperform symmetric governance protocols.**
Systems using AND-entry (all conditions required) for stable-state declaration and OR-exit (any single violation sufficient) for reactivation should experience fewer premature stability declarations AND fewer delayed exits compared to symmetric AND/AND or OR/OR protocols. If symmetric protocols match performance, the asymmetry claim (derived from TLG §5.3) is weakened.

**Criterion 7 — Minimum diversity determines vulnerability, not average.**
The domain with the lowest internal differentiation (Dint) should be the primary contamination entry point. If contamination entry points are uniformly distributed regardless of per-domain Dint, or if mean Dint is a stronger predictor, the minimum-aggregation claim is falsified. (Derived from TLG §9.2 via GRT.)

**Criterion 8 — Progressive withdrawal must reduce re-entry frequency.**
Systems governed by staged human withdrawal (active → audit → periodic review → exit) should require fewer collapse-recovery restarts than fixed-epoch phase transitions. If fixed-epoch systems achieve equal or lower re-entry frequency, the protocol's advantage is not established. (Derived from TLG §13.2.2.)

**Extended Falsification Framework (F4–F7) — Cross-theory governance criteria:**

```
F4 — Triple concordance must detect SCM earlier than dual:
  Systems with low f_esc + R > 1 should be flagged by R-ρ-f_esc
  but missed by R-ρ alone (cannot distinguish genuine vs
  governance-maintained stability).
  Falsification: triple provides no detection benefit over dual.

F5 — Stability Saturation must produce observable degradation:
  Systems with clean profiles (high ρ, low f_esc, SCC ≥ τ4)
  must subsequently show: elevated τ_recovery, Dint declining,
  or SR → 0. If no degradation follows apparent health,
  the SSS claim is unsupported.

F6 — Cumulative measurement must outperform reactive:
  λlog → θd calibration → constraint updates should detect trends
  earlier with fewer false alarms than per-event threshold systems.
  Falsification: reactive equals or exceeds cumulative.

F7 — Silent Criticality must be detectable via perturbation:
  Pre-collapse systems must show elevated τ_recovery and
  increasing cross-domain MI under perturbation testing.
  Falsification: no measurable difference from genuinely stable.

Complete falsification hierarchy:
  Criteria 1-5:   core RBIT predictions (information theory)
  Criteria 6-8:   TLG governance predictions (architecture)
  F4-F7:          cross-theory predictions (dynamics × governance)
```

(See Recovery Theory §Extended Falsification Framework and VST v1.5 §11.4 for derivations.)

---

## Status & Maturity

| Aspect | State |
|--------|-------|
| Core concepts | Defined and stable |
| Operational measurement (ρ) | Defined and usable |
| Physical grounding (Landauer) | Established — formal integration pending |
| Formal proofs | Not yet complete — see Open Problems |
| Implementation spec | Not yet specified |

### RBIT Working Paper v1.0 — Testable Predictions (with explicit falsification)

Four testable predictions with explicit observables, failure conditions, and expected regime transitions:

```
P1 — Sustained Negative Gap → Intent Replacement:
  Observable: accumulated divergence D_c under sustained Δρ < 0.
  Protocol: hold evaluation protocol fixed; measure D_c over τ windows.
  Failure condition: if D_c stabilizes without divergence under 
    sustained Δρ < 0 and no mitigation, Theorem 1 is falsified.
  Expected: D_c grows at least linearly (≥ η·τ per Lemma 1.1).

P2 — Contamination Boundary Existence:
  Observable: recovery success rate as function of contamination duration.
  Protocol: measure P_rec(t) across systems with varying τ exposure.
  Failure condition: if recovery probability does not decay beyond 
    boundary N ≤ ⌈D*/η⌉, the boundary model is falsified.
  Expected: discontinuous drop in P_rec at boundary N.

P3 — Calibrated Degradation Advantage:
  Observable: post-absorption ρ under calibrated vs. full delivery.
  Protocol: identical information, matched evaluation protocol, 
    immature receiver layer.
  Failure condition: full delivery ≥ calibrated degradation in 
    post-absorption ρ over maturation window.
  Expected: calibrated degradation produces higher ρ by preserving 
    sender-controlled compression.

P4 — SCM Co-occurrence Signature:
  Observable: simultaneous high V (coherence) + low H (hidden detection).
  Protocol: two-phase supervision-withdrawal experiment.
  Failure condition: if high V always implies high H, SCM 
    co-occurrence model is wrong.
  Expected: direct-label supervision produces V-H co-occurrence 
    (high V, low H after withdrawal = SCM signature).
  
  RBIT Working Paper Appendix E validation:
    Case 1 (direct labels): Phase 2 H = 0.038 (collapsed)
    Case 2 (meta-constraints): Phase 2 H = 0.899 (maintained)
    Case 1 shows high V + low H = SCM operational signature.
    Three-way decomposition confirms: heuristic rules, not "meta" 
    framing, are the operative mechanism.
```

### Experimental Validation Summary (RBIT + NAT Working Papers)

```
RBIT Appendix E — Bandit Withdrawal Experiment:
  2-arm hidden-regime bandit with supervision withdrawal at t=500.
  Three conditions: direct labels (Case 1), meta-constraints (Case 2), 
  noise baseline (Case 3).
  Results: 
    H(t) crossover at t× = 505 (within 5 steps of withdrawal)
    Case 2 H = 0.899, Case 1 H = 0.038
    Case1-Heuristic ablation H = 0.906 ≈ Case2 → heuristics are mechanism
    Parameter robustness: qualitative ordering holds across a ∈ {0.15, 0.35, 0.50}
    SCM co-occurrence: Case 1 shows high V + low H (Prediction P4 confirmed)

NAT Appendix D — 2-Agent Mediation Experiment:
  Two-agent coordination under partial observability.
  Deceptive regime (hidden contamination) + safe regime.
  Phase 1: communication; Phase 2: withdrawal.
  Results:
    Meta-constraint agents: detection H(t) = 0.603 (Phase 2)
    Direct signaling: H(t) = 0.462
    Proxy access ablation: effect = +0.14 (consistent across conditions)
    Signal format effect: ≈ 0 (meta vs direct indistinguishable when proxy equalized)
    → Structural mediation (3-layer proxy), not signal format, sustains coordination

NAT Appendix E — Mediation Layer Ablation:
  Same experiment without mediation layer (v1).
  Results: 2 of 4 predictions FAILED.
    Joint detection: 0.188 (FAIL: Case 1 > Case 2 → wrong direction)
    Coordination collapse: 0.021 (FAIL: Case 2 highest → wrong direction)
  Failure mechanism: unfiltered partner action → mutual reassurance loop → SCM
  3-layer mediation proxy (EWMA β=0.08 → suspicion β=0.06 → bounded w=0.08) 
  breaks the feedback loop.
  → Direct evidence for NAT Processing Isolation principle.
```

This is a **theoretical framework document**, not an implementation specification. The component theories of the DFG framework remain valid as standalone works and gain additional coherence when read on this foundation.

*For the governance architecture built on this foundation, see:*
*[Three-Layer Governance Architecture](../three-layer-architecture/)*

---

## References

**Information Theory**

Shannon, C. E. (1948). *A Mathematical Theory of Communication.* Bell System Technical Journal, 27(3), 379–423.

Landauer, R. (1961). *Irreversibility and heat generation in the computing process.* IBM Journal of Research and Development, 5(3), 183–191.

**Information Bottleneck Theory**

Tishby, N., Pereira, F. C., & Bialek, W. (2000). *The information bottleneck method.* Proceedings of the 37th Annual Allerton Conference, 368–377.

Tishby, N., & Zaslavsky, N. (2015). *Deep learning and the information bottleneck principle.* IEEE Information Theory Workshop (ITW), 1–5.

Shwartz-Ziv, R., & Tishby, N. (2017). *Opening the black box of deep neural networks via information.* arXiv:1703.00810.

Saxe, A. M., Bansal, Y., Dapello, J., et al. (2018). *On the information bottleneck theory of deep learning.* ICLR 2018.
— Showed compression phase depends on activation function choice; absent with ReLU. Cited in IB comparison section.

Goldfeld, Z., van den Berg, E., Greenewald, K., et al. (2019). *Estimating information flow in deep neural networks.* ICML 2019.
— Demonstrated unreliability of binning-based MI estimates for continuous activations. Cited in IB comparison section.

Alemi, A. A., Fischer, I., Dillon, J. V., & Murphy, K. (2017). *Deep variational information bottleneck.* ICLR 2017.

**Transformer Representation Analysis**

Tenney, I., Das, D., & Pavlick, E. (2019). *BERT rediscovers the classical NLP pipeline.* ACL 2019. arXiv:1905.05950.
— Lower transformer layers encode syntactic structure, upper layers encode semantic relationships — cited in the Single-Agent Grounding section.

Elhage, N., Nanda, N., Olsson, C., et al. (2021). *A mathematical framework for transformer circuits.* Transformer Circuits Thread [web report, Anthropic]. Retrieved from https://transformer-circuits.pub/2021/framework/index.html
— Circuit-level analysis of information processing across transformer layers — cited in the Single-Agent Grounding section. Note: this is a web report series, not a peer-reviewed journal article.

Rogers, A., Kovaleva, O., & Rumshisky, A. (2020). *A primer in BERTology: What we know about how BERT works.* Transactions of the Association for Computational Linguistics, 9, 842–866.
— Survey of representation analysis studies across BERT layers; provides additional empirical support for the resolution stratification claim in the Single-Agent Grounding section.

**Thermodynamics and Complex Systems**

Bennett, C. H. (1982). *The thermodynamics of computation — a review.* International Journal of Theoretical Physics, 21(12), 905–940.
— Formal treatment of the relationship between logical reversibility and thermodynamic cost; provides theoretical context for the Landauer connection in the Physical Basis section.

**Predictive Processing and Active Inference**

Friston, K. (2010). *The free-energy principle: a unified brain theory?* Nature Reviews Neuroscience, 11(2), 127–138. https://doi.org/10.1038/nrn2787
— Foundational statement of the free-energy principle and Active Inference framework; cited in the Relationship to Predictive Processing section for structural correspondence with RBIT's resolution gap and Vector Storm concepts.

Friston, K., FitzGerald, T., Rigoli, F., Schwartenbeck, P., & Pezzulo, G. (2017). *Active inference: a process theory.* Neural Computation, 29(1), 1–49. https://doi.org/10.1162/NECO_a_00912
— Process-level formulation of Active Inference including precision weighting; cited for structural correspondence with calibrated degradation in RBIT.

**ML Security — Data Contamination Vulnerability**

Biggio, B., Nelson, B., & Laskov, P. (2012). *Poisoning attacks against support vector machines.* ICML 2012.
— Early formal treatment of data poisoning; establishes that targeted contamination of training data degrades classifier boundaries.

Steinhardt, J., Koh, P. W., & Liang, P. (2017). *Certified defenses for data poisoning attacks.* NeurIPS 2017.
— Empirical and theoretical analysis of poisoning rate thresholds (~3-5% onset of sharp performance degradation); cited for contamination onset threshold correspondence in Recovery Theory.

Koh, P. W., & Liang, P. (2017). *Understanding black-box predictions via influence functions.* ICML 2017.
— Influence functions measure individual training point contribution to model output; cited for High-Context contamination weight correspondence in Recovery Theory.

Cohen, J., Rosenfeld, E., & Kolter, J. Z. (2019). *Certified adversarial robustness via randomized smoothing.* ICML 2019.
— Certified defense radius r provides formal lower bound on perturbation tolerance; cited for immunity capacity correspondence in Recovery Theory.


---

## Appendix: Bridge Hypothesis — Resolution-Based Free Energy Functional (RFEF)

*Note.* This appendix proposes a heuristic control functional for reasoning about stability tradeoffs in resolution-layered systems. It is not a reformulation of variational free energy or a derivation from first principles. The functional is offered as a structured summary of the design constraints described in the main text, not as a formal proof or claim of physical equivalence.

> *This appendix is not required for understanding the core RBIT framework. It is presented as a formal hypothesis and structural scaffold for readers familiar with Active Inference and control theory. The formulations here are hypotheses, not proven claims.*
#### 1. Layer State Observables

For each layer ℓ, the following quantities are observable:

```
ρ_ℓ   = resolution-proxy (classification reliability)
Δρ_ℓ  = ρ_{ℓ+1} − ρ_ℓ   (resolution gap)
B_ℓ   = buffer layer thickness
E_ℓ   = escalation frequency (unresolved conflict proxy)
C_ℓ   = bounded resource expenditure (thermodynamic/compute constraint)
```

#### 2. Resolution-Based Free Energy Functional

**Primary representation — health vector (no weights required):**

F_RBIT is treated primarily as a **five-component health vector**, not a scalar score. Cross-architecture falsification uses directional concordance across components, not scalar comparison. Scalar aggregation is optional and restricted to within-architecture monitoring.

```
F_RBIT(ℓ) := (f₁, f₂, f₃, f₄, f₅)

  f₁ = (1 − ρ_ℓ)             [misclassification — higher = worse]
  f₂ = Φ(−Δρ_ℓ)              [resolution mismatch — higher = worse]
  f₃ = Ψ(B_ℓ)                [buffer instability — higher = worse]
  f₄ = E_ℓ                   [escalation load — higher = worse]
  f₅ = C_ℓ                   [resource dissipation — higher = worse]
```

All five components are normalized to [0, 1] before any comparison (unit-free). Each is independently interpretable: f₁ tracks classification quality, f₂ tracks resolution mismatch, f₃ tracks buffer health, f₄ tracks governance load, f₅ tracks resource pressure.

**Cross-architecture falsification criterion (concordance-based):**

```
Instability increasing:   majority of (f₁,...,f₅) rising simultaneously
Instability decreasing:   majority of (f₁,...,f₅) falling simultaneously
Discordant (ambiguous):   components diverge — domain-specific check required

Cross-validation with S_norm (VST):
  Concordant:   S_norm rising AND majority of F_RBIT components rising → confirmed
  Discordant:   S_norm rising BUT F_RBIT components stable → architecture-specific
                S_norm stable BUT F_RBIT components rising → local layer issue
```

Falsification criteria 1, 4, and 5 use sign concordance (directional agreement) and rank-order monotonicity, not scalar threshold comparison. This eliminates weight arbitrariness from all cross-theory claims.

**Optional scalar aggregation (within-architecture monitoring only):**

When a single summary signal is operationally convenient, scalar aggregation uses equal weights with robustness verification:

```
F_RBIT_scalar(ℓ) = (1/5) · Σᵢ fᵢ    [equal-weight baseline]

Weight robustness check:
  Claims are restricted to regimes invariant under weight perturbation
  δwᵢ ∈ [−0.1, +0.1] around equal weights.
  If a conclusion inverts under this perturbation, it is not reported
  as a robust finding.
```

The equal-weight baseline is not claimed to be optimal. It is the minimum-assumption default. Architecture-specific weights may be calibrated from operational logs but are not required for any falsification test in this framework.

**Function class specification for Φ and Ψ:**

Both Φ and Ψ are chosen from the **hinge function class** (default) or the **logistic function class** (when saturation is architecturally motivated). The specific form affects scaling but not directional tests.

```
Default (hinge):
  Φ(x)  = max(0, x)              x = −Δρ (positive when mismatch)
  Ψ(B)  = max(0, B₀ − B)        B₀ = reference buffer thickness (see below)

  Properties: monotone, bounded below by 0, zero below reference point,
              linear above — interpretable and reviewer-transparent.

Alternative (logistic, use when saturation at extremes is required):
  Φ(x)  = 1 / (1 + exp(−k(x − x₀)))
  Ψ(B)  = 1 / (1 + exp(k(B − B₀)))

  k = steepness parameter (architecture-calibrated)
  Properties: monotone, bounded [0,1], smooth — prevents extreme values
              from dominating the scalar sum.
```

**B₀ initialization — rolling bootstrap (architecture-independent):**

B₀ is not an architecture-defined constant. It is initialized through Phase-0 bootstrapping as a rolling high-quantile estimate of observed buffer capacity, ensuring that the reference reflects what the system actually achieves in stable operation — not what a designer assumed.

```
During Phase 0 (burn-in window):
  B₀(t) = rolling_quantile(B_observed, q = 0.90)

  q = 0.90: 90th percentile of observed buffer thickness
  Rolling window: same N₀ as Phase 0 duration (domain-velocity calibrated)

Rationale for high quantile over maximum:
  max: locks onto outlier early observations → biased reference
  Q₉₀: robust to early spikes, reflects sustained high-buffer states → stable reference

After Phase 0 → Phase 1 transition:
  B₀ is fixed at the final Phase 0 Q₉₀ estimate
  Recalibration permitted at same trigger points as τ re-estimation:
    (1) Seed Handover phase transition
    (2) New domain added to system scope
    (3) Collapse recovery restart

Cross-architecture comparison:
  B₀ is expressed as a fraction of maximum observed buffer capacity
  (B₀_normalized = B₀ / B_max_observed) when comparing across architectures
  This preserves architecture independence in cross-system falsification tests.
```

*Connection to GRT θ_drift bootstrapping:* B₀ initialization follows the same philosophy as θ_drift(0) = Q₉₅ − Q₅₀ from Phase 0 statistics. Both use observed operational history rather than design priors as the calibration anchor. The common principle: **reference points are earned by the system, not assigned by the designer.**

*Justification for hinge as default:* The hinge form makes the reference point (B₀) explicit and the cost linear above it. It introduces no free curvature parameters. The logistic form is appropriate when the system is known to saturate. In the absence of saturation evidence, hinge is preferred.

Note: (1 − ρ_ℓ) = misclassification rate, so f₁ increases as ρ decreases.
Stable operation corresponds to regimes in which all five F_RBIT components
remain bounded under increasing interaction complexity.

#### 3. τ₁–τ₃ as Regime-Switching Control

Define the instability signal G_ℓ as the **dominant component of F_RBIT(ℓ)** — the highest-valued fᵢ after normalization, or the count of components simultaneously rising. The τ protocol implements discrete, event-triggered governance steps — not continuous gradient descent:

```
G_ℓ > τ₁  →  MARK
               Triggered when: f₁ (misclassification) OR f₄ (escalation) rises
               above baseline — earliest anomaly signal, single-component
               u_ℓ = monitoring + signal logging

G_ℓ > τ₂  →  SOFT CORRECT
               Triggered when: ≥ 2 components rising simultaneously,
               OR f₂ (resolution mismatch) enters positive territory
               — local attractor instability, loop risk
               u_ℓ ≈ instability-reducing step (η₂)
               via: boundary tightening, seed injection,
                    calibrated degradation

G_ℓ > τ₃  →  HARD CORRECT
               Triggered when: ≥ 3 components rising simultaneously,
               OR majority trend is monotonically worsening across window W
               — system leaves local stability basin
               u_ℓ ≈ large corrective step (η₃ ≫ η₂)
               via: loop severance, attractor reset,
                    structural realignment
```

η₂, η₃: architecture-defined step-size parameters (exact calibration: open problem).

*Minimum gap requirement between thresholds:* τ₂ − τ₁ must be sufficient to allow at least one full evaluation window W between MARK and SOFT CORRECT activation. If τ₁ and τ₂ are set too close, the MARK → monitoring phase is effectively skipped. Operationally: set τ₁ at the single-component threshold and τ₂ at the two-component threshold — this structural gap is enforced by the counting criterion, not by numerical proximity.

> *The τ₁–τ₃ protocol can be interpreted as a regime-switching control policy
> implementing discrete approximations to instability-reducing steps on F_RBIT
> when structural instability exceeds locally tolerable bounds. Under the vector
> representation, thresholds correspond to component-count conditions rather
> than scalar magnitude levels — eliminating weight sensitivity from the
> switching logic.*

The continuous formulation dS/dt ∝ −∇F_RBIT is presented for structural
analogy only. The operational form is the event-triggered switching above.

#### 4. Degradation Calibration as Precision-Matched Transmission

Degradation level D_{ℓ←ℓ+1} is a monotone function of Δρ_{ℓ+1,ℓ}:

```
Δρ >> 0   →  lower degradation (richer seed transmissible)
Δρ ≈ 0    →  increased degradation (layer near capacity)
Δρ < 0    →  transmission restricted → contain / upper intervention
```

In Active Inference terms, this corresponds to precision-matched message passing:
the sender adjusts signal resolution to match what the receiver can incorporate
without forced compression. Exact functional form of D(Δρ): open problem.

#### 5. Rest Mode as Steady State

```
Rest Mode condition:  d(F_RBIT)/dt ≈ 0 for all five components,
                      but F_RBIT ≠ (0,0,0,0,0)

Operationally:
  Each fᵢ bounded and non-monotone over evaluation window W
  No component in sustained rising trend
  At least one component > 0 (residual instability maintained)

Not: zero instability (impossible)
Not: all components at zero (structurally absent)
But: bounded fluctuation equilibrium —
     information intake and internal dissipation remain balanced
     across all five dimensions simultaneously,
     preventing long-term accumulation on any single axis
```

*Rest Mode in the scalar approximation (F_RBIT_scalar ≈ const):* when the optional equal-weight scalar is used for monitoring, dF_RBIT_scalar/dt ≈ 0 is a necessary but not sufficient condition. Sufficient condition requires per-component stability — a scalar that is stable because two rising components cancel two falling components does not satisfy Rest Mode. The per-component criterion is primary.

#### 6. Relationship to Active Inference (Carefully Bounded)

> The proposed functional is not claimed to be equivalent to variational free
> energy used in Active Inference frameworks. However, both formulations share
> a structural role: instability arises when prediction or interpretation capacity
> becomes mismatched to incoming complexity, and corrective dynamics act to
> restore a manageable representational regime.

```
Active Inference signal   →   RBIT structural analog
──────────────────────────────────────────────────────
Prediction error          →   f₁: Classification error (1 − ρ)
Precision Π               →   ρ (resolution-proxy, structural analog)
Free energy F             →   F_RBIT vector (f₁,...,f₅)
Precision-weighted update →   Calibrated degradation D(Δρ)
Policy update             →   τ₁–τ₃ component-count switching
Steady state              →   Rest Mode (all fᵢ bounded, non-monotone)
```

**Epistemic status:** F_RBIT is a proposed structural analogy. The vector representation makes this clearer than a scalar sum: each fᵢ has a distinct Active Inference analog, and no claim is made that the components combine in the same way as variational free energy terms. The correspondence is presented to aid interpretation and identify open formal problems — not to claim derivation from or equivalence with Active Inference.

---

## Document Structure

### Original RBIT Document (Section Map)

| Section | Contents |
|---------|----------|
| 1. Resolution and Vector Space Maturity | Resolution definition, three-tier hierarchy, buffer layer thickness, resolution-proxy |
| 2. Why Discretization Is Necessary | Scaling failure of continuous processing, governance thresholds as designed minimum units |
| 3. Degradation as Space Preservation | Intent preservation mechanism, space management, tree vs. seed distinction |
| 4. Upscaling as Maturity Expression | Definition, upscaling vs. escalation, trigger conditions |
| 5. The Degradation-Upscaling Cycle | Full cycle, formal representation R_{t+1}, failure modes |
| 6. Seeds as Minimum Sufficient Information | Definition, calibration, recalibration as layer resolution grows |
| 7. Fractal Resolution Structure | Resolution hierarchy, bidirectional management, residual resolution floor |
| 8. Data Classification as Discretization | Four types, classification as resolution matching |
| 9. Relationship to Existing Information Theory | Shannon, Kolmogorov complexity, dynamic minimum sufficient description |
| 10. Open Problems | Open problems with current status |
| 11. Relationship to DFG Component Theories | Connections to Vector Storm, Network Architecture, Governance Rules, Three-Layer |

### README Extensions (Not in Original Document)

| README Section | Contents | Status |
|----------------|----------|--------|
| Physical Basis | Restructured: combinatorial + governance arguments primary; Landauer as supporting motivation | Updated v1.1 |
| Substrate Principle (D0) | Geometry alignment as substrate interpretation; contamination = geometry mismatch projection | New v1.1 |
| Operational Contamination Boundary | N-step behavioral criterion; contamination = absence of return path | New v1.1 |
| Single-Agent Grounding | Transformer hierarchy, attention allocation, failure mode reinterpretation, Externalization Principle, system-level additions beyond existing explanations | Updated v1.1 |
| Information Bottleneck Comparison | 5 structural differences; IB vs RBIT positioning; mutual limitations | New v1.1 |
| Active Inference Relationship | Structural correspondence, ρ–precision hypothesis, positioning | Conceptual draft |
| Seed Sufficiency Test Protocols | Operational validation via SR, RDE, NCR, RIR metrics; D7 Boundary Agent for Test 3 | New v1.1 |
| f Boundary Conditions | S-equation constraints on f(A_t, D_t) shape | New v1.1 |
| Fractal Conditional Necessity | SOC-grounded scaling argument; conditional on R ≈ 1 regime | New v1.1 |
| Falsification Criteria | 5 specific criteria for principled rejection of core claims | New v1.1 |
| Appendix: RFEF | F_RBIT functional, τ regime-switching, Bridge Hypothesis | Formal hypothesis only |

---

*Timestamped: February 23, 2026*
*DFG Framework · Resolution-Based Information Theory v1.6*
