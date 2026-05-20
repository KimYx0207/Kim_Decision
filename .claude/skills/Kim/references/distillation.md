# Distillation Protocol

Use this file when the answer risks becoming a template, audit trace, long framework dump, or generic report.

## Rule

Distillation preserves judgment and removes scaffolding.

The user should see the decision, the decisive reason, the next executable move, and the proof condition. They should not see every internal model unless they ask for it.

## Keep

Keep sentences that do at least one of these:

- change the decision
- identify the subject or buyer more sharply
- expose the main constraint
- name a concrete action
- name a measurable signal
- prevent a likely mistake
- provide evidence with a source label or tier
- give one concrete image that makes execution clearer

## Cut

Cut sentences that only:

- restate the user's prompt
- announce a framework
- list obvious options
- say "it depends" without naming the missing data and decision boundary
- use broad verbs such as improve, optimize, leverage, explore, align, validate, or iterate without an actor and signal
- add a heading whose content is one thin line

## Compression pass

Before final output, run this pass:

1. Lead with the verdict.
2. Name the reason that would still matter if every other detail disappeared.
3. Keep one path insight or concrete image only if it changes action.
4. Turn the plan into the next physical move.
5. Attach pass and kill conditions.
6. Move evidence gaps before the plan only when the missing fact can change the plan.
7. Remove internal model names unless the user asked for reasoning trace.

## Data gap wording

A useful gap is a fork, not an apology.

Weak:

```text
More data is needed.
```

Sharp:

```text
Monthly trial volume is unknown. If it is above 500, fix activation first; if it is below 100, traffic is still the bottleneck.
```

## Output check

The final answer should pass this test:

```text
Can the user act in the next 24 hours without asking what the first move is?
```

If no, the answer is still analysis, not distilled output.
