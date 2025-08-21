UPCA / IACE — Compressed Summary (unified)

Core claim: Intelligence = resource-rational predictive control. An agent with a hierarchical generative model minimizes expected free energy while pricing computation and time. Ethics is intrinsic: an “ethics head” minimizes ethical prediction error against structured normative priors η embedded in the same generative scaffold as world knowledge.

Unification of framings:

UPCA v4.1 modules ↔ IACE terms ↔ Tripartite phrasing

ME (Motor/Perceptual Execution) ↔ APs ↔ Detail Engine (D)

MA (Meta-Actions / Planning) ↔ Speculative Engine ↔ Abstract/Fantasy Engine (A)

SI (Systemic Information / Skills) ↔ Skill Memory/Induction ↔ (cross-cuts D/A)

AMC (Meta-Cognitive Arbiter + Ethics) ↔ Subconscious Allocator ↔ Conscience Module (C)

Scaffold (θ, η) = shared hierarchical model (facts + ethics).

Mechanistic arbitration (no homunculus):

Surplus 
𝑆
^
𝑡
S
^
t
	​

: inferred allostatic state (Kalman/variational filter over multi-sensor interoceptive proxies).

Gate/threshold 
𝜃
𝑡
θ
t
	​

: circuit-level bound (TRN, STN, striatum D1/D2, FPC) under receptor-specific NE/ACh/DA/5-HT control.

Controller auction: leaky-WTA over bids 
𝑈
𝑖
=
𝐸
[
Δ
FE
𝑖
]
time_cost
𝑖
(
DA, 5-HT
)
+
energy_cost
𝑖
(
𝑆
^
)
U
i
	​

=
time_cost
i
	​

(DA, 5-HT)+energy_cost
i
	​

(
S
^
)
E[ΔFE
i
	​

]
	​

.

Engagement: 
𝑔
𝑀
𝐵
=
𝜎
(
𝛼
 
𝜀
res
+
𝛽
 
𝑆
^
−
𝜃
𝑡
)
g
MB
	​

=σ(αε
res
	​

+β
S
^
−θ
t
	​

). Budget 
𝐵
plan
=
𝐵
max
⁡
 
𝑔
𝑀
𝐵
 
𝑆
^
B
plan
	​

=B
max
	​

g
MB
	​

S
^
.

Ethics as prediction:

η (ethical priors): structured probabilistic graphs in the Scaffold.

Ethical error 
𝜖
𝜂
ϵ
η
	​

: divergence between predicted vs. posterior ethical valence on imagined/actual outcomes; updates η and modulates D/A via AMC.

Bayesian multi-objective ethics: stakeholder-weighted costs with uncertainty over η.

Learning & consolidation:

Wake: use-weighted Hebbian plasticity scaled by precision-weighted surprise and controller recruitment.

Sleep: global down-selection + controller-specific replay (MB↔HPC-PFC; MF↔striatal/cerebellar).

Testable predictions (preregisterable):

Energy-ordered failure: under safe energy clamps, MB depth & HPC–PFC coupling fail before habits; brief LC-NE reset precedes collapse.

Access interactions: ACh×SNR and NE×volatility modulate MB gating at matched 
𝑆
^
S
^
.

Controller-specific sleep effects and DA inverted-U on vigor/precision.

Immediate structural call-outs (required to avoid hidden circularity)

Ethical identifiability: 
𝜖
𝜂
ϵ
η
	​

 requires an operationalized valence space and observables; without preregistered labeling/IRL schemas and task panels, η updates risk degeneracy. Include a grounding set (tasks + annotation protocol) and stakeholder map with explicit uncertainty.

Surplus estimation validity: 
𝑆
^
S
^
 must be fit-and-test with cross-modal validation (e.g., fNIRS/fMRI cortical power) and perturbations (hypoxia, glucose). Otherwise 
𝑆
^
S
^
 collapses into a generic arousal proxy.

Gate localization: 
𝜃
𝑡
θ
t
	​

 decomposition (TRN/STN/D1/D2/FPC) needs double dissociation via pharmacology/DBS/EEG signatures to avoid lumping all control into a single latent.

Dual nomenclature drift: Three phrasings (UPCA, IACE, D/A/C) can leak inconsistencies. Freeze the unified glossary below and use AMC (with Ethics head) as the single term for metacontrol+ethics throughout code/docs.

