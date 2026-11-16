# Roadmap

Four phases, about four weeks. Pace confirmed on 2026-11-16: it fits around work.

Started: ____

## Phase 1: learn the machine (days 1 to 2)

- [ ] Watch "Agentic AI for Research" and the five step videos
- [ ] Install the vault: the first-run steps in [README.md](../README.md)
- [ ] Run all eight steps on Sumpter's Sample Report data, unchanged, on a branch of its own
- [ ] Fill in [tracker/STEPS.md](../tracker/STEPS.md) and [PILOT_LOG.md](../PILOT_LOG.md) as the steps close

Exit: I can say what each step writes into the Report and the Appendix.

Exit met: [ ] on ____

## Phase 2: pilot on my own data, contract untouched (week 1)

- [ ] Choose one dataset and one question. Public or non-confidential data only. Candidates: a football model dataset, or a public insurance or market dataset. Leaning football as of 2026-11-16, not final. The question is still to be chosen. Open decision 1.
- [ ] Run the eight steps on a branch of its own
- [ ] Send no `FRAMEWORK` messages during this phase
- [ ] Log every correction in the pilot log

Exit: a complete `Report.md` and `Appendix.md`, plus a pilot log with at least one entry per step or an explicit note that none was found.

Exit met: [ ] on ____

## Phase 3: build the framework (week 2)

Wait for lessons 1.8, 2.1 and 2.2 before starting. They were not live on 2026-11-16.

- [ ] Group the pilot-log entries by error type
- [ ] Change the contract through the `FRAMEWORK` prefix where the pilot log supports it
- [ ] Put my own conventions in [framework/FRAMEWORK.md](../framework/FRAMEWORK.md)
- [ ] Write the domain skills in the style of lesson 2.3, starting from the three stubs in `.claude/skills/`
- [ ] Run the report checker on the Phase 2 report and log what it caught and what it missed

Exit: a framework file and at least three skills, each traceable to a pilot-log entry.

Exit met: [ ] on ____

## Phase 4: second project and publication hygiene (weeks 3 to 4)

- [ ] Re-run on a new question using the framework, on a new branch from `main`
- [ ] Cover reproducibility, open science, and AI-use rules and ethics for publication
- [ ] Reproducibility check: clone the repository clean, rebuild the environment, re-run the scripts, compare the figures

Exit: a second report that starts where the first ended, plus a reproducibility check (a clean-clone re-run reproduces the figures).

Exit met: [ ] on ____

## Doing the task unaided

Sumpter says the user should regularly do the task without the agent. [TO FILL: which step I do unaided and how often. Open decision 5.]

| Date | What I did unaided | What was hard |
| --- | --- | --- |

## Kill criteria

Status of all four: PROPOSED, not agreed. Confirm or edit each one. Open decision 4.

| # | Trigger | Action | Status |
| --- | --- | --- | --- |
| 1 | Setup takes more than one day | Stop and use Sumpter's sample vault as is | Proposed |
| 2 | I cannot explain a test without the agent | Stop the pilot and revise traditional statistics first | Proposed |
| 3 | The pilot log is empty after a full run | Assume I am not checking. Re-run one step and look harder | Proposed |
| 4 | Confidential data appears in `Attachments/` | Stop and remove it | Proposed |

Note, 2026-11-16: Obsidian, Claudian and VS Code were already set up before the vault was generated. What is left of setup for criterion 1 is `uv` and `Code/setup_env.sh`.

## Other risks

| Risk | Handling |
| --- | --- |
| Deskilling | The section "Doing the task unaided" above |
| Exploratory results get presented as confirmed | The report checker flags it (check 4) |
| Hallucinated citations | The contract already requires opening each cited work. That rule stays. The report checker lists citations with no verification record (check 5) |

## Open decisions

Mine to make. The numbers are fixed, because other files refer to them.

| # | Decision | Status |
| --- | --- | --- |
| 1 | Pilot dataset and question | Open. Leaning football as of 2026-11-16. Dataset and question not chosen |
| 2 | Whether the pace of about four weeks fits around my job | Decided 2026-11-16: yes |
| 3 | Whether to add Codex support, since Uppsala names it | Decided 2026-11-16: no, Claude only |
| 4 | The kill criteria above | Open. None of the four is confirmed or edited yet |
| 5 | Which step I do unaided, and how often | Open |
| 6 | What counts as "labelled exploratory" in a report, and where the label goes. Upstream has no rule. The definition goes in `framework/FRAMEWORK.md` | Open |
| 7 | Whether I want a verification marker on each citation | Decided 2026-11-16: no marker. Upstream's Analysis Log record is enough |
| 8 | Whether this vault gets a private remote. Upstream's promotion rule pushes, and with no remote the agent will report a failed push each time | Open |
| 9 | Whether a `FRAMEWORK` message authorises the agent to push | Open |
