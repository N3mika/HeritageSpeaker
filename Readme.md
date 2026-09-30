# Heritage Spanish 400 Level Reviewer Dataset

This release contains 598 learner-turn annotations for comparing original AI-generated analysis with final human adjudication across written-norm, speech-aware, and variation-sensitive levels. The compact workbook is designed for reviewer inspection while excluding the full learner transcripts.

## Included file

- [Heritage 400 Level Reviewer Ready Compact AI vs Human](https://github.com/N3mika/HeritageSpeaker/blob/main/Heritage_400Level_final.xlsx)

The workbook contains two sheets:

- `Reviewer Data` contains the paired AI and human annotations.
- `Codebook` contains annotation labels and their meanings.

## Annotation levels

- `WCEA` evaluates the transcript against edited written Spanish.
- `SCEA` evaluates residual errors after ordinary spontaneous-speech organization is considered.
- `VSA` evaluates whether a residual difference is a learner error or a socially meaningful variety or bilingual feature.

## AI and human columns

Every annotation field is presented as an adjacent AI and human pair. The AI column records the original model annotation. Source shorthand such as `same` has been expanded to the referenced span or explanation so that the compact dataset remains readable. The human column records the final adjudicated annotation and is authoritative.

When the reviewers agreed with the AI annotation, the same value appears in both columns. When human review removed a span or target because it no longer applied, the human cell is blank and the pair is highlighted as a mismatch.

## Mismatch colors

Mismatch colors are applied to both cells in an AI and human pair. The colors supplement the cell values; they do not replace them.

| Color | Hex value | Mismatch type |
| --- | --- | --- |
| Pale red | `#F4CCCC` | Label, status, subtype, or decision |
| Pale yellow | `#FFF2CC` | Span |
| Pale blue | `#DDEBF7` | Target |
| Pale purple | `#E4DFEC` | Explanation |
| Pale green | `#E2F0D9` | Feedback action |
| No mismatch fill | — | AI and human values agree |

The darker colors in the header row identify workbook sections and are not mismatch indicators.

## Spans and targets

WCEA and SCEA spans reproduce the learner-produced material associated with the stage-specific annotation. Targets provide the corresponding minimal correction.

VSA spans and targets provide trace evidence. They use direct VSA evidence when available and otherwise retain the relevant SCEA or WCEA span and target. For a VSA `ERROR`, the target is a minimal correction. For a VSA `NON_ERROR` with a documented variation category, the target can be interpreted as an optional alternative rather than a required correction.

## Feedback actions

- `CORRECT_ERROR` means that the retained learner error should receive a minimal correction.
- `PROVIDE_ALTERNATIVE_FORMS_AS_OPTIONAL` means that alternative forms may be offered without treating the learner form as an error.
- A blank feedback cell means that neither of these learner-facing actions applies. This includes cases with no relevant error or variation and cases that remain `UNCERTAIN`.

AI feedback is derived from the AI VSA status and decision. Human feedback is derived from the final human VSA status and decision.

## Privacy and transcript access

The workbook uses anonymized speaker identifiers and does not include the full transcript, recording identifiers, timestamps, or reviewer comments. Short transcript spans are retained only where needed to make an annotation traceable.

Access to the original transcribed learner text may be provided upon request by contacting the main author. 
