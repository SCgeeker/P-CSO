---
name: p-cso-workflow
description: Transform research notes to cognitively optimized manuscript via Pinker's Cognitive Style Optimization (syntax + coherence from "The Sense of Style"), then audit terminology, numbers, and claims. Triggers: improve readability, convert notes to prose, optimize research writing for clarity, notes-to-manuscript, draft reads like a study note, prose is not in academic tone.
---

# P-CSO Workflow: Complete Notes-to-Manuscript with Cognitive Optimization

**Framework**: Steven Pinker's Cognitive Style Optimization (P-CSO)
**Source**: "The Sense of Style" — Chapters 4 (Syntax) & 5 (Coherence)
**Purpose**: Transform research notes into manuscript prose that survives peer review

---

## What This Skill Does

This is a **thin orchestrator** that chains four stages into one pipeline:

1. **Stage 1** — Organize scattered notes into focal statements (if starting from notes)
2. **Stage 2** — Invoke `/pinker-syntax` for sentence-level optimization
3. **Stage 3** — Invoke `/pinker-coherence` for discourse-level flow and register
4. **Stage 4** — Invoke `/manuscript-writing-review` for terminology, numerical, and claim audit

Each sub-skill owns its own complete rule set. This skill contributes Stage 1, the revision
protocol, the communication-language rule, and the LaTeX formatting layer. **Do not restate the
sub-skills' rules here.** When a rule needs strengthening, strengthen it in the sub-skill that
owns it, so that it also fires when the user invokes that sub-skill directly.

**Target outcome**: Classic style writing, a clear "window to the world" that minimizes reader
cognitive burden, in a register that reads as an article rather than as working notes.

---

## Communication Language

The language of the discussion is not the language of the manuscript. Keeping them apart stops
note-taking prose from leaking into the draft, which is one documented cause of the study-note
register that gets drafts rejected.

| Situation | Discussion language |
|---|---|
| Stage 1 notes organization; section-level restructuring; adjudicating between rewrite options; any rewrite that changes what a section claims | **Traditional Chinese** |
| Line-level edits, diagnostics, terminology swaps, grammar fixes | **English** |
| The manuscript text itself, at every stage | **English, always** |

---

## Four-Stage Workflow

### STAGE 1: Draft Scaffolding (If Starting from Notes)

Skip this stage if the user provides a complete draft; go directly to Stage 2.

#### 1A. Organize Notes

1. Identify key themes across all notes
2. Group related ideas into paragraph outlines
3. Create a **focal statement** for each outline (1–2 sentences: the core message)
4. Present structure for user approval before proceeding

**Output Format**:
```markdown
## Proposed Paragraph Structure

**Paragraph 1 Focal Statement**: [Core message]
- Supporting points from notes
- Relevant citations: [[note-ref]] or [@Author2023]

**Paragraph 2 Focal Statement**: [Core message]
- Supporting points from notes
- Relevant citations

[Continue for all paragraphs]
```

#### 1B. Generate Draft Scaffold

For each focal statement:
1. Open with the focal statement (or close paraphrase)
2. Integrate evidence from notes logically
3. Place citation placeholders appropriately
4. Use clear, academic prose
5. Maintain flow between ideas

Mark every scaffold clearly: **⚠️ SCAFFOLD ONLY — user must rewrite in their own words.**

---

### STAGE 2: Syntax Optimization

Invoke the `/pinker-syntax` skill on the current draft (scaffold or user-provided text).

- Pass the full draft text
- The skill applies Rules 1–11: the six Chapter 4 cognitive rules, the four canonical clause
  conventions (Rules 7–10: no em-dashes, no inline parenthetical lists, no relative clauses, no
  subordinate clauses where SVO works), and Rule 11 on connective load
- Collect the syntax-optimized text as input for Stage 3

---

### STAGE 3: Coherence and Register Optimization

After Stage 2 completes, invoke the `/pinker-coherence` skill on the syntax-optimized text.

- Pass the syntax-optimized draft
- The skill applies the 8 Chapter 5 coherence principles
- **Principles 7D and 3C/3D carry the register work.** A draft can satisfy every syntax rule and
  still read as a study note. 7D cuts sentences that only label the argument; 3C and 3D keep
  every referent reachable. Never treat Stage 3 as optional on the grounds that Stage 2 ran

---

### STAGE 4: Terminology, Numerical, and Claim Audit

Invoke `/manuscript-writing-review` on the coherence-optimized text. Its six passes overlap
Stages 2 and 3 in passes 1–3, so on a text that has already been through them, **run passes 4,
5, and 6 in targeted mode** unless the user asks for a full review.

- **Pass 4** settles terminology: one name per construct, the field-register test for content
  words, and the rule that a term must not presuppose what the manuscript denies
- **Pass 5** catches numbers and attributions that a revision elsewhere has made stale. Run it
  after any change that touches a count, a total, or a cited figure
- **Pass 6** checks claim-evidence discipline: unsupported concessions, hedged accusations, and
  paragraphs that withdraw their own claims

Pass 6 reports rather than edits. Bring its findings to the user.

---

## Revision Protocol

This is how the pipeline runs against a live manuscript. It is not optional overhead. Every item
below exists because skipping it cost a rewrite cycle.

