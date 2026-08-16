# HER2 Computational Oncology Portfolio

## Integrated Computational Investigation of HER2-Positive Breast Cancer

This portfolio presents an integrated **computational oncology and bioinformatics workflow focused on HER2-positive breast cancer**.

The project combines structural bioinformatics, drug discovery, molecular docking, molecular dynamics simulation, RNA-Seq analysis, and functional enrichment analysis to investigate HER2-associated molecular mechanisms and potential therapeutic insights.

The portfolio was developed as a practical demonstration of computational biology and bioinformatics skills using publicly available biological data, established computational tools, and reproducible analysis workflows.

---

##  Project Objectives

The major objectives of this portfolio were to:

* Prepare and analyze the HER2 target protein structure.
* Screen phytochemicals for drug-likeness and ADMET properties.
* Investigate protein–ligand interactions through molecular docking.
* Evaluate the stability of a protein–ligand complex using molecular dynamics simulation.
* Perform RNA-Seq quality control, preprocessing, and genome alignment.
* Perform Gene Ontology and KEGG pathway enrichment analysis.
* Integrate structural, molecular, transcriptomic, and functional perspectives of HER2-associated breast cancer biology.

---

#  Overall Computational Workflow

```text
                    HER2-Positive Breast Cancer
                              │
                              ▼
                     HER2 Target Selection
                         PDB: 5TDN
                              │
              ┌───────────────┴───────────────┐
              ▼                               ▼
       Structural Analysis              Phytochemical
       & Protein Preparation              Screening
              │                               │
              │                         ADMET Analysis
              │                               │
              └───────────────┬───────────────┘
                              ▼
                    Molecular Docking
                              │
                              ▼
                 Protein–Ligand Interactions
                              │
                              ▼
                 100 ns Molecular Dynamics
                         Simulation
                              │
                              ▼
                   Molecular Stability
                         Analysis
                              │
                              │
        ┌─────────────────────┴─────────────────────┐
        ▼                                           ▼
     RNA-Seq                              Functional Enrichment
     Analysis                                  Analysis
        │                                           │
   FASTQC / QC                                GO Analysis
        │                                           │
   Preprocessing                              KEGG Analysis
        │                                           │
   HISAT2 / hg38                                   │
        │                                           │
        └─────────────────────┬─────────────────────┘
                              ▼
                   Integrated Interpretation
```

---

#  Projects

| Project                  | Description                                                         | Status    |
| ------------------------ | --------------------------------------------------------------------| ----------|
| 01_Protein_Preparation   | HER2 (5TDN) protein preparation and structural analysis             | Completed |
| 02_ADMET_Analysis        | ADMET screening of *Ventilago madraspatana* phytochemicals          | Completed |
| 03_Molecular_Docking     | Molecular docking of selected phytochemicals against HER2           | Completed |
| 04_Molecular_Dynamics    | 100 ns molecular dynamics simulation of the HER2–ligand complex     | Completed |
| 05_RNASeq_Galaxy         | RNA-Seq quality control, preprocessing and alignment using Galaxy   | Completed |
| 06_Functional_Enrichment | GO and KEGG functional enrichment analysis of HER2-associated genes | Completed |

---

# 1️⃣ Protein Preparation of HER2

## Objective

The HER2 receptor protein was prepared for downstream computational analysis and molecular docking.

### Target Information

* **Target:** HER2
* **PDB ID:** 5TDN
* **Disease Context:** HER2-positive breast cancer
* **Analysis Area:** Structural Bioinformatics

### Major Steps

* Retrieval of the HER2 protein structure.
* Protein structure inspection.
* Removal of unwanted molecules where appropriate.
* Protein preparation for docking.
* Structural quality assessment.
* Ramachandran plot analysis.

### Tools Used

* Protein Data Bank (PDB)
* Discovery Studio Visualizer
* PyMOL

The prepared HER2 structure was subsequently used as the receptor for molecular docking studies.

---

# 2️⃣ ADMET Screening of Phytochemicals

## Objective

Phytochemicals obtained from *Ventilago madraspatana* were evaluated for drug-likeness and pharmacokinetic properties before molecular docking.

