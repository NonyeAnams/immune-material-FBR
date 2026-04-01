# Computational Immunophenotyping of Biomaterial-Induced Foreign Body Response
This project presents a computational analysis of immune and stromal cell dynamics following biomaterial implantation, using publicly available single-cell RNA sequencing (scRNA-seq) data.

The study focuses on macrophage functional heterogeneity and fibroblast activation programs, with the goal of identifying transcriptional signatures and candidate immune–stromal interactions associated with fibrotic remodeling.

## Biological Question
How does biomaterial implantation reshape immune cell states—particularly macrophages—and how are these immune programs linked to fibroblast activation and fibrosis-associated remodeling?

## Dataset
- **Source:** Gene Expression Omnibus (GEO)
- **Accession:** GSE203099
- **Description:** Single-cell RNA-seq profiles from biomaterial implantation sites capturing immune and stromal cell populations during foreign body response.
  | Raw data are not included in this repository and can be obtained directly from GEO.

## Analysis Overview
The analysis follows a structured workflow:
- Quality control, normalization, and global clustering
- Annotation of major immune and stromal cell populations
- Subclustering and transcriptional characterization of macrophage states
- Identification of fibroblast activation programs associated with extracellular matrix (ECM) production
- Exploratory analysis of macrophage–fibroblast ligand–receptor interactions

## Repository Structure
```
immune_material_scRNA/
│
├── data/
│   ├── raw/ # Not included (available from GEO)
│   └── processed/
│
├── notebooks/
│   ├── 01_qc_preprocessing.ipynb
│   ├── 02_celltype_annotation.ipynb
│   ├── 03_macrophage_fibroblast_states.ipynb
│   └── 04_interaction_analysis.ipynb
│
├── figures/
|
|──Mini_Report_FBR_scRNA.pdf
|   
│
├── environment.yml
└── README.md
```

## Key Results
- Immune infiltration following biomaterial implantation is dominated by macrophages/monocytes, alongside fibroblasts and additional immune subsets
- Macrophages exhibit pronounced functional heterogeneity, including:
  - inflammatory states
  - interferon-responsive programs
  - antigen presentation signatures
  - tissue remodeling–associated profiles
- A subset of macrophage populations is enriched for pro-fibrotic transcriptional programs
- Fibroblasts display diverse activation states, including:
  - ECM-producing (fibrotic) programs
  - TGF-β–responsive phenotypes
- Ligand–receptor analysis identifies candidate macrophage–fibroblast signaling interactions associated with fibrotic remodeling

  | All inferred interactions are transcriptional and hypothesis-generating.
  
## Methods Summary
- Single-cell analysis performed using Scanpy
- Gene program scoring based on curated, biologically relevant gene sets
- Ligand–receptor analysis focused on known immune–stromal signaling pathways
- Data visualization using Matplotlib and Scanpy plotting functions
Detailed methodology is provided in the notebooks and accompanying report.

## Reproducibility
To reproduce the analysis:
```bash
conda env create -f environment.yml
conda activate immune_material
```
Run notebooks sequentially:
  1. 01_qc_preprocessing.ipynb
  2. 02_celltype_annotation.ipynb
  3. 03_macrophage_fibroblast_states.ipynb
  4. 04_interaction_analysis.ipynb

## Limitations
- Analysis is based on a single dataset
- Transcriptional signatures do not establish causality
- Ligand–receptor interactions are inferred and require experimental validation

## Author
**Chinonye Precious Anams**      
MSc Cell Biology and Genetics

Independent bioinformatics project (2026)
