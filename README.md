# **SSH MRIQCeption Analysis**

This project contains R code to analyze local MRIQC data and compare it to API-sourced data. The analysis includes data preparation, visualizations, and tables for comprehensive metric comparisons.

---

## **Features**
- **Data Preparation**:
  - Combine local and API datasets with consistent metric formatting.
  - Extract key metadata and metrics from API JSON files.
- **Rain Cloud Plots**:
  - Visualize distributions and comparisons for various metrics.
- **Summary Tables**:
  - Generate detailed tables showcasing the top and bottom values for each metric.

---

## **Getting Started**

### **Prerequisites**
Ensure the following are installed:
- **R**: Version `>= 4.0.0`
- **RStudio** (recommended for running the scripts)
- Required R packages (install using the script below):
  ```R
  install.packages(c("tinytex", "tidyverse", "readr", "haven", "ggplot2", 
                     "knitr", "report", "easystats", "patchwork", "infer", 
                     "purrr", "scales", "broom", "BFpack", "brms", "janitor", 
                     "parameters", "ggdist", "labelled", "pwr", "tidyquant", 
                     "ggthemes", "kableExtra", "httr", "jsonlite", "ggbeeswarm"))

Clone this repository: 
git clone https://github.com/your-username/SSH-MRIQCeption-Analysis.git
Open the R Markdown file (MRIQCeption_Analysis.Rmd) in RStudio.


Usage

Prepare Input Files:
Place the API JSON file (e.g., bold.json) and the local TSV file (e.g., group_bold.tsv) in accessible paths.
Update the paths in the script:
"/path/to/bold.json"  # API data
"/path/to/group_bold.tsv"  # Local data

Run the Analysis:
Execute the R Markdown file to:
Load and clean the data.
Generate Rain Cloud plots for each metric.
Produce summary tables for the top and bottom values.

Output:
Plots: Visualizations for each metric comparing local and API datasets.
Tables: Top and bottom 10 values for each metric in the local dataset.


Example Metrics Analyzed

efc (Entropy Focus Criterion)
fber (Foreground-Background Energy Ratio)
fd_mean (Mean Framewise Displacement)
snr (Signal-to-Noise Ratio)






