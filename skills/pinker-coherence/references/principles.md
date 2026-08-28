# Pinker Coherence — Full Principle Definitions and Operational Detail

Reference companion to `SKILL.md`. Read this before drafting a revision; consult `examples.md` for calibration on hard cases.

---

## Negative Constraints — Scan First

Before applying the principles, scan for these patterns. Any match is a violation to fix:

1. **No subject drift** — do not shift the grammatical subject from sentence to sentence without warrant. The subject position is the reader's spotlight; moving it arbitrarily produces confusion even when every individual sentence is clear.
2. **No buried lede** — do not discover the topic and point only in the last sentence. State the governing topic at the outset.
3. **No synonymomania in comparisons** — do not use different words for the same entity when comparing or contrasting two things. Hold all language constant except the one word that marks the actual difference (Rule of One Variable).
4. **No ambiguous connective** — do not use "while" when you mean contrast (it also means temporal overlap); do not use "also" when you mean contrast (it signals similarity). Choose the precise connective The same fault occurs with "and" used for contrast, cause or concession; sentence-level conjunction load is `/pinker-syntax` Rule 11.
5. **No redundant connectives** — do not write "the reason is because"; "reason" already encodes explanation. Use "the reason is that."
6. **No disproportionate space** — do not devote 90% of a passage to opposing the main claim while only 10% argues for it. Proportion of verbiage signals proportion of importance.
7. **No unnamed thematic jumps** — do not move between thematic concepts without naming the connecting thread. Label each theme explicitly; use a cluster of related terms within each.
8. **No negating an unfamiliar proposition** — do not negate a claim the reader does not yet hold. First establish it as a plausible thought, then knock it down.

---

## Principle 1: Establish Topic and Point

**Pinker Concept**: Don't bury the lede; reveal topic and point upfront

**Problem**: Readers forced to read several sentences before understanding what the text is about or why it matters.

**Solution**: State topic (subject matter) and point (argument/purpose) in opening sentences.

