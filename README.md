# SenNet Manuscript
This repository contains the code and data used to reproduce the analyses in the SenNet manuscript "**Senescence Chromatin-Activated Retrotransposons in Stromal Microenvironment Promotes Hematopoietic Aging and Malignancy**", including sequence-based SenNet models and single-cell transcriptomic/epigenomic analyses.

## SenNet
The [SenNet](SenNet/) folder includes code for all SenNet deep learning models across scRNA-seq, TSS (GRO-Cap), H3K27ac, and ATAC modalities. Note: BigWig signals required for model training should be downloaded from the corresponding GEO datasets.
- [SenNet_RNA.ipynb](SenNet/SenNet_RNA.ipynb) It contains code for SenNet-RNA model to evaluate the senescent level from scRNA-seq dataset. 
- [SenNet_TSS.ipynb](SenNet/SenNet_TSS.ipynb) It contains the SenNet-TSS sequence model to learn the senescent-related motifs from GRO-Cap data. 
- [SenNet_H3K27ac.ipynb](SenNet/SenNet_H3K27ac.ipynb) SenNet-H3K27ac model is used to capture the sequence dependents for H3K27ac activation of RLTR6/MMVL30. 
- [SenNet_ATAC.ipynb](SenNet/SenNet_ATAC.ipynb) SenNet-ATAC model is used to capture the sequence dependents for ATAC signal activation of RLTR6/MMVL30. 

## scRNA_scATAC
The [scRNA_scATAC](scRNA_scATAC/) folder contains the scRNA and scATAC analyses code for hematopoietic and non hematopoietic cells from mouse bone marrow in Jupyter Notebook format. Please download the relevant scRNA-seq and scATAC-seq datasets from GEO before running these analyses.
- [All_bone_marrow.ipynb](scRNA_scATAC/All_bone_marrow.ipynb) It contains code for tSNE plot of all bone marrow cells scRNA-seq data.
- [NonHematopoietic_bone_marrow.ipynb](NonHematopoietic_bone_marrow.ipynb) The code for analyzing stromal cells from young and aged mouse bone marrow.
- [Progeria_bone_marrow.ipynb](Progeria_bone_marrow.ipynb) The scRNA-seq data analyses of bone marrow stromal cells from Progeria mouse model.
- [scATAC_bonemarrow.ipynb](scATAC_bonemarrow.ipynb) Chromatin accessibility of young and aged mouse bone marrow stromal cells. 

## Data
[Data](Data/) contains datasets required to reproduce part of the analysis.

Large files are hosted on [Zenodo](https://zenodo.org/records/17620290) :
Included files:
- Individial_TE_timeseries_UniqueQuantify_correlation_combineFullLength.txt
- SenNet_RNA.torch

## Dependencies
The R and python environment can be set up through Anaconda or pip.
SenNet model are estabilished on pytorch framework. The bigwig signal are processing through [Selene](https://github.com/kathyxchen/selene.git). 
scRNA-seq and scATAC-seq data analyses require R packages such as Seurat, ggplot2, viridis, reshape2 and Signac.


