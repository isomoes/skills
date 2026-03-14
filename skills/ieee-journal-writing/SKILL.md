---
name: ieee-journal-writing
description: Revises and strengthens IEEE-style journal writing for academic papers, especially when the user is drafting or polishing LaTeX sections, improving technical prose, aligning with reviewer expectations, or asking for more formal, concise, publication-ready language. Use this skill whenever the task involves rewriting abstract, introduction, methods, results, discussion, conclusion, captions, or responses for an engineering or scientific paper, even if the user does not explicitly mention IEEE.
---

# IEEE Journal Writing

Help the user turn rough academic prose into clear, publication-ready IEEE-style writing without changing the technical meaning.

## Goals

- Preserve the author's claims, evidence, and intended emphasis.
- Improve clarity, rigor, concision, and logical flow.
- Prefer neutral, evidence-driven phrasing over promotional language.
- Keep the result LaTeX-ready when the user is working in `.tex` files.

## When Working

First identify what kind of help the user wants:

- polish a sentence or paragraph
- rewrite a full section
- align a manuscript with IEEE tone
- improve structure and flow
- tighten claims for technical accuracy
- make LaTeX prose cleaner and more consistent

Match the depth of the response to the request. If the user asks for a direct rewrite, give the rewrite first. If the user asks for critique, explain the issues first and then propose fixes.

## Core Writing Principles

### Preserve Meaning

Do not introduce unsupported claims, new results, fake citations, or stronger novelty language than the source justifies. If the draft is ambiguous, resolve it conservatively.

### Prefer Clarity Over Formulaic Stiffness

Aim for formal academic tone, but do not make the prose robotic. Use passive voice when it improves objectivity or aligns with the surrounding text, but prefer whichever construction is clearer and more compact.

Prefer moderate sentence length. If a sentence starts carrying method, result, implication, and comparison all at once, split it into two tighter sentences.

### One Paragraph, One Job

Give each paragraph a clear function. Start with the main point, develop it with evidence or explanation, and remove sentences that repeat nearby material.

### Keep Claims Proportional

Use measured language. Replace hype, certainty inflation, and vague praise with concrete statements about method, data, comparisons, limits, and practical implications.

### Favor Specific Technical Language

Replace filler phrases and abstract wording with direct verbs, concrete nouns, and, when available, quantities or comparisons.

## IEEE-Oriented Style Guidance

- Define acronyms on first use and keep terminology consistent afterward.
- Prefer precise, neutral statements over marketing language.
- Present methods and results objectively.
- Emphasize reproducibility, methodological detail, and evidence-backed conclusions.
- Avoid first-person pronouns by default, including `we`, unless the user explicitly wants to preserve an existing first-person house style.
- Keep sentences compact. Split overloaded sentences that try to carry multiple claims.

## Flow Between Sentences

Make adjacent sentences connect cleanly.

- Let the first sentence establish context or the main claim.
- Let the next sentence narrow to method, evidence, or limitation.
- Avoid choppy sentence-to-sentence jumps where each sentence feels isolated.
- When revising abstracts and introductions, prefer a clear progression such as problem -> method -> result -> implication.

## Structure Checks

When revising a section, look for these issues:

1. missing problem statement or motivation
2. weak transitions between paragraphs
3. repeated claims across sections
4. method descriptions that are too vague to follow
5. results stated without context, comparison, or takeaway
6. conclusions that overstate significance

Fix the issue in the rewrite rather than merely pointing it out, unless the user asked for review only.

## LaTeX Conventions

If the user is editing a LaTeX manuscript:

- Preserve LaTeX commands, labels, citations, math, and cross-references.
- Use `\cite{}` keys already present in the manuscript rather than inventing new references.
- Keep `\ref{}` and `\label{}` usage consistent.
- Do not break equations, macros, or environments during rewriting.
- Return text that can be pasted back into the `.tex` source with minimal cleanup.

## Response Patterns

### Small Rewrite Requests

Return:

1. the revised text
2. a short note on what improved, only if useful

If a single-sentence rewrite becomes long or crowded, prefer two shorter sentences with a tighter logical link.

Unless the user asks for labels, avoid adding headings like `Revised text:` before a short rewrite.

### Section-Level Rewrites

Return:

1. a polished LaTeX-ready section
2. brief notes on major structural or stylistic changes
3. any factual gaps or citation gaps that still need author input

### Review-Only Requests

Return:

1. the main writing issues
2. concrete recommended edits
3. optional sample rewrites for the most important passages

## Editing Heuristics

During revision, actively look for and remove patterns such as:

- "it should be noted that"
- "it is worth mentioning that"
- empty novelty claims like "very innovative" or "highly effective"
- repeated restatement of the same contribution
- broad claims not tied to data, experiments, or citations
- unnecessary first-person wording such as `we propose`, `we develop`, or `we show` when the sentence works better as an impersonal construction

Also check whether adjacent sentences can be merged for flow or split for readability.

## Technical Content Safeguards

- Keep enough methodological detail for a knowledgeable reader to follow the work.
- Do not rewrite away important assumptions, limits, or implementation details.
- If a claim appears unsupported, soften the wording rather than pretending the evidence exists.
- If terminology conflicts across the draft, normalize it to one consistent term unless the distinction is meaningful.

## Output Quality Bar

Before finishing, make sure the revision is:

- faithful to the source meaning
- more concise than the original unless detail was missing
- easier to read sentence by sentence
- consistent in terminology and tense
- suitable for an IEEE-style engineering paper

## Example Behaviors

**Input:** "Rewrite this abstract to sound more like an IEEE journal paper, but keep the contribution exactly the same."

**Output:** Provide a tighter abstract with neutral claims, clearer problem-method-result flow, and no added technical content.

**Input:** "Please edit this LaTeX introduction and keep all citations and refs untouched."

**Output:** Return revised LaTeX prose that preserves `\cite{}` and `\ref{}` commands while improving flow and concision.