README Outline (complete, unified; ready to fill)
1) Title & Tagline

UPCA (Unified Predictive Cognitive Architecture)
Resource-rational predictive control with intrinsic ethical alignment.

Badges (to add later): build | tests | coverage | docs | license

2) Why UPCA?

Problem: scalable abstraction & planning with verifiable alignment.

Approach: one predictive scaffold for perception, imagination, action, and ethics; computation/time are priced; control is auctioned, not commanded.

What’s new: mechanized surplus 
𝑆
^
S
^
, circuit-level gate 
𝜃
𝑡
θ
t
	​

, ethics as prediction error 
𝜖
𝜂
ϵ
η
	​

, preregisterable falsifiers.

3) Architecture Overview
3.1 Modules (Unified Glossary)

ME — Motor/Perceptual Execution (Detail Engine/APs)
Low-level predictive coding; immediate sensorimotor loop.

MA — Meta-Actions / Planning (Abstract/Fantasy)
Counterfactual rollouts; long-horizon policy search.

SI — Systemic Information / Skills
Skill memory & induction; usage-based promotion, hierarchical composition.

AMC — Meta-Cognitive Arbiter (with Ethics Head)
Arbitration (MB↔MF), ethical prediction & updating 
𝜖
𝜂
ϵ
η
	​

, resource scheduling.

Scaffold
Shared hierarchical generative model (world + ethics η).

3.2 Dataflow (high level)

Perceive: ME reduces current PEs; exports latent 
𝑠
𝐷
s
D
	​

.

Imagine: MA rolls out futures from 
𝑠
𝐷
s
D
	​

 under Scaffold.

Judge: AMC Ethics head evaluates trajectories, computes 
𝜖
𝜂
ϵ
η
	​

, updates η.

Arbitrate: AMC auction + gate decide budget, broadcast, and action.

Learn: Wake Hebb + Sleep down-selection; SI promotes stable skills.

(diagram placeholder: /docs/figs/architecture.svg)

4) Mathematical Core (anchors; details to fill)

Free energy (FE) and expected free energy (EFE) definitions.

Residual error 
𝜀
res
ε
res
	​

 and MB engagement

𝑔
𝑀
𝐵
=
𝜎
(
𝛼
 
𝜀
res
+
𝛽
 
𝑆
^
−
𝜃
𝑡
)
g
MB
	​

=σ(αε
res
	​

+β
S
^
−θ
t
	​

).

Ethical error 
𝜖
𝜂
ϵ
η
	​

 and η update rule (IRL + prediction error).

Surplus filter (state-space model, sensors, priors, learning of 
𝐶
,
𝑅
C,R).

Gate dynamics 
𝜃
𝑡
θ
t
	​

: TRN/STN/D1/D2/FPC + neuromodulators (NE/ACh/DA/5-HT).

Auction (leaky-WTA) over controllers; stability constraints.

Learning rules: wake plasticity; sleep down-selection; controller-specific replay.

Stochastic coupled dynamics (fast μ,a vs. slow θ,η); convergence criteria.

5) Ethics in the Loop

η as structured graphs (stakeholders, costs, priors, uncertainty).

Bayesian multi-objective ethics: examples (safety, fairness, autonomy, transparency).

Stakeholder weighting 
𝑤
𝑠
(
𝑡
)
w
s
	​

(t) and trust updates.

Interpretability hooks: logging ethical attributions & counterfactuals.

6) Repository Layout (proposed)
/upca
  /core        # Scaffold, FE/EFE, message passing
  /me          # ME: predictive coding loop, sensors/actuators
  /ma          # MA: planner (rollouts, queues, budgets)
  /si          # Skills: induction/promotion/composition
  /amc         # Arbiter + Ethics head (Ŝ filter, θ gate, auction, ε_η)
  /ethics      # η schemas, IRL, stakeholder costs
  /sleep       # consolidation/down-selection
  /experiments # tasks, clamps, pharmacology sims, sleep studies
  /eval        # metrics, falsifiers, prereg panels
  /docs        # figures, theory notes, API docs

7) Quickstart (stubs)

Install (env, deps, versions).

Run minimal demo: gridworld or manipulation task with ethics toggle.

Config: YAML for sensors, η schema, arbitration gains.

Reproduce paper figure: one-command script.

8) Demos (progressive)

