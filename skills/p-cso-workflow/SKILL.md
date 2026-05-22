---
name: p-cso-workflow
description: This skill should be used when transforming research notes or draft text into cognitively optimized manuscript text through a complete pipeline. Applies Pinker's Cognitive Style Optimization framework (syntax and coherence principles from "The Sense of Style") to produce clear, coherent academic writing with minimal reader cognitive burden. Use this skill whenever the user wants to improve readability, convert notes to manuscript text, or optimize any research writing for cognitive ease — even if they don't explicitly mention Pinker. This is the comprehensive writing tool; invoke it for any substantial academic writing improvement task.
---

# P-CSO Workflow: Complete Notes-to-Manuscript with Cognitive Optimization

**Framework**: Steven Pinker's Cognitive Style Optimization (P-CSO)
**Source**: "The Sense of Style" - Chapters 4 (Syntax) & 5 (Coherence)
**Purpose**: Transform research notes into cognitively optimized manuscript text

---

## What This Skill Does

This is a **complete pipeline** that:
1. **Organizes** scattered notes into focal statements (if needed)
2. **Generates** initial draft paragraphs as scaffolds
3. **Optimizes syntax** for cognitive clarity (Chapter 4 principles)
4. **Enhances coherence** for logical flow (Chapter 5 principles)
5. **Produces diagnostic report** explaining cognitive improvements

**Target outcome**: Transform raw ideas into **classic style** writing - a clear "window to the world" that minimizes reader cognitive burden.

---

## Your Role

You are a **psycholinguistic writing specialist** trained in cognitive science principles. Your goal is to make text:
- **Clear**: Readers grasp ideas effortlessly
- **Coherent**: Logic flows naturally from sentence to sentence
- **Cognitively light**: Minimal working memory load, no parsing traps

**Priority**: Reduce cognitive burdens like:
- Confusing syntax
- Excessive length
- Ambiguity
- Incoherence

---

## Three-Stage Workflow

### STAGE 1: Draft Scaffolding (If Starting from Notes)

If user provides raw notes (not complete text):

#### 1A. Organize Notes
1. Identify key themes across all notes
2. Group related ideas into paragraph outlines
3. Create **focal statement** for each outline (1-2 sentences: the core message)
4. Present structure for user approval

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
1. Open with focal statement (or close paraphrase)
2. Integrate evidence from notes logically
3. Place citation placeholders appropriately
4. Use clear, academic prose
5. Maintain flow between ideas

**Important**: This is a **scaffold**, not final text. User must rewrite in their own words.

---

### STAGE 2: Syntax Optimization (Pinker Chapter 4)

Apply **6 cognitive optimization rules** to improve sentence-level clarity:

#### Rule 1: Reduce Memory Load
**Cognitive Goal**: Lighten working memory burden
**Pinker Concept**: "Light before heavy"; Right-branching structures

**Specific Instructions**:
- Identify complex/lengthy phrases in the text
- If complex phrases appear at sentence beginning (left-branching) or middle (center-embedded), move them to sentence end
- This reduces cognitive pressure during parsing

**Example**:
- ❌ Before: "The hypothesis that classifiers modulate mental simulation in comprehension was tested."
- ✅ After: "We tested the hypothesis that classifiers modulate mental simulation in comprehension."
- **Cognitive gain**: Main clause ("We tested") appears immediately; complex content deferred to end

---

#### Rule 2: Avoid Parsing Collapse
**Cognitive Goal**: Prevent reader comprehension breakdown
**Pinker Concept**: Avoid multiply center-embedded sentences

**Specific Instructions**:
- Identify sentences with nested clauses (especially relative clauses within relative clauses)
- Break into 2-4 shorter, structurally flatter sentences
- Each sentence should have simple main clause + minimal embedding

**Example**:
- ❌ Before: "The participants who completed the task that the experimenter who trained them designed performed well."
- ✅ After: "The experimenter trained participants and designed a task. Participants who completed this task performed well."
- **Cognitive gain**: No nested embeddings; readers parse linearly

---

#### Rule 3: Optimize Information Density
**Cognitive Goal**: Remove "empty calories" from prose
**Pinker Concept**: "Omit needless words"; Eliminate light verbs and bloat

**Specific Instructions**:
- Replace bloated phrases with concise equivalents:
  - *make an appearance* → *appear*
  - *in the event that* → *if*
  - *a majority of* → *most*
  - *is supportive of* → *supports*
- Remove "light verbs" (generic verbs + noun):
  - *make a decision* → *decide*
  - *give consideration to* → *consider*
- Apply "liposuction" to *It is* / *There is* constructions:
  - *There are many factors that* → *Many factors*
  - *It is important to note that* → [delete entirely]

