# R Bootcamp for Social Scientists

A free, four-session introduction to R for social scientists, from first steps to regression, visualisation and an introduction to machine learning. Written and taught by [Marta Antonetti](https://github.com/dr-antonetti-marta) at the London School of Economics (2026 edition).

No prior coding experience needed.

Four R sessions built around one real dataset: road-safety statistics for Great Britain, 1969-1984, including the introduction of the 1983 seatbelt law. Each session builds on the last, so work through them in order.

- `scripts/Session1.Rmd` — R basics: syntax, variable types, importing/exporting data, subsetting
- `scripts/Session2.Rmd` — descriptive statistics, hypothesis testing, linear regression, regression tables
- `scripts/Session3.Rmd` — data visualization (`ggplot2`), regression tables, coefficient plots
- `scripts/Session4.Rmd` — count/logistic/ordered-logit models, an exploratory mini-project, decision trees, an intro to machine learning

Each file opens with a short "Welcome" or topic note explaining what that session covers and why. Read that first, not just the code.

## Getting started

1. **Download** this repository: click the green **Code** button above → **Download ZIP**, then unzip it somewhere sensible (Documents, not Downloads) and keep its contents together. (If you use Git: `git clone https://github.com/dr-antonetti-marta/r-bootcamp.git`.)
2. **Create an RStudio Project in it**: File → New Project → Existing Directory → choose this folder → Create Project. Everything you do will live inside that project.
3. In the Files pane, open `scripts/Session1.Rmd` and work through it top to bottom, either chunk by chunk (Ctrl/Cmd+Enter, or the green play button) or all at once with the **Knit** button.
4. Then Session 2, 3 and 4, in that order.

## About the data

- **You don't need to download anything.** The main dataset (`Seatbelts`) is built into R.
- Session 1 turns it into a data frame and saves a copy as a CSV in a `data/` folder that it creates next to `scripts/`. Later sessions load that file.
- **If a later session can't find the file** (you skipped Session 1, or your working directory is somewhere unexpected) it rebuilds exactly the same data from the built-in dataset automatically, so you are never blocked.
- One dataset in Session 3 (the "trust experiment") is clearly labeled as fully simulated for teaching, not real survey data.

## Packages

The sessions use a few packages (`tidyverse`, `stargazer`, `broom`, `rpart`, ...). The first time you run a session, R will install what's missing; that can take a few minutes, so it's worth doing before class if you can. After a package is installed you can comment out its `install.packages(...)` line (or leave it; reinstalling is harmless, just slow).

## Tasks

Most sessions include one or more **Task** sections with instructions but no code. These are for you to do yourself (or in pairs) before moving on. Session 4's final project is deliberately open-ended: you choose a question, test it, and write up what you found and what you *can't* conclude.

## If something goes wrong

- **"cannot open file" or "object not found" errors:** check you created the project in the right folder and opened the Rmd from the `scripts/` folder. Running `getwd()` in the Console shows where R currently is.
- **"there is no package called ...":** run `install.packages("name")` for that package, then try again.
- **A chunk fails halfway:** later chunks depend on earlier ones, so run the file from the top rather than starting in the middle (the Session 4 project section is the one exception; it sets itself up).

## Solutions

This repository contains the **student versions** only: tasks come with instructions but no worked answers, so that solutions don't circulate among future cohorts. If you're an instructor or self-learner and would like the solutions, email me at [m.antonetti@lse.ac.uk](mailto:m.antonetti@lse.ac.uk).

## Licence

© 2026 Marta Antonetti. This material is licensed under [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/): you're free to use, share and adapt it, including for your own teaching, as long as you credit the author.
