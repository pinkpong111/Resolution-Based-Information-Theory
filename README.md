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

*Scope.* RBIT is primarily an architectural information theory — a framework for designing how information should transform as it moves between layers of different resolution capacity. References to thermodynamics (Landauer) and predictive processing (Active Inference) provide structural motivation and correspondence, not derivation or physical reduction. RBIT does not claim to be a physical theory of computation or a reformulation of Bayesian inference.

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

*Trim point derivation from F_RBIT.* For a vector v with size s(v), the optimal trim range is bounded by two conditions derivable from the F_RBIT functional:

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

Key requirement: `f(A_t, D_t) > 0` requires `D_t > 0` — absorption must be sender-controlled at a positive resolution gap. The exact form of `f` remains an open problem.

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

RBIT's residual resolution floor — the minimum below which the lowest layer cannot further discriminate — is therefore not a design choice. It is a resource-bounded irreducibility floor (thermodynamically motivated):

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