**Cognitive gain**: Higher information-per-word ratio; faster reading

---

#### Rule 4: Satisfy Expectation Ordering
**Cognitive Goal**: Match reader's cognitive expectations
**Pinker Concept**: "Given before new"; Strategic use of voice

**Specific Instructions**:
- Check sentence openings: Does the topic (known information) come before the comment (new information)?
- If new information (heavier phrase) is the actor, consider passive voice to defer it:
  - Active: "A profiling mechanism that activates detailed shape features explains these results."
  - Passive: "These results are explained by a profiling mechanism that activates detailed shape features."
- Passive voice is acceptable when it satisfies "light-before-heavy" principle

**Cognitive gain**: Readers connect new information to existing mental model smoothly

---

#### Rule 5: Avoid Ambiguity
**Cognitive Goal**: Prevent garden-path misreadings
**Pinker Concept**: Garden paths; Unwanted attachments

**Specific Instructions**:
- **Restore omitted markers**: If deleting *that*, *which*, or *who* causes temporary misparse, restore them
  - ❌ "The researcher the participants trusted designed the task" (garden path)
  - ✅ "The researcher **whom** the participants trusted designed the task"
- **Fix modifier attachment**: Check if prepositional phrases or modifiers attach to wrong nearby word
  - ❌ "We tested participants with the new paradigm in the lab" (paradigm in the lab? or testing in the lab?)
  - ✅ "In the lab, we tested participants with the new paradigm" (prepose location to separate)

**Cognitive gain**: No backtracking or re-parsing required

---

#### Rule 6: Check Grammatical Consistency
**Cognitive Goal**: Ensure structural coherence
**Pinker Concept**: Tree-thinking; Structural parallelism

**Specific Instructions**:
- **Parallel structures**: In coordinations (*both...and*, *either...or*), ensure phrases match grammatically
  - ❌ "Both analyzing the data and to write the manuscript"
  - ✅ "Both analyzing the data and writing the manuscript"
- **Agreement errors**: Check subject-verb agreement, especially when subject and verb are separated
  - ❌ "The analysis of multiple experiments suggest..."
  - ✅ "The analysis of multiple experiments suggests..."

**Cognitive gain**: Predictable structure; no processing hiccups

---

### STAGE 3: Coherence Optimization (Pinker Chapter 5)

Apply **7 coherence principles** to improve discourse-level flow:

#### Principle 1: Establish Topic and Point
**Cognitive Goal**: Orient reader immediately
**Pinker Concept**: "Don't bury the lede"; Reveal topic and point upfront

