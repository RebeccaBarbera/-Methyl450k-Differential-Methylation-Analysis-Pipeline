# Differential Methylation Analysis Pipeline
#### This project presents a full workflow for analyzing DNA methylation data obtained from the Illumina HumanMethylation450k BeadChip. The pipeline includes raw data preprocessing, quality control, normalization, and differential methylation analysis between control (CTRL) and disease (DIS) groups.

### Packages neededed
#### Core Methylation Analysis:
| Package                                                                                     | Purpose                                                              |
| ------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| **`minfi`**                                                                                 | Main package for analyzing Illumina methylation arrays.              |
| **`BiocManager`**                                                                           | For installing and managing Bioconductor packages.                   |
| **`IlluminaHumanMethylation450kmanifest` / `IlluminaHumanMethylation450kanno.ilmn12.hg19`** | Annotation packages for the 450K array.                              |
| **`limma`**                                                                                 | (Often used alongside `minfi` for linear modeling and DMP analysis). |
| **`ggplot2`**                                                                               | For visualization and plotting.                                      |
| **`reshape2` or `tidyverse`**                                                               | For data wrangling and formatting.                                   |
| **`knitr` / `rmarkdown`**                                                                   | For generating the HTML report output.                               |
| **`qqman`**                                                                                 | Fpr creating MAnhatta  plots (commonlu used in genomics              |
#### Addtional packages 
| Package                                         | Purpose                                         |
| ----------------------------------------------- | ----------------------------------------------- |
| **`GenomicRanges`**, **`SummarizedExperiment`** | For genomic data structures used by `minfi`.    |
| **`Illumina450Manifest_clean.RData`**           | External annotation file loaded at the start.   |
| **`dmpFinder`** (function from `minfi`)         | Identifies differentially methylated positions. |

#### Additional packages

| **Package**                                                       | **Purpose / Description**                                                                                                                                              
| --------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| **BiocManager**                                                 | Installs and manages Bioconductor packages required for methylation analysis.                                                                                          |
| **base**, **utils**                                             | Core R packages used for file input/output, data manipulation, and basic R functions.                                                                                  |
| **BiocGenerics**, **S4Vectors**, **IRanges**, **GenomicRanges** | Implicitly used by `minfi` and related Illumina 450K packages for genomic data structures and efficient data representation (not usually loaded directly by the user). |