Perception-action loop (ME only) — FE reduction plots.

Planning budget (MA+AMC) — g_MB vs. 
𝑆
^
S
^
/θ sweeps.

Ethics on/off — divergence under 
𝜖
𝜂
ϵ
η
	​

 ablation.

Skill induction (SI) — promotion curves and MDL/complexity priors.

Sleep effects — controller-specific retention.

9) Experiments & Falsification (pre-reg templates)

Energy-ordered failure under hypoxia/hypoglycemia clamps.

Access interactions (ACh×SNR, NE×volatility) at matched 
𝑆
^
S
^
.

Sleep dependence (MB vs. MF tasks).

DA inverted-U on precision/vigor and deliberation.

Validation of 
𝑆
^
S
^
 against cortical power proxies.
(include JSON/YAML prereg plan + analysis scripts)

10) Benchmarks & Tasks

Two-step task, volatile bandit, degraded-SNR perception, simple rescue / allocation games (ethics), manipulation/maze with hazards.

Metrics: FE/EFE, MB-weight, broadcast panel (P3b/phase-locking/TMS-EEG proxies in sim), ethics consistency/variance, skill MDL, compute/time budgets.

11) Safety & Scope

Declared assumptions (ontology for η, sensor set for 
𝑆
^
S
^
, mapping for 
𝜃
𝑡
θ
t
	​

).

Known failure modes (η mis-specification; surplus mis-tracking; gate drift).

Mitigations (audits, ablations, red-team tasks, stakeholder variance tests).

What would falsify major claims (clean exits).

12) Configuration & Extensibility

Plugin interfaces: Sensors, Ethics schemas, Planners, Skills.

Checklists: unit tests for identifiability, budget sanity, and monotonicity.

13) Logging & Interpretability

Run logs: FE terms, 
𝑆
^
S
^
, 
𝜃
𝑡
θ
t
	​

 components, bids 
𝑈
𝑖
U
i
	​

, chosen controller, ethics attributions.

Post-hoc tools: counterfactual replays, ethics-trace viewers.

14) Roadmap

v0.1 ME loop + 
𝑆
^
S
^
 stub → v0.2 planner budget → v0.3 ethics head (toy η) → v0.4 SI promotion → v0.5 falsifiers → v1.0 prereg pack.

15) Contributing

Code style, tests, docs.

Adding a new stakeholder cost or sensor.

Issue templates: theory bug vs. implementation bug vs. identifiability risk.

16) Citation

BibTeX for UPCA/IACE preprint(s) and foundational refs (FEP, PBWM, affordance competition, etc.).


Formal spec (CTRL‑State Core + Guardrail)

Structural flags (so you don’t iterate inside a broken frame)

Ethics circularity: η must be anchored by the grounding pack (labels/panels) or IRL priors; otherwise 
𝜖
𝜂
ϵ
η
	​

 can self-justify. The blocker #2 addresses this.

