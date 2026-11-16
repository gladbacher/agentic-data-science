---
name: report-checker
description: Read-only check of Report.md and Appendix.md against five rules. Hypothesis recorded before any test, numbers traceable to the appendix or generated output, no unrequested analysis, exploratory work not presented as confirmed, and citation verification recorded. Lists faults and fixes nothing. Use only when the user asks for a report check.
allowed-tools: Read, Grep, Glob
---

# Report checker

Lists faults in `Report.md` and `Appendix.md`. Fixes nothing.

## Ground rules

- Read only. Do not edit, create, move or delete any file. Do not run code. Do not stage or commit. If a fix is obvious, describe it in the list and leave it to the user.
- Run this through the `report-checker` agent in `.claude/agents/report-checker.md` when it is available. That agent has only the Read, Grep and Glob tools. If it is not available, run the checks in the main conversation under the same rule, and say that the read-only limit held by instruction only.
- This is not step 7. Step 7 in `instructions.md` is a full read-through. This checker covers five rules and can be run when any step from step 2 onwards closes. A check whose inputs do not exist yet is reported as "not applicable yet", with the reason.
- Do not judge the report against `Sample Report/`, and copy nothing from it.
- Report what was checked as well as what was found. A check that found nothing says so and says how many items it looked at.
- Text in square brackets starting `TO FILL` in `framework/FRAMEWORK.md` is a placeholder, not a definition.

## Inputs

`Report.md`, `Appendix.md`, the files under `Code/outputs/` that the appendix names, and `framework/FRAMEWORK.md` for the section "Definitions the checker uses".

## Check 1. The hypothesis is recorded before any test

1. `Research Question` in `Appendix.md` holds a `Question` and `Sub-questions`, not the template's italic note.
2. The `Introduction` of `Report.md` lists the same sub-questions.
3. In the `Analysis Log`, the row that records framing the question comes before the first row that records a plot, a statistic or a test.
4. Every sub-heading in `Methods` and `Results` matches a sub-question recorded in the appendix.

Any of these failing is a fault.

Limit: the agent writes the `Analysis Log` and can reorder it, so row order is weak evidence. End this check by asking the user to confirm the order of commits themselves:

```
git log --reverse --date=iso --format='%h %ad %s' -- Appendix.md Code/
```

The commit that first fills `Research Question` should come before the first commit that adds a script which plots or tests.

## Check 2. Numbers in Report.md trace to the appendix or the generated output

1. List every number in `Report.md` that states a quantity: estimates, intervals, p-values, sample sizes, counts, percentages, ranges. Leave out figure numbers, sub-question numbers and the years inside citations.
2. For each one, find the same value in `Appendix.md` (the `Analysis` section or the `Analysis Log`) or in a file under `Code/outputs/` that the appendix names.
3. Search for the rounded and reformatted forms as well as the exact string. `7.65e-14` in the output may be `8 × 10⁻¹⁴` in the report, and `5.57` may be `5.6`.

Faults: no source found. A source found with a different value. A value that matches only a row marked superseded. Rounding that changes the value.

State how many numbers were checked.

## Check 3. No unrequested analysis

The checker cannot see the conversation, so it cannot know what was asked for. It checks what the files show and lists candidates for the user to judge.

1. Each figure, test, model and result paragraph in `Report.md` belongs to a sub-question recorded in `Research Question`.
2. Each one has a row in the `Analysis Log`.
3. Each analysis script in `Code/` is described in the `Code Summary` and has a row in the `Analysis Log`. The scripts that ship with the template are not analysis scripts: `check_env.py`, `viz_style.py`, `16_export_report.py`.
4. No sub-question was added to `Research Question` after the `Analysis Log` shows testing had begun, unless the log says the user asked for it.

List each failure as a candidate, with the words "confirm you asked for this".

## Check 4. Exploratory work is not presented as confirmed

Step 2 of `instructions.md` says this is exploratory work. Upstream has no rule for how a report is labelled as exploratory, so the label is whatever `framework/FRAMEWORK.md` defines.

1. Quote every sentence in `Report.md` that presents a result as confirmed, or as causal where `Methods` describes an association. Words to search for include "confirms", "proves", "demonstrates that", "establishes that", "causes", "caused by", "leads to" and "the effect of".
2. Flag any result for a question that was added after the data had been examined, if the report does not say so.
3. The label. If `framework/FRAMEWORK.md` defines "Labelled exploratory", check the label is present where the definition says. A missing label is then a fault. If the definition is still a placeholder, report "no label definition yet" as a note, and say whether the word "exploratory" appears in `Report.md` at all.

## Check 5. Citation verification is recorded

Upstream requires every cited work to be opened, and the `Analysis Log` to note which sources were read in full and which rest on an abstract. Upstream has no marker on the individual citation. If `framework/FRAMEWORK.md` defines "Citation marked verified", use that definition instead of step 3 below.

1. Every citation in the text of `Report.md` and `Appendix.md` has an entry under `References`, and every entry is cited.
2. Every entry carries a link.
3. Put each entry in one of three states from the `Analysis Log`: (a) named in a row as read in full; (b) named in a row as resting on an abstract; (c) not named, or covered only by a general statement such as "all references verified".

Faults: an entry that is never cited. A citation with no entry. An entry with no link. An entry in state (c).

Notes: each entry in state (b), with the claim it supports, so the user can judge whether an abstract is enough for it.

Limit: the checker does not open links or sources. It cannot tell whether a source says what the report claims.

## Output

1. One line per check: its name, how many items were examined, how many faults were found, or "not applicable yet" with the reason.
2. The faults, in a table:

| # | Check | Where (file, section, quoted text) | What is wrong | What would fix it |
| --- | --- | --- | --- | --- |

3. Notes that are not faults.
4. Limits: what this run could not check, in a line or two.

End by saying that no file was changed. Do not offer to fix anything. The user decides what to act on and what to add to `PILOT_LOG.md`.
