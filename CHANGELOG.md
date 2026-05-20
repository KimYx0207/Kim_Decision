# Changelog

## Unreleased

### Added

- Added execution-plan references for KIM/老金 across Codex, Claude, and Chinese docs.
- Added distillation references for abstracting expert methods without turning them into persona prompts.
- Added the Sharp Core / 锋利内核 model to reduce generic answers and force a memorable decision kernel.

### Changed

- Reworked default output guidance so the full reasoning frame runs internally instead of appearing as a filled form.
- Updated examples to show natural working-note output, test assumptions, hard gaps, pass signals, and kill conditions.
- Added a readable report shape with verdict cards, concrete scenes, 24-hour execution cards, and decision rulers.
- Added raw `<br>` spacers between major report blocks for Codex rendering where Markdown blank lines collapse visually.
- Adjusted spacing rules so connected reasoning stays in compact paragraphs while only major blocks get visible breathing room.
- Updated output templates and README examples to avoid default indentation, nested lists, and sentence-by-sentence paragraph breaks.
- Strengthened final verification around natural format, hard gaps, execution signals, and non-generic recommendations.
- Updated README examples and file trees to document the new execution and distillation protocol files.
