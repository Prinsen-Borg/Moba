# portfolio/

The IT initiatives portfolio. The source of truth is `initiatives.md`, one row per initiative.

## Test: does the repository setup work?

Open this folder (or `departments/IT/`) in Claude and ask, **without mentioning colours, fonts or layout**:

> Make a one-page overview of the IT initiatives in Moba style.

The setup works if the result:
- uses the Moba look (navy and grey, an amber button, a serif headline, flat white cards) without being told;
- takes its content from `initiatives.md` and labels the statuses as still to be verified;
- uses the status scale from `departments/IT/AGENTS.md`;
- contains no budgets.

Save the result as `tools/it-portfolio/index.html` at the repository root.