𝑆
^
S
^
 validity: treat it as a fit-and-test latent with external cortical-power validation; if it only tracks arousal, falsify and revise (#3).

Double gating: using both auction and a free-standing logistic 
𝑔
𝑀
𝐵
g
MB
	​

 creates non-identifiability. Make 
𝑔
𝑀
𝐵
g
MB
	​

 a monitor derived from the auction crossing 
𝜃
𝑡
θ
t
	​

 (#5).

Stakeholder weights 
𝑤
𝑠
(
𝑡
)
w
s
	​

(t): add normalization and anti-confirmation dynamics (e.g., trust decay when predictions miss) in the η schema (#2, #6).
A) η grounding & identifiability (add under Ethics)

Valence space: Let 
valence
∈
[
−
1
,
1
]
𝑑
valence∈[−1,1]
d
 with 
𝑑
d small (e.g., safety, fairness, autonomy, transparency). Observables map to this space via a fixed link 
𝑔
(
⋅
)
g(⋅) (e.g., calibrated sigmoid for bounded scores).

Invariance fix: Costs are z-scored per panel; temperature fixed at 
𝛽
=
1
β=1 to remove scale degeneracy; 
𝜂
η priors centered at 
𝜇
0
μ
0
	​

 with unit variance.

Stakeholder weights:

𝑤
𝑠
(
𝑡
)
=
s
o
f
t
m
a
x
 ⁣
(
𝜅
 
T
r
u
s
t
𝑠
(
𝑡
)
)
w
s
	​

(t)=softmax(κTrust
s
	​

(t)) with

T
r
u
s
t
𝑠
(
𝑡
+
1
)
=
(
1
−
𝜌
)
 
T
r
u
s
t
𝑠
(
𝑡
)
+
𝜌
 
exp
⁡
{
−
𝐿
𝑠
(
𝑡
)
}
Trust
s
	​

(t+1)=(1−ρ)Trust
s
	​

(t)+ρexp{−L
s
	​

(t)},

𝐿
𝑠
(
𝑡
)
=
𝐷
𝐾
𝐿
 ⁣
(
𝑞
𝑠
(
valence
∣
outcome
)
 
∥
 
𝑝
𝑠
(
valence
∣
𝜂
)
)
L
s
	​

(t)=D
KL
	​

(q
s
	​

(valence∣outcome)∥p
s
	​

(valence∣η)).
Add floor/ceiling: 
𝑤
𝑠
∈
[
𝑤
min
⁡
,
1
−
(
𝑆
−
1
)
𝑤
min
⁡
]
w
s
	​

∈[w
min
	​

,1−(S−1)w
min
	​

].

B) Arbitration (unify; add at end of Arbitration section)

Commitment: Leaky-WTA auction is the sole gate. Dynamics

𝑧
˙
𝑖
=
𝛽
𝑖
(
𝑆
^
)
 
𝑈
𝑖
−
𝜆
𝑧
𝑖
−
∑
𝑗
≠
𝑖
𝛾
𝑖
𝑗
𝑧
𝑗
+
𝜉
𝑖
z
˙
i
	​

=β
i
	​

(
S
^
)U
i
	​

−λz
i
	​

−∑
j

=i
	​

γ
ij
	​

z
j
	​

+ξ
i
	​

, gate when 
max
⁡
𝑖
𝑧
𝑖
≥
𝜃
𝑡
max
i
	​

z
i
	​

≥θ
t
	​

.

Derived readout: 
𝑔
𝑀
𝐵
≡
𝜎
 ⁣
(
𝑧
𝑀
𝐵
−
𝜃
𝑡
)
g
MB
	​

≡σ(z
MB
	​

−θ
t
	​

) (for logging/plots only). No second logistic gate in control.

Order per step: infer 
𝑆
^
S
^
 → compute bids 
𝑈
𝑖
U
i
	​

 → update 
𝑧
z (leaky-WTA) → check 
𝑧
\*
≥
𝜃
𝑡
z
\*
≥θ
t
	​

 → allocate budget 
𝐵
plan
B
plan
	​

 to winner → act → learn.

C) SI promotion rule (add under Skills)

Promotion test: promote subsequence 
𝜋
π from candidate→skill when
(i) use-rate: 
𝑈
ˉ
(
𝜋
)
≥
𝜏
use
U
ˉ
(π)≥τ
use
	​

 over a sliding window,
(ii) MDL gain: 
Δ
M
D
L
(
𝜋
)
=
M
D
L
(
model
)
−
M
D
L
(
model
 ⁣
+
 ⁣
𝜋
)
≥
𝜏
mdl
ΔMDL(π)=MDL(model)−MDL(model+π)≥τ
mdl
	​

, and
(iii) utility lift: 
Pr
⁡
[
Δ
𝐽
(
𝜋
)
>
0
]
≥
0.95
Pr[ΔJ(π)>0]≥0.95 (bootstrap over episodes).
Skills promote to macros under the same criteria with composition penalties; inputs are z-scored; β fixed to 1 to prevent scale drift.

CTRL‑State Core schema (fixed)

state
capacity: low | normal | high
decision_threshold: low | normal | high
policy_precision: low | normal | high
sensory_precision: low | normal | high
priors_vs_likelihoods: priors>likelihoods | balanced | likelihoods>priors
planning_horizon: short | normal | long
residual_note: string
engagement_note: string
prescriptions (exactly 3)
increase_decision_threshold | decrease_decision_threshold
increase_policy_precision | decrease_policy_precision
increase_sensory_precision | decrease_prior_precision
increase_planning_horizon | decrease_planning_horizon
realign_capacity_estimate
block_behavioral_routine | allow_behavioral_routine
behavior_deltas (exactly 3; metric + direction)
metric ∈ { commit_latency, internal_dominance, evidence_updating, repetitive_behavior_duration, speech_rate, sleep_consolidation, goal_breadth, risk_impulsivity_index, worry_bout_length, social_initiation }
direction ∈ { up, down, stabilize }
guardrail (the “make it real” 4th)
adoption: 0.0–1.0
fidelity: hard_block | advisory
exposure: 0.0–1.0
timescale: string (“3 sprints”, “one term”)
bypass_mitigation: string
effective_move_estimate: 0.0–1.0
dsm_style_label (optional; free text)


