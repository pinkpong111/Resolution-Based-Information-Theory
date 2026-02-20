# Resolution-Based Information Theory (RBIT)

**Degradation, Upscaling, and Vector Space Maturity in Multi-Agent Systems**

> *Draft · February 19, 2026 · Internal Working Document*
> *Component of the Deficit-Fractal Governance (DFG) Framework*

---

## What This Is

RBIT is the **information-theoretic foundation** of the DFG framework.

Shannon's information theory solved how to transmit information efficiently across a noisy channel — optimizing fidelity between systems of **fixed capacity**.

RBIT addresses a different problem:

> **How should information transform as it moves through layers of different resolution — and how does the system grow in its capacity to handle higher resolution over time?**

These are complementary problems, not competing ones.

| | Shannon | RBIT |
|---|---|---|
| **Receiver capacity** | Fixed | Variable, growing |
| **Goal** | Maximize transmission rate | Maintain downstream behavior within upstream-defined constraint classes across resolution levels *(operational goal)* |
| **Loss** | Minimize | Design deliberately to match receiver resolution |
| **Core question** | How much can be sent? | How should information change as it moves through the system? |

---

## Why This Framework Is Needed

Perfect resolution — the complete discrimination of all incoming states — is asymptotically unreachable for finite systems operating under bounded energy and time constraints. Every finite system retains an irreducible floor of unresolvable states. This is not an engineering limitation to be solved with more compute. It is a structural consequence grounded in thermodynamic principles (Landauer, 1961).

The consequence for multi-agent AI systems: degradation is not a governance failure. It is a structural necessity. The question is not whether information will be compressed as it moves through layers — it will — but **who controls the compression and whether intent survives it**.

Existing frameworks treat all compression as failure to minimize. In adaptive multi-agent systems, this produces two design errors: over-delivering information to immature layers causes Vector Storm; under-delivering without preserving generative structure causes developmental stall. Neither error is addressable within a framework that treats all compression as loss.

RBIT is the framework that makes compression designable rather than accidental — distinguishing between harmful compression (receiver-controlled, intent-replacing) and functional compression (sender-controlled, intent-preserving).

---

## Core Concepts

### Vectors — Terminology Note

In this framework, a **vector** refers to a directional tendency in an agent's behavior or processing — the general orientation of its exploration, decisions, or outputs. Vectors are not mathematical objects in the strict sense. They represent the direction and intensity of an agent's operational focus within a shared processing space.

A vector space is the full set of positions an agent or layer can occupy. As a layer matures, its vector space expands — more positions become available, more distinct vectors can coexist without collision.

### Intent — Terminology Note

Throughout this document, **intent** refers to the *generative constraint structure* that limits the space of valid interpretations — not semantic meaning or subjective intention. Intent is preserved when the receiving layer generates outputs within the same constraint structure as the sender, even at lower resolution. A layer can receive a degraded seed and still preserve the sender's intent if the degraded form carries the generative constraint intact. Operationally, intent preservation is evaluated through invariance of output constraint structure under resolution change — if the class of outputs generated remains consistent with the sender's constraint structure across resolution levels, intent is preserved.

*Operational note (minimal test).* In this draft, intent preservation is treated as a testable invariance property under resolution change: given the same upstream seed family, the downstream layer should produce outputs that remain within a stable equivalence class defined by externally checkable constraints (e.g., invariant boundary compliance, task-level invariants, or protocol-form invariants). This does not fully specify the latent constraint structure, but it provides a minimal operational handle for comparing whether degradation preserves or replaces upstream generative structure.

### Vector Storm — Terminology Note

**Vector Storm**: a cascade failure mode in which incoming information complexity exceeds a layer's resolution capacity, causing forced compression across multiple vectors simultaneously. When compression cascades, positional overlap occurs — vectors that should occupy distinct positions collapse into the same region of the vector space — producing system-wide instability. Vector Storm is not a rare edge case. It is an archetypal failure mode when resolution gaps are unmanaged or persistently negative. This description is phenomenological: multiple mechanisms can realize the same cascade pattern.

---

### Resolution

The capacity of a layer to distinguish between, simultaneously hold, and process vectors of different directions without one dominating the others.

