# README
# Acute Myeloid Leukemia Heatmap Analysis Documentation 
======================

A bioinformatics analysis pipeline for visualizing RNA-seq data from acute myeloid leukemia (AML) samples using clustering heatmaps.

## Overview
--------

This project analyzes RNA-seq data from 19 AML model mice samples 
, focusing on treatment responses in IDH2 and TET2 mutant AML models. The analysis uses the pheatmap package for visualization and includes comprehensive data preprocessing and quality control steps.

## Project Structure
-----------------

```markdown
aml_heatmap_analysis/
├── data/
│   └── SRP070849/
│       ├── SRP070849.tsv
│       └── metadata_SRP070849.tsv
├── plots/
│   └── aml_heatmap.png
├── results/
│   └── top_90_var_genes.tsv
└── analysis.Rmd
```

## Requirements
------------

### R Packages

* pheatmap
* magrittr
* readr
* dplyr
* tibble
* sessioninfo

### Data Files

* RNA-seq expression data (SRP070849.tsv)
* Sample metadata (metadata_SRP070849.tsv)

## Installation
------------

```r
# Install required packages
if (!("pheatmap" %in% installed.packages())) {
    install.packages("pheatmap")
}
if (!("magrittr" %in% installed.packages())) {
    install.packages("magrittr")
}
if (!("readr" %in% installed.packages())) {
    install.packages("readr")
}
if (!("dplyr" %in% installed.packages())) {
    install.packages("dplyr")
}
if (!("tibble" %in% installed.packages())) {
    install.packages("tibble")
}
if (!("sessioninfo" %in% installed.packages())) {
    install.packages("sessioninfo")
}
```

## Usage
-----

1. Clone the repository:
```bash
git clone https://github.com/your-username/aml_heatmap_analysis.git
```

2. Download the required data files from [refine.bio](https://www.refine.bio/experiments/SRP070849) and place them in the `data/SRP070849/` directory.

3. Run the analysis:
```r
# Set working directory
setwd("path/to/aml_heatmap_analysis")

# Run the analysis
rmarkdown::render("analysis.Rmd")
```

## Output Files
--------------

* `plots/aml_heatmap.png`: The final annotated heatmap visualization
* `results/top_90_var_genes.tsv`: Genes selected for the heatmap (top 25% by variance)

## Citation
--------

This analysis uses data from Shih et al., 2017 
. The code structure is adapted from the [refine.bio-examples notebook](https://alexslemonade.github.io/refinebio-examples/03-rnaseq/clustering_rnaseq_01_heatmap.html).

## Contributing
------------

Contributions are welcome! Please submit pull requests with:
1. Clear documentation of changes
2. Updated session info
3. Maintained code style consistency

## License
-------

[MIT License](LICENSE)
