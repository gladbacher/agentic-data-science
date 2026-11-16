# Step tracker

One checklist per upstream step. The items restate rules from `instructions.md` in short form. Where they differ, `instructions.md` is right.

This file is blank on `main`. Fill it in on the analysis branch, so each analysis has its own copy.

Analysis: ____  Branch: ____  Data: ____

For each step: tick the items, write what I checked myself without taking the agent's word for it, and count the agent errors I caught. Every error counted here has a row in [PILOT_LOG.md](../PILOT_LOG.md).

## Step 1: Import and scope the data

Writes: `Data Summary` in the appendix. `Report.md` is not touched.

Started: ____  Closed: ____

- [ ] The source file is in `Attachments/`, unmodified, and holds no confidential employer data
- [ ] Provenance recorded: where the file came from, when, its checksum, and why this file
- [ ] The agent asked whether this is the best available form of the data
- [ ] The file was described before it was judged
- [ ] The unit of every column is recorded, and whether it is a measurement or a model output
- [ ] Scope, missing data, panel structure, cleaning and accepted-as-is decisions recorded, each with its reasoning and cost
- [ ] The description of data that will not be used was deleted once the scope was decided
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 2: Frame the research question

Writes: `Research Question` in the appendix, then the questions into the `Introduction` of the report.

Started: ____  Closed: ____

- [ ] I stated the question or hypothesis myself, in my own terms
- [ ] Nothing was tested: no statistics, plots, correlations or "just to check" calculations
- [ ] The work used column names, documented meanings and the `Data Summary` only
- [ ] Feasibility assessed: the variables are present, coverage is adequate, the structure of the data does not undermine the answer
- [ ] `Research Question` has its three parts: `Discussion`, `Question`, `Sub-questions`
- [ ] Each sub-question names its variables and what would count as an answer either way
- [ ] The questions are in the `Introduction`, with the background placeholder in the opening position
- [ ] The `Introduction` anticipates no result and no limitation
- [ ] I can say what each variable measures without asking the agent
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 3: Visualisation

Writes: Figures into `Results` in the report. Workings into `Analysis` in the appendix.

Started: ____  Closed: ____

- [ ] One sub-question at a time
- [ ] Each chart was proposed (what it plots, the axes, the rows, what a reader would see) and I agreed before it was made
- [ ] Where the orientation was open, both versions were made and I chose
- [ ] The observations are plotted before any fitted line
- [ ] One script per figure, writing to `Code/outputs/figures/`, with a dark variant
- [ ] No figure refits a model that is reported elsewhere
- [ ] Figures are numbered in order of appearance. Captions say what the figure shows, not what it means
- [ ] The type is readable at the width of the note, and each label is tied to its point
- [ ] Each variable keeps one colour across all figures
- [ ] No number in the text was read off a figure
- [ ] The agent compared the figures and captions with the sample's, for shape and not content, and said what it found
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 4: Statistical tests

Writes: `Methods` and `Results` in the report. Workings and diagnostics into `Analysis` in the appendix.

Started: ____  Closed: ____

- [ ] One sub-question at a time
- [ ] Each test was proposed with what it estimates and the assumptions it rests on, and I agreed before it ran
- [ ] The assumptions were checked against the data, not asserted
- [ ] The outcome was confirmed to be a measurement, not an interpolated or modelled series
- [ ] The standard errors match the structure of the data, and the agent said which were used and why
- [ ] Each result has its estimate, its interval and the number of observations
- [ ] The number that carries each claim was re-derived by a second route
- [ ] `Methods` and `Results` use the same sub-headings in the same order, and `Methods` describes only what `Results` reports
- [ ] Checks that changed nothing are in the appendix, not the report
- [ ] The report does not grade the evidence
- [ ] I can explain each test without the agent. If not, kill criterion 2 in the roadmap applies
- [ ] The agent compared `Methods` and `Results` with the sample's and said what it found
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 5: Conclusions and limitations

Writes: `Discussion` and `Limitations` in the report.

Started: ____  Closed: ____