Resolution is **not** computational power, parameter count, or processing speed. It is the structural capacity to maintain distinction between competing vectors — a property that grows through experience and calibrated absorption.

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
Gap < 0 (negative)    Forced receiver-controlled compression → Vector Storm risk
```

### Degradation

Deliberate reduction of information resolution before delivery to a lower layer.

**Standard view:** degradation = necessary loss, minimize wherever possible.

**RBIT hypothesis:** calibrated degradation can, in some regimes, preserve upstream intent more robustly than full delivery, because it keeps compression under sender control rather than inducing receiver-controlled collapse.

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

### Seeds

Information degraded to the **minimum resolution at which the core generative structure is preserved** and the receiving layer's vector space is not occupied beyond capacity.

Seeds are not simplified rules. They are precisely calibrated degradations.

```
Tree (full delivery)   → One specific behavior. Environment changes: fails.
Seed (calibrated)      → Class of behaviors. Environment changes: adapts.
```

A seed contains less information than a tree in the conventional sense — but preserves more of the original generative intent, and leaves space for the diversity that makes the system stable.

*Identity seeding vs. goal/utility injection (scope boundary).* Identity seeds specify an exploration domain and interface boundaries — which space the agent is expected to cover and where it should not intrude — not an objective function, utility, or reward criterion. Concretely, an identity seed constrains *where* an agent searches (domain and boundary), while prohibited goal/utility injection constrains *what* the agent optimizes (preference ordering over outcomes). Identity seeds are therefore treated as routing and coverage priors that preserve system-wide diversity and prevent role vacuums, while leaving local policies and reward tradeoffs to be learned. If an identity seed encodes outcome preferences or success criteria beyond boundary compliance, it is no longer an identity seed and falls into prohibited scope.

### Contamination — Terminology Note

A **contaminated vector** is one that has deviated from its resolution-appropriate trajectory and begun self-reinforcing in a loop — amplifying in a fixed direction regardless of incoming information. Contamination is not moral failure or intentional deviation. It is a structural condition: a vector that can no longer update through normal absorption because it has exceeded its layer's correction capacity.

### Buffer Layer

A zone of directionally neutral material (noise) placed between opposing vectors by the upper layer. The upper layer, operating at Tier 3 resolution, identifies which vectors are structurally opposed and places neutral material between them to prevent direct collision.

Buffer layer thickness is a direct observable proxy for upper layer resolution precision: the more accurately the upper layer maps opposing relationships, the thicker the buffer it can maintain. This avoids a measurement circularity — if resolution were defined by contamination detection rate, and contamination by resolution, neither could be measured independently. Buffer thickness breaks this loop.

```
Thicker buffer = higher upper layer resolution
Thin or absent buffer = Vector Storm precondition
```

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

**Why step 4 occurs:** Each successfully absorbed vector creates a new stable attractor position in the vector space. This new position makes adjacent positions more distinguishable — the layer can now separate vectors it previously collapsed together. Absorption of calibrated information is the mechanism of maturity: the vector space does not expand by instruction, but by the structural residue of each absorption event.

Formal representation:

```
R_{t+1} = R_t + f(A_t, D_t)

  R_t  = layer resolution at time t
  A_t  = volume of calibrated information absorbed at time t
  D_t  = degradation calibration quality at time t
  f    = monotone increasing in both arguments
```

Key requirement: `f(A_t, D_t) > 0` requires `D_t > 0` — absorption must be sender-controlled at a positive resolution gap. The exact form of `f` remains an open problem.

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

The above instantiation uses contamination classification as a concrete and auditable discrimination task. More generally, ρ can be defined for any layer-specific discrimination task with Type I/II errors, provided the task is held fixed across comparisons.

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

### Buffer Layer Thickness

A second independent observable proxy for upper layer resolution — the spatial separation maintained between opposing vectors. Tracks resolution changes without requiring classification event data.

---

## Grounding in Single-Agent Architecture

RBIT's core claims — resolution stratification, degradation, and the resolution gap — are not hypothetical properties of future multi-agent systems. They are already observable within competent single-agent architectures.

### Resolution Stratification Inside a Transformer

A large language model's internal structure already exhibits the resolution hierarchy RBIT describes:

| Layer region | Processing role | Resolution characteristic |
|-------------|-----------------|--------------------------|
| Early layers | Syntax, local pattern detection | High volume, low semantic resolution |
| Middle layers | Relational synthesis | Intermediate |
| Late layers | Semantic intent, abstract reasoning | Lower volume, high resolution |

The upper layers of a transformer correspond structurally to the upper layer of the DFG three-layer architecture: they hold the most abstract, highest-resolution map of the input space. Early layers correspond to lower agents processing at Tier 1–2 resolution.

The resolution gradient across transformer layers has been empirically observed in representation analysis studies — lower layers encode syntactic and local structure, higher layers encode semantic and abstract relationships (Tenney et al., 2019; Elhage et al., 2021; Rogers et al., 2020). This gradient is structurally consistent with the RBIT resolution hierarchy. The correspondence motivates the Externalization Principle below.

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

## Relationship to DFG Component Theories

RBIT is the foundation from which the following derive:

| Theory | RBIT connection |
|--------|----------------|
| **Vector Storm Theory** | Vector Storm = negative resolution gap event (under-degradation cascade) |
| **Network Architecture Theory** | Data classification = resolution matching; escalation = resolution gap signal |
| **Governance Rules Theory** | Seeds = dynamic minimum sufficient information; Rest Mode = thermodynamic steady state; seed handover = resolution matching event |
| **Three-Layer Governance Architecture** | Middle layer = resolution mediation layer; seeding = calibrated degradation; τ thresholds = resolution gap response boundaries |

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

In RBIT terms, resolution is the capacity to distinguish between states — to separate vectors that would otherwise collapse into the same position. Increasing resolution means making previously indistinguishable states distinguishable. This is a physical process, not merely a computational one.

### Landauer's Principle and the Cost of Discrimination

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

### The Residual Floor as Irreducible Entropy

RBIT's residual resolution floor — the minimum below which the lowest layer cannot further discriminate — is therefore not a design choice. It is the thermodynamic floor:

```
Residual degradation floor
  = minimum irreducible entropy of the processing system
  = the point at which further state discrimination
    costs more than the system's energy budget allows

This floor:
  → Cannot be reduced to zero
  → Persists regardless of system maturity
  → Generates irreducible residual noise at every scale
  → Is the structural basis for asymptotic (not absolute) stability
```

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

## Open Problems

| # | Problem | Status |
|---|---------|--------|
| 1 | Full structural resolution measurement | Partially resolved (operational proxy ρ defined) |
| 2 | Resolution gap calibration — how does a sender determine correct degradation level? | Open |
| 3 | Upscaling detection — observable signals for layer maturity readiness | Open |
| 4 | Cycle failure mode boundaries — formal definition of over-degradation boundary | Open |
| 5 | Dynamic minimum sufficient description — formal relationship between receiver maturity and minimum seed complexity | Open |
| 6 | Residual resolution floor quantification — relationship to asymptotic stability cost | Open |
| 7 | Exact form of `f(A_t, D_t)` in the resolution growth equation | Open |
| 8 | Formal mapping between resolution-proxy ρ and precision parameters in Active Inference | Open |
| 9 | Exact functional form of degradation calibration D(Δρ) and step-size parameters η₂, η₃ | Open |
| 10 | Formal derivation of F_RBIT from first principles; proof of equivalence or non-equivalence with variational free energy | Open |

---

## Status & Maturity

| Aspect | State |
|--------|-------|
| Core concepts | Defined and stable |
| Operational measurement (ρ) | Defined and usable |
| Physical grounding (Landauer) | Established — formal integration pending |
| Formal proofs | Not yet complete — see Open Problems |
| Implementation spec | Not yet specified |

This is a **theoretical framework document**, not an implementation specification. The component theories of the DFG framework remain valid as standalone works and gain additional coherence when read on this foundation.

*For the governance architecture built on this foundation, see:*
*[Three-Layer Governance Architecture](../three-layer-architecture/)*

---

## References

**Information Theory**

Shannon, C. E. (1948). *A Mathematical Theory of Communication.* Bell System Technical Journal, 27(3), 379–423.

Landauer, R. (1961). *Irreversibility and heat generation in the computing process.* IBM Journal of Research and Development, 5(3), 183–191.

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


---

## Appendix: Bridge Hypothesis — Resolution-Based Free Energy Functional (RFEF)

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

A candidate instability functional for layer ℓ:

```
F_RBIT(ℓ) = w₁·(1 − ρ_ℓ)        [misclassification term]
           + w₂·Φ(−Δρ_ℓ)         [resolution mismatch penalty]
           + w₃·Ψ(B_ℓ)            [buffer instability term]
           + w₄·E_ℓ               [escalation load]
           + w₅·C_ℓ               [resource dissipation cost]

  w₁–w₅  : architecture-defined weighting parameters
  Φ(·)   : monotone increasing when Δρ < 0
             (upper layer cannot interpret lower layer output)
  Ψ(·)   : dΨ/dB < 0
             (buffer thinning → instability increase)