### Dataset

A set of phytochemical compounds from *Ventilago madraspatana* was screened computationally.

### Major Steps

* Identification of phytochemical compounds.
* Retrieval of compound information.
* SMILES retrieval using PubChem.
* Evaluation of physicochemical properties.
* Assessment of drug-likeness.
* Prediction of ADME properties.
* Evaluation of toxicity-related parameters.

### Tools Used

* IMPPAT
* PubChem
* SwissADME

The ADMET screening helped prioritize compounds with comparatively favorable computational drug-like properties for subsequent molecular docking analysis.

---

# 3️⃣ Molecular Docking Against HER2

## Objective

Molecular docking was performed to investigate the potential binding of selected *Ventilago madraspatana* phytochemicals to the HER2 target protein.

### Major Steps

* Preparation of receptor and ligand structures.
* Conversion and preparation of ligand files.
* Definition of the docking region.
* Molecular docking using PyRx.
* Ranking of docked compounds.
* Analysis of binding interactions.
* Visualization of protein–ligand interactions.

### Interaction Analysis

The docked complexes were examined using structural visualization to investigate interactions such as:

* Hydrogen bonding
* Hydrophobic interactions
* Van der Waals interactions
* Other ligand–protein contacts

### Tools Used

* PyRx
* Discovery Studio Visualizer
* PubChem
* PDB

The docking analysis provided a computational assessment of the potential binding behavior of the selected phytochemicals toward HER2.

---

# 4️⃣ Molecular Dynamics Simulation

## Objective

A **100 ns molecular dynamics (MD) simulation** was performed to investigate the dynamic stability and behavior of the selected HER2–ligand complex.

### Simulation Analysis

The trajectory was evaluated using several structural and dynamic parameters:

* Root Mean Square Deviation (RMSD)
* Root Mean Square Fluctuation (RMSF)
* Radius of Gyration (Rg)
* Solvent Accessible Surface Area (SASA)
* Principal Component Analysis (PCA)
* Dynamic Cross-Correlation Matrix (DCCM)
* MM/GBSA-based binding energy analysis

### Major Parameters

**RMSD:** Used to evaluate overall structural stability during the simulation.

**RMSF:** Used to assess residue-level flexibility.

**Radius of Gyration:** Used to evaluate compactness of the protein structure.

**SASA:** Used to assess changes in solvent exposure.

**PCA:** Used to investigate dominant collective motions.

**DCCM:** Used to analyze correlated and anti-correlated residue motions.

**MM/GBSA:** Used to estimate protein–ligand binding energetics.

### Tools Used

* CHARMM-GUI
* GROMACS
* Molecular dynamics analysis tools

The 100 ns simulation provided a dynamic perspective of the HER2–ligand complex beyond static molecular docking.

---

# 5️⃣ RNA-Seq Analysis Using Galaxy

## Objective

RNA-Seq data associated with HER2-positive breast cancer were analyzed using the **Galaxy platform** to demonstrate a reproducible NGS data-processing workflow.

### Major Steps

```text
Raw FASTQ Data
      ↓
FASTQC
      ↓
Raw Quality Assessment
      ↓
Quality Trimming / Preprocessing
      ↓
Post-Trimming FASTQC
      ↓
HISAT2 Alignment
      ↓
Human hg38 Reference Genome
      ↓
Aligned RNA-Seq Reads
```

### Quality Control

FASTQC was used to evaluate:

* Basic sequencing statistics
* Per-base sequence quality
* Per-sequence quality
* Per-base sequence content
* GC content
* Sequence duplication levels
* Overrepresented sequences
* Per-base N content
* Sequence length distribution

### Preprocessing

The sequencing reads were processed to remove low-quality regions and adapter contamination before alignment.

Post-trimming FASTQC was performed to assess the quality of the processed reads.

### Genome Alignment

The processed reads were aligned to the **human hg38 reference genome using HISAT2**.

### Tools Used

* Galaxy
* FASTQC
* HISAT2
* NCBI SRA
* Human hg38 reference genome

This project demonstrates practical experience in NGS quality control, RNA-Seq preprocessing, and genome alignment.

