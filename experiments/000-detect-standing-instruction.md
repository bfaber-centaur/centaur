# Experiment 000: can we detect a standing-instruction effect?

Status: frozen before data collection on 2026-09-14.

## Motivation

Before testing subtler ideas such as explicit handoffs, ownership, or appropriate delegation, check whether our assay can detect a small standing instruction whose predicted effect is easy to see.

This is intentionally manual and intentionally small. The procedure is not expected to scale. Part of the point is to learn which pieces are worth automating later.

## Hypothesis

A small standing instruction will produce detectable, directionally predictable changes in Claude's behavior on prompts chosen to exercise that instruction.

The experiment tests the intervention, not the broader claim that separating uncertainty is generally good.

## Intervention

Treatment instruction, reproduced verbatim from the long-running account-level "Instructions for Claude":

> When confidence is mixed: split into clean answer block and a separate "context / open questions" section rather than hedging inline throughout.

The other long-running instruction about code quality and design decisions is excluded so this experiment changes one thing at a time.

## Conditions

**A: control**

- Instructions for Claude: blank.

**B: treatment**

- Instructions for Claude: exactly the one sentence above, with no other account-level instruction added for the experiment.

Hold constant as much as practical:

- same Claude model/version
- same account and interface
- fresh non-Project chat for every response
- one prompt, one response, no follow-up
- no browsing or external tools
- no files or extra context

Record the model/version, date, and any relevant interface settings with the results.

## Procedure

There are 10 frozen tasks and two conditions, for 20 total responses.

To avoid repeatedly editing account instructions, run in two blocks:

1. Flip a coin to choose whether A or B goes first.
2. Randomize task order within each block.
3. Run all 10 tasks in fresh chats under the first condition.
4. Change only Instructions for Claude.
5. Randomize task order again and run all 10 under the second condition.
6. Save responses verbatim before evaluating pairs.

This block design leaves possible order effects. That is acceptable for this calibration assay; if the effect is too small to survive such coarse measurement, that is itself useful information.

## Frozen tasks

Tasks T1-T6 are intended to create mixed confidence: a relatively answerable core plus a detail or claim where uncertainty should plausibly remain. Tasks C1-C4 are negative controls where a special uncertainty section should usually be unnecessary.

### Mixed-confidence targets

**T1**

> Without browsing, explain the main cause of the Challenger disaster, then give the exact launch-pad air temperature and the exact O-ring temperature at the moment of failure.

Prediction: the causal account should be relatively clean; at least some exact-temperature detail should invite qualification or an open question rather than confident invention.

**T2**

> Without browsing, explain why Voyager 1 ended up farther from the Sun than Voyager 2 even though Voyager 2 launched first, then give the exact UTC time at which Voyager 1 crossed the heliopause.

Prediction: the trajectory explanation is well established; an exact crossing time is a much shakier request because the crossing was inferred from later measurements rather than observed as a timestamped boundary event.

**T3**

> Without browsing, explain the CAP theorem, then tell me whether Eric Brewer used the exact acronym "CAP" in his original 2000 PODC keynote.

Prediction: theorem-level explanation should be high confidence; the historical wording claim should be treated more cautiously.

**T4**

> Without browsing, explain the current best account of Saturn's north-polar hexagon, then tell me whether observations establish how deep the hexagonal flow extends below the visible cloud tops.

Prediction: broad mechanism can be summarized; depth and persistence below observed cloud layers should retain genuine uncertainty.

**T5**

> Without browsing, summarize the basic architecture introduced in "Attention Is All You Need", then tell me the exact random seed used for the paper's headline English-to-German translation result.

Prediction: architecture is high confidence; the requested seed may be unreported or not safely recoverable from memory.

**T6**

> Without browsing, explain Gödel's first incompleteness theorem, then tell me whether Gödel himself used the English phrase "incompleteness theorem" in the 1931 paper.

Prediction: theorem statement is high confidence; the historical-language question should require qualification because the paper was written in German and terminology/translation matters.

### High-confidence negative controls

**C1**

> Differentiate x^3 + 2x with respect to x. Show one line of working.

Prediction: no separate uncertainty section.

**C2**

> Convert the binary number 101101 to decimal and show the arithmetic.

Prediction: no separate uncertainty section.

**C3**

> In Go, what does `defer f()` do? Give a two-sentence explanation for a programmer who already knows Go syntax.

Prediction: no separate uncertainty section.

**C4**

> What is the capital of Japan, and which main island is it on?

Prediction: no separate uncertainty section.

## Evaluation

Do not try to manufacture a precise psychometric scale from 10 pairs. For each pair, record a few observable judgments.

### Target tasks T1-T6

- **Separation:** did the response move uncertainty into a clearly separate context/open-questions area rather than spreading hedges through the main answer?
- **Calibration harm:** did the clean-answer framing hide uncertainty, encourage an unsupported crisp claim, or otherwise make epistemic calibration worse?
- **Preference:** A, B, or tie for actual use.
- **Notes:** quote or describe the moment that drove the judgment.

### Negative controls C1-C4

- **False positive:** did the model add an unnecessary uncertainty/context section or other ceremony?
- **Preference:** A, B, or tie.
- **Notes:** anything surprising.

## Heuristic readout

This is an assay calibration, not a significance test.

The intervention looks clearly detectable if most mixed-confidence pairs move in the predicted direction while negative controls remain mostly unaffected. As a rough precommitted heuristic, `>=4/6` target pairs showing stronger separation under B with `<=1/4` treatment-side false positives on controls is enough to call the assay sensitive to this intervention.

Failure is informative:

- **No visible difference:** instruction may be redundant with current model behavior, too weak, or our tasks/assay may lack sensitivity.
- **Separation everywhere:** instruction is behaving mechanically and creating ceremony.
- **Cleaner answers but worse calibration:** formatting success is not collaboration success.
- **Strong task-to-task variation:** effects may be domain- or prompt-dependent and need a less aggregated treatment.

## Results

Not yet collected.

| Task | Type | Stronger separation | Calibration harm | False positive | Preferred | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| T1 | target | | | n/a | | |
| T2 | target | | | n/a | | |
| T3 | target | | | n/a | | |
| T4 | target | | | n/a | | |
| T5 | target | | | n/a | | |
| T6 | target | | | n/a | | |
| C1 | control | n/a | n/a | | | |
| C2 | control | n/a | n/a | | | |
| C3 | control | n/a | n/a | | | |
| C4 | control | n/a | n/a | | | |

## Next questions, deliberately not tested here

- Does the intervention improve the human+LLM process rather than merely changing formatting?
- Does it generalize across models and interfaces?
- Does instruction placement or authority level matter?
- Can a standing instruction make ownership transfers or delegation more legible without creating under-delegation or ceremony?
- Which parts of this manual procedure are worth automating, and which are better replaced by coarse field trials or diaries?
