# Agent log

Add a dated entry each time you work with your AI coding agent, with the newest entry at the bottom. Each entry records what you asked the agent, what it produced, and what you checked or changed. Paste your key prompts in exactly as you typed them. Include at least one time the agent got something wrong, and how you caught it.

Copy this outline for each entry:

```markdown
## YYYY-MM-DD: What you worked on

- **Asked:** "Paste your prompt here."
- **Agent produced:** What it made or changed.
- **Checked or changed:** How you checked it, and what you fixed.
```

## 2026-11-17: Built the median sale-price page

- **Asked:** "READ Agents.md and docs/data_description_sheet.md first. Then replace the placeholder index.html with a page that shows the median sale price for each city, computed from data/college_town_home_sales.csv. Leave out sales under $10,000 and state that rule on the page."
- **Agent produced:** Replaced the placeholder `index.html` with a plain HTML, CSS and JavaScript page. The script loads the CSV, leaves out sales below $10,000, groups the remaining sales by city and state, and renders each city's median and sales count.
- **Checked or changed:** Read `AGENTS.md` and `docs/data_description_sheet.md` before analysis. Confirmed the CSV header and computed reference medians and totals with Python: 35,402 sales were included and 40 were excluded. Also fixed the repository instruction mismatch by locating the actual uppercase `AGENTS.md` file after the lowercase `Agents.md` path was not present.

## 2026-11-17: Added a median-price bar chart

- **Asked:** "Add a bar chart comparing median home sale prices across cities."
- **Agent produced:** Added a responsive horizontal bar chart above the existing city table, using the same browser-computed medians and the same $10,000 exclusion rule.
- **Checked or changed:** Kept the chart data-derived and dependency-free, sorted bars from highest to lowest median, and added compact mobile styling.

## 2026-11-17: Fixed the median-price bar-chart scale

- **Asked:** "Fix the horizontal bar chart for median sale price by city. Make each bar length proportional to its median on a common zero-based scale, keep the cities sorted highest to lowest, retain dollar labels, and add a labeled price axis."
- **Agent produced:** Updated `index.html` so bar tracks and bars use block-level sizing, bars use a shared $0-to-$1 million scale for the current data, and a labeled axis with ticks is rendered above the chart.
- **Checked or changed:** Verified the chart in a browser and checked computed bar widths against the median values, with Davis at 88.9% and Urbana at 22.99% of the common scale.
