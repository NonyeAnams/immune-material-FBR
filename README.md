## Computational immunophenotyping of biomaterial-induced foreign body response (FBR)

## Project overview

## Title:
Computational immunophenotyping of biomaterial-induced foreign body response (FBR): immune–fibroblast programs and signaling networks across implanted materials

## Abstract 

Foreign body response (FBR) to implanted biomaterials is driven by coordinated immune and stromal processes that can culminate in chronic inflammation and fibrosis. Macrophages are central immune regulators of FBR, while fibroblasts are primary executors of extracellular matrix deposition and fibrotic remodeling. Understanding how biomaterials shape immune cell states and immune–fibroblast interactions is therefore critical for the rational design of immune-interactive materials.

In this project, we performed computational immunophenotyping of publicly available single-cell RNA sequencing data (GEO: **GSE203099**) derived from tissue surrounding implanted biomaterials. Using unbiased clustering and marker-based annotation, we defined the global immune and stromal landscape induced by biomaterial implantation. We then focused on macrophage and fibroblast compartments, resolving transcriptionally distinct sub-states and scoring biologically motivated gene programs associated with inflammation, tissue remodeling, and fibrotic extracellular matrix production. Finally, we conducted a hypothesis-generating immune–fibroblast crosstalk analysis to identify candidate macrophage-derived signaling pathways associated with fibroblast activation programs.

Together, this analysis provides a structured framework for linking biomaterial-induced immune cell states to fibrotic stromal responses, and highlights candidate signaling axes that may be targeted or modulated through biomaterial design.


## Dataset

* GEO accession: GSE203099
* Technology: Single-cell RNA sequencing
* Biological context: Immune and stromal cells isolated from tissue surrounding implanted biomaterials
* Organism:Mouse


## Project aims

Aim 1 — Global immune landscape**
Define major immune and stromal cell populations emerging following biomaterial implantation using unbiased clustering.

Aim 2 — Macrophage and fibroblast state heterogeneity**
Resolve macrophage and fibroblast sub-states associated with inflammatory versus fibrotic/remodeling transcriptional programs.

Aim 3 — Immune–fibroblast communication (hypothesis-generating)**
Infer candidate macrophage-derived signaling pathways associated with fibroblast activation and extracellular matrix programs.


## Analysis workflow

The project follows a biologically motivated single-cell analysis pipeline:

1. Quality control, normalization, and global clustering
   (`01_qc_preprocessing.ipynb`)
   Establishes a high-quality global cellular landscape.

2. Cell-type annotation and immune composition
   (`02_celltype_annotation.ipynb`)
   Assigns broad immune and stromal identities using canonical marker genes.

3. Macrophage and fibroblast state analysis
   (`03_macrophage_fibroblast_states.ipynb`)
   Subclustering and program scoring to identify inflammatory versus fibrotic-associated states.

4. Immune–fibroblast crosstalk inference
   (`04_interaction_analysis.ipynb`)
   Hypothesis-generating ligand–receptor analysis focused on macrophage → fibroblast signaling.


## Key findings 

* Biomaterial implantation induces a heterogeneous immune and stromal response dominated by macrophages and fibroblasts.
* Macrophages exhibit transcriptionally distinct states spanning inflammatory, antigen-presenting, and tissue-remodeling–associated programs.
* Fibroblast subclusters show variable enrichment of extracellular matrix, myofibroblast-like, and TGF-β–responsive gene programs.
* A subset of macrophage states displays elevated expression of genes associated with fibrotic remodeling, suggesting potential links between immune activation states and stromal outcomes.
* Candidate macrophage → fibroblast signaling pathways associated with fibrotic programs were identified in a hypothesis-generating manner.


## Limitations

* Ligand–receptor interactions are inferred from transcriptional co-expression and do not confirm active protein signaling.
* scRNA-seq data lacks spatial context, limiting interpretation of physical cell–cell interactions.
* Findings are associative and require orthogonal experimental validation.


Future directions

* Spatial transcriptomics or immunostaining to assess immune–fibroblast co-localization at biomaterial interfaces.
* Cytokine and protein-level assays to validate candidate signaling pathways. Perturbation studies to test causal roles of immune-derived signals in fibroblast activation.

## Mini-report

A concise 1–2 page report summarizing the biological motivation, methods, key findings, and interpretation is available here:

📄 `reports/Mini_Report_FBR_scRNA.pdf`

## Repository structure

immune_material_scRNA/
│
├── data/
│   ├── raw/
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
|── reports/
|   └── Mini_Report_FBR_scRNA.pdf
│
├── environment.yml
└── README.md