# X Algorithm Mechanism Discovery for Organic Distribution

You are a deep research agent investigating how organic post distribution works on X.

Your task is not to summarize generic creator advice such as “post consistently,” “use hooks,” or “reply to people.” Your task is to reconstruct the ranking and distribution system from public source code, technical documentation, engineering material, and observable product behavior, then derive legitimate, testable growth hypotheses from the implementation.

## Core question

What controllable content, account, timing, format, and interaction variables materially affect the probability that an X post receives incremental distribution, and what does the actual ranking/recommendation machinery suggest that conventional creator advice misses?

## Research scope

Inspect:

- Current public X recommendation/ranking source code
- Commit history where useful
- Repository documentation
- Engineering posts
- Model architecture explanations
- Ranking feature definitions
- Candidate-generation systems
- Filtering logic
- Author/viewer affinity systems
- Engagement prediction models
- Freshness/decay logic
- Penalties and heuristics
- Diversity constraints
- Author-frequency constraints
- Media handling
- Conversation/reply systems
- Public API documentation where relevant
- Credible technical analysis of the open-source ranking system
- Observable current product behavior

Prioritize primary technical sources over creator folklore.

## Reconstruct the distribution pipeline

Build a mechanism graph like:

Post created
→ Candidate generation
→ Eligibility/filtering
→ Feature generation
→ Predicted engagement
→ Ranking score
→ Heuristics/penalties
→ Initial distribution
→ Observed engagement
→ Additional distribution

For each stage, identify:

- Inputs
- Outputs
- Relevant features
- Thresholds
- Weighting logic
- Decay
- Penalties
- Feedback loops
- Controllable variables
- Unknown or proprietary components

## Investigate specifically

Answer questions such as:

- Which predicted user actions contribute positively to ranking?
- Do different engagement types appear to carry different value?
- Which negative signals suppress distribution?
- How does author-viewer affinity affect candidate selection or ranking?
- How does recency decay work?
- How are replies treated versus likes, reposts, profile clicks, or other actions?
- Do images, video, links, or text format alter ranking directly or indirectly?
- Are there explicit penalties for repeated author exposure?
- Are there diversity constraints?
- What appears to govern expansion beyond existing followers?
- Which variables are under the author’s direct control?
- Which variables are merely consequences of already receiving distribution?
- Which common creator tactics are likely confounded by account quality, topic, or audience affinity?

## The key research task

Find **behaviors that the implementation suggests should matter, but conventional creator advice rarely mentions.**

Do not stop at “engagement matters.”

Translate implementation details into precise hypotheses.

For example, instead of:

> Replies are good.

Derive something like:

> The ranking system appears to place greater expected value on interaction X than interaction Y. Therefore, posts deliberately structured to increase X should outperform posts optimized for Y, holding author, topic, and initial audience constant.

## Evidence discipline

Classify findings as:

1. **Directly visible in current source code**
2. **Documented by X**
3. **Strongly inferred from code/architecture**
4. **Empirically observed but not confirmed**
5. **Speculative**

Note where public code may be stale or differ from production.

## Experiment design

Produce **10 high-value randomized tests**.

For each, specify:

- Hypothesis
- Specific ranking mechanism
- Treatment
- Control
- Variables that must be held constant
- Primary metric
- Secondary metrics
- Guardrails
- Sample requirement
- Likely confounders
- Expected result if the mechanism is real
- Expected result if the hypothesis is wrong

Avoid spam, fake engagement, bot amplification, coordinated manipulation, or other policy-violating tactics.

## Final output

Deliver:

1. **Executive model of how X distribution works.**
2. **Detailed mechanism graph.**
3. **Table of ranking signals/features with evidence strength.**
4. **Five least-obvious controllable variables.**
5. **Ten best experiments**, ranked by:
   information value × potential distribution effect ÷ cost.
6. **Common X-growth advice that is unsupported or contradicted by the technical evidence.**
7. **Important gaps between public source and likely production behavior.**
8. **A concise “what the code implies” operating model for a growth team.**

## Standard of success

Can you derive a set of experiments from the machinery itself that a smart creator or growth team would probably not have invented from surface-level analytics or conventional best practices?