---

# 6️⃣ Functional Enrichment Analysis

## Objective

Functional enrichment analysis was performed on HER2-associated genes to identify enriched biological functions and pathways.

Two major functional analysis approaches were used:

* Gene Ontology (GO)
* KEGG pathway enrichment

---

## Gene Ontology Analysis

GO enrichment analysis was performed across three categories.

### Biological Process (BP)

Identifies biological processes significantly represented within the selected gene set.

### Cellular Component (CC)

Identifies cellular structures and compartments associated with the gene products.

### Molecular Function (MF)

Identifies molecular activities and functions associated with the genes.

---

## KEGG Pathway Analysis

KEGG enrichment analysis was performed to identify biological pathways associated with the HER2-related gene set.

The analysis provides pathway-level information that complements individual gene-level interpretation.

### Visualization

The enrichment results were visualized using:

* GO Biological Process bar plots
* GO Cellular Component bar plots
* GO Molecular Function bar plots
* KEGG pathway bar plots
* Corresponding enrichment result tables

### Tools Used

* R
* Bioconductor
* Gene Ontology
* KEGG

This project provides a functional and pathway-level interpretation of HER2-associated molecular biology.

---

#  Software & Tools

The portfolio uses a range of computational biology and bioinformatics tools.

### Structural Bioinformatics

* Protein Data Bank (PDB)
* PyMOL
* Discovery Studio Visualizer

### Drug Discovery

* IMPPAT
* PubChem
* SwissADME
* PyRx

### Molecular Dynamics

* CHARMM-GUI
* GROMACS

### NGS & Transcriptomics

* Galaxy
* FASTQC
* HISAT2
* NCBI SRA
* Human hg38 reference genome

### Functional Genomics

* R
* Bioconductor
* Gene Ontology
* KEGG

---

#  Research Focus

| Parameter          | Details                                                                                  |
| ------------------ | ---------------------------------------------------------------------------------------- |
| **Disease**        | HER2-positive breast cancer                                                              |
| **Target Gene**    | ERBB2 / HER2                                                                             |
| **Target Protein** | HER2                                                                                     |
| **PDB ID**         | 5TDN                                                                                     |
| **Ligand Source**  | *Ventilago madraspatana* phytochemicals                                                  |
| **Research Area**  | Computational Oncology                                                                   |
| **Approaches**     | Structural Bioinformatics, Drug Discovery, MD Simulation, RNA-Seq, Functional Enrichment |

---

#  Integrated Research Approach

The portfolio combines multiple computational approaches rather than relying on a single analysis method.

### Structural Perspective

HER2 protein preparation and structural analysis provide the foundation for receptor-based computational studies.

### Drug Discovery Perspective

ADMET screening and molecular docking were used to investigate the potential of plant-derived phytochemicals as candidate HER2-targeting compounds.

### Dynamic Perspective

Molecular dynamics simulation was used to investigate the stability and behavior of the selected protein–ligand complex over time.

### Transcriptomic Perspective

RNA-Seq analysis provides a genome-wide approach for examining gene expression-related information in the HER2-positive breast cancer context.

### Functional Perspective

GO and KEGG enrichment analysis provides biological interpretation of HER2-associated genes and pathways.

---

#  Key Outcomes

The completed portfolio demonstrates:

* HER2 protein structure preparation.
* Structural quality assessment.
* Phytochemical identification and screening.
* Drug-likeness and ADMET evaluation.
* Protein–ligand molecular docking.
* 2D and 3D interaction analysis.
* 100 ns molecular dynamics simulation.
* RMSD, RMSF, Rg and SASA analysis.
* PCA and DCCM analysis.
* MM/GBSA-based binding energy analysis.
* RNA-Seq quality control using FASTQC.
* RNA-Seq preprocessing and trimming.
* HISAT2-based alignment to hg38.
* GO Biological Process enrichment.
* GO Cellular Component enrichment.
* GO Molecular Function enrichment.
* KEGG pathway enrichment.
* Biological interpretation of computational results.

---

#  Skills Demonstrated

## Bioinformatics

