# R for Marine Science — MB5370

This repository contains my R scripts, analysis documents, and supporting datasets from the R for Marine Science workshop series in MB5370 (Techniques in Marine Science 1) at James Cook University.

Across the workshops, I practiced working with different environmental datasets, from importing and cleaning raw records to producing figures and interpreting ecological patterns. The exercises also gave me a chance to work with topics I am interested in, particularly marine habitats and the way ecological data are communicated.

## Workshops

### Workshop 1 — Data wrangling and visualization

I worked through importing different file formats, inspecting data structures, and using `dplyr` to filter, group, and summarize observations. The analysis document uses the `palmerpenguins` dataset to compare body mass among penguin species and islands, with boxplots and mean estimates displayed alongside standard deviation and standard error.

- [R script](code/R4MS_W1.R)
- [Quarto analysis](code/R4MS_W1_analysis.qmd)
- [Rendered HTML report](code/R4MS_W1_analysis.html)
- [Body mass boxplot](outputs/figures/R4MS_W1_penguin_boxplot.png)
- [Body mass by species (standard deviation)](outputs/figures/R4MS_W1_penguin_SD.png)
- [Body mass by species (standard error)](outputs/figures/R4MS_W1_penguin_SE.png)
- [Summary table](outputs/tables/R4MS_W1_penguin_summary.csv)

### Workshop 2 — Ross River estuary fish surveys

This exercise focused on bringing together multiple datasets collected across the Ross River estuary in Townsville. I worked with fish catch records, site metadata, a species dictionary, and environmental sensor measurements. The workflow includes standardizing site and species names, joining the different datasets, accounting for recorded absences, and examining fish abundance and environmental differences across estuarine zones.

Salinity was the main environmental variable explored, although temperature and turbidity were also considered when interpreting the patterns.

- [Analysis document](code/R4MS_W2_FinalEx.qmd)
- [Rendered HTML report](code/R4MS_W2_FinalEx.html)
- [Sensor processing script](code/R4MS_diw_sensor.R)
- [Fish abundance figure](outputs/figures/R4MS_W2_fish_abundance.png)

### Workshop 3 — Kelp forest ecology and scientific figures

For the final workshop, I examined macroalgal biomass data from coastal Maine, drawing on the study and dataset by Yiu et al. (2025). The aim was to evaluate how the original published figures communicated differences in kelp and other macroalgal groups, then reconstruct alternative visualizations using R and `ggplot2`.

I aggregated taxon-level observations into quadrat-level algal groups and compared biomass distributions across four regions. The reconstructed figures display individual observations alongside regional means, while also illustrating some of the trade-offs involved in choosing how ecological data are presented. The analysis is descriptive, and the report discusses limitations related to missing values, sampling structure, and visual interpretation.

- [Quarto analysis and written interpretation](code/R4MS_W3_Kelp.qmd)
- [Rendered HTML report](code/R4MS_W3_Kelp.html)
- [Macroalgal biomass figure](outputs/figures/R4MS_W3_macroalgal_biomass.png)
- [Kelp and turf algae comparison](outputs/figures/R4MS_W3_kelp_turf_comparison.png)
- [Source dataset](data/workshop3/Data1_macroalgae_biomass.csv)

## Repository structure

- `code/` — R scripts, Quarto/R Markdown analysis documents, and rendered HTML reports
- `data/workshop1/`, `data/workshop2/`, and `data/workshop3/` — workshop datasets and source materials
- `outputs/figures/` — exported figures
- `outputs/tables/` — exported summary tables

## Running the analyses

The code was written in R and RStudio, with reports prepared in Quarto or R Markdown. The scripts use packages including `tidyverse`, `ggplot2`, `readxl`, `palmerpenguins`, and `here`; package requirements vary by workshop.

Several scripts use `here::here()` to reference the `data/` and `outputs/` folders. For that reason, they are best run with the repository opened as an RStudio project and the existing folder structure kept intact. The source analysis documents and rendered HTML reports for all three workshops are included. GitHub may show HTML files as source code or offer them for download; download an HTML report and open it in a browser to view the formatted document.

## About this work

These exercises were completed as part of my postgraduate marine biology coursework at James Cook University. They reflect my developing skills in R, data management, ecological analysis, and scientific visualization. The kelp workshop was particularly relevant to my interest in temperate marine ecosystems and macroalgal ecology.