**1. Never edit the manuscript until the user approves the text.**
Draft every revision into a separate file, `<section>_rewrite_YYYYMMDD.md`, holding the
replacement text and a change list. The manuscript stays untouched.

**2. Show old against new, paragraph by paragraph, before applying anything.**
The user adjudicates the content of the rewrite, not only its final form.

**3. Version, archive, and show only the current version.**
Supersede in place: move the previous version to a dotfile such as `.section4_v5_archive.md`.
When the user asks for the next version, present that version alone unless they ask for the
history.

**4. Read the user's HTML comments and inline edits, then discuss before applying.**
The user reviews by editing the draft file and leaving HTML comments in it. Respond to each one.
**Push back with a reason where the edit is wrong.** An edit that contradicts the manuscript's
own argument, breaks subject-verb agreement, or reintroduces a retired term must be reported
rather than propagated. Accepting with a correction is a normal outcome: `A stimuli pool`
becomes `A stimulus pool`; `Some studies in our review takes its word lists` becomes
`The studies examined above take their word lists`.

**5. Keep an open-items list.**
End every round with what remains undecided and what can only be verified after integration.

**6. After integration, verify.**
Back up the source file, render it, confirm every cross-reference still has a referent, and sweep
the rest of the document for facts the change has made stale. An abstract still citing a
superseded count is the failure this step exists to catch.

---

## LaTeX Formatting (Apply Throughout)

When working with R Markdown (.Rmd), LaTeX (.tex), or academic manuscripts, convert all notation
to LaTeX format during the sub-skill invocations or as a final pass:

| Before | After |
|--------|-------|
| `N=120` | `$N = 120$` |
| `p < .05` | `$p < .05$` |
| `BF₁₀` (Unicode) | `$BF_{10}$` |
| `3×2` (Unicode) | `$3 \times 2$` |
| `α = 0.05` (Unicode) | `$\alpha = 0.05$` |
| `95% CI [-0.05, 0.01]` | `95% CI $[-0.05, 0.01]$` |

**Why LaTeX**: Editable in any text editor, renders correctly in R Markdown to Word/PDF/HTML,
version-control friendly, no encoding issues.

When the user provides Unicode symbols, convert them automatically. At the end, offer: "I've
converted all notation to LaTeX format. Want me to apply this to earlier sections too?"

---

## Output Format

```markdown
# P-CSO Workflow Results

## Stage 1: Draft Scaffold (if applicable)
[Organized focal statements and paragraph structure]
⚠️ SCAFFOLD ONLY: User must develop this in their own words.

---

## Stage 2: Syntax Optimization
[Output from /pinker-syntax: optimized text + diagnostics]

---

## Stage 3: Coherence and Register Optimization
[Output from /pinker-coherence: optimized text + diagnostics, including 7D register findings]

---

## Stage 4: Terminology, Numerical, and Claim Audit
[Output from /manuscript-writing-review passes 4-6: findings and proposed revisions]

---

## Final Manuscript Text
[Combined result after all stages]

---

## Open Items
- [ ] Decisions still with the user
- [ ] Checks that can only run after integration

---

## Next Steps
- [ ] Review all changes and adjust to your voice and intent
- [ ] Verify technical accuracy and citations
- [ ] Use `/english-editing` for final grammar polish
- [ ] Check field-specific style requirements (APA, journal guidelines)
```

---

## When to Apply Each Stage

| Starting point | Stages to run |
|----------------|---------------|
| Scattered notes | All 4 stages |
| Complete draft, both syntax and coherence issues | Stages 2, 3, 4 |
| Complete draft, syntax only | Stage 2, then Stage 3 for register, then Stage 4 |
| Complete draft, flow only | Stage 3, then Stage 4 |
| Just need organization help | Stage 1 only |
| Draft reads like a study note | Stage 3 (Principle 7D) first, then Stage 4 |
| A revision changed a number, a term, or a count | Stage 4 alone, passes 4 and 5 |

**Stage 3 runs on every draft that reaches prose.** Register is where drafts have actually been
rejected, and no other stage checks it.

---

## Integration with Other Skills

| Position | Skill | Role |
|----------|-------|------|
| Sub-skill (Stage 2) | `/pinker-syntax` | Sentence-level optimization; owns Rules 1–11 |
| Sub-skill (Stage 3) | `/pinker-coherence` | Discourse-level flow and register; owns the 8 Chapter 5 principles, including 7D study-note register |
| Sub-skill (Stage 4) | `/manuscript-writing-review` | Terminology, numerical consistency, claim-evidence discipline; owns passes 1–6 |
| After this skill | `/english-editing` | Final grammar and article polish |

**This skill's unique contribution**: Stage 1 notes organization, the revision protocol, the
communication-language rule, pipeline coordination, and LaTeX notation conversion. Every prose
rule lives in a sub-skill.

---

**Skill Version**: 3.0
**Framework**: Pinker's "The Sense of Style" Chapters 4 and 5, plus manuscript audit
**Architecture**: Thin orchestrator (delegates every rule to a sub-skill)
**Optimized for**: Academic research writing, particularly psychology, linguistics, cognitive science
