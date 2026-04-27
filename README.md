# Quantitative Factor Analysis: Low-Return-Day Fund Flow Signal

## Overview

This project constructs and evaluates a quantitative trading factor based on fund flow patterns during low-return days. The hypothesis is that fund flow behavior on the worst-performing days within a rolling window may contain predictive signal for future returns.

## Methods

- **Factor Construction:** For each stock, a 20-day rolling window identifies the 4 lowest-return days (bottom 20%). The factor value is the average net fund flow ratio `(buy_value - sell_value) / (buy_value + sell_value)` on those days.
- **IC Analysis:** Calculated the daily cross-sectional Information Coefficient (Spearman correlation between factor values and next-period returns) to evaluate predictive power.
- **Portfolio Analysis:** Sorted stocks into quintile groups by factor value and computed cumulative returns per group to visualize monotonicity.

## Key Findings

- Mean IC was approximately 0.007 
- The IC time series showed random oscillation around zero with no clear trend
- The factor showed weak predictive power in this dataset, suggesting low-return-day fund flows alone may not be a strong standalone signal

## Tools

- R (tidyverse, ggplot2)

## Files

- `qa_factor_analysis.Rmd` — R Markdown source code
- `qa_factor_analysis.html` — Rendered report with charts
