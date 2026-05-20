# Debugging Example

## Visible output

Do not change the plan again yet. The repeated failure means the system lacks evidence, not effort.

First capture the smallest reproducible case: what input entered, what output appeared, what changed recently, and which assumption was supposed to hold. The useful moment is when the failure stops being a mood and becomes a record.

## Plan

Run one evidence pass before editing.

- Input: failing case, last known good case, recent change.
- Action: compare the two and write one falsifiable hypothesis.
- Output: a reproduction note plus one targeted fix or rollback.
- Pass condition: the same input produces the same failure twice.
- Kill condition: if the failure cannot be reproduced, stop fixing and improve logging or observation first.

## Author check only, not user output

- Root cause gate: phenomenon, reproduction, recent change, evidence, hypothesis, minimum test.
- Risk: broad rewrites hide the cause.
- Feedback: every fix must produce a clearer signal than the previous attempt.
