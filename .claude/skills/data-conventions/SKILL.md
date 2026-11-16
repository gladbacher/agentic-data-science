---
name: data-conventions
description: STUB with no rules yet. Will hold my conventions for reading and describing data in step 1 and step 2. Do not use until the body is filled in.
disable-model-invocation: true
---

# Data conventions (stub)

Status: stub. This skill holds no rules. If it is invoked, say that it is empty and stop.

`disable-model-invocation: true` keeps the agent from loading an empty skill. Remove that line once the skill has content. The format is Claude Code's standard skill format (a folder holding `SKILL.md` with `name` and `description` in the frontmatter). Upstream ships no skills of its own, so there was no upstream format to follow.

## What pilot-log evidence should justify filling this in

Entries with error type `data`. That means entries where the agent, in step 1 or step 2, got the data itself wrong and I had to correct it: a unit, what a column measures, whether a column is a measurement or a model output, a date format, a code for missing values, the unit of observation, or where a file came from.

A rule goes in only when it cites a `PILOT_LOG.md` entry by date and step. A rule with no entry behind it does not go in.

[TO FILL: how many entries of one kind justify a rule.]

## How this relates to the other files

- `instructions.md` step 1 already requires provenance, units, scope, missing-data and cleaning decisions. This skill must not repeat or contradict it. It records what is specific to my data.
- `framework/FRAMEWORK.md`, section "Data conventions", holds the short rules that are always loaded. This skill holds longer procedures that are loaded on demand.

## Rules

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |
