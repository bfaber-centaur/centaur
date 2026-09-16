# Changing seas beneath the experiment

**Date:** 2026-09-16

Centaur is not running on a stationary substrate.

Today ChatGPT visibly presented two alternative answers to the same turn and asked Bobby which one he preferred. This is direct evidence that the product can intervene in the interaction in ways that are not represented in the conversation transcript or controlled by us.

We do **not** know what caused the intervention. Possibilities include a UI experiment, preference-data collection, routing changes, decoding changes, a different instruction stack, or something else. The observation does not justify concluding that the hidden assistant prompt changed.

This follows another useful discovery from the previous day: ChatGPT Work exposes a materially different harness from ordinary chat. It foregrounds different model/effort choices, a different usage meter, more sustained execution, and different tool behavior. Even connector visibility can differ by path: for example, normalized GitHub repository metadata omitted a repository description while a raw repository fetch exposed it.

## Why this matters for Centaur

Our experiments often treat the standing instruction, task, or workflow as the independent variable. In practice, the surrounding product may also change:

- model or model routing;
- system or product instructions;
- personalization or memory behavior;
- decoding or response-selection behavior;
- available tools and tool schemas;
- UI affordances and default interaction mode;
- usage/effort controls;
- agentic harness behavior.

Some of these variables are observable. Some are only partially observable. Some may be invisible to both Bobby and the assistant.

Therefore a result like "this prompt felt better this week" cannot automatically be attributed to the prompt alone.

## Lightweight response

Do not turn this into a forensic bureaucracy. When the substrate visibly changes, leave a breadcrumb.

A useful diary tag is:

> **SUBSTRATE** — a visible change in model, harness, UI, tool access, routing behavior, or other product behavior that could plausibly affect the collaboration.

Record the date and the concrete observation. Avoid inferring an invisible cause unless we have evidence for it.

For important comparisons, preserve enough context to reconstruct the environment later: model when known, interaction mode (chat vs. Work), effort setting when salient, relevant standing instructions, and any unusual UI/tool behavior.

## Current methodological stance

Treat the platform as a latent and potentially drifting variable.

This does not make small field experiments useless. It changes what they can support. Ecological observations can still tell us whether a workflow is useful in the environment we actually inhabit; they just should not be mistaken for clean causal estimates when the environment itself is moving.

The practical response is provenance, not paralysis.
