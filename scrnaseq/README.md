# sc/sn-RNA-seq pipeline for [dGTEx and NHP-dGTEx Consortiums](https://test.gtexportal.org/)

This repository contains all components of the scRNA-seq/snRNA-seq pipeline used by the dGTEx and NHP-dGTEx Consortiums, including preprocessing, alignment, quantification, and quality control.

<!---
## Docker image
The GTEx RNA-seq pipeline is provided as a Docker image, available at https://hub.docker.com/r/broadinstitute/gtex_rnaseq/

To download the image, run:
```bash
docker pull broadinstitute/gtex_rnaseq:V10
```
-->

#### Pipeline components
The following are various components of our pipeline (some essential and some optional):
* [Cellranger](https://support.10xgenomics.com/single-cell-gene-expression/software/overview/welcome): generating single cell 3’ RNA-seq Gene Expression (GEX) data
* [Cellranger atac](https://support.10xgenomics.com/single-cell-atac/software/overview/welcome): generating single cell ATAC data produced by the 10x Genomics Chromium platform
* [Cellranger arc](https://support.10xgenomics.com/single-cell-multiome-atac-gex/software/overview/welcome): generating chromatin accessibility and 3' gene expression data from the same cell produced by the 10x platform
* [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/): sequencing quality control
* [Souporcell](https://github.com/wheaton5/souporcell): clustering mixed-genotype scRNAseq experiments by individual
* [CellBender](https://github.com/broadinstitute/CellBender): eliminating technical artifacts from high-throughput scRNA-seq data

Versions used across our releases:
|         | V1      | post-V1 |
| ------- | ------- | -------|
| Cellranger      | [v7.2.0](https://console.cloud.google.com/storage/browser/_details/d-nhp-gtex-resources/software/cellranger-7.2.0.tar.gz;tab=live_object) | |
| Cellranger-atac | [v2.1.0](https://console.cloud.google.com/storage/browser/_details/d-nhp-gtex-resources/software/cellranger-atac-2.1.0.tar.gz;tab=live_object) | |
| Cellranger-arc  | [v2.0.2](https://console.cloud.google.com/storage/browser/_details/d-nhp-gtex-resources/software/cellranger-arc-2.0.2.tar.gz;tab=live_object) | |
| Cellbender      |   |  |
| Souporcell      |   |  |
| Genome          | GRCh38/hg38  |  |
| GENCODE         | [v45](https://www.gencodegenes.org/human/release_45.html) |  |


##  Setup steps
#### Reference genome and annotation
All reference files and softwares are available at [gs://d-nhp-gtex-resources](https://console.cloud.google.com/storage/browser/d-nhp-gtex-resources).

#### Building cellranger references
Instead of prebuilt cellranger references, custom references were built using new GENCODE version (as specified in the table)
```bash
# build the cellranger reference:
ToDo

# build the cellranger-atac reference:
ToDo

# build the cellranger-arc reference:
ToDo
```

## Running the pipeline
We run various components of pipeline in the following way:
* Cellranger: [cumulus workflow]()
* Cellbender:
* Souporcell: [cumulus workflow]()
