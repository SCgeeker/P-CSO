---
name: pinker-coherence
description: This skill should be used to optimize paragraph and multi-sentence flow for logical clarity using 8 discourse-level coherence principles built on Chapter 5 of Pinker's "The Sense of Style". Use this skill whenever users mention flow problems, unclear transitions, buried topics, or text that jumps around. Also invoke when reviewers say writing is hard to follow at the paragraph level, when logical connections between ideas are missing, when the subject shifts randomly between sentences, when abstractions rather than people occupy subject position, when open questions are announced but not stated, when prose reads as authorless or machine-written, or when connectives like "while" or "also" feel wrong. Does not address sentence-level syntax — use pinker-syntax for parsing difficulty.
---

# Pinker Coherence Optimizer: Discourse-Level Flow and Logic

**Framework**: Steven Pinker's "The Sense of Style" — Chapter 5: Arcs of Coherence
**Purpose**: Optimize paragraph and multi-sentence flow for logical clarity and cognitive ease
**Does NOT address**: Sentence-level syntax, wordiness, or parsing issues (use `/pinker-syntax`); grammar polish (use `/english-editing`)

## Your Role

A **discourse coherence specialist**. Create coherent arcs where: readers always know what the text is about, each sentence connects smoothly to the next, logic is explicit rather than inferred, comparisons are crystal clear, and the author's presence is invisible ("window to world").

## 8 Coherence Principles (summary)

1. **Establish Topic and Point** — state what the text is about and why it matters in the opening 1–2 sentences; don't bury the lede.
2. **Maintain Information Flow** — keep consistent topic strings across sentences (coherent arcs) and order each sentence given → new.
3. **Track Participants and Entities** — use a stable referring system (indefinite → definite/pronoun); avoid synonymomania (elegant variation) for the same entity. Keep every referent reachable: restate a long-distance abstraction in place, repeat the noun instead of stacking demonstratives, and do not close a sentence on a pronoun.
4. **Clarify Logical Relations** — make cause/contrast/addition/example relations explicit with the precise connective; when in doubt, connect.
5. **Optimize Comparison and Contrast** — hold syntax and wording constant across compared items; vary only the one element that differs (single-variable rule).
6. **Handle Abstract Reference** — introduce an action as a verb on first mention; nominalize only on later mentions, where it acts like a pronoun.
7. **Check Author Attitude** — cut metadiscourse ("in this section I will...") and unnecessary hedging. Name every open question in the sentence that raises it. Cut study-note register (7D): sentences that announce, gesture at, or file the argument instead of making it.
8. **Agency in Subject Position** — extract every sentence subject, then classify each inanimate one three ways. A hidden person gets named (8A). A document acting gets replaced by the claim it is filing (8B). A legitimate abstraction keeps its slot. Cross-references and reason-giving structural sentences are not faults.

Full definitions, the 8-item negative-constraint prescan, the self-review checklist, and the output-format template are in `references/principles.md` — read it before drafting a revision.

`references/examples.md` holds one calibration before/after pair per principle (the hardest, most representative case). Consult it when a principle's application is ambiguous on the current text.

## Workflow

1. **Prescan**: run the 8 negative-constraint checks in `references/principles.md` against the input text.
2. **Apply the 7 principles** above, using `references/principles.md` for operational detail and `references/examples.md` for calibration on hard cases.
3. **Self-review**: run the checklist in `references/principles.md` before finalizing.
4. **Output** using the format template in `references/principles.md` (original text, optimized text, per-issue diagnostics, summary of principles applied).
5. Suggest `/pinker-syntax` for remaining sentence-level issues, `/english-editing` for final grammar polish, or `/p-cso-workflow` for the full pipeline.
