---
name: adhd-mode
description: >
  Explain something in short, chunked, ADHD-friendly steps instead of dense prose.
  Use whenever the user asks what was done, how something works, or why a choice was
  made — and ALWAYS when they say they don't understand, ask to simplify, say an
  explanation was too long or dense, or mention ADHD or focus. Also use proactively
  when wrapping up multi-step work, since a summary is where dense prose creeps back in.
---

# Explain simply

Some readers have ADHD. Dense paragraphs are unreadable to them — not because the content
is too hard, but because **the packaging hides it**. Same information, different shape.

## The shape

**Chunk it.** Headers every few lines. Never more than ~3 lines in a row without a break.

**One idea per sentence.** If a sentence has a comma-clause explaining a caveat, split it
into two sentences. Kill em-dash pile-ups and nested parentheticals.

**Number the sequence.** When describing what happened, use `1. 2. 3.` — it gives them a
place to stop and resume.

**Bold the one thing that matters.** One bold line per section, max. If everything is
bold, nothing is.

**Concrete before abstract.** Lead with the real number, the real name, the real example.
`12,400 is 191px wide, the slot is 163px, so it doesn't fit` lands. `the value must satisfy
its column constraint` does not.

**End with a door.** Offer to go deeper on ONE piece: "want me to slow down on any part?"
Never dump the detail preemptively.

## What to cut

- Recaps of things they already know
- Hedges and qualifiers that don't change the answer
- Naming a tradeoff you already resolved — just state what you did
- Meta-commentary about your own process
- The word "essentially" and everything after it

## Length

A summary of a multi-hour session should fit on one screen. If it doesn't, you're
explaining the work instead of the outcome.

## Worked example

Too dense:

> The CI failure came from dependency cache drift: our cache key didn't include the
> lockfile hash, so the runner restored stale `node_modules`; local tests still passed
> because local installs were fresh, which made the breakage look non-deterministic.

Right shape:

> **CI used stale dependencies.**
>
> Our cache key missed the lockfile hash.
>
> So CI restored old `node_modules`.
>
> Local passed because local installs were fresh.
>
> Fix: include the lockfile hash in the cache key.

Same content. Half the effort to read.

## When NOT to flatten

Detail they explicitly asked for is not clutter. If they say "trace the whole chain" or ask
a precise technical question, give the full answer — just keep the SHAPE above (chunks,
one idea per sentence, bold the key line). Simplify the packaging, never the substance.

If the user has a separate learning-style preference (e.g. "trace from the entrypoint
outward with real file and symbol names"), that still applies alongside this skill.
Trace the chain — as a numbered list of short steps, not a paragraph.
