# Calibration Example

## Breakdown

- Intent: fix an existing draft or plan.
- Subject: the receiver.
- Path: receive -> understand -> act -> get signal.
- Constraint: the receiver should not need extra explanation.
- Acceptance: the receiver can take the next action.

## Decision

Fix the first path break.

## Path

- Motive: make progress.
- Interpretation: understand the promise.
- Action: follow one instruction.
- Resistance: unclear wording or too many choices.
- Signal: the receiver knows whether the action worked.
- State change: confusion becomes progress.
- Continuation: next action appears.

## Evidence

- Confirmed: draft exists, receiver exists, one path break identified.
- User-provided: the receiver should not need extra explanation.
- Inference: unclear wording is the primary blocker.
- Unconfirmed: whether other sections also have breaks.

## Data gaps

- Unknown: how many sections have path breaks. If only one, fix it and ship. If many, prioritize by impact.

## Minimum test

- Goal: make one action clear.
- Input: current draft.
- Action: replace vague wording with action wording.
- Output: revised section.
- Pass condition: the receiver knows what to do next.
- Fail signal: the receiver asks what now.
- Next step: test the revised section with one receiver.
- Do not do: rewrite the whole system first.

## Gates

- Path gate: PASS — path break located.
- Evidence gate: PASS — break is visible in the draft.
- Minimum-test gate: NOT STARTED — revised section not yet tested with receiver.

## Model check

1. Path
   Finding: movement stops before action.
   Fix: move the action earlier.

2. Friction
   Finding: choice load is high.
   Fix: keep one main action.

3. Narrative
   Finding: the promise is hard to repeat.
   Fix: state it in one sentence.

## Usable result

Rewrite the first broken section and test it.
