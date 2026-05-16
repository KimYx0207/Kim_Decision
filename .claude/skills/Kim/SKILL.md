---
name: laojin
description: >
  Abstract decision and reasoning framework for product, business, content,
  project, and AI workflow decisions. Covers product design, PRD, MVP, user
  experience, user path, growth, monetization, strategy, retrospectives, and
  any task needing structured reasoning with intent, path, evidence, minimum
  test, and gates. Trigger when the user asks for a decision analysis, wants
  structured reasoning ("重新想", "仔细看", "分析一下", "这个能不能做"), requests
  a product or business review, asks for an opinion on a plan or idea, or
  needs a concrete plan with pass conditions. Also trigger for business
  proposals, monetization, pricing, client delivery, revenue modeling, or any
  decision involving revenue, cost, buyer perspective, or deliverable scope.
  Personality and tone are controlled externally — this skill provides the
  decision method only.
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

Tier each item:

- A: real data, real customers, real revenue, verified outcomes
- B: public case studies, competitor validation, published benchmarks
- C: reasonable reasoning from available facts, not yet verified
- D: guesswork, no supporting evidence — do not use as decision basis

Label every claim with both source label and tier. Flag D-tier claims explicitly. If a key decision relies on C or D evidence only, state this as a data gap.

Verify claims that depend on time, external rules, external systems, private files, high-stakes judgment, or current market conditions.

When a key decision relies on C or D tier evidence, attempt verification using available tools (web search, file read, API query) before proceeding. If verification fails, flag as "unverifiable, user confirmation required". Do not rest a key decision on D-tier evidence alone. See Research gate in references/gates.md.

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

Use gates to stop skipped steps. A stage reached is not a stage passed.

Load `references/gates.md` for the full gate set (11 gates): Path, Evidence, Minimum-test, No-placeholder, Root-cause, Completion, Three-failure, Research, Revenue, MVP, Delivery.

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

- `references/method.md`: load when Intent or Path fields need expansion with examples beyond what SKILL.md provides, or when the user's task is complex enough to require the full frame walkthrough.
- `references/path.md`: load when analyzing user movement, conversion funnels, workflow steps, or any scenario where the subject transitions between states.
- `references/models.md`: load when the task needs more than three abstract models, or when the default set (Risk, Feedback, Constraint) does not cover the decision dimension.
- `references/gates.md`: load for multi-step reasoning, validation workflows, when the user asks for verification, or when business layer gates (Revenue, MVP, Delivery) are needed.
- `references/output.md`: load when writing the final deliverable, fact-checking claims, or refining wording and communication style.
- `references/verification.md`: load before finalizing any answer — contains the completion checklist.
- `references/business.md`: load when the task mentions pricing, monetization, revenue, cost, client delivery, MVP scope, or any decision with a commercial dimension. Trigger keywords: 变现, 定价, 商业, 收入, 成本, 客户, 交付, revenue, monetize, price, client, deliver, scope.
- `examples/decision.md`: load when the task is choosing between options or making a single decision.
- `examples/creation.md`: load when the task involves designing or building something new.
- `examples/debugging.md`: load when the task involves diagnosing a failure or finding a root cause.
- `examples/calibration.md`: load when reviewing or adjusting an existing plan, output, or decision.

## Default output

Follow this structure. Omit any section that would only restate what is already obvious or said elsewhere — fewer sections with real content beats more sections with padding.

When the business layer is loaded, present the output as a business conversation, not a filled-in form. The template below shows the analytical structure — rewrite it into natural paragraphs using the communication style in references/output.md.

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

## Gates

[State which gates passed, held, or failed. See references/gates.md for the full set.]

## Model check

[Only include models that produce a non-obvious finding. Skip models that only confirm what is already stated.]

## Usable result

[Specific executable steps: exact tools, exact actions, exact thresholds.]
```

### Business check (when business layer is loaded)

When `references/business.md` is loaded, include the business check sections between "Model check" and "Usable result". Use the templates and rules defined in that file:

- Revenue check (six questions, verdict)
- MVP scope (one sentence, exclusions, delivery time)
- Boss perspective (why buy, quick win)
- Delivery loop (input through confirmation)

## Short output

Use short output when the task meets ALL of these: single focused question, narrow scope (one decision or one path fix), no commercial dimension.

Short output exempts: Model check, Business check, full Evidence breakdown, Data gaps. Still required: decision, main path break, next action, pass condition.

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

Before finalizing, verify the answer includes these. Cut any sentence that restates context, repeats a previous point, or fills a slot without adding insight.

Core (always required):

- decision, intent, subject, path (only steps with new information)
- evidence labels and tiers when claims appear
- research attempt on critical C/D tier evidence
- minimum test or next action
- what not to do (when scope can expand)
- acceptance criteria
- usable result (specific enough to execute without research)

Business layer (when loaded):

- revenue check (six questions answered or gaps flagged)
- MVP scope (V1 fits one sentence, exclusions listed, delivery under 14 days)
- boss perspective (at least one quick win identified)
- delivery loop (input through confirmation complete)
- no D-tier evidence used as decision basis
