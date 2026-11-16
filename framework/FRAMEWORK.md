# Personal framework

*My additions to the working contract. `CLAUDE.md` imports this file after `instructions.md`.*

## How this file relates to the contract

- `instructions.md` is upstream's contract. This file adds rules to it. It never overrides one.
- If a rule here conflicts with `instructions.md`, follow `instructions.md` and tell me about the conflict. Do not resolve it silently.
- A message prefixed `FRAMEWORK` changes `instructions.md`, as that file says. It does not change this file. Edit this file only when I ask for a change to `framework/FRAMEWORK.md` by name.
- Each rule below cites the `PILOT_LOG.md` entry that justified it. A rule with no entry behind it is marked as a standing rule and says where it came from.
- Text in square brackets starting `TO FILL` is a placeholder for me. It is not a rule. Ignore it when working.

## Where my files live in git

Upstream keeps the template on `main` and each analysis on its own branch (`instructions.md`, "Promoting template changes to `main`"). My files follow the same split.

| Files | Kind | Rule |
| --- | --- | --- |
| `framework/`, `.claude/skills/`, `.claude/agents/`, `PILOT_LOG.md`, `plan/` | Template-level | Commit them on their own, touching no analysis content, and cherry-pick the commit onto `main`. |
| `tracker/STEPS.md` | Analysis content | Blank on `main`. Filled in on the analysis branch and never promoted. |

Ask me before any push. Whether a `FRAMEWORK` message authorises a push is an open decision in `plan/ROADMAP.md`.

## Data-handling rules

| # | Rule | Source | Added |
| --- | --- | --- | --- |
| 1 | No confidential employer data enters `Attachments/` or any other file in this vault. Only public or non-confidential data is used here. If a file may be employer data, stop, tell me, and do nothing further with it. | Standing rule (HANDOFF.md section 2) | At setup |

[TO FILL: what counts as confidential for my employer and how to recognise it in a file.]

[TO FILL: further data-handling rules, each citing its pilot-log entry.]

## Data conventions

Status: empty.

[TO FILL after the pilot: conventions for the data I work with. For example how I name columns, which units and date formats I expect, how I record a source. Each rule cites its pilot-log entry.]

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |

## Statistics defaults

Status: empty.

[TO FILL after the pilot: my defaults where `instructions.md` step 4 leaves a choice open. Each rule cites its pilot-log entry.]

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |

## Chart style

Status: empty. `Code/viz_style.py` and step 3 of `instructions.md` already set the figure conventions. Record only additions here. A change to `viz_style.py` itself is a template change under upstream's promotion rule.

[TO FILL after the pilot: chart conventions beyond `viz_style.py`. Each rule cites its pilot-log entry.]

| # | Rule | Pilot-log entry | Added |
| --- | --- | --- | --- |

## Definitions the checker uses

The `report-checker` reads these. Until they are filled in it reports the matching item as a note, not a fault.

- Labelled exploratory: [TO FILL: what wording marks a report as exploratory, and in which section it must appear. Upstream has no rule for this. Open decision 6 in `plan/ROADMAP.md`.]
- Citation marked verified: [TO FILL, or leave as it is. With no definition here the checker uses upstream's record: the Analysis Log entry that says which sources were read in full and which rest on an abstract. Open decision 7 in `plan/ROADMAP.md`.]