- [ ] The paragraph structure of the `Discussion` was agreed before it was written
- [ ] The `Discussion` is organised by theme, not by sub-question
- [ ] `Limitations` is a section of its own, after `Discussion`
- [ ] No caveat appears in both `Methods` and `Limitations`
- [ ] No new analysis was done in this step
- [ ] Nothing is in `Discussion` or `Limitations` that is not already in `Results` or the appendix
- [ ] Exploratory results are not presented as confirmed
- [ ] Any count of items in the text matches the number of items
- [ ] The agent compared `Discussion` and `Limitations` with the sample's and said what it found
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 6: Background and abstract

Writes: The background in the `Introduction`, the `Abstract`, the title, and the references.

Started: ____  Closed: ____

- [ ] The structure of the background was agreed before any prose
- [ ] The agent opened each source, and I saw the sources before the prose
- [ ] I fetched the paywalled sources myself. They are in `Attachments/literature/`, which git ignores
- [ ] The `Analysis Log` says which sources were read in full and which rest on an abstract
- [ ] Every reference has a link, and every link resolves
- [ ] The background carries no result, stated or implied
- [ ] The `Abstract` was written last, carries no numbers, says nothing new, and names the prior work it refers to
- [ ] The agent offered two or three titles and I chose
- [ ] The agent compared the background and the abstract with the sample's and said what it found
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 7: Read through

Writes: A list of faults. A row in the `Analysis Log`, even if nothing was found.

Started: ____  Closed: ____

- [ ] The report was read in order, in one pass
- [ ] Each sub-question is asked in the `Introduction`, given a method in `Methods`, answered in `Results` and discussed in `Discussion`
- [ ] Every number was re-checked against the generated output, including the counts that describe the data
- [ ] Nothing is orphaned: no figure, reference, heading or defined term left unused
- [ ] Every claim in the `Abstract` traces to a section
- [ ] The references were checked against their sources
- [ ] The faults were listed, not fixed
- [ ] The outcome is recorded in the `Analysis Log`
- [ ] I ran the report checker and compared its list with the read-through list
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Step 8: Export

Writes: A Word file or a PDF in the project root, beside `Report.md`.

Started: ____  Closed: ____

- [ ] The agent quoted the `Disclaimer` back in full, and I confirmed that wording in answer to being asked
- [ ] The confirmation is recorded in the `Analysis Log`
- [ ] The agent asked which format, and installed only what that format needs
- [ ] The export ran as a script from the vault root, and the command is in the `Code Summary`
- [ ] The export is in the project root. `Report.md` remains the source of truth
- [ ] Checked in the output: captions, dropped characters, dead links, the reference list, figures beside their captions
- [ ] The output was read back and checked mechanically, not trusted on its exit code
- [ ] The agent asked whether the step was complete, and I answered

What I verified myself, without taking the agent's word for it:

> 

Agent errors caught: 0

## Course progress

"Agentic AI for Statistics and Data Science". Lesson numbers follow the course overview page. Status is one of: not started, watched, applied. Lessons 1.8, 2.1 and 2.2 were not live on 2026-11-16.

| Lesson | Title | Status | Notes |
| --- | --- | --- | --- |
| 1.1 | Step by step working with AI | Not started |  |
| 1.2 | Importing data | Not started |  |
| 1.3 | Deciding on a hypothesis | Not started |  |
| 1.4 | Visualisation | Not started |  |
| 1.5 | Traditional statistics versus agentic statistics | Not started |  |
| 1.6 | Statistical analysis | Not started |  |
| 1.7 | Turning analysis into a report | Not started |  |
| 1.8 | Best practices for working with agentic AI | Not live on 2026-11-16 | Listed as available Monday 16 November 2026. Recheck. |
| 2.1 | How context is set up | Not live on 2026-11-16 | Listed as available Monday 23 November 2026. Recheck. |
| 2.2 | Adapting your own framework | Not live on 2026-11-16 | Listed as available Monday 16 November 2026. Recheck. The lesson sidebar numbers this 2.3. |
| 2.3 | Matt Pocock's Skills | Not started | The lesson sidebar numbers this 2.2. |
| 2.4 | A football data framework | Not started |  |
| 2.5 | A statistical machine learning framework | Not started |  |
| 2.6 | Ethical aspects of agentic AI | Not started |  |
| 2.7 | Fully automated research? | Not started |  |

Prerequisite course "Agentic AI for Research" (11 lessons): ____
