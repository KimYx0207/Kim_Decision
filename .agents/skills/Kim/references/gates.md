# Gates

## Core-problem gate

No method expansion before the real problem is named.

Required:

```text
core problem
decision or artifact requested
evidence that would change the answer
smallest useful output
```

Fail if the answer displays framework scaffolding but does not move the user's decision forward.

## Clarification gate

No broad questionnaire before the smallest blocking question.

Ask only when missing information would change:

```text
deliverable
decision
scope
risk
first action
```

If the gap can be inspected locally, inspect first. If it can be assumed safely, proceed and label the assumption.

## Path gate

No full plan before path.

Required:

```text
Subject
Motive
Interpretation
Action
Resistance
Signal
State Change
Continuation
```

## Evidence gate

Verify or label uncertainty when a claim depends on:

```text
time
external rules
external systems
private files
high-stakes judgment
current market conditions
```

## Minimum-test gate

No large system before a minimum test.

Required:

```text
Goal
Input
Action
Output
Pass condition
Fail signal
Next step
Do not do
```

## No-placeholder gate

Do not leave placeholders.

Avoid:

```text
TBD
TODO
later
proper handling
optimize as needed
improve experience
complete the loop
```

Write:

```text
actor
input
action
output
pass condition
```

## Root-cause gate

For repeated failure, collect evidence before changing the solution.

Required:

```text
symptom
reproduction path
recent change
evidence
hypothesis
minimum validation
```

## Completion gate

Do not say done without checking:

```text
acceptance criteria
unconfirmed facts
open risks
placeholders
usable result
```

## Three-failure gate

After three failed attempts, stop and reframe.

Check:

```text
intent
path
root cause
model choice
missing input
scope
alternative path
```

## Research gate

When a key decision relies on C or D tier evidence, attempt verification before proceeding.

External research is mandatory when the answer depends on:

```text
current versions
APIs or docs
regulations or rules
prices or schedules
security advisories
market or company status
third-party tool behavior
source-backed public claims
```

Steps:

1. Identify which C/D evidence would change the decision if upgraded
2. Use available tools to search: web search, file read, API query, documentation lookup
3. If found → upgrade tier (C→B or D→C), cite source
4. If not found → mark as "unverified" and state: "unverifiable, user confirmation required"

Rules:

- Do not proceed with a key decision resting on D-tier evidence alone
- At least one attempt to verify each critical C/D claim
- Prefer official or primary sources before commentary
- User requests for "latest", "verify", "search", or "cite" always trigger research
- Local/user-provided material can stay local-only when no external changing fact affects the decision
- If no search tools are available, skip the search and flag the gap explicitly

## Revenue gate

Load: references/business.md

Required:

```text
Revenue model
Payer
Why pay now
Deal size
Delivery cost
Repeat purchase
```

If questions 1-3 unanswered → downgrade to "do not proceed".

## MVP gate

Load: references/business.md

Required:

```text
V1 scope (one sentence)
Explicit exclusions
Fastest delivery (days)
Minimum customer
Minimum deal size
Failure criteria
```

If scope exceeds one sentence or no exclusions → compress.

## Delivery gate

Load: references/business.md

Required:

```text
Input
Process
Output
Acceptance criteria
Client confirmation
Reuse potential
```

If input through confirmation incomplete → deliverable not ready.
