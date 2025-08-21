Formal spec (CTRL‑State Core + Guardrail)

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
Name locked

“CTRL-State Core v1.0” is the canonical name. I will not rename or refactor this spec.
