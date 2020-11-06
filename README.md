# ST-analysis
General notes and resources on how to analyze Spatial Transcriptomics data

## Resources of interest
- http://spatialomics.net/

## Software to handle ST data

### R
- [Seurat v3.2](https://satijalab.org/seurat/v3.2/spatial_vignette.html) developed by Rahul Satija lab.
- [STUtility](https://github.com/jbergenstrahle/STUtility) developed by Joseph Bergenstråhle and Ludvig Larsson from  Joakim Lundeberg lab.
- [Giotto](http://spatialgiotto.rc.fas.harvard.edu/) developed by Ruben Dries from Guo-Cheng Yuan lab.

### Python
- [scanpy](https://scanpy-tutorials.readthedocs.io/en/latest/spatial/basic-analysis.html) developed by Giovanni Palla from Fabian Theis Lab.
- [Tangram](https://github.com/broadinstitute/Tangram) Tangram is a Python package, written in PyTorch, for mapping single-cell (or single-nucleus) gene expression data onto spatial gene expression data. The single-cell dataset and the spatial dataset should be collected from the same anatomical region/tissue type, ideally from a biological replicate, and need to share a set of genes (usually from twenty to a thousand). Tangram aligns the single-cell data in space by fitting gene expression on those genes. We mostly work with transcriptomic data (typically 10Xv3 for scRNAseq data; MERFISH or Visium as spatial data).
- [stLearn](https://www.biorxiv.org/content/10.1101/2020.05.31.125658v1.full) with the corresponding [vignette](https://stlearn.readthedocs.io/en/latest/). Developed by Duy Pham from Quan Nguyen lab. We have developed an analysis method that exploits all three data types: Spatial distance, tissue Morphology, and gene Expression measurements (SME) from ST data. This combinatorial approach allows us to more accurately model underlying tissue biology, and allows researchers to address key questions in three major research areas: cell type identification, cell trajectory reconstruction, and the study of cell-cell interactions within an undissociated tissue sample.

### Tools of interest
- [SpatialDE](https://www.nature.com/articles/nmeth.4636) developed by Valentine Svensson. A statistical test to identify genes with spatial patterns of expression variation from multiplexed imaging or spatial RNA-sequencing data.
- [MISTy](https://saezlab.github.io/misty/) developed by Jovan Tanevski from Saez-Rodriguez lab.  Multiview Intercellular SpaTial modeling framework (**MISTy**) is an explainable machine learning framework for knowledge extraction and analysis of single-cell, highly multiplexed, spatially resolved data. MISTy facilitates an in-depth understanding of marker interactions by profiling the intra- and intercellular relationships.
- [PROGENy](https://www.bioconductor.org/packages/release/bioc/vignettes/progeny/inst/doc/ProgenySingleCell.html). Developed by Alberto Valdeolivas from Saez-Rodriguez lab. Estimates the activity of 14 relevant signaling pathways based on consensus gene signatures obtained from perturbation experiments.
- [Omnipath](https://saezlab.github.io/OmnipathR/articles/OmnipathMainVignette.html) Saez-Rodriguez lab. A comprehensive collection of molecular biology prior knowledge from 103 databases, with focus on literature curated human and rodent signaling pathways. Software suite for functional omics data analysis and mechanistic modeling of intra- and inter-cellular signaling.
- [DOROTHEA](https://bioconductor.org/packages/release/data/experiment/html/dorothea.html) Saez-Rodriguez lab.This package contains human and mouse TF regulons. The human regulons were curated and collected from different types of evidence such as literature curated resources, ChIP-seq peaks, TF binding site motifs and interactions inferred directly from gene expression. The mouse regulons were constructed by mapping the human gene symbols to their orthologs in mice. Those regulons can be coupled with any statistical method that aims to analyse gene sets to infer TF activity from gene expression data. Preferably the statistical method viper is used.
- [Histolab](https://github.com/histolab/histolab) The aim of this project is to provide a tool for Whole Slide Images (WSI) processing in a reproducible environment to support clinical and scientific research. Histolab is designed to handle WSIs, automatically detect the tissue, and retrieve informative tiles, and it can thus be integrated in a deep learning pipeline.
- [Spaniel](https://www.biorxiv.org/content/10.1101/619197v1) developed by Rachel Queen
- [starmapVR](https://github.com/holab-hku/starmapVR) developed by Andrian Yang to visualize single-cell and spatial omic data in 3D
- [Baysor](https://www.biorxiv.org/content/10.1101/2020.10.05.326777v1.full) developed by Viktor Petukhov from Kharchenko lab. Bayesian Segmentation of Spatial Transcriptomics Data (**-ISH + In situ sequencing**) (Baysor), which optimizes segmentation considering the likelihood of transcriptional composition, size and shape of the cell. The Bayesian approach can take into account nuclear or cytoplasm staining, however can also perform segmentation based on the detected transcripts alone.
- [MEFISTO](https://biofam.github.io/MOFA2/MEFISTO.html) developed by Britta Velten, it is a flexible and versatile toolbox for modelling high-dimensional data when spatial or temporal dependencies between the samples are known. MEFISTO maintains the established benefits of factor analysis for multi-modal data, but enables performing spatio-temporally informed dimensionality reduction, interpolation and separation of smooth from non-smooth patterns of variation. Moreover, MEFISTO can integrate multiple related datasets by simultaneously identifying and aligning the underlying patterns of variation in a data-driven manner.

#### Deconvolution tools
- [SPOTlight](https://github.com/MarcElosua/SPOTlight) developed by Marc Elosua from Holger Hey lab.
- [Stereoscope](https://github.com/almaan/stereoscope) developed by Alma Andersson from Lundeberg Lab.
- [cell2location](https://github.com/BayraktarLab/cell2location) developed by Vitalii Kleshchevnikov from Bayraktar lab. 
- [Robust Cell Type Decomposition](https://github.com/dmcable/RCTD) developed by Dylan M. Cable from Irizarry lab.

#### Cell-Cell interactions
- [CellPhoneDB](https://github.com/Teichlab/cellphonedb) developed by Roser Vento. CellPhoneDB is a publicly available repository of curated receptors, ligands and their interactions. Subunit architecture is included for both ligands and receptors, representing heteromeric complexes accurately. This is crucial, as cell-cell communication relies on multi-subunit protein complexes that go beyond the binary representation used in most databases and studies.
- [scTalk](https://github.com/VCCRI/scTalk/) developed by Farbehi. N scTalk is an R package for intercellular communication (ligand-receptor) analysis from scRNA-seq data and implements the method described in [Farbehi et al](https://elifesciences.org/articles/43882).
- [NATMI](https://www.nature.com/articles/s41467-020-18873-z) developed by Rui Hou. NATMI uses connectomeDB2020 (a database of 2293 manually curated ligand-receptor pairs with literature support) to predict and visualise cell-to-cell communication networks from single-cell (or bulk) expression data. GitHub repo [here](https://github.com/forrest-lab/NATMI/).

#### Deep learning tools
- [Deeplearning-digital-pathology](https://github.com/zhaoxuanma/Deeplearning-digital-pathology) This repository contains utilities for virtual slides and images classification and semantic segmentation with Keras and Caffe and an extension class of ImageDataGenerator of Keras to generate batches of images with data augmentation for segmentation. Demo code is provided for reference.
## General Comments
Things to keep in mind when pre-processing the data

- Optimal Read length for confident mapping Spaceranger v1.1.0
<img src="img/spaceranger-v1.1.0_read-length.png" width="500">
- Make sure the slice images form the Visium slide contain all the dotted borders and corners. These are necessary to automatically align the image and the spots.

## QC
[STUtility](https://ludvigla.github.io/STUtility_web_site/Quality_Control.html) shows a great workflow on how to carry out QC analysis on ST data!
- Remove all spots not overlapping tissue. When there are tissueless regions within the capture areas, especially within the tissue there might be some lateral diffusion and reads may map to those spots. It is important to remove those spots manually using spaceranger prior to alignment!
- Before processing the data check that there are no empty spots overlaying the tissue.
- Explore number of reads and genes on the slice
- Explore mitochondrial content on the slice
```
mt.genes <- grep(pattern = "^MT-")
```
- Explore ribosomal content on the slice
```
ribo.genes <- grep(pattern = "^RPL|^RPS")
```
- No hard thresholds are set to remove spots based on the prior parameters. It is important to understand the biology of the tissue under study in order to process the data accordingly. 
