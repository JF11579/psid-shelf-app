# psid-shelf-app
Browser-based catalog for the PSID-SHELF dataset (10-row sample version)
#
# psid-shelf-app

A browser-based catalog and explorer for the **PSID-SHELF** dataset — built to make one of social science's most powerful longitudinal datasets approachable for the rest of us.

🔗 **Live site:** [psid-shelf-app.netlify.app](https://psid-shelf-app.netlify.app)

---

## What this is

The Panel Study of Income Dynamics (PSID) has followed thousands of American families since 1968 — across generations, through every wave of social and economic change. The **PSID-SHELF** harmonized longitudinal file (Pfeffer, Daumler & Friedman, 2025) makes that data dramatically easier to use. But for newcomers, even the harmonized version can feel like a wall.

This app is a way in. It's a single-page browser tool with three tabs:

- **Variable Finder** — search 30 topic areas by plain language or variable name
- **Data Explorer** — preview what each topic's data actually looks like
- **Raw PSID Lookup** — translate raw PSID variable codes into something readable

It runs entirely in your browser. No accounts, no installs, no servers.

## What you see here vs. the full dataset

The version of the app in this repo and on the live site shows **10-row previews** of each topic. That's enough to understand the structure and decide whether SHELF is right for your project — but it isn't analytically usable.

To work with the real data, you need to download SHELF yourself from OpenICPSR (free; registration required) and run the data through a local copy of this app. SHELF's terms don't permit redistribution, so this repo provides the tool, not the data.

## Getting the full data (the recipe)

1. **Register and download SHELF** from OpenICPSR:
   [doi.org/10.3886/E194322](https://doi.org/10.3886/E194322)
   You'll get a Stata `.dta` file.
2. **Split the `.dta` into 30 topic CSVs.** *(Split script coming soon — currently in development. The 30 topics expected by the app are: covid, demographics, depression, earnings_nominal, earnings_real, education, employment, expenditures (4 sub-topics), family_income, family_structure, geography, health_chronic, health_general, housing, race_ethnicity, time_use, and wealth (10 sub-topics).)*
3. **Point a local copy of `index.html` at your CSVs** and open it in any modern browser.

Until step 2's script is published here, you can read the [PSID-SHELF User Guide](https://www.openicpsr.org/openicpsr/project/194322) for variable definitions and topic structure.

## Local use

```bash
git clone https://github.com/JF11579/psid-shelf-app.git
cd psid-shelf-app
open index.html   # or just double-click it
```

That's it. The app is one self-contained HTML file with the previews baked in.

## Attribution

PSID-SHELF was created by:

- **Fabian T. Pfeffer**, Ludwig-Maximilians-Universität München
- **Davis Daumler**, University of Michigan
- **Esther Friedman**, University of Michigan

Cite the dataset as:
> Pfeffer, Fabian T., Daumler, Davis, and Friedman, Esther. *PSID-SHELF, 1968–2021: The PSID's Social, Health, and Economic Longitudinal File (PSID-SHELF), Beta Release.* Ann Arbor, MI: ICPSR [distributor], 2025-02-24. https://doi.org/10.3886/E194322V2

This app is an independent project. It is not affiliated with or endorsed by the SHELF team or the PSID.

## Related

- **The PSID Book** — a longer-form companion at [joe-foley.gitbook.io/psid-book](https://joe-foley.gitbook.io/psid-book)
- **Analysis notebooks** — [PSID_For_the_Rest_of_US](https://github.com/JF11579/PSID_For_the_Rest_of_US)

## License

The code in this repository is released under the MIT License (see `LICENSE`). This license covers the app code only — the underlying PSID-SHELF data is governed by ICPSR's terms of use.

---

*Built by [Joe Foley](https://github.com/JF11579). Issues and pull requests welcome.*

