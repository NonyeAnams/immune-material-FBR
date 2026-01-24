# Computational Immunophenotyping of Biomaterial-Induced Foreign Body Response

This repository contains an independent mini-project analyzing immune and stromal responses to biomaterial implantation using publicly available single-cell RNA sequencing (scRNA-seq) data. The project focuses on macrophage and fibroblast transcriptional states and explores candidate immune–stromal communication programs associated with fibrotic remodeling.

---

## Biological Question

How do implanted biomaterials shape immune cell states—particularly macrophages—and how are these immune programs associated with fibroblast activation and fibrotic remodeling?

---

## Dataset

- **Source:** Gene Expression Omnibus (GEO)
- **Accession:** GSE203099
- **Description:** Single-cell RNA-seq profiles from biomaterial implantation sites capturing immune and stromal cell populations during foreign body response.

Raw data are not included in this repository and can be obtained directly from GEO.

---

## Analysis Overview

The analysis follows a biologically motivated workflow:

1. Quality control, normalization, and global clustering of all cells
2. Annotation of major immune and stromal cell types
3. Subclustering and functional characterization of macrophage states
4. Identification of fibroblast activation programs associated with extracellular matrix production
5. Hypothesis-generating analysis of macrophage–fibroblast ligand–receptor interactions

---

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
---

## Key Results

- Macrophages and monocytes dominate the immune landscape following biomaterial implantation, alongside fibroblasts and other immune subsets.
- Macrophages exhibit substantial functional heterogeneity, including inflammatory, interferon-associated, antigen presentation, and tissue remodeling–associated states.
- A subset of macrophage states is enriched for pro-fibrotic–associated gene programs.
- Fibroblasts display diverse activation programs, including ECM-high and TGF-β–responsive states consistent with fibrotic remodeling.
- Ligand–receptor analysis identifies candidate macrophage–fibroblast signaling pathways associated with fibrotic fibroblast programs.

All identified interactions are transcriptionally inferred and hypothesis-generating.

---

## Methods Summary

- Single-cell analysis performed using **Scanpy**
- Program scoring based on curated biologically motivated gene sets
- Ligand–receptor analysis focused on known immune–stromal signaling axes
- Visualization using Matplotlib and Scanpy plotting functions

Details are provided in the notebooks and the accompanying mini-report.

---

## Reproducibility

To reproduce the analysis:

```bash
conda env create -f environment.yml
conda activate immune_material
```
- Run notebooks sequentially from 01_qc_preprocessing.ipynb to 04_interaction_analysis.ipynb.


## Limitations

- Analysis is based on a single publicly available dataset
- Transcriptional associations do not imply causality
- Ligand–receptor interactions are inferred and require experimental validation

## Author
Chinonye Precious Anams

MSc Cell Biology and Genetics

Independent project (2026)