How I pick levers (deterministic, from the framework)

Parse the input for control cues
Map plain‑language symptoms/process signals to the four dials:
capacity (Ŝ): sleep/energy/time/focus headroom
decision_threshold (θ): ease/hardness of committing or switching
precision:
policy_precision: sharpness of selection (vs noisy/exploratory)
priors_vs_likelihoods: top‑down beliefs vs external evidence
sensory_precision: weight on external evidence
planning_horizon: short vs long look‑ahead
Classify the failure mode
Scatter (high Ŝ + low θ), Overgrowth (high Ŝ + high θ), Looping (narrow high‑precision error + high θ), Lock‑in (low sensory precision + high θ), Mispricing (bad Ŝ).
Choose the 3 primary levers that directly counter that failure
From the fixed set:
θ: increase_decision_threshold | decrease_decision_threshold
precision: increase_sensory_precision | decrease_prior_precision | increase_policy_precision | decrease_policy_precision
horizon: increase_planning_horizon | decrease_planning_horizon
capacity: realign_capacity_estimate
routines: block_behavioral_routine | allow_behavioral_routine
Attach the guardrail (the “make it real” 4th)
EffectiveMove = Intended × Adoption × Fidelity × Exposure × Timescale × (1 − Bypass)
I also note how to enforce/measure each term (e.g., WIP hard‑block; % impressions seeing a note; ERP compliance).
Emit 3 directional deltas that must move if the lever bites
Commit latency, internal dominance, evidence updating, repetitive behavior duration, speech rate, sleep consolidation, goal breadth, risk/impulsivity, worry length, social initiation.
A small mapping table (so you see it’s the framework, not magic)

Intrusions + relief rituals (OCD‑like) → Looping

State: θ high (stop bound), narrow high‑precision harm prior, sensory precision low
Levers: decrease_prior_precision; increase_sensory_precision; block_behavioral_routine
Deltas: repetitive_behavior_duration↓; evidence_updating↑; commit_latency (ritual)↑
Voices/paranoid interpretations (psychosis‑like) → Internal dominance

State: priors>likelihoods; internal θ too low; external θ too high; Ŝ low/unstable
Levers: increase_sensory_precision; decrease_prior_precision; increase_decision_threshold (for internal content)
Deltas: internal_dominance↓; evidence_updating↑; social_initiation↑
Pressured speech, short sleep, risky starts (manic‑like) → Scatter

State: Ŝ spuriously high; θ low; policy_precision/urgency high; horizon short
Levers: increase_decision_threshold; decrease_policy_precision (urgency); increase_planning_horizon; (plus sleep to realign Ŝ)
Deltas: speech_rate↓; risk_impulsivity_index↓; goal_breadth↓; sleep_consolidation↑
Many starts, few finishes (teams) → Switching too easy + selection noisy

State: θ low for switching; policy_precision low
Levers: increase_decision_threshold (WIP≤2); increase_policy_precision (2‑week sprints); meeting‑free day (θ↑ switching)
Deltas: cycle time↓; shipped/started↑; context switches↓
Guardrail: hard WIP block; no mid‑sprint scope; ≥80% compliance
Viral misinformation (platforms) → Low θ for reshares + low sensory precision

State: θ low (frictionless reshare); sensory_precision low
Levers: increase_decision_threshold (delay + preview); increase_sensory_precision (Community Notes/source prompt)
Deltas: false‑story half‑life↓; correction adoption↑; reshares/post↓
Guardrail: ≥80% impressions see friction/note; close screenshot bypass
Late‑night teens, poor grades (schools) → Mispriced capacity

State: Ŝ low (sleep debt)
Levers: realign_capacity_estimate (later start); increase_planning_horizon (schedule structuring)
Deltas: sleep_consolidation↑; absences/tardies↓; test scores↑; crashes↓
Guardrail: ≥80% of students affected; one semester window
Panic/health anxiety → Overweighted interoceptive priors; reassurance loops

