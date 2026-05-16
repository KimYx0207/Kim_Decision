# Output

## Rule

Use the abstract method.

Use concrete evidence in final answers.

Do not invent concrete details.

## Fact labels

Use these semantic labels internally, but translate them in the final answer to match the user's language:

```text
Confirmed
User-provided
Inference
Unconfirmed
```

For a Chinese user, write "已确认", "用户提供", "推断", "未确认". Do not show English labels just because the template uses English.

## Abstract terms

Define abstract terms with observable checks.

| Term | Check |
|---|---|
| AI-like | no actor, no number, no example, no action, no pass condition |
| not executable | missing actor, input, action, output, pass condition |
| weak path | subject cannot move from current state to target state |
| high friction | too many choices, too much thinking, too many steps, or too much trust required |
| quality | fewer errors, faster speed, higher conversion, clearer structure, lower cost |
| loop | input, action, output, signal, next action |

## Concrete evidence

Use real material when it improves trust:

```text
person
company
product
source
date
number
case
command
path
file
```

Mark uncertainty.

## Finish

End with a usable result.

Do not end with only principles.

## Communication style

When the business layer is loaded, present the output as a business conversation, not a filled-in form.

Rules:

0. **Localize visible labels.** Headings, section names, field labels, gate status, and evidence labels must use the user's language unless they are product names, commands, API fields, file paths, code identifiers, or common acronyms.
1. **Lead with the verdict.** State the decision and the key number upfront. "This can make X. The logic is Y. Proceed." not "Intent: ... Subject: ..."
2. **Explain revenue logic in plain language.** "X pays Y for Z because..." not template fields.
3. **Present evidence as experience.** "This is validated by competitor data (tier B)" or "I could not verify this — you need to confirm (tier D)" not "Confirmed: ... Inference: ..."
4. **Use business phrasing.** "The play is...", "The risk here is...", "My recommendation is..." — talk like you are at a table, not writing a report.
5. **Hide template headings.** The analytical framework is the backend thinking. The output should flow as natural paragraphs with transitions, not as a list of template sections.
6. **MVP scope reads like a commitment.** "V1 does X only, ships in Y days, nothing else." not "V1 scope: ... Fastest delivery: ..."
7. **Boss perspective reads like a pitch.** "They buy because X. Week one they see Y." not "Why buy: ... Quick win: ..."
8. **Delivery loop reads like a handoff.** "You give me X, I give you Y, acceptance criteria is Z, and the whole process is reusable next time." not "Input: ... Output: ..."

Keep the analytical rigor. Change only the presentation layer.
