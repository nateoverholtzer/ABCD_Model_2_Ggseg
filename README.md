# ABCD Model Extraction and ggseg Visualization Template

## Overview

This R Markdown template provides a streamlined workflow for extracting statistical results from linear mixed-effects models (LME) fitted on ABCD Study brain imaging outcomes and visualizing them using the ggseg package. The template automates the process of extracting standardized betas, p-values, confidence intervals, and effect sizes from multiple brain regions, then maps them onto anatomical brain plots.

## Key Features

- **Automated extraction**: Pull standardized coefficients, p-values, Cohen's f², and 95% confidence intervals from lists of LME models
- **ABCD-to-ggseg mapping**: Convert ABCD brain region nomenclature to ggseg atlas labels (Desikan-Killiany atlas)
- **Multiple visualization options**: Generate brain plots with various statistical thresholds (uncorrected p < 0.05, FDR-corrected, all results)
- **Forest plots**: Create publication-ready forest plots showing effect estimates with confidence intervals
- **Flexible metric display**: Plot either standardized betas or Cohen's f² (useful when standardization affects significance, e.g., interaction effects)

## What You'll Need

1. Fitted LME models (as a list of `lmerMod` objects, one per brain region)
2. An ABCD-to-ggseg mapping file (CSV linking ABCD region names to ggseg labels)
3. Your predictor names and brain region variable names

## Workflow

1. Fit your models on both standardized and unstandardized data
2. Extract effects using the provided `extract_effects()` function
3. Organize results into a tibble with proper ggseg labels
4. Generate brain plots and forest plots

   <img width="5475" height="2700" alt="image" src="https://github.com/user-attachments/assets/cd010e37-4f41-4f9b-b58c-5c078daa273d" />


## Applications

This template is ideal for researchers working with ABCD Study data who want to:
- Visualize neuroimaging associations across multiple brain regions
- Compare effects across different predictors or conditions
- Create publication-ready brain visualizations
- Perform comprehensive statistical summaries with multiple correction methods

The code is fully generalizable and can be adapted to any ABCD brain imaging analysis with linear mixed-effects models.
