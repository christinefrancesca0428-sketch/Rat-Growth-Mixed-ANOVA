# Rat-Growth-Mixed-ANOVA
Mixed-design repeated measures ANOVA analysis of rat growth under different treatments.

## Project Overview
This repository performs a two-way mixed-design repeated measures Analysis of Variance (ANOVA) on classical rat growth data (Box, 1950). The study investigates the effect of three treatment conditions (Control, Thiouracil, and Thyroxin) administered via drinking water across five weekly measurement occasions (Week 0 to Week 4) The sample consists of N=27 rats across 135 total observations after removing three rats from the Thyroxin group due to mortality.

## Research Objectives
* Test whether growth trajectories over time significantly depend on the treatment administered (Treatment x Time interaction).
* Assess the primary main effects of treatment group (Between-subjects) and time (Within-subjects) on body weight (y).
* Evaluate normality (Shapiro-Wilk), extreme outliers, homogeneity of variance (Levene's test), homogeneity of covariance matrices (Box's M test), and sphericity (Mauchly's test with 
* Conduct one-way ANOVAs and Tukey HSD tests at each week, as well as repeated-measures ANOVAs and paired t-tests (Holm-adjusted) within each treatment group.

## Dataset Description
The analysis uses the long-format rats dataset from the nlmm R package (135 rows x 4 columns)

Group Sample Sizes:
* Control: n=10 (50 observations)
* Thiouracil: n=10 (50 observations)
* Thyroxin: n=7 (35 observations)

## Instructions for Reproduction
1. Install Dependencies. Run the following R command to install required packages (```r
install.packages(c("nlmm", "tidyverse", "rstatix", "ggpubr", "rmarkdown", "knitr"))```).
2. Run Analysis Script. Execute Rat_Growth_Mixed_ANOVA.R in R or RStudio to run data formatting, plots, assumption checks, mixed ANOVA, and post-hoc comparisons.
3. Compile HTML Report. To build the dynamic HTML report from source, execute in the R console (```rrmarkdown::render("Rat_Growth_Mixed_ANOVA.Rmd", output_format = "html_document")```). Alternatively, open Rat_Growth_Mixed_ANOVA.Rmd in RStudio and click Knit.



