# Methodology

## Workflow

1. Collect weekly chart data.
2. Clean raw data.
3. Generate song and artist tables.
4. Aggregate chart statistics.
5. Explore chart patterns and generate hypotheses.
6. Add Spotify audio features.
7. Add additional metadata.
8. Analyse long-term trends.

---

## Data Sources

**Working dataset**

- Kaggle (compiled from Official Charts data)

**Validation source**

- Official Charts Company (UK)

---

## Scope of Analysis

Although the dataset starts in 1952, this project focuses on the period from 1983 onwards.

The analysis starts in January 1983 because this marks the beginning of a consistent weekly Top 100 chart format in the dataset.

Earlier years contain Top 15, Top 50 or Top 75 charts, which would reduce comparability over time.

The Top 100 charts therefore form the analytical foundation of this project.
Smaller chart ranges, such as the Top 50, are used later as analytical perspectives rather than as the primary dataset.

---

## Data Cleaning

During data validation, duplicate chart entries occurring in a small number of New Year weeks were identified.

These records were exact duplicates across all available columns and were therefore removed using `drop_duplicates()`.

During exploratory analysis, additional duplicate chart entries within the same chart week were identified. These records created artificial overlapping chart runs and were removed from the cleaned chart history before run-level and gap analyses.

The original raw dataset remains unchanged throughout the project. A cleaned chart dataset is created separately for all subsequent analyses.

---

## Data Quality

After removing exact duplicate records, only three weeks contained incomplete Top 50 data.

The missing chart positions are:

- Position 42 (15 May 1988 – 21 May 1988)
- Position 43 (18 June 1995 – 24 June 1995)
- Position 46 (24 January 1988 – 30 January 1988)

Since these represent only three missing entries across more than 2,100 weekly charts, they have a negligible impact on the planned analyses.

These remaining anomalies will be verified against the Official Charts Company and stored separately in `missing_chart_entries.csv`.

The correction file will be appended automatically during the data preparation pipeline.

---

## Exploratory Analysis

After constructing the chart statistics table, exploratory analyses are performed to investigate recurring chart patterns such as new entries, re-entries, chart run duration, gaps between chart runs, temporal developments and seasonal behaviour.

The objective of these analyses is not to establish causal relationships, but to generate hypotheses that can later be explored using Spotify metadata and additional contextual information.