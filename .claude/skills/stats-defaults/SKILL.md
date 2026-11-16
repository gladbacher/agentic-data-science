---
name: stats-defaults
description: STUB with no rules yet. Will hold my default choices for the statistical tests in step 4. Do not use until the body is filled in.
disable-model-invocation: true
---

# Statistics defaults (stub)

Status: stub. This skill holds no rules. If it is invoked, say that it is empty and stop.

`disable-model-invocation: true` keeps the agent from loading an empty skill. Remove that line once the skill has content. The format is Claude Code's standard skill format (a folder holding `SKILL.md` with `name` and `description` in the frontmatter). Upstream ships no skills of its own, so there was no upstream format to follow.

## What pilot-log evidence should justify filling this in

Entries with error type `method`. That means entries where, in step 4, the agent proposed a test whose assumptions the data did not meet, named an assumption without checking it, used standard errors that did not match the structure of the data, misstated what a test estimates, or made a choice I then changed. Also entries where I could not explain the proposed test without the agent. Those point to what I need to revise, and belong in the roadmap as well.

A rule goes in only when it cites a `PILOT_LOG.md` entry by date and step. A rule with no entry behind it does not go in.

[TO FILL: how many entries of one kind justify a rule.]

## How this relates to the other files

- `instructions.md` step 4 already sets the rules for proposing, checking and reporting a test. This skill records my defaults where that step leaves a choice open.
- `framework/FRAMEWORK.md`, section "Statistics defaults", holds the short rules that are always loaded.

## Rules

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |
