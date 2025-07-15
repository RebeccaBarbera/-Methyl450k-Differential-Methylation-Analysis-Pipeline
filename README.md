# Differential Methylation Analysis Pipeline
###### This project presents a full workflow for analyzing DNA methylation data obtained from the Illumina HumanMethylation450k BeadChip. The pipeline includes raw data preprocessing, quality control, normalization, and differential methylation analysis between control (CTRL) and disease (DIS) groups.

### packages neededed
#### Core Methylation Analysis:
minfi – Core package for processing Illumina methylation arrays (loading IDATs, normalization, QC, extracting Beta/M-values, etc.)
IlluminaHumanMethylation450kmanifest – Provides the manifest file with probe details
IlluminaHumanMethylation450kanno.ilmn12.hg19 – Provides annotation for the 450k array probes.

#### Visualization:
- gplots – For heatmap.2 to generate heatmaps
- qqman – For creating Manhattan plots (commonly used in genomics)
- Base R graphics – For plot(), legend(), boxplot(), density(), etc.

#### Statistical Analysis:
- stats – Base R package used for PCA (prcomp), p-value correction (p.adjust)
- minfi– Provides dmpFinder() for differential methylation analysis

#### Data Handling / Utilities:
- BiocManager – For installing Bioconductor packages
- base, utils – Core R packages used for file reading, data manipulation
- Optional / Mentioned:
BiocGenerics, S4Vectors, IRanges, GenomicRanges – Implicitly used by minfi and 450k packages (you don't call them directly)


