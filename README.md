# centaur

Centaur is a small applied-epistemology and workflow project asking:

**How can I use LLMs better?**

The original prototype focused on turn-taking between a human and a coding agent. This reboot treats turn-taking as one hypothesis among many.

For now, the project is deliberately small. Rather than starting with a large harness or a theory of ideal human-LLM collaboration, Centaur will make small workflow hypotheses explicit, test them against real interactions, and keep, revise, or discard them based on what happens.

Working v0 success criterion:

> Make tacit practice explicit enough that we can inspect it, disagree with it, and deliberately try alternatives.

Current work:

- [literature.md](literature.md): a short orientation to relevant prompting and human-AI collaboration work.
- [Experiment 000](experiments/000-detect-standing-instruction.md): check whether a tiny standing instruction produces a detectable, directionally predictable behavioral effect before trying to measure subtler collaboration questions.
- [Experiment 000 results](results/000-detect-standing-instruction.md): the standing-instruction assay produced a clear structural effect on all six targets and no targeted false positives on the four controls.
- [Experiment 001](experiments/001-durable-state-field-test.md): a one-week field test of a broader collaboration prompt aimed at durable state, convergence, and legible handoffs.
- [Experiment 001 results](results/001-durable-state-field-test.md): no clear ecological behavior shift was noticed; a separate unsolicited-continuation tic was substantially more salient.
- [Experiment 002](experiments/002-terse-standing-instructions.md): a terse four-rule standing prompt, with a primary black-box probe asking whether a user-level stop condition can suppress unsolicited continuations.
- [Changing seas beneath the experiment](notes/2026-09-16-changing-seas.md): a note on substrate drift and why visible product/harness changes should be logged rather than silently treated as fixed experimental conditions.
- [Prompt impressions](prompt-impressions/2026-09-16-chatgpt-base.md): dated, explicitly non-authoritative snapshots of how the assistant functionally perceives its current base prompting and harness.