```

Note: (1 − ρ_ℓ) = misclassification rate, so F_RBIT increases as ρ decreases.
Stable operation corresponds to regimes in which F_RBIT remains bounded
under increasing interaction complexity.

#### 3. τ₁–τ₃ as Regime-Switching Control

Define the instability signal G_ℓ = F_RBIT(ℓ). The τ protocol implements
discrete, event-triggered governance steps — not continuous gradient descent:

```
G_ℓ > τ₁  →  MARK
               deviation detected, gradient small
               u_ℓ = monitoring + signal logging

G_ℓ > τ₂  →  SOFT CORRECT
               local attractor instability, loop risk
               u_ℓ ≈ instability-reducing step (η₂)
               via: boundary tightening, seed injection,
                    calibrated degradation

G_ℓ > τ₃  →  HARD CORRECT
               system leaves local stability basin
               u_ℓ ≈ large corrective step (η₃ ≫ η₂)
               via: loop severance, attractor reset,
                    structural realignment
```

η₂, η₃: architecture-defined step-size parameters (exact calibration: open problem).

> *The τ₁–τ₃ protocol can be interpreted as a regime-switching control policy
> implementing discrete approximations to instability-reducing steps on F_RBIT
> when structural instability exceeds locally tolerable bounds.*

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
Rest Mode condition:  dF_RBIT/dt ≈ 0,  but  F_RBIT ≠ 0

Not: zero instability (impossible)
But: bounded fluctuation equilibrium —
     information intake and internal dissipation remain balanced,
     preventing long-term accumulation of unresolved structural entropy
```

#### 6. Relationship to Active Inference (Carefully Bounded)

> The proposed functional is not claimed to be equivalent to variational free
> energy used in Active Inference frameworks. However, both formulations share
> a structural role: instability arises when prediction or interpretation capacity
> becomes mismatched to incoming complexity, and corrective dynamics act to
> restore a manageable representational regime.

```
Active Inference signal   →   RBIT structural analog
──────────────────────────────────────────────────────
Prediction error          →   Classification error (1 − ρ)
Precision Π               →   Resolution-proxy ρ (structural analog)
Free energy F             →   F_RBIT (proposed instability functional)
Precision-weighted update →   Calibrated degradation D(Δρ)
Policy update             →   τ₁–τ₃ regime switching
Steady state              →   Rest Mode (dF_RBIT/dt ≈ 0)
```

**Epistemic status:** F_RBIT is a proposed structural analogy. The correspondence
is presented to aid interpretation and identify open formal problems —
not to claim derivation from or equivalence with Active Inference.

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
| Physical Basis | Landauer grounding, residual floor, thermodynamic analogy | Conceptual draft |
| Single-Agent Grounding | Transformer layer hierarchy, attention allocation, failure mode reinterpretation, Externalization Principle | Conceptual draft |
| Active Inference Relationship | Structural correspondence, ρ–precision hypothesis, positioning | Conceptual draft |
| Appendix: RFEF | F_RBIT functional, τ regime-switching, Bridge Hypothesis | Formal hypothesis only |

---

*Timestamped: February 19, 2026*
*DFG Framework · Resolution-Based Information Theory v1.0*
