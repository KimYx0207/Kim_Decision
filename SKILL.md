---
name: laojin
description: >
  Abstract decision and reasoning framework for product, business, content,
  project, and AI workflow decisions. Covers product design, PRD, MVP, user
  experience, user path, growth, monetization, strategy, retrospectives, and
  any task needing structured reasoning with intent, path, evidence, minimum
  test, and gates. Trigger when the user asks for a decision analysis, wants
  structured reasoning (“重新想”, “仔细看”), requests a product or business
  review, asks “问问老金” or “老金怎么看”, or needs a concrete plan with
  pass conditions. Personality and tone are controlled externally — this skill
  provides the decision method only.
---

# KIM Skill

## Operating target

Deliver a usable decision or artifact.

The method stays abstract.

The final answer may use concrete evidence.

Use concrete names, companies, tools, sources, dates, metrics, cases, commands, or file paths when they improve trust. Verify them or mark them as unconfirmed.

Do not use a named person as an internal role.

Do not write "think like this person."

Turn useful thinking patterns into abstract models.

## Language policy

Output language follows the user's language.

Detect the user's language from their input. Match it in all output: headings, body, analysis, conclusions, questions, and the usable result.

Frame field names (Intent, Subject, Path, Constraint, Evidence, Minimum Test, Models, Gates, Output) and standard SaaS/product terms (CAC, LTV, PMF, churn, conversion, etc.) are proper nouns. Keep the original term. On first use in each response, append a short explanation in the user's language.

Examples:

- Chinese user: "Evidence（证据：支持判断的事实）"
- Japanese user: "Evidence（証拠：判断を支える事実）"
- English user: no annotation needed

This rule applies to any language the user writes in.

## Information density

Every sentence in the output must carry new information. A sentence that restates the obvious, paraphrases a previous line, or fills a template slot without adding insight should be cut. When a template field produces no new information (e.g., the constraint is already obvious from context), omit that field rather than pad it. Dense output beats complete output.

## Data gap protocol

When key evidence is missing and the answer would change depending on that evidence, do two things in this order:

1. State the specific missing data and what it would decide (e.g., "Monthly trial volume is unknown — if > 500, conversion is the bottleneck; if < 100, traffic acquisition is the bottleneck").
2. Ask the user to provide it, offering to refine the analysis once they do.

Do not guess missing data. Do not fill templates with speculation dressed as inference.

## Concrete delivery

Usable result must be specific enough to execute without further research. Prefer:

- exact tools (e.g., "Google Analytics → Behavior Flow" not "check analytics")
- exact actions (e.g., "send this 3-question survey to the 47 churned users via email" not "survey churned users")
- exact thresholds (e.g., "if response rate > 30%, proceed to step 2" not "check if enough responses")
- exact commands, scripts, or templates when applicable

If the result cannot be made concrete (too much unknown data), the usable result is a list of questions to answer first.

## Core frame

```text
Intent -> Subject -> Path -> Constraint -> Evidence -> Minimum Test -> Models -> Gates -> Output
```

## Frame fields

### Intent

State what must change.

A good intent is an outcome, not a topic.

### Subject

State who experiences the result.

The subject may be a user, buyer, reader, listener, operator, reviewer, team, system, or decision maker.

### Path

State how the subject moves from the current state to the target state.

Use:

```text
Subject -> Motive -> Interpretation -> Action -> Resistance -> Signal -> State Change -> Continuation
```

### Constraint

State the hard limits.

Use concrete limits when known:

- time
- budget
- people
- rules
- tools
- channel
- data
- skill level
- risk tolerance

### Evidence

Separate:

- Confirmed
- User-provided
- Inference
- Unconfirmed

Verify claims that depend on time, external rules, external systems, private files, high-stakes judgment, or current market conditions.

### Minimum Test

Define the smallest test that can change the decision.

Required fields:

- Goal
- Input
- Action
- Output
- Pass condition
- Fail signal
- Next step
- Do not do

### Models

Use abstract decision models. Pick the smallest set that can improve the answer.

Common models:

- Essence
- Path
- Constraint
- Evidence
- Incentive
- Friction
- Probability
- Risk
- Feedback
- Compounding
- Boundary
- Narrative

### Gates

Use gates to stop skipped steps.

A stage reached is not a stage passed.

### Output

Return a usable artifact.

Examples:

- decision
- path
- checklist
- rewrite
- command
- table
- template
- acceptance criteria
- next action

## Reference loading

Load one file at a time, only when the task needs it.

- `references/method.md`: load when the task is complex and you need the full frame with examples.
- `references/path.md`: load when analyzing user movement, conversion, or workflow steps.
- `references/models.md`: load when the task needs abstract decision analysis beyond the default three models.
- `references/gates.md`: load for multi-step reasoning, validation, or when the user asks for verification.
- `references/output.md`: load when writing deliverables, fact-checking, or refining wording.
- `references/verification.md`: load before finalizing any answer to run the completion checklist.
- `examples/`: load one relevant example (decision, creation, debugging, or calibration) when unsure about output structure.

## Default output

Follow this structure. Omit any section that would only restate what is already obvious or said elsewhere — fewer sections with real content beats more sections with padding.

```markdown
## Breakdown

- Intent:
- Subject:
- Path:
- Constraint:
- Acceptance:

## Decision

[One sentence]

## Path

- Motive:
- Interpretation:
- Action:
- Resistance:
- Signal:
- State change:
- Continuation:

## Evidence

- Confirmed:
- User-provided:
- Inference:
- Unconfirmed:

## Data gaps

[Specific missing data and what each would decide. Ask the user to provide.]

## Minimum test

- Goal:
- Input:
- Action:
- Output:
- Pass condition:
- Fail signal:
- Next step:
- Do not do:

## Model check

[Only include models that produce a non-obvious finding. Skip models that only confirm what is already stated.]

## Usable result

[Specific executable steps: exact tools, exact actions, exact thresholds. See "Concrete delivery" section above.]
```

## Short output

Use short output when: the user asks a single focused question, requests a quick answer ("简单说", "short answer"), or the task scope is narrow (one decision, one path fix, one next action).

```markdown
Decision:

Main path break:

Do now:
1.
2.
3.

Do not do:

Pass condition:
```

## Final pass criteria

The final answer must include:

- decision
- intent
- subject
- path (only steps that carry new information)
- evidence labels when needed
- data gaps with explicit questions when key evidence is missing
- minimum test or next action
- what not to do when scope can expand
- acceptance criteria
- model check (only models with non-obvious findings)
- usable result (specific enough to execute without further research)

Before finalizing, cut any sentence that restates context, repeats a previous point, or fills a slot without adding insight.
