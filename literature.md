# Literature orientation

Centaur starts from a practical question: how should a human and an LLM divide work without accidentally degrading judgment, attention, or output quality?

This is not yet a systematic literature review. It is a short map of work that motivates the first experiments and gives us useful failure modes to watch for.

## Standing instructions should earn their context

Anthropic's current Claude Code guidance recommends keeping CLAUDE.md short, human-readable, and limited to information that applies broadly. It explicitly suggests treating the file like code: prune it, inspect failures, and test whether changing an instruction actually changes behavior. It also distinguishes advisory instructions from deterministic hooks.

- Anthropic, [Best practices for Claude Code](https://code.claude.com/docs/en/best-practices)

OpenAI reports a similar failure mode from Codex: a large monolithic AGENTS.md consumed scarce context, made priorities harder to distinguish, went stale, and was difficult to verify. Their summary is useful shorthand: give the agent a map, not a 1,000-page instruction manual.

- OpenAI, [Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)

Working implication for Centaur: prefer small, behaviorally specific standing instructions that arise from observed problems. Treat prompt changes as interventions to test rather than doctrine to accumulate.

## Human-AI collaboration is a mixed-initiative problem

Long before LLMs, mixed-initiative HCI studied how people and automated systems should share control. Horvitz identifies recurring problems that still look familiar: systems guessing user goals badly, acting at the wrong time, misjudging the costs and benefits of automation, and failing to give users good opportunities to guide or correct the system.

- Eric Horvitz, [Principles of Mixed-Initiative User Interfaces](https://www.microsoft.com/en-us/research/publication/principles-mixed-initiative-user-interfaces/), CHI 1999

This suggests that maximum automation and maximum human control are both poor default objectives. The interesting object is the joint system and when initiative should move between participants.

## Better AI output does not guarantee better human-AI performance

Microsoft Research defines appropriate reliance as accepting correct AI outputs while rejecting incorrect ones. Its synthesis of roughly 50 papers emphasizes both over-reliance and under-reliance as possible failures of human+AI systems.

- Passi, Dhanorkar, and Vorvoreanu, [Appropriate reliance on Generative AI: Research synthesis](https://www.microsoft.com/en-us/research/publication/appropriate-reliance-on-generative-ai-research-synthesis/), 2024

Follow-up work warns that interventions intended to reduce over-reliance can themselves backfire and should be tested with users rather than assumed beneficial.

- Vorvoreanu et al., [Fostering appropriate reliance on GenAI: Lessons learned from early research](https://www.microsoft.com/en-us/research/publication/fostering-appropriate-reliance-on-genai-lessons-learned-from-early-research/), 2025

Working implication for Centaur: measure costs as well as benefits. An instruction that reduces one failure mode may create ceremony, under-delegation, misplaced confidence, or extra cognitive load.

## Research style: get feedback before building infrastructure

Neel Nanda's mechanistic-interpretability research advice emphasizes tight empirical feedback loops, quick and dirty experiments, aggressive red-teaming of hypotheses, and delaying heavy infrastructure until the cheap version has revealed what actually matters.

- Neel Nanda, [Concrete Steps to Get Started in Transformer Mechanistic Interpretability](https://www.neelnanda.io/mechanistic-interpretability/getting-started-old) (now deprecated as onboarding guidance, still cited here for its research-process advice)

Terence Tao gives a complementary example of division of intellectual labor in semi-automated proof: the human supplies high-level tactics while the proof assistant performs calculations and provides checkable verification.

- Terence Tao, [A tool to verify estimates, II: a flexible proof assistant](https://terrytao.wordpress.com/2025/05/09/a-tool-to-verify-estimates-ii-a-flexible-proof-assistant/), 2025

Working implication for Centaur: start with small falsifiable workflow changes, keep a human-readable record of predictions and failures, and automate only after manual use reveals where the real friction is.

## Current working cautions

These are hypotheses suggested by the literature and by lived use, not settled principles:

- The relevant outcome is performance of the human+model process, not model output in isolation.
- Persistent instructions consume attention/context and may create side effects.
- Prompt effects can be confounded with model, interface, personalization, task choice, and changes in the human's own behavior.
- Personal bottlenecks differ. One user may need to protect judgment and exploration; another may need to protect attention and review bandwidth.
- Small controlled assays and coarse field diaries may answer different questions. Both can be useful.

The first experiment therefore asks a deliberately boring question: can we detect the behavioral effect of one small standing instruction at all?
