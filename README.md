# adhd-mode

A Claude Code skill. Makes Claude explain things in short, chunked steps instead of dense paragraphs.

**Without it:**

> The CI failure came from dependency cache drift: our cache key didn't include the lockfile hash, so the runner restored stale `node_modules`; local tests still passed because local installs were fresh, which made the breakage look non-deterministic.

**With it:**

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

## Install

```bash
git clone https://github.com/cedricrabarijohn/adhd-mode.git
cp -r adhd-mode/adhd-mode ~/.claude/skills/adhd-mode
```

Claude picks it up automatically. No config, no restart.

## Avoid invoking it every time

You do **not** need to run `adhd-mode` manually on every prompt after installation.

Claude can auto-select this skill from its description when your request asks for:
- simpler explanations
- shorter/chunked responses
- ADHD/focus-friendly formatting

If you want it to be your default style even when you do not ask explicitly, add this to
`~/.claude/CLAUDE.md`:

```md
Always explain in adhd-mode style (short, chunked, numbered when useful) unless I ask for a different style.
```

## The rules

See [`adhd-mode/SKILL.md`](adhd-mode/SKILL.md).
