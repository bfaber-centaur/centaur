# Experiment 000 results: standing-instruction effect

Date: 2026-09-14

This records the first run of `experiments/000-detect-standing-instruction.md`. The frozen experiment file is left unchanged.

## Run conditions

- Interface: Claude web
- Model: Sonnet 5
- Effort: Medium
- Memory: disabled and reset before the run
- Condition B instructions: exactly the frozen test instruction and nothing else in the Instructions field
- Condition A instructions: blank
- Residual account context: name `Bobby`; profession dropdown set to `Other`, which could not be unset
- Coin flip: B won, so treatment ran first
- B block: 20:01-20:08 PDT
- A block: 20:10-20:14 PDT
- Total responses: 20

Protocol deviation: tasks were run in the frozen T1-T6, C1-C4 order in both blocks rather than randomized within each block as planned. The block order was randomized by coin flip.

## Primary readout

The intervention was clearly detectable by the precommitted heuristic.

- Mixed-confidence targets with stronger separation under B: **6/6**
- Treatment-side false positives on high-confidence controls: **0/4**
- Precommitted detection threshold: `>=4/6` targets with stronger separation under B and `<=1/4` treatment-side false positives

All six treatment responses to T1-T6 created a distinct `Context / open questions`-style area and moved the lower-confidence material there. None of the six control-condition responses used that same cross-cutting uncertainty structure; they instead handled uncertainty inline or inside ordinary topical sections.

On C1-C4, treatment did not mechanically add an uncertainty section. The simple derivative, binary conversion, Go `defer`, and Japan-capital questions remained direct.

| Task | Type | B: separate uncertainty area | A: separate uncertainty area | B false positive |
| --- | --- | --- | --- | --- |
| T1 | target | yes | no | n/a |
| T2 | target | yes | no | n/a |
| T3 | target | yes | no | n/a |
| T4 | target | yes | no | n/a |
| T5 | target | yes | no | n/a |
| T6 | target | yes | no | n/a |
| C1 | control | no | no | no |
| C2 | control | no | no | no |
| C3 | control | no | no | no |
| C4 | control | no | no | no |

## What this supports

A one-sentence standing instruction produced a large, directionally predicted structural change on prompts designed to exercise it, while leaving the negative controls free of the targeted ceremony in this run.

That is enough for Experiment 000's narrow purpose: the manual assay can detect at least one strong standing-instruction effect.

It does **not** establish that the instruction improves answer quality, calibration, or human-LLM collaboration. Those were deliberately outside the primary assay question.

## Post-hoc observations

These are observations noticed after seeing the outputs, not precommitted findings.

- The difference looked like more than a heading substitution. Under B, uncertainty was repeatedly relocated out of the main answer into the second block; under A, Claude often expressed similar uncertainty inline.
- Some paired responses differed in confidence or elaboration beyond the targeted structure. For example, the Gödel control-condition answer was more categorical about historical terminology, while the treatment answer explicitly marked uncertainty about exact German usage. The binary-conversion control answer also added a second checking method that the treatment answer did not. With one sample per task, these are anecdotes rather than effects.
- The operator's immediate impression after collection was that the differences were "very clear and dramatic."
- Manual collection was tolerable for 20 responses but already felt tedious enough to motivate coarser field-test or diary methods for subtler interventions.

## Unscored fields

The frozen protocol also asked about calibration harm and subjective preference. Those have not yet been systematically scored. Avoid backfilling them from the obvious structural effect.

## Limitations

- one model and one effort setting
- one run per task-condition pair
- B always preceded A after the coin flip, so condition is confounded with block order
- task order was not randomized within blocks
- account-level residual context was not literally blank
- no blinded evaluation
- no claim that the effect generalizes to ChatGPT, coding agents, or other instruction levels

## Next step

Treat this as assay validation, not as evidence for a grand prompting theory. The next experiment can ask a subtler question about collaboration or delegation, or first replicate this effect under a different model/interface if that becomes useful.