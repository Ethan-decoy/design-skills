---
name: data-visualization
description: "Design, improve, or review data visualizations in software. Use when the user builds charts, dashboards, or visual reports, needs to see comparisons, trends, distributions, or anomalies, or wants a chart reviewed for aesthetics and accuracy."
---

# Data Visualization

This is an English translation of [SKILL.md](SKILL.md). The Chinese original is the primary version for maintenance and validation.

Determine what question readers need the data to answer and what decision they will make with it. Inspect real fields, samples, and metric definitions. Identify units, granularity, time ranges, denominators, or aggregation methods that could change the conclusion. When a material definition is missing, state the assumption or ask a focused question. Label illustrative data as such.

## Make the reading match the meaning of the data

Choose a representation based on what readers need to judge. To compare magnitudes, use position or length on a shared scale. When showing change over time, preserve time order and intervals. To show a distribution, make its spread or concentrations visible. When readers need to look up exact values, use a table or direct labels where appropriate.

Check whether the relationships implied by the graphic hold. When bar length represents absolute magnitude, use a zero baseline. To make small changes easier to see, consider point positions or clearly labeled differences. Distinguish missing observations, measured zeroes, and estimates. For example, a period of interrupted device collection can be shown as a labeled gap, while a measured zero belongs at zero. When adjacent charts have different scales, make the difference visible.

Guide the reading order with sorting, alignment, whitespace, and labels. Give colors consistent meanings for categories, increasing values, or deviations from a baseline. Use line styles, symbols, or direct labels to help readers distinguish important series. Give thresholds and anomalies the attention they need while keeping ordinary data readable. When a chart is part of a software interface, follow the product's established state meanings. After filtering or changing a selection, make the title, summary, and chart reflect the same scope.

## Verify and review

When building or improving a visualization, deliver the requested chart proposal, finished visualization, or software implementation. Check units, scales, legends, and labels at the actual viewing size. Examine edge cases that can change the reading, such as long category names, gaps in observations, or an unfinished reporting period.

With raw records, recompute representative readings or comparisons using the metric definition. With only a summary table, check chart readings against the table using the same definitions and identify any upstream aggregations still to verify. With only a screenshot, inspect the visible scales, encodings, labels, and hierarchy. Identify conclusions that still require the underlying data.

When reviewing, explain in the conversation what readers may conclude, which specific encoding supports or interferes with that judgment, and how to improve accuracy and visual expression. When the user asks you to change the chart, implement the change using the confirmed metric definitions and check the result.
