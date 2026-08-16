# adhd-mode

A Claude Code skill that makes Claude explain things in short, chunked steps instead of dense paragraphs.

**The problem.** Dense prose isn't hard because the content is hard. It's hard because the packaging hides it. Same information, wrong shape.

**The fix.** This skill teaches Claude a different shape: short chunks, one idea per sentence, numbered steps, one bold line per section.

---

## What it does

When active, Claude stops writing like this:

> The verification pass exposed that the rule I wrote — "value size follows the column width" — was a post-hoc rationalization that happened to predict mobile correctly but didn't describe what actually drove the desktop choices, so it's really two rules: a floor, and a weight rule.

And starts writing like this:

> **I got a rule wrong.**
>
> I wrote: "number size follows the column width."
>
> Then I drew it, and it was wrong. It works on phone by accident, not because the rule is right.
>
> The real rule is two things:
> 1. Does it fit? If not, smaller.
> 2. Is it crowded (caption, image nearby)? If yes, smaller.

Same content. Half the effort to read.

---

## When it kicks in

- You ask what Claude did, how something works, or why a choice was made
- You say "I don't understand," "too dense," or "simplify that"
- You mention ADHD or focus
- Claude wraps up a multi-step task (summaries are where dense prose creeps back in)

---

## The rules it follows

1. **Chunk it.** Headers every few lines. Never more than ~3 lines in a row.
2. **One idea per sentence.** Split comma-clauses into two sentences.
3. **Number the sequence.** `1. 2. 3.` gives you a place to stop and resume.
4. **Bold one thing per section.** If everything is bold, nothing is.
5. **Concrete before abstract.** Real numbers and real names, not "the value must satisfy its constraint."
6. **End with a door.** "Want me to go deeper on any part?" — never dump detail preemptively.

## What it cuts

- Recaps of things you already know
- Hedges that don't change the answer
- Tradeoffs already resolved (just state what was done)
- Meta-commentary about the process itself

## What it never cuts

Detail you actually asked for. Say "trace the whole chain" and you get the whole chain — just still chunked, not a wall of text.

---

## Install

Clone this repo, then copy (or symlink) the `explain-simply/` folder into your Claude Code skills directory:

```bash
git clone https://github.com/cedricrabarijohn/adhd-mode.git
cp -r adhd-mode/explain-simply ~/.claude/skills/explain-simply
```

Claude picks it up automatically — no config, no restart.

---

## Why this exists

Built for ADHD, but the shape helps most people. Dense prose is a tax everyone pays; some people just pay it in full every single time.
