# adhd-mode

A Claude Code skill. Makes Claude explain things in short, chunked steps instead of dense paragraphs.

**Without it:**

> The verification pass exposed that the rule I wrote — "value size follows the column width" — was a post-hoc rationalization that happened to predict mobile correctly but didn't describe what actually drove the desktop choices, so it's really two rules: a floor, and a weight rule.

**With it:**

> **I got a rule wrong.**
>
> I wrote: "number size follows the column width." Then I drew it, and it was wrong.
>
> The real rule is two things:
> 1. Does it fit? If not, smaller.
> 2. Is it crowded? If yes, smaller.

Same content. Half the effort to read.

## Install

```bash
git clone https://github.com/cedricrabarijohn/adhd-mode.git
cp -r adhd-mode/adhd-mode ~/.claude/skills/adhd-mode
```

Claude picks it up automatically. No config, no restart.

## The rules

See [`adhd-mode/SKILL.md`](adhd-mode/SKILL.md).