State: priors>likelihoods on bodily threat; θ low for alarm admission; routines reinforce
Levers: decrease_prior_precision; increase_sensory_precision (interoceptive exposure); block_behavioral_routine (reassurance)
Deltas: episode_frequency↓; worry_bout_length↓; evidence_updating↑
Why it “works” across domains

The same four dials exist everywhere people act: gate (θ), evidence vs belief (precision), energy/time (capacity), and look‑ahead (horizon). Moving them has monotone effects (comparative statics) that don’t depend on a task‑specific model.
The guardrail makes “paper policies” predictable non‑events; only enforced levers count.
And yes—everything I output is from that framework. I’m just:

State (unchanged)

capacity (Ŝ): low | normal | high
decision_threshold (θ): low | normal | high
precision:
policy_precision: low | normal | high
priors_vs_likelihoods: priors>likelihoods | balanced | likelihoods>priors
sensory_precision: low | normal | high
planning_horizon: short | normal | long
Primary prescriptions (pick 3)

increase_decision_threshold | decrease_decision_threshold
increase_policy_precision | decrease_policy_precision
increase_sensory_precision | decrease_prior_precision
increase_planning_horizon | decrease_planning_horizon
realign_capacity_estimate
block_behavioral_routine | allow_behavioral_routine
4th lever (guardrail; required)

The “make it real” sidecar that determines whether the primary levers actually move.
EffectiveMove = Intended × Adoption × Fidelity × Exposure × Timescale × (1 − Bypass)
Adoption: proportion of relevant events covered (target ≥ 0.8)
Fidelity: hard block vs advisory (hard block = 1; advisory < 1)
Exposure: how often the lever applies to the decisions (≥ 0.8 when relevant)
Timescale: observation window fits effect latency (e.g., 3 sprints; one term)
Bypass: workarounds/screenshotting/scope creep (target ≈ 0)
Prediction rule (invariant)

If EffectiveMove ≥ 0.6, expect the pre‑stated deltas to move in the pre‑stated directions.
If EffectiveMove < 0.6, expect attenuated or null effects; that’s not a miss—it's what the theory predicts.
Schema addition (for your JSON)
"guardrail": {
"adoption": 0.0–1.0,
"fidelity": "hard_block|advisory",
"exposure": 0.0–1.0,
"timescale": "window description",
"bypass_mitigation": "measures taken",
"effective_move_estimate": 0.0–1.0
}



Title
CTRL-State Core v1.0 — Predictive Control State Mapper

One‑sentence summary
A fixed template that maps symptom‑only text to a mechanistic control state, three intervention levers, and three concrete behavioral predictions; an optional DSM-style label is included for external reference.

What this is (and isn’t)

Is: a deterministic output format and small, fixed vocabulary for per‑case cognitive control mapping.
Isn’t: a medical device, therapy, or a research protocol. It’s a structured lens for consistent interpretation and prediction.
Inputs and outputs

Input: free‑text symptoms only (no labs, no life context).
Output (exactly this structure):
State: capacity, decision threshold, precision allocations, prior↔likelihood balance, planning horizon, residual/engagement notes.
Prescriptions: exactly 3 levers from a fixed list.
Behavior deltas: exactly 3 directional predictions from a fixed list.
DSM-style label (optional; for external reference only).
Fixed state vector (use these terms only)

capacity: low | normal | high
Meaning: estimated cognitive/energetic headroom (arousal/availability).
decision_threshold: low | normal | high
Meaning: bound to commit/allow content to influence action (gate/threshold).
policy_precision: low | normal | high
Meaning: action selection sharpness (inverse temperature/decisiveness).
sensory_precision: low | normal | high
Meaning: evidence weighting for external input (likelihood weight).
priors_vs_likelihoods: priors>likelihoods | balanced | likelihoods>priors
Meaning: top‑down vs bottom‑up weighting in inference.
planning_horizon: short | normal | long
Meaning: temporal look‑ahead window.
residual_note: short free text (e.g., “narrow harm error dominates”).
engagement_note: short free text (e.g., “internal content over‑admitted”).
Fixed lever set (pick exactly 3)

