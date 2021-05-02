# NanoHack21
NanoString Spatial Omics Hackathon 2021

Our solution offers a flexible analysis and interactive visulisation workflow for exploration of the NanoString GeoMx® Digital Spatial Profiler data.
Here we demonstrate it on the NanoString GeoMx® human kidney dataset in conjunction with the publicly available signle cell RNA sequencing (scRNA-seq) reference dataset of human kidney from [Young et al., Science 2018](https://science.sciencemag.org/content/361/6402/594.editor-summary). This approach can also be used for other such datasets.

The solution consists of:
1. Unbiased analysis of the NanoString GeoMx® whole transcriptome dataset
2. Interactive web-based visualisation of the NanoString GeoMx® dataset
3. Analysis of cell-cell communication networks and their dysregulation in context of kidney disease


To perform the analyses included in this solution, the user will need to provide the following files:
- NanoString GeoMx® human kidney dataset (or other NanoString GeoMx® dataset)
- Signle cell RNA sequencing (scRNA-seq) reference dataset of human kidney from [Young et al., Science 2018](https://science.sciencemag.org/content/361/6402/594.editor-summary) (or other scRNA-seq reference dataset)


## 1.

## 2.

## 3. Cell-cell communication analysis

Using [CellPhoneDB](https://www.cellphonedb.org/)

CellPhoneDB is a publicly available repository of curated receptors (R), ligands (L) and their interactions.

Here we implement an approach adapted for NanoString GeoMx® Digital Spatial Profiler data. To correctly infer expression of genes encoding ligands and receptors in cell types present in NanoString data, we use it in conjunction with a publicly accessible signle cell RNA sequencing (scRNA-seq) reference dataset from [Young et al., Science 2018](https://science.sciencemag.org/content/361/6402/594.editor-summary) that has been prior used to perform cell type deconvolution of each NanoString region of interest (ROI).

The proposed pipeline consists of the following steps:
1. Preparing files containing manually curated L/R interactions (notebook S0)
2. Generating the CellPhone database (notebook S1)
3. Preparing the signle cell RNA sequencing (scRNA-seq) dataset for CellPhoneDB (notebook S2)
4. Extracting all interactions from the scRNA-seq reference dataset (notebook S3)
5. Performing differential expression (DE) analysis of the NanoString ROIs (notebook S4)

    (here the user can focus on a particular comparison of interest, in this demonstrative workflow we compare abnormal and healthy glomeruli, as annotated by pathology in NanoString dataset, to explore potential dysregulation of cell-cell communication networks in abnormal glomeruli)


6. Intersecting the DE genes from (5) with all possible interactions between cell types colocated in space as inferred from prior cell type deconvolution of each NanoString ROI using scRNA-seq reference dataset.
7. Visualising results


Our approach offers the user flexibility in choice of parameters in the analysis workflow which includes 
comparison of interest and various statistical 



# prerequisite
## Creating conda env

**conda env create -f environment.yml**

to install the kernel into your Jupyter notebook

**python -m ipykernel install --user --name nanostring-hack-2021 --display-name "Nanostring Hack 2021"**