* NGS Data Analysis
* RNA-Seq Analysis
* Functional Enrichment Analysis
* Gene Ontology Analysis
* KEGG Pathway Analysis
* Sequence Quality Control
* Genome Alignment
* Biological Data Interpretation

## Computational Biology

* Protein Structure Analysis
* Protein Preparation
* Molecular Docking
* Protein–Ligand Interaction Analysis
* Molecular Dynamics Simulation
* Trajectory Analysis
* Binding Energy Analysis

## Drug Discovery

* Phytochemical Screening
* ADMET Analysis
* Drug-Likeness Evaluation
* Virtual Screening
* Structure-Based Drug Discovery

## Programming & Data Analysis

* R
* Bioconductor
* Python
* Data Visualization
* Computational Workflow Development

---

#  Repository Structure

```text
HER2-Computational-Oncology-Portfolio-Updated/
│
├── 01_Protein_Preparation/
│   └── README.md
│
├── 02_ADMET_Analysis/
│   └── README.md
│
├── 03_Molecular_Docking/
│   └── README.md
│
├── 04_Molecular_Dynamics/
│   ├── images/
│   └── README.md
│
├── 05_RNASeq_Galaxy/
│   ├── RNA-Seq analysis outputs
│   ├── FASTQC results
│   ├── Alignment results
│   └── README.md
│
├── 06_Functional_Enrichment/
│   ├── GO enrichment results
│   ├── KEGG enrichment results
│   └── README.md
│
└── README.md
```

---

#  Project Status

| Project               | Status      |
| --------------------- | ----------- |
| Protein Preparation   | ✅ Completed |
| ADMET Analysis        | ✅ Completed |
| Molecular Docking     | ✅ Completed |
| Molecular Dynamics    | ✅ Completed |
| RNA-Seq Analysis      | ✅ Completed |
| Functional Enrichment | ✅ Completed |

## Portfolio Status: COMPLETED ✅

All six computational projects have been completed and documented as part of the HER2 Computational Oncology Portfolio.

---

# Future Scope

The portfolio can be further expanded through:

* Differential gene expression analysis.
* Identification of significantly upregulated and downregulated genes.
* Integration of transcriptomic and structural findings.
* Multi-omics analysis.
* Gene–pathway network analysis.
* Identification of hub genes.
* Biomarker discovery.
* AI/ML-assisted drug discovery.
* Drug repurposing studies.
* Larger-scale virtual screening.
* Experimental validation of computational predictions.
* Preparation of results for research publication.

---

#  Significance

HER2-positive breast cancer is an important molecular subtype of breast cancer in which HER2-driven signaling contributes to tumor growth and progression.

This portfolio demonstrates how multiple computational approaches can be integrated to investigate different levels of cancer biology:

```text
Protein Structure
       ↓
Drug–Target Interaction
       ↓
Molecular Stability
       ↓
Gene Expression
       ↓
Biological Pathways
       ↓
Integrated Computational Oncology
```

The combination of structural bioinformatics, drug discovery, molecular dynamics, transcriptomics, and functional enrichment provides a broader computational framework for investigating HER2-associated cancer biology.

---

#  Research Interests

* Computational Oncology
* Cancer Bioinformatics
* Structural Bioinformatics
* Drug Discovery
* Molecular Docking
* Molecular Dynamics
* RNA-Seq Analysis
* Functional Genomics
* Biomarker Discovery
* AI/ML in Drug Discovery

---

#  Conclusion

This HER2 Computational Oncology Portfolio demonstrates an end-to-end computational approach to investigating HER2-positive breast cancer.

Starting from **HER2 protein preparation**, the workflow progresses through **phytochemical ADMET screening, molecular docking, molecular dynamics simulation, RNA-Seq analysis, and functional enrichment**.

Together, these projects demonstrate practical experience in **bioinformatics, computational biology, structural analysis, drug discovery, NGS data analysis, and functional genomics**, providing a foundation for further research in computational oncology and cancer drug discovery.

---

##  Portfolio Status

Six Projects Completed | Computational Oncology | Bioinformatics | Drug Discovery | Cancer Research

---

