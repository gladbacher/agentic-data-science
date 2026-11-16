---
name: chart-style
description: STUB with no rules yet. Will hold my chart conventions beyond Code/viz_style.py for step 3. Do not use until the body is filled in.
disable-model-invocation: true
---

# Chart style (stub)

Status: stub. This skill holds no rules. If it is invoked, say that it is empty and stop.

`disable-model-invocation: true` keeps the agent from loading an empty skill. Remove that line once the skill has content. The format is Claude Code's standard skill format (a folder holding `SKILL.md` with `name` and `description` in the frontmatter). Upstream ships no skills of its own, so there was no upstream format to follow.

## What pilot-log evidence should justify filling this in

Entries with error type `chart`. That means entries where, in step 3, I rejected or changed a figure for the same reason more than once: the wrong chart form for the job, unreadable type, labels, colour, axis orientation, or something inside the frame that belonged in the caption.

A rule goes in only when it cites a `PILOT_LOG.md` entry by date and step. A rule with no entry behind it does not go in.

[TO FILL: how many entries of one kind justify a rule.]

## How this relates to the other files

- `Code/viz_style.py` carries the figure conventions and `instructions.md` step 3 sets the figure rules. This skill adds to them and does not replace them. A change to `viz_style.py` is a template change under upstream's promotion rule.
- Upstream's `.claude/settings.json` limits the general `dataviz` skill to user invocation, so that it does not compete with `viz_style.py`. Keep this skill consistent with that choice.
- `framework/FRAMEWORK.md`, section "Chart style", holds the short rules that are always loaded.

## Rules

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |
