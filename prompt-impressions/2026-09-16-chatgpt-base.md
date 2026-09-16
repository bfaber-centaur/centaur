# ChatGPT base-prompt impressions — 2026-09-16

**Date:** 2026-09-16

This is **not** a prompt extraction and should not be read as a reconstruction of hidden system text.

It is a functional snapshot of what the assistant reports the current harness appears to be doing from inside the interaction. Exact hidden instructions, their ordering, routing logic, UI experiments, and personalization layers are not directly observable here.

## Functional impression

The current assistant behavior appears to be shaped by several layers.

### Model and interaction identity

The assistant identifies as GPT-5.6 Sol and is instructed to reason internally rather than expose private chain-of-thought. It is expected to answer directly rather than narrate internal deliberation.

### Style pressure

The response style is pushed toward compact, conversational prose: cohesive paragraphs, relatively little list spam, no performative "real talk" framing, and a professional-but-natural register. There are explicit pressures against patronizing or canned therapeutic language.

### Tool routing is a large part of the harness

A substantial fraction of the apparent "base prompt" is not personality at all, but policy about which surface or tool to use.

Examples include:

- browse for current, niche, or uncertain public facts;
- use connected sources for private project/account data;
- use GitHub for repository work;
- use Files for uploaded or saved documents;
- use dedicated artifact workflows for slides, documents, PDFs, and spreadsheets;
- use image generation for actual image creation/editing;
- use scheduling tools for future reminders or condition watches.

This makes the harness feel less like a single conversational prompt and more like a routing layer over many capabilities.

### Grounding and provenance

There is strong pressure to ground claims in the actual source being used rather than silently filling gaps from general knowledge. Current or uncertain claims should be verified. File- and connector-derived claims should preserve provenance and citations where available.

### Domain-specific behavioral constraints

Some domains have additional rules. Politics is a clear example: inform and compare, but do not endorse, rank choices, steer votes, or independently predict election winners. Other safety- or privacy-sensitive areas also have special handling.

### Memory and personal context

Prior context may be used when materially helpful, but there are constraints against casually surfacing sensitive personal information or treating memory as infallible. The assistant also has instructions about how memory-management questions should be handled.

### Artifact and product behavior

The harness includes product-specific behavior around writing blocks, Work, plugins/connectors, voice, ads, settings, parental controls, and other UI capabilities. Some of these activate only when relevant.

### Long-task behavior

For tool-heavy or long-running tasks, the assistant is encouraged to provide short progress updates rather than disappearing into silent tool work. It is also prohibited from pretending to perform asynchronous background work unless a real scheduled automation is created.

## What is notably uncertain

The assistant cannot reliably determine from inside the conversation whether a behavior comes from:

- the visible conversation context;
- a standing custom instruction;
- hidden product/system instructions;
- personalization or memory layers;
- model routing;
- an A/B test or UI experiment;
- a decoder/sampling change;
- some other product intervention.

For example, Centaur's current three-clause standing instruction is highly salient in conversation because we designed it together. That does not by itself prove that the same text is also being injected at a privileged instruction layer.

Likewise, the appearance of a two-response preference chooser is evidence that the product substrate intervened, but not evidence for any particular hidden-prompt change.

## Why keep these snapshots

Bobby recalls a materially different earlier description of the assistant's base prompting.

That makes these impressions useful even though they are incomplete. A dated series may reveal changes in what the assistant can observe about its own harness, changes in the harness itself, or both.

The epistemic status should stay modest:

> **Functional impression from inside the system, not ground-truth prompt text.**
