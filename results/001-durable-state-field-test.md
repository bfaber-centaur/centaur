# Experiment 001 results: durable state, convergence, and legible handoff

Date: 2026-09-22

This records the field run of `experiments/001-durable-state-field-test.md`. The frozen experiment file is left unchanged.

## Run shape

Experiment 001 was deliberately ecological rather than controlled: the standing instruction remained active during ordinary ChatGPT use for roughly one week, across research, writing, software, and reflective conversations.

The treatment contained three ideas:

1. preserve consequential state outside chat;
2. do not reopen converged choices without a concrete reason;
3. use model capabilities aggressively while keeping substantive handoffs legible.

The intended readout was not a score. It was whether any of those clauses produced memorable helpful, harmful, or annoying changes during normal work.

## Primary observation

The operator reported **no clear behavioral shift attributable to the standing instruction**.

In particular, there was no memorable recurring pattern of:

- consequential state being surfaced for capture more often;
- converged choices staying settled because of the prompt;
- substantive handoffs becoming newly legible;
- ceremony, timidity, or over-freezing caused by the prompt.

This is best treated as a weak/null ecological result, not as evidence that the clauses had no effect. The intervention was broad, ordinary tasks varied, and there was no clean control condition.

The absence of salient effects is still useful because Experiment 000 had shown that a standing instruction could produce a large, obvious effect under a targeted assay. Detectability in a synthetic battery did not translate into an equally conspicuous effect in ordinary use here.

## A stronger behavioral signal appeared elsewhere

During the same period, a different recurring behavior became unusually salient across unrelated conversations: responses often ended by packaging a bounded continuation or next step, commonly in a small finite structure such as a three-question check, three-part plan, or explicit offer to continue.

That motif was more noticeable than any effect attributable to Experiment 001.

The operator had not deliberately requested it, and it appeared across topics. This does **not** establish whether the cause was model checkpoint, product harness, higher-priority prompting, reinforcement history, conversation adaptation, or some mixture.

It does create a useful black-box target: can a terse user-level instruction suppress a conspicuous recurring tendency?

## Substrate caveat

The run also coincided with visible product/harness variation already recorded in [the changing-seas note](../notes/2026-09-16-changing-seas.md), including a two-response preference chooser and growing awareness of materially different Chat and Work harnesses.

Centaur therefore should not treat the surrounding platform as stationary during field tests.

A user-preference prompt can remain unchanged while model routing, product instructions, UI treatments, tool access, memory behavior, or other hidden variables change beneath it.

## What this supports

Experiment 001 supports only a modest conclusion:

> A broad three-clause collaboration prompt produced no clearly memorable ecological effect during this week of ordinary use, while an apparently upstream continuation style was conspicuous enough to notice repeatedly.

That contrast motivates a narrower next intervention.

## Limitations

- no randomized control week
- no blinded evaluation
- task mix changed naturally over the week
- no complete interaction log was scored
- awareness of the prompt could alter human behavior
- the treatment bundled three distinct ideas
- the surrounding product/harness visibly changed during the run
- absence of memorable effects is weaker evidence than a measured absence

## Transition

Experiment 002 keeps the useful ideas but compresses them into shorter declarative rules and adds an explicit stop condition.

The main new probe is whether a user-level preference can reduce unsolicited continuation behavior that appears to be a strong model/product tendency.
