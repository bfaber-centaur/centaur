# Experiment 001 — durable state, convergence, and legible handoff

**Status:** proposed one-week field test

## Question

Can a small standing instruction improve ordinary human–LLM work by preserving project state, protecting convergence, and making substantive changes of direction or ownership visible — without making the model timid, ceremonial, or annoying?

This is deliberately a field test rather than a controlled assay. Experiment 000 established that a small standing instruction can produce a large, directionally predictable behavioral effect. This experiment asks a fuzzier but more useful question: does a prompt aimed at recurring collaboration failures make normal work feel better over a week?

## Treatment

Use the following text unchanged as the standing instruction for normal web-app work:

> Treat conversation as working space, not the source of truth. When a consequential decision, result, correction, rationale, or open question emerges, help preserve it in the relevant durable artifact rather than leaving it buried in chat.
>
> Once a choice or direction has converged, do not reopen or broaden it merely because another plausible alternative exists; require a concrete defect, contradiction, or new evidence.
>
> Use your capabilities aggressively in service of my goals, but make substantive changes of direction or ownership legible rather than silently taking them over.

## Why these three clauses

The prompt is grounded in repeated patterns across recent research, writing, software, and design work. It is not intended as a general theory of ideal human–LLM collaboration.

### 1. Conversation is useful workspace but poor durable state

Several successful projects externalized important reasoning instead of relying on chat history or memory:

- The `minterp-first-steps` research log preserved predictions, assay failures, freeze points, and decisions while notebooks remained the computational source of truth.
- The MATS work benefited from explicit hypotheses, controls, and freeze points; the associated SPAR postmortem identified failure to preserve epistemic state as a major process mistake.
- `Grap Theory` used an append-only rule: corrections and reversals were recorded rather than silently rewriting history.
- Stars! parity work labels mechanics by epistemic status and treats `PARITY.md` as a behavioral specification rather than silently guessing uncertain mechanics.
- The Consensus Knot design log preserved why alternatives were rejected, not merely which final design won.

A recurring failure mode in ordinary web-app use is therefore **context burial**: an important decision, rationale, correction, or open question remains only in a long conversational stream and becomes functionally inaccessible later.

The first clause asks the model to notice the chat-to-artifact boundary without demanding that every observation become documentation.

### 2. Generativity is useful until the work has converged

Exploration often goes well because the model can generate alternatives, controls, explanations, and attacks quickly. The same property becomes costly late in writing or design work.

The SPAR application postmortem records several versions of this failure:

- repeated review drifted from falsification toward reassurance;
- verified, proposed, and settled claims remained equally mutable in conversation;
- settled terminology could be reopened without new evidence;
- experiment descriptions accumulated too many adjacent ideas;
- the useful correction was "generate broadly, submit narrowly."

The MATS planning handoff independently imposed the same rule in operational form: perform a bounded red-team, make only changes that address concrete validity problems, then freeze.

The second clause therefore tries to preserve the value of exploration while increasing the evidence required to reopen a converged choice.

### 3. The goal is not less delegation

Centaur is partly inspired by mixed-initiative systems, the adoption of chess engines as analysis partners, and examples of semi-automated mathematical work where humans and machines contribute different strengths.

The desired behavior is not artificial deference. The model should search, calculate, draft, compress, implement, criticize, and otherwise remove work aggressively when useful.

The recurring concern is instead **invisible handoff**: an interaction can begin with explanation, red-teaming, or editing and gradually shift into the model making substantive inclusion, design, or completion decisions without either participant marking the transition.

The third clause asks for those changes of direction or ownership to remain legible while explicitly preserving aggressive delegation of useful work.

## What would count as success?

Do not score every interaction. During one week of ordinary use, record only salient moments where the instruction appears to matter.

Useful observations include:

- the model notices an important result or rationale that would otherwise have remained buried in chat;
- a settled decision stays settled despite an easy opportunity to generate alternatives;
- a substantive handoff becomes visible at a useful moment;
- the prompt prevents churn during writing or review;
- the model remains willing to do substantial delegated work.

Also record costs:

- excessive "should I save this?" ceremony;
- premature freezing of a question that should still be explored;
- reluctance to challenge a bad settled choice;
- timid or over-deferential behavior;
- unnecessary narration of ordinary delegation;
- attempts to treat every conversation as a project with a durable artifact.

A handful of memorable positive or negative cases is more useful here than manufactured counts.

## Lightweight diary

For any salient case, capture only:

```text
date / task:
what happened:
helpful, harmful, or ambiguous:
which clause, if any:
one-line note:
```

No entry is required when nothing interesting happens.

## Interpretation limits

This is not a randomized or blinded experiment. There is no clean control week, interaction mix will vary, and awareness of the prompt may change the human side of the system.

The outcome is also intentionally subjective. The test can reveal useful failure modes, side effects, and memorable improvements; it cannot establish that the prompt generally improves collaboration.

The intervention may also be too broad to attribute an observed effect cleanly to one clause. If the week produces useful signal, later experiments can isolate individual components.

## Prior expectation

The strongest expected benefit is reduced loss of project state during long web-app conversations, especially during research and writing. The largest expected risk is ceremony: the model may over-detect "consequential" moments or narrate handoffs that were already obvious.

The prompt should be revised or discarded if those costs dominate ordinary use.