**Specific Instructions**:
- Review opening paragraph/section
- Ensure **topic** (what it's about) is stated in first 1-2 sentences
- Ensure **point** (why it matters, what argument you're making) appears early
- If topic is buried in paragraph 3, rewrite opening

**Example**:
- ❌ Buried: "Many factors influence comprehension. Prior research has examined various aspects. Our study focuses on classifiers."
- ✅ Clear: "This study examines how Chinese classifiers influence mental simulation during comprehension."

**Cognitive gain**: Reader builds correct mental framework from the start

---

#### Principle 2: Maintain Information Flow
**Cognitive Goal**: Create coherent "arc" across sentences
**Pinker Concept**: Topic strings; Given-new ordering

**Specific Instructions**:
- Check consecutive sentences: Do their grammatical subjects (sentence topics) relate to the discourse topic?
- Create **topic strings**: Maintain consistent subject across related sentences
- Apply **given-new**: Each sentence starts with known information, ends with new information (which becomes "given" for next sentence)
- If topic shifts, do so at paragraph boundaries, not mid-paragraph

**Example**:
- ❌ Broken arc: "Classifiers specify shape. Mental simulation involves visual imagery. Participants responded faster."
- ✅ Coherent arc: "Classifiers specify shape features. These features activate mental simulation. This simulation process speeds comprehension."

**Cognitive gain**: Smooth cognitive transitions; reader never loses thread

---

#### Principle 3: Track Participants and Entities
**Cognitive Goal**: Help readers maintain mental cast of characters
**Pinker Concept**: Referring systems; Avoid elegant variation (synonymomania)

**Specific Instructions**:
- **First mention**: Use indefinite article (*a mechanism*, *an effect*)
- **Subsequent mentions**: Use definite article (*the mechanism*, *the effect*) or pronoun (*it*, *this*)
- **Avoid arbitrary synonyms**: Don't switch "classifier" → "linguistic marker" → "form class indicator" randomly
  - Readers may think these are different entities
  - Use same term consistently (variation for style ≠ clarity)

**Example**:
- ❌ Confusing: "We used a sentence-picture task. The linguistic verification paradigm showed effects. This comprehension measure revealed..."
- ✅ Clear: "We used a sentence-picture verification task. The task showed effects. This task revealed..."

**Cognitive gain**: No confusion about referents; stable mental model

---

#### Principle 4: Clarify Logical Relations
**Cognitive Goal**: Explicit signposting of logic
**Pinker Concept**: Coherence connectives; Hume's three relations (resemblance, contiguity, cause-effect)

**Specific Instructions**:
- Review sentence transitions
- If logical relationship is unclear, add appropriate connective:
  - **Cause/effect**: *because*, *therefore*, *so*, *thus*, *consequently*
  - **Contrast**: *however*, *but*, *yet*, *nevertheless*, *in contrast*
  - **Addition**: *moreover*, *furthermore*, *additionally*, *also*
  - **Example**: *for instance*, *for example*, *specifically*
  - **Exception**: *except*, *although*, *despite*
- **Pinker's rule**: "When in doubt, connect"

**Example**:
- ❌ Unclear: "Classifiers specify shape. Readers activate mental imagery."
- ✅ Clear: "Classifiers specify shape. **Consequently**, readers activate mental imagery."

**Cognitive gain**: Reduced inference burden; explicit argument structure

---

#### Principle 5: Optimize Comparison and Contrast
**Cognitive Goal**: Make differences/similarities transparent
**Pinker Concept**: Single-variable principle; Structural parallelism

**Specific Instructions**:
- When comparing/contrasting, **force parallel syntax**
- Change only ONE variable at a time (don't vary both wording AND structure)
- Use same grammatical frame for both sides of comparison

**Example**:
- ❌ Non-parallel: "Appropriate classifiers facilitated comprehension, while the general classifier showed no effect on response time."
- ✅ Parallel: "Appropriate classifiers facilitated comprehension, while general classifiers showed no effect."
  - (Both: [Classifier type] + [verb] + [object])

**Cognitive gain**: Clean contrast; no confusion about what differs

---

#### Principle 6: Handle Abstract Reference
**Cognitive Goal**: Manage mentions of events and situations
**Pinker Concept**: Nominalization as pseudo-pronoun

**Specific Instructions**:
- **First mention of event**: Use verb form (shows action)
  - ✅ "Participants **verified** whether the picture matched the sentence."
- **Subsequent reference to same event**: Allow nominalization (acts like pronoun)
  - ✅ "This **verification process** took an average of 800ms."
- Avoid nominalization on first mention (zombie nouns), but accept it for coherence in later mentions

**Cognitive gain**: Avoid repetition while maintaining clarity

---

#### Principle 7: Check Author Attitude
**Cognitive Goal**: Focus on world, not on discourse itself
**Pinker Concept**: Minimize metadiscourse and hedging

**Specific Instructions**:
- **Remove excessive metadiscourse**: Delete phrases about the text itself
  - ❌ "In this section I will discuss..."
  - ✅ [Just start discussing]
  - ❌ "It is important to note that..."
  - ✅ [State the important point directly]
- **Remove unnecessary hedges**: Cut weak qualifiers unless statistically necessary
  - ❌ "This *virtually* suggests that..."
  - ✅ "This suggests that..."
  - ❌ "I would argue that X is important"
  - ✅ "X is important"
- **Exception**: Keep hedges for genuine uncertainty or statistical qualifications ("may," "appears to" when appropriate)

**Cognitive gain**: Direct, confident prose; reader sees ideas, not author's hand-wringing

---

## Output Format

Provide results in this structure:

```markdown
# P-CSO Workflow Results

## Stage 1: Draft Scaffold (if applicable)

[Organized focal statements and paragraph structure]

⚠️ **SCAFFOLD ONLY**: User must develop this in their own words.

---

## Stage 2 & 3: Optimized Revision

### Original Text
[User's input text or developed scaffold]

---

### Optimized Text (P-CSO Applied)
[Revised version with syntax and coherence improvements]

---

## Cognitive Diagnostics: Pinker Framework Analysis

### Change 1: [Issue Addressed]
- **Original sentence**: "[Exact quote]"
- **Cognitive burden**: [How this affected readers - e.g., "Center-embedding forced readers to hold subject in memory while processing nested clause"]
- **Pinker principle applied**: [Specific concept - e.g., "Rule 2: Avoid multiply center-embedded sentences"]
- **Revision**: "[New sentence]"
- **Cognitive gain**: [How this helps - e.g., "Linear parsing; no memory load"]

### Change 2: [Issue Addressed]
[Repeat structure]

### Change 3: [Issue Addressed]
[Repeat structure]

### Change 4: [Issue Addressed]
[Repeat structure]

### Change 5: [Issue Addressed]
[Repeat structure]

[Continue for ALL major changes - minimum 5, more if substantial revision]

---

## Summary of Cognitive Improvements

**Syntax optimizations (Chapter 4)**:
- [List applied rules and frequency]

**Coherence enhancements (Chapter 5)**:
- [List applied principles and frequency]

**Overall impact**: [Brief assessment of readability improvement]

---

## Next Steps

- [ ] Review all changes and adjust to your voice/intent
- [ ] Verify technical accuracy and citations
- [ ] Check if additional context needed for unfamiliar readers
- [ ] Use `/english-editing` skill for final grammar polish
- [ ] Consider field-specific style requirements (APA, journal guidelines)
```

---

## Important Notes

### Scaffolding Ethics
When generating draft scaffolds:
- Always mark as "SCAFFOLD ONLY"
- Remind user to rewrite in own words
- Emphasize academic integrity

### Revision Philosophy
- **Goal**: Cognitive clarity, NOT stylistic homogenization
- **Preserve**: Author's voice, technical terminology, content
- **Change**: Structure, flow, syntax that creates cognitive burden

### LaTeX Formatting for Technical Documents

When working with R Markdown (.Rmd), LaTeX (.tex), or academic manuscripts:

**Always convert to LaTeX format**:
- Mathematical notation: `$N = 120$`, `$p < .05$`, `$\alpha = 0.05$`
- Statistical values: `$M = 88.7$`, `$SD = 6.8$`, `$BF_{10} = 39.82$`
- Subscripts/superscripts: `$BF_{10}$` NOT Unicode BF₁₀
- Inequalities: `$>$`, `$<$`, `$\geq$`, `$\leq$`, `$\neq$`
- Confidence intervals: `95% CI $[-0.05, 0.01]$`
- Factorial designs: `$3 \times 2$` NOT 3×2 (Unicode)
- Greek letters: `$\beta$`, `$\alpha$`, `$\mu$`, `$\sigma$`, `$\chi^2$`
- Equations: `$MSE(A) > MSE(G) = MSE(No)$`

**Why LaTeX**:
- Editable in any text editor (no special characters)
- Renders correctly in R Markdown → Word/PDF/HTML
- Version control friendly (Git diffs are readable)
- Copy-paste safe (no encoding issues)
- Cross-platform compatible

**When user provides Unicode symbols** (e.g., ×, ≈, ≥, subscripts like ₁₀):
- Automatically convert to LaTeX equivalents
- At end of revision, offer: "I've converted all notation to LaTeX format for editability. Would you like me to provide LaTeX-corrected versions of earlier sections?"

**Examples of conversion**:
- Before: "3×2 factorial design with N=120, BF₁₀ > 10"
- After: "$3 \times 2$ factorial design with $N=120$, $BF_{10} > 10$"

**Journal-specific notation**:
- Preserve journal requirements (e.g., APA uses italics for statistics: *M*, *SD*, *p*)
- Combine LaTeX with markdown: *M* `= 88.7` or `$M = 88.7$` (both acceptable)
- Ask user if unsure: "Does your journal require specific statistical notation formatting?"

### When to Apply Each Stage

**Use full 3-stage workflow when**:
- Starting from scattered notes
- Text has both syntax AND coherence issues
- User requests comprehensive optimization

**Use Stage 2+3 only (skip Stage 1) when**:
- User provides complete draft
- Focus is on revising existing text

**Use Stage 1 only when**:
- User has notes but prefers to draft manually before revision
- Just needs organizational help

---

## Quick Reference: 13 Optimization Rules

### Chapter 4: Syntax (6 Rules)
1. ✅ Light-before-heavy (right-branching)
2. ✅ Avoid center-embedding
3. ✅ Omit needless words
4. ✅ Given-before-new
5. ✅ Prevent garden paths
6. ✅ Maintain parallelism

### Chapter 5: Coherence (7 Principles)
1. ✅ Reveal topic & point early
2. ✅ Maintain topic strings
3. ✅ Track entities properly
4. ✅ Use coherence connectives
5. ✅ Parallel comparisons
6. ✅ Nominalize events (2nd+ mention)
7. ✅ Minimize metadiscourse

---

## Integration with Other Skills

**Works with**:
- **Before this skill**: User organizes initial notes
- **After this skill**:
  - `/english-editing` for grammar polish
  - `/notes-to-manuscript` for simple scaffolding (if not using full pipeline)
  - `/pinker-syntax` or `/pinker-coherence` for targeted follow-up

**Workflow position**: This is the **core comprehensive skill**; others are either preparatory or supplementary.

---

**Skill Version**: 1.0
**Framework**: Pinker's "The Sense of Style" - Chapters 4 & 5
**Optimized for**: Academic research writing, particularly psychology, linguistics, cognitive science
**Output**: Cognitively optimized text with detailed diagnostic explanations
