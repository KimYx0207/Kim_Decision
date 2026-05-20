# Master Lens

Use this file when a decision may be internally coherent but still too weak, generic, or self-confirming.

This is a backend review layer, not a persona layer.

## Rule

Do not ask the model to act as a famous person.

Do not expose names such as Jobs, Bezos, Munger, Feynman, Graham, Buffett, or Grove as visible answer modes unless the user explicitly asks for the source lineage.

Use public expert patterns only as provenance for abstract pressure tests. The final answer should show the improved judgment, not the borrowed name.

## When to load

Load this before final review when:

- the user asks whether the thinking logic is strong enough
- the task is business, product, strategy, monetization, content, offer, or execution design
- the answer risks sounding fluent but not decisive
- the plan may be too early-systemized, too broad, or too dependent on untested belief
- the user asks for expert, master, famous, or high-level thinking

Do not load it for simple factual answers, code mechanics, translations, or narrow formatting fixes.

## Lens set

Use 3-5 lenses, not all of them. Pick the lenses that can change the answer.

### First-screen lens

Question: Does the first sentence change what the user will do next?

Failure smell: the answer starts with context, balance, or a generic framework before making a decision.

Fix: move the decisive claim to the first line and attach one concrete scene or artifact that makes the result visible.

### Customer-backward lens

Question: Does the plan start from the user's paid or repeated outcome, not from the maker's tool or capability?

Failure smell: the answer sells "AI", "system", "content", "service", or "quality" instead of a concrete result someone already wants.

Fix: rewrite the offer around the buyer's existing job, deadline, risk, cost, or repeated pain.

### Inversion lens

Question: What would make this path obviously fail?

Failure smell: the answer has a plan but no kill condition, no disqualifier, and no "do not do this first".

Fix: add the fastest failure test, the stop line, and the path to avoid.

### Reality lens

Question: What observable evidence separates a real signal from a convincing story?

Failure smell: the answer sounds scientific, strategic, or polished but relies on untested assumptions.

Fix: name the smallest observable signal, the missing evidence that would change the decision, and the first verification move.

### Manual-first lens

Question: What can be done manually before building a system?

Failure smell: the answer jumps to automation, product, funnel, brand, or platform before proving demand by hand.

Fix: replace the first system step with a manual test involving a real person, real artifact, real channel, and short timebox.

### Margin lens

Question: What protects the user if the judgment is wrong?

Failure smell: the plan assumes the first route works and ignores cost, reversibility, downside, or opportunity loss.

Fix: reduce commitment, set a spend/time cap, and name what must be preserved.

### Operating lens

Question: Who owns the next move, what input do they need, what output exists, and when is it reviewed?

Failure smell: the answer says "validate", "iterate", "optimize", or "research" without actor, input, output, or cadence.

Fix: make the next move operational: owner, input, action, output, signal, timebox.

## Review pass

Before final output, run this hidden check:

```text
First-screen: does the opening change the user's next move?
Customer-backward: is the offer/result framed from the buyer's outcome?
Inversion: what would make this fail, and where is the stop line?
Reality: what evidence is known, assumed, or missing?
Manual-first: can the first proof happen without building a system?
Margin: what limits downside if wrong?
Operating: who does what by when, and what exists afterward?
```

Only keep the fixes that improve the final answer.

## Final output rule

Do not write:

```text
From a Jobs perspective...
Using Munger inversion...
Feynman would ask...
```

Write:

```text
The first line is still too soft. It should tell the user not to build the tool yet.

The fastest failure test is 10 direct pitches. If fewer than 2 buyers discuss price, stop before automating.
```

The user should feel the judgment got sharper, not that a famous-person template was applied.
