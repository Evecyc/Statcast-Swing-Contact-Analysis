# Statcast Swing Contact Analysis

[Live Demo](https://evecyc.github.io/Statcast-Swing-Contact-Analysis/)

## Project

This project analyzes how swing path tilt relates to contact quality in baseball using Statcast pitch-level data.

The full analysis covers multiple questions about swing mechanics and offensive performance. This repository focuses on my individual contribution: examining how swing path tilt relates to sweet spot probability, hard-hit probability, and expected wOBA across different pitch heights.

## Code structure

`swing_contact_analysis.Rmd` follows this analysis workflow:

1. Data loading and cleaning
2. Feature engineering
3. Exploratory data analysis
4. Regression modeling
5. Model evaluation
6. Visualization and interpretation

## Dependencies

Main R packages:

```r
tidyverse
ggplot2
janitor
pROC
patchwork
```

## How to run

Open `swing_contact_analysis.Rmd` in RStudio and click `Knit`.

Or render it locally with:

```r
rmarkdown::render("swing_contact_analysis.Rmd")
```

The output will be generated as `swing_contact_analysis.html`.

## Experiment setting

Main explanatory variable:

- swing path tilt

Main outcomes:

- sweet spot probability
- hard-hit probability
- expected wOBA

Context variable:

- pitch height group

Binary outcomes are modeled using logistic regression. Expected wOBA is modeled using linear regression.

## Main findings

The analysis suggests that the relationship between swing path tilt and contact quality is nonlinear and depends on pitch height.

Key findings:

- Low pitches tend to benefit from higher swing path tilt.
- Middle-height pitches show stronger outcomes around moderate tilt values.
- High pitches generally perform better with lower or moderate tilt.
- There is no single optimal swing path tilt across all pitch heights.

## Attribution

This repository presents my individual contribution to a team research project. The full report is included for project context and contribution breakdown.
