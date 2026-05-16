# Debugging Example

## Breakdown

- Intent: restore a broken path.
- Subject: the operator.
- Path: run -> fail -> inspect -> test -> pass.
- Constraint: avoid extra damage.
- Acceptance: the same failing path passes.

## Decision

Collect evidence before changing the solution.

## Path

- Motive: unblock work.
- Interpretation: identify the failing step.
- Action: capture the full symptom.
- Resistance: guessing.
- Signal: reproduction result.
- State change: symptom becomes hypothesis.
- Continuation: minimal fix and verification.

## Evidence

- Confirmed: path is broken, symptom exists.
- User-provided: avoid extra damage.
- Inference: symptom suggests one root cause.
- Unconfirmed: actual root cause (symptom is not cause).

## Data gaps

- Unknown: full reproduction path. Without reproduction, any fix is a guess. Capture exact steps before proceeding.

## Minimum test

- Goal: prove one root cause.
- Input: full symptom and reproduction path.
- Action: change one variable.
- Output: test result.
- Pass condition: failing path passes.
- Fail signal: same failure remains.
- Next step: keep the fix or reframe the hypothesis.
- Do not do: stack multiple changes.

## Gates

- Path gate: PASS — fail → inspect → test → pass path is defined.
- Evidence gate: HOLD — reproduction not yet captured; do not apply fix.
- Minimum-test gate: NOT STARTED — reproduction steps not yet written.

## Model check

1. Root cause
   Finding: symptom is not cause.
   Fix: reproduce first.

2. Small change
   Finding: multiple changes hide evidence.
   Fix: change one variable.

3. Completion
   Finding: a fix without verification is not done.
   Fix: rerun the failing path.

## Usable result

Write reproduction steps, make one change, verify the same path.
