# Agentic data analysis vault

David Sumpter's human-agentic data analysis template, plus three layers of my own: a framework file, a pilot log, and a pace and checkpoint layer. Upstream's README is kept unchanged as [README.upstream.md](README.upstream.md). Read it once: it explains the eight steps.

## First run, in order

1. Install Obsidian, the Claudian plugin, Claude Code and `uv`: [Setup.md](Setup.md), sections 1 and 2.
2. Build the Python environment: `cd Code && ./setup_env.sh`.
3. Open this folder as an Obsidian vault and check that Claude Code is the provider selected in Claudian.
4. Ask the agent which skills and agents it can see. It should name `report-checker`. If it does not, Claudian is not loading `.claude/skills/` or `.claude/agents/`. Note that in [PILOT_LOG.md](PILOT_LOG.md).
5. Read [plan/ROADMAP.md](plan/ROADMAP.md) and settle the open decisions at the bottom of it.
6. Start a branch for each analysis: `git switch -c <name>`. `main` stays the template.
7. Phase 1: on a branch, work through the eight steps with the prompts in [Sample Report/Analysis Steps.md](Sample%20Report/Analysis%20Steps.md). Never edit anything inside `Sample Report/`.
8. As each step closes: tick [tracker/STEPS.md](tracker/STEPS.md), add rows to [PILOT_LOG.md](PILOT_LOG.md), and ask the agent to run the report checker.

## Rules to keep in view

- No confidential employer data goes anywhere in this vault. Public or non-confidential data only.
- To change the contract, prefix a message with `FRAMEWORK`. The agent then edits `instructions.md` in a commit of its own. That is upstream's convention and this vault follows it.
- My own conventions go in [framework/FRAMEWORK.md](framework/FRAMEWORK.md). That file adds to the contract and never overrides it. I edit it directly, or ask for a change to it by name.
- `tracker/STEPS.md` is filled in on the analysis branch. `PILOT_LOG.md`, `plan/`, `framework/` and `.claude/` changes are committed on their own and cherry-picked to `main`, so the next analysis sees them.
- Unsettled: upstream's README says the agent will not commit or push unless asked, while the `FRAMEWORK` section of `instructions.md` tells it to commit, cherry-pick to `main` and push both branches. Decide whether a `FRAMEWORK` message authorises a push before sending the first one. It is listed in the roadmap.

## Git layout

If `bootstrap.py` set up git (its default), `main` holds upstream's history up to the tag `upstream-base`, plus one commit that adds my files. `git diff upstream-base -- instructions.md` shows every change made to the contract since. The `upstream` remote is fetch-only. To take upstream updates: `git fetch upstream && git merge upstream/main`. Re-running `bootstrap.py` never overwrites a file that differs from its template, so it does not bring in upstream updates.

## Attribution and licence

Based on human-agentic-data-analysis by David Sumpter (Vivid-Insights), https://github.com/Vivid-Insights/human-agentic-data-analysis, commit 6a536839e3d5f83fba7602ac129437b2a9861581, licensed CC BY 4.0. See [LICENSE](LICENSE), which also carries the disclaimer of warranties.

Changes from upstream: `CLAUDE.md` gains one section that imports `framework/FRAMEWORK.md`. Upstream's `README.md` is renamed `README.upstream.md` and this file takes its place. Added: `framework/`, `.claude/skills/`, `.claude/agents/`, `tracker/`, `plan/`, `PILOT_LOG.md`. Every other upstream file, including `instructions.md`, is unchanged at generation. My additions are offered under the same licence.
