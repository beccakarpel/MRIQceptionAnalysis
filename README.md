# **SSH MRIQCeptionAnalysis**

This repository contains R code, written in a Quarto Markdown file (`MRIQCeptionAnalysis.qmd`), to analyze local MRIQC data and compare it to API-sourced data. The analysis includes data preparation, Rain Cloud plots, and summary tables for a comprehensive comparison of metrics.

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
- **Quarto**: For running `.qmd` files ([Install Quarto](https://quarto.org/docs/get-started/))
- **RStudio** (recommended for running the `.qmd` file)
- Required R packages:
  ```R
  install.packages(c("tinytex", "tidyverse", "readr", "haven", "ggplot2", 
                     "knitr", "report", "easystats", "patchwork", "infer", 
                     "purrr", "scales", "broom", "BFpack", "brms", "janitor", 
                     "parameters", "ggdist", "labelled", "pwr", "tidyquant", 
                     "ggthemes", "kableExtra", "httr", "jsonlite", "ggbeeswarm"))


 ## **Installation**
1. Clone this repository: git clone https://github.com/beccakarpel/MRIQCeptionAnalysis.git
2. Open the MRIQCeptionAnalysis.qmd file in RStudio or any Quarto-compatible editor.

## **Usage**

### **Prepare Input Files**
Place the API JSON file (e.g., bold.json) and the local TSV file (e.g., group_bold.tsv) in accessible paths.
Update the paths in the script:
"/path/to/bold.json"  # API data
"/path/to/group_bold.tsv"  # Local data


## **Run the Analysis**
Open the MRIQCeptionAnalysis.qmd file.
Render the file using Quarto:
In RStudio: Click the Render button.
From the terminal: Run quarto render MRIQCeptionAnalysis.qmd.
The rendered output will include:
Plots: Visualizations for each metric comparing local and API datasets.
Tables: Top and bottom 10 values for each metric in the local dataset.



## **Example Metrics Analyzed**

efc (Entropy Focus Criterion)
fber (Foreground-Background Energy Ratio)
fd_mean (Mean Framewise Displacement)
snr (Signal-to-Noise Ratio)
dvars_std (Standardized DVARS)
fwhm_avg (Average Full Width at Half Maximum)
tsnr (Temporal Signal-to-Noise Ratio)


## **Features Explained**
### **Rain Cloud Plots**
Rain Cloud plots combine boxplots, jittered data points, and density distributions. They provide an intuitive visualization of data distributions and highlight differences between local and API datasets.

### **Summary Tables**
The analysis generates tables summarizing the top and bottom 10 values for each metric. These are particularly useful for identifying patterns or outliers in the data.


