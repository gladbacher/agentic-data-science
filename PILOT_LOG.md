# Pilot log

Every point where the agent was wrong, or where I corrected it. One row per event, added when it happens.

- Log an error even if it was caught at once.
- If a step closes with nothing to log, add a row that says so. A step with no row is a step I did not check.
- No confidential data in this file.
- When a rule is adopted, add where it went to the last column: `framework/FRAMEWORK.md`, a skill, or `instructions.md` through a `FRAMEWORK` message.
- This file is template-level. Commit changes to it on their own and cherry-pick them to `main`, so the log carries over to the next analysis.

Error types, a starter list to edit: `data`, `method`, `chart`, `scope` (did work that was not asked for, or ran ahead), `writing`, `citation`, `contract` (broke a rule in `instructions.md`), `other`.

| Date | Step | What the agent did | Error or correction | Error type | Rule it implies |
| --- | --- | --- | --- | --- | --- |