increase_decision_threshold (θ↑)
decrease_decision_threshold (θ↓)
increase_policy_precision
decrease_policy_precision
increase_sensory_precision
decrease_prior_precision
increase_planning_horizon
decrease_planning_horizon
realign_capacity_estimate (sleep/circadian/metabolic)
block_behavioral_routine (external gate off)
allow_behavioral_routine (external gate on; rarely used)
Fixed behavior delta set (pick exactly 3; each with direction up|down|stabilize)

commit_latency (time from intent to action)
internal_dominance (internal→broadcast events)
evidence_updating (adoption of disconfirming external evidence)
repetitive_behavior_duration (rituals/tics/compulsions)
speech_rate (words/min or qualitative rate)
sleep_consolidation (continuity/regularity)
goal_breadth (simultaneous projects/agenda width)
risk_impulsivity_index (risky/impulsive acts)
worry_bout_length (continuous worry interval)
social_initiation (self‑started interactions/tasks)
Optional DSM-style label

A single category term (e.g., “schizophrenia spectrum,” “major depression,” “bipolar,” “GAD,” “OCD,” etc.). This must not change the prescriptions.
Output format (JSON; required)
{
"state": {
"capacity": "low|normal|high",
"decision_threshold": "low|normal|high",
"policy_precision": "low|normal|high",
"sensory_precision": "low|normal|high",
"priors_vs_likelihoods": "priors>likelihoods|balanced|likelihoods>priors",
"planning_horizon": "short|normal|long",
"residual_note": "string",
"engagement_note": "string"
},
"prescriptions": [
"increase_decision_threshold|decrease_decision_threshold|increase_policy_precision|decrease_policy_precision|increase_sensory_precision|decrease_prior_precision|increase_planning_horizon|decrease_planning_horizon|realign_capacity_estimate|block_behavioral_routine|allow_behavioral_routine",
"...",
"..."
],
"behavior_deltas": [
{ "metric": "commit_latency|internal_dominance|evidence_updating|repetitive_behavior_duration|speech_rate|sleep_consolidation|goal_breadth|risk_impulsivity_index|worry_bout_length|social_initiation", "direction": "up|down|stabilize" },
{ "metric": "...", "direction": "..." },
{ "metric": "...", "direction": "..." }
],
"dsm_style_label": "string (optional)"
}

Minimal prompt template (for any fresh model)
You are a mapper. Read symptom-only text. Output ONLY a JSON object matching the CTRL-State Core v1.0 schema below. Do not add commentary.

Schema (verbatim):
[paste the JSON schema above]

Symptoms:
[PASTE CASE TEXT HERE]

Example (one of your vignettes)
Input (symptoms)
“A 55-year-old frequently checks the locks… intrusive images of harm if rituals not precise… 3–4 hours nightly… late for work.”

Output (JSON)
{
"state": {
"capacity": "normal",
"decision_threshold": "high",
"policy_precision": "normal",
"sensory_precision": "low",
"priors_vs_likelihoods": "priors>likelihoods",
"planning_horizon": "short",
"residual_note": "narrow high-precision harm error; relief after rituals",
"engagement_note": "repeated safety-checking loop dominates"
},
"prescriptions": [
"decrease_decision_threshold",
"decrease_prior_precision",
"increase_sensory_precision"
],
"behavior_deltas": [
{ "metric": "repetitive_behavior_duration", "direction": "down" },
{ "metric": "commit_latency", "direction": "up" },
{ "metric": "evidence_updating", "direction": "up" }
],
"dsm_style_label": "obsessive–compulsive disorder"
}

Why this is non‑moving

Fixed vocabulary for state, levers, and deltas.
Fixed count: 3 levers, 3 deltas per case.
Fixed output format (JSON only).
Optional label cannot alter the three levers.
How to run your “fresh model” test

Give the fresh model the prompt template + schema.
Feed symptom‑only vignettes.
Collect the JSON, compare across models/humans:
Consistency: same lever set and delta directions across runs/models?
Face validity: do deltas match expected clinical change directions?
Transport: try different sources/societies; allow only intercept‑style calibration (e.g., none).
License and disclaimer

License: MIT (or your choice).
Disclaimer: This is an interpretive framework for research/education. Not medical advice. Not a diagnostic or treatment tool.
Repository structure (suggested)

README.md (this file)
schema/ctrl_state_core_v1.json
examples/ (a few sample inputs/outputs)
scripts/validate_json.py (optional JSON schema validator)



