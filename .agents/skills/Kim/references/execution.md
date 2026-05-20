# Execution Protocol

Use this file when the user asks for a plan, delivery path, validation run, operational protocol, or implementation sequence.

## Rule

Execution output must make the next move physically performable.

Do not stop at strategy. Convert judgment into an actor, input, action, output, signal, and stop condition.

## Execution unit

Every executable step should answer:

- Actor: who performs the step.
- Input: what material, data, file, buyer, user, or case they start with.
- Action: the exact operation.
- Output: the artifact, record, decision, or changed state produced.
- Pass signal: what proves the step worked.
- Fail signal: what proves the step should stop or change.
- Timebox: when to inspect the signal.

If a step cannot name its output or signal, it is not executable yet.

## First move

The first move should be the smallest action that can change the decision.

Prefer:

- a buyer conversation over a deck
- a reproducible case over a broad rewrite
- one shipped artifact over a roadmap
- one observable user action over a preference survey
- a paid or high-friction signal over casual interest

## Kill condition

Every plan needs a kill condition.

A kill condition is not pessimism. It protects time and forces learning.

Good kill conditions name:

- the tested assumption
- the signal threshold
- the timebox or sample size
- the next action after failure

Example:

```text
If 10 direct offers produce no price conversation within 7 days, stop building the product and rewrite the offer around a narrower buyer pain.
```

## No hidden work

Do not hide major effort behind words such as "prepare", "improve", "research", "validate", "launch", or "optimize".

Replace them with the concrete operation:

- "prepare" -> "write a 150-word offer and send it to 10 named buyers"
- "research" -> "compare 5 current competitor pricing pages and record price, buyer, promise, proof, and onboarding step"
- "validate" -> "ask 10 qualified users to complete the task and count completion without help"
- "launch" -> "publish the page, send the email to the existing list, and measure paid replies for 48 hours"
- "optimize" -> "change only the step named by at least 3 failed users"

## Output shape

Use this structure internally:

```markdown
Decision:
First move:
Execution path:
- Actor:
- Input:
- Action:
- Output:
- Pass signal:
- Fail signal:
- Timebox:
Kill condition:
Do not do:
```

In visible output, compress this into natural language unless the user asks for a checklist or protocol.