**How to Apply**:
1. Review first paragraph or section opening
2. Ask: Is the **topic** (what it's about) stated in first 1-2 sentences?
3. Ask: Is the **point** (why it matters, what you're arguing) clear early?
4. If topic appears in sentence 3+, rewrite opening

**Cognitive gain**: Readers build correct mental framework from the start; no wasted processing

---

## Principle 2: Maintain Information Flow

**Pinker Concept**: Topic strings; given-new ordering; coherence arcs

**Problem**: Sentence topics jump around randomly, breaking the cognitive thread readers are following.

**Solution**: Create **coherent arcs** by maintaining consistent topic strings and given-new progression.

**How to Apply**:

**A. Check Topic Strings**
- Examine consecutive sentences' grammatical subjects
- Do they relate to the same discourse topic?
- If topic shifts, does it happen at paragraph boundary (not mid-paragraph)?

**B. Apply Given-New Ordering**
- Each sentence should start with "given" (known from prior context)
- Each sentence should end with "new" (information being introduced)
- The "new" information becomes "given" for the next sentence

**Cognitive gain**: Smooth transitions; reader never loses the thread

---

## Principle 3: Track Participants and Entities

**Pinker Concept**: Referring systems; avoid elegant variation (synonymomania)

**Problem**: Arbitrary synonym switching makes readers unsure if you're referring to the same thing or introducing new entities.

**Solution**: Use consistent referring patterns; avoid "elegant variation" that sacrifices clarity.

**How to Apply**:

**A. Follow Referring System Rules**
- **First mention**: Indefinite article + full noun phrase — e.g. "We used *a sentence-picture verification task*"
- **Second+ mention**: Definite article or pronoun — e.g. "*The task* showed significant effects" / "*It* revealed differences between conditions"

**B. Avoid Synonymomania**
Don't randomly vary terms for the same entity across mentions.

**Exception**: Vary for clarity when necessary, but not for mere stylistic "elegance"

**Cognitive gain**: No confusion about what you're referring to; stable mental model of entities

**C. Keep the Referent Available**

A referring expression works only if the reader can still reach its referent. Three failures, all from drafts a domain expert rejected:

**Long-distance abstract anaphora.** "The order above" pointed back across eight paragraphs. No reader carries an abstraction that far. Restate the condition where it is used, and repeat the noun on purpose:

- Before: "That is a question about the consolidation window, and the condition set out above applies to it."
- After: "That is a question about the consolidation window, and a study reaches the consolidation window only when its retention interval spans a full night of sleep."

The repetition of "consolidation window" is the fix, not a fault. Repeating the noun is the standard remedy for an overloaded pronoun or demonstrative, and it outranks the ban on repetition in B.

**Stacked abstract anaphors.** "This line" (pointing at "sleep-dependent evidence") followed by "agreement" (a bare nominalization) sent the reader back twice inside one sentence. Replace both with the full noun phrase: "They report less convergence among the sleep-dependent studies than among any others in their review."

**Closing on a pronoun.** A sentence that ends on a pronoun subject leaves the reader holding a variable: "...so an investigation of memory settles the retention interval before it asks about encoding depth." Close on the noun: "...so the retention interval is the prior question in any consolidation study."

**D. Do Not Use a Term Before the Reader Owns the Concept**

Naming a concept is given-before-new at document scale (Principle 2). Check where the concept is established relative to where the term is used. If the reader has not been given it yet, state the content instead of naming it. "The two stages are ordered" names a relation the reader acquires only later in the same section; the sentence has to carry the relation itself: "A study reaches the consolidation stage only when its retention interval spans a full night of sleep."

**Cognitive gain**: The reader never stops to search backwards for what a word points at

---

## Principle 4: Clarify Logical Relations

**Pinker Concept**: Coherence connectives; Hume's three relations (resemblance, contiguity, cause/effect)

**Problem**: Readers must infer logical relationships between sentences, creating unnecessary cognitive burden.

**Solution**: Make logic explicit with coherence connectives. Pinker's rule: "When in doubt, connect."

**How to Apply**:
1. Review sentence transitions
2. Identify logical relationship: cause/effect? contrast? addition/continuation? example/elaboration? exception?
3. If relationship isn't obvious, add appropriate connective

**Connective Inventory**:
- **Cause/Effect**: *because*, *therefore*, *thus*, *so*, *consequently*, *as a result*
- **Contrast**: *however*, *but*, *yet*, *nevertheless*, *in contrast*, *on the other hand*
- **Addition**: *moreover*, *furthermore*, *additionally*, *also*, *in addition*
- **Example**: *for instance*, *for example*, *specifically*, *such as*
- **Elaboration**: *that is*, *in other words*, *namely*
- **Exception**: *except*, *although*, *despite*, *even though*
- **Sequence**: *first*, *second*, *finally*, *then*, *next*

**Cognitive gain**: Reduced inference burden; argument structure is transparent

---

## Principle 5: Optimize Comparison and Contrast

**Pinker Concept**: Single-variable principle; structural parallelism

**Problem**: Varying both wording AND structure in comparisons confuses readers about what actually differs.

**Solution**: Use identical syntactic frames; change ONLY the contrasting element (single variable).

**How to Apply**:
1. Identify comparisons/contrasts in text
2. Extract the syntactic frame
3. Ensure both sides use the SAME frame
4. Change ONLY the element being contrasted

**Cognitive gain**: Crystal-clear contrasts; no confusion about what differs

---

## Principle 6: Handle Abstract Reference (Events and Situations)

**Pinker Concept**: Nominalization as pseudo-pronoun

**Problem**: How to refer back to actions or events without repetition?

**Solution**: **First mention = verb** (shows action); **later mentions = nominalization** (acts as pronoun for that event).

**How to Apply**:

**A. First Mention: Use Verb Form** — show the action dynamically, e.g. "Participants **verified** whether the picture matched the sentence."

**B. Subsequent Reference: Allow Nominalization** — now you can nominalize to refer back (like a pronoun), e.g. "This **verification process** took an average of 800ms."

**Important**: Don't nominalize on first mention (creates a "zombie noun"), e.g. avoid "The **verification** of picture-sentence matching was performed by participants" — prefer "Participants **verified** that pictures matched sentences."

**Cognitive gain**: Avoid repetition while maintaining clarity; events referenced like entities

---

## Principle 7: Check Author Attitude (Minimize Metadiscourse)

**Pinker Concept**: Classic style as "window to world"; avoid metadiscourse and excessive hedging

**Problem**: Excessive commentary about the text itself distracts from content; unnecessary hedging weakens prose.

**Solution**: Focus on the world/ideas being shown; remove the author's visible hand.

**How to Apply**:

**A. Remove Metadiscourse** — delete phrases that discuss the text rather than the topic:
- "In this section, I will discuss..." → just start discussing
- "It is important to note that..." → state the important point directly
- "As mentioned above..." → rely on coherent flow, or briefly restate if necessary
- "The purpose of this study is to..." → "This study examines..." / "We tested..."

**B. Remove Unnecessary Hedging** — cut weak qualifiers unless statistically necessary:
- "This *virtually* suggests that..." → "This suggests that..."
- "It *seems* that X is important" → "X is important"
- "I would argue that..." → just make the argument
- "*Somewhat* faster response times" → "Faster response times" (with effect size if needed)

**C. Name Every Open Question**

An open question earns its place only when the sentence says what the question is. A
promise that something is unresolved, with the content withheld, gives the reader nothing
to hold.

- "One question stays open at this point." → names nothing. Either state the question or cut it.
- "The test also carries an unsettled question." → names nothing.
- "Whether the numeral variant occurs often enough to support type counts is an open question." → keep. The question is in the sentence.

**Test**: could the reader restate the question after reading the sentence? If not, the
sentence is a placeholder.

**Exception — keep hedges when genuinely needed**:
- Statistical uncertainty: "The effect *may* generalize to other languages" (when data doesn't confirm)
- Appropriate qualifiers: "Results *suggest* causation" (when correlational)
- Scope limitations: "This *appears* to be the first study..." (when literature search incomplete)

**D. Cut Study-Note Register**

Metadiscourse also appears in forms that carry no canned phrase, and those are the ones that survive every other check. A draft can pass all of `/pinker-syntax` and principles 1 through 7C and still be rejected for reading as a study note rather than an article. The test, applied sentence by sentence: **does this sentence advance the argument, or does it only label the argument?** Cut every sentence that only labels.

Five markers, all taken from real rejected drafts:

1. **Announcing what the paragraph is about to do.** "The two stages are ordered." / "They did not assemble the word list casually." / "Two consequences follow." / "Free recall is one case inside the battery." State the consequence and delete the announcement: "A study reaches the consolidation stage only when its retention interval spans a full night of sleep, so the retention interval is the prior question in any consolidation study."

2. **Opening a paragraph on a cross-reference.** Four of five paragraphs in one draft opened with `Section \@ref(...)`. A filing location is not a claim. Open on the claim and move the reference mid-paragraph or to the end: "A study takes its word list from a published norming set or from an earlier experiment, and neither source records sleep history."

3. **Authorial gesture and elliptical emphasis.** "The retention interval does." / "and the reviewers say as much" / "that independence is the point" / "Stating it is what the criterion adds" / "show why". Each one points at the argument instead of making it. Delete it and let the next sentence do the work.

4. **Reporting a stance instead of making the claim.** "We read this record as convergent" / "they name semantic control as the reason" / "We suggest that". Make the claim.

5. **Runs of short flat observations.** Three or four flat statements circling a principle read as notes toward a paragraph. Write the one sentence that states the principle.

End a paragraph on a claim, not on a pointer to another section.

**Do not overcorrect.** A cross-reference carrying information the reader needs is not a fault, and neither is a reason-giving structural sentence (see 8B).

**Cognitive gain**: Reader sees ideas clearly, not author's uncertainty; the page argues instead of annotating, and reads as an article rather than as working notes


---

## Principle 8: Agency in Subject Position

**Pinker Concept**: Classic style shows a person doing something; abstractions that displace agents produce the flat, authorless register readers describe as "machine-written"

**Problem**: An abstraction occupies the subject slot and takes a verb only a human can perform. Principle 2 does not catch this, because a consistent topic string of abstractions passes a drift check. Principle 6 does not catch it either, because the nominalization is grammatical and may be on a later mention.

**Why it needs its own check**: the fault sits between the two existing skills. `/pinker-syntax` Rule 3 inspects one sentence at a time and sees a well-formed clause. `/pinker-coherence` Principle 2 inspects the sequence of subjects and sees a stable topic. Neither asks whether the subject is capable of the action.

### How to Apply

**Step 1 — Extract.** List the grammatical subject of every sentence in the passage. Do
this explicitly; do not scan by impression.

**Step 2 — Mark animacy.** Tag each subject animate (a person, a named author, a research
group) or inanimate.

**Step 3 — Classify every inanimate subject into one of three types.** Run both tests in
order.

*Test A, the person test*: could a human be named as the doer, and would the sentence be
truer for naming them?

*Test B, the document test*: is the subject a text — a section, this article, a framework,
a table, a body of research — performing an act that only a claim or an author can perform?

| Test A | Test B | Type | Repair |
|---|---|---|---|
| yes | — | **hidden person** | name the person |
| no | yes | **document as agent** | state the claim, not its filing location |
| no | no | **legitimate abstraction** | leave it |

**Step 4 — Report the ratio per paragraph**, split by type. Flag any paragraph where the
first two types together outnumber the third.

### 8A: Hidden person

The subject is an abstraction standing in for people who acted.

| Pattern | Hidden agent |
|---|---|
| "The study found / The paper argues / The reviews agree" | the authors |
| "The data suggest" (when the claim is an inference) | the analyst |
| "This index was adopted" | whoever adopted it |
| "The framework requires X" | whoever adopts the framework |
| "Research has examined" | researchers |

### 8B: Document as agent

The subject is a text doing what only a claim or an author can do. Naming a person does
not repair these: "Table 1 shows" does not improve as "Chen shows", because the table is
the evidence. State what is true instead of where it sits.

- "The sections that follow establish that the difference is consequential." → state the claim.
- "Two consequences follow for the sections in between." → state the consequences.
- "Sleep does, and the sections after this one measure it." → "Sleep does, and that gain is what the consolidation index measures."

**Two kinds of text-as-subject are not faults and must be kept.**

*A cross-reference that tells the reader where a definition lives.* "Section \@ref(criterion)
states the value that draws the boundary" is information the reader needs, not a filing
location.

*A structural sentence that gives a reason.* "A formal criterion has no claim on a
cognitive scientist's attention until the cost of working without it is visible" justifies
an ordering decision. "That criterion is the subject of the next section" only announces
one.

The failing cases are those that report the document's plan while withholding the content:
the reader learns where the writer put something instead of what is true.

### The discrimination test is the whole principle

Applied mechanically, an animacy rule destroys good prose. A passage that analyses how an instrument behaves *should* have the instrument as its subject. Never revise an inanimate subject without running Step 3 on it.

**Common displaced agents in academic prose**

| Pattern | Hidden agent |
|---|---|
| "The study found / The paper argues / The reviews agree" | the authors |
| "The data suggest" (when the claim is an inference) | the analyst |
| "This index was adopted" | whoever adopted it |
| "The framework requires X" | whoever adopts the framework |
| "Research has examined" | researchers |

**Legitimate inanimate subjects**

| Pattern | Why it stays |
|---|---|
| "The paradigm is blind to the distinction by construction" | a structural property of the paradigm |
| "A retention interval is a duration in the experimental design" | a definitional fact |
| "The contrast produced no effect" | a result, not an act |
| "Section 4 states the framework" | a document locating its own content |

**Cognitive gain**: the reader sees who is doing what; the critique acquires a target; the prose stops reading as authorless.

---

## Self-Review Checklist

After completing all revisions, run this checklist **before finalizing output**. If any check fails, fix it.

- [ ] No sentence has a subject that is unconnected to the subject of the previous sentence without a warranted transition
- [ ] Topic and point are stated in the first 1–2 sentences of each paragraph
- [ ] The same entity is referred to with the same term throughout any comparison or contrast
- [ ] Every connective precisely matches the logical relation it signals (contrast → "however/in contrast"; elaboration → "moreover/furthermore"; cause → "therefore/consequently")
- [ ] No "while" used for contrast; no "also" used for contrast
- [ ] Space devoted to each claim is proportionate to its importance in the argument
- [ ] Every open question is named in the sentence that raises it
- [ ] Every sentence advances the argument; no sentence only labels it (7D)
- [ ] No paragraph opens on a cross-reference, and none ends on a pointer to another section
- [ ] Every demonstrative and pronoun has a referent the reader can still reach; long-distance abstractions are restated in place
- [ ] No sentence closes on a pronoun where a noun would close it
- [ ] No term is used before the section that gives the reader its concept
- [ ] Every thematic jump is labeled — the connecting thread is named, not assumed
- [ ] Every sentence subject has been extracted and marked animate or inanimate
- [ ] Every inanimate subject has been classified by Test A and Test B, not by impression
- [ ] No cross-reference or reason-giving structural sentence was removed as an 8B fault
- [ ] No legitimate abstraction was forced into an agent frame
- [ ] Original meaning and evidence are fully preserved — no claims added or removed

This step catches the most common failure mode: fixing one coherence problem while inadvertently introducing another.

---

## Output Format

```markdown
# Pinker Coherence Optimization Results

## Original Text
[User's input text]

---

## Optimized Text
[Revised version with coherence improvements]

---

## Coherence Diagnostics (Chapter 5 Framework)

### Issue 1: [Specific Problem]
- **Principle violated**: [Which of 7 principles]
- **Original passage**: "[Quote]"
- **Cognitive burden**: [How this affected readers - e.g., "Topic shift mid-paragraph broke coherence arc"]
- **Fix applied**: "[Revised passage]"
- **Cognitive gain**: [How this helps - e.g., "Consistent topic string maintains reader's mental model"]

### Issue 2: [Specific Problem]
[Repeat structure]

[Continue for every issue actually found. There is no minimum. Clean text yields no entries. Never manufacture a finding to reach a count. A candidate inspected and rejected may be recorded as a no-violation entry with its reason.]

---

## Summary

**Principles applied**:
- Principle 1 (Topic/Point): [X instances]
- Principle 2 (Info flow): [X instances]
- Principle 3 (Entity tracking): [X instances]
- Principle 4 (Logic connectives): [X instances]
- Principle 5 (Comparisons): [X instances]
- Principle 6 (Abstract reference): [X instances]
- Principle 7 (Metadiscourse): [X instances]
- Principle 8 (Agency in subject position): [X hidden persons named, X documents restated, X legitimate abstractions kept]

**Overall impact**: [Brief assessment - e.g., "Established clear coherence arcs; added 8 logical connectives; eliminated 5 metadiscourse phrases"]

---

## Next Steps
- [ ] Review changes for content accuracy
- [ ] Verify logical flow matches your intended argument
- [ ] Use `/pinker-syntax` if sentence complexity needs work
- [ ] Use `/english-editing` for final grammar polish
```
