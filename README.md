<div align="center">

# 🧬 HER2 Computational Oncology Portfolio

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=22&pause=1000&color=8A2BE2&center=true&vCenter=true&width=650&lines=Molecular+Docking+%E2%86%92+MD+Simulation;RNA-seq+%E2%86%92+GO+%26+KEGG+Enrichment;Targeting+HER2+in+Breast+Cancer" alt="Typing SVG" />

**An integrated in-silico pipeline for discovering HER2-targeting phytochemicals in breast cancer: from docking to dynamics to transcriptomics.**

[Overview](#-overview) • [Key Features](#-key-features) • [Tech Stack](#️-tech-stack) • [Workflow](#-workflow) • [Results](#-results) • [Project Structure](#-project-structure) • [Getting Started](#-getting-started) • [Roadmap](#️-roadmap) • [Author](#-author)

[![PyRx](https://img.shields.io/badge/PyRx-Docking-1f6feb?style=for-the-badge)](https://pyrx.sourceforge.io)
[![SwissADME](https://img.shields.io/badge/SwissADME-ADMET-2ea043?style=for-the-badge)](http://www.swissadme.ch)
[![GROMACS](https://img.shields.io/badge/GROMACS-100%20ns%20MD-f0883e?style=for-the-badge)](https://www.gromacs.org)
[![Galaxy](https://img.shields.io/badge/Galaxy-RNA--seq-d29922?style=for-the-badge)](https://usegalaxy.org)
[![HISAT2](https://img.shields.io/badge/HISAT2-hg38-8957e5?style=for-the-badge)](https://daehwankimlab.github.io/hisat2/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org)

</div>

---

## 🎯 Overview

HER2 (ERBB2) is overexpressed in roughly 20% of breast cancers and drives an aggressive disease subtype. This project combines **structure-based drug discovery** with **transcriptomic analysis** to identify and evaluate plant-derived compounds that may inhibit HER2.

The work was carried out during my bioinformatics internship at **BioNome** (May – Aug 2026).

> [!NOTE]
> All analyses in this repository are computational (in silico). Experimental validation would be required to confirm any candidate's activity.

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## ✨ Key Features

<details open>
<summary><b>💊 Drug Discovery (click to expand/collapse)</b></summary>
<br/>

- **Protein Preparation**: HER2 structure cleaned and prepared for docking
- **ADMET Profiling**: drug-likeness and pharmacokinetics evaluated with SwissADME
- **Molecular Docking**: virtual screening of 14 phytochemicals against HER2 using PyRx
- **Shortlisting**: top 5 candidates selected on binding affinity and ADMET properties
- **Molecular Dynamics**: 100 ns GROMACS simulation with RMSD, RMSF, radius of gyration and SASA analysis

</details>

<details>
<summary><b>🧪 Transcriptomics (click to expand)</b></summary>
<br/>

- **Quality Control**: FastQC assessment across 9 quality metrics, before and after trimming
- **Alignment**: reads mapped to the human reference genome (hg38) with HISAT2
- **Functional Enrichment**: GO and KEGG pathway analysis

</details>

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| **Docking** | PyRx (AutoDock Vina) |
| **ADMET** | SwissADME |
| **Molecular Dynamics** | GROMACS |
| **RNA-seq** | Galaxy, FastQC, HISAT2 |
| **Enrichment** | GO, KEGG |
| **Languages** | Python, R |

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 🔄 Workflow

```mermaid
flowchart LR
    A[HER2 structure<br/>preparation] --> B[Docking<br/>14 phytochemicals]
    B --> C[ADMET filtering<br/>SwissADME]
    C --> D[Top 5 candidates]
    D --> E[100 ns MD<br/>GROMACS]
    F[RNA-seq reads] --> G[FastQC<br/>quality control]
    G --> H[HISAT2<br/>hg38 alignment]
    H --> I[GO & KEGG<br/>enrichment]
    E --> J[Integrated<br/>interpretation]
    I --> J
```

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 📊 Results

<div align="center">

| Metric | Value |
|:---:|:---:|
| Compounds screened | **14** |
| Shortlisted candidates | **5** |
| Best binding affinity | **−7.7 kcal/mol** |
| MD simulation length | **100 ns** |
| Reference genome | **hg38** |

</div>

<details open>
<summary><b>🖼️ Figures (click to expand/collapse)</b></summary>
<br/>

<h3 align="center">⚛️ Molecular Dynamics (100 ns)</h3>
<p align="center">
  <img src="04_Molecular_Dynamics/images/rmsd.png" width="45%" alt="RMSD" />
  <img src="04_Molecular_Dynamics/images/rmsf.png" width="45%" alt="RMSF" />
</p>
<p align="center">
  <img src="04_Molecular_Dynamics/images/rg.png" width="45%" alt="Radius of gyration" />
  <img src="04_Molecular_Dynamics/images/sasa.png" width="45%" alt="SASA" />
</p>

<h3 align="center">🧪 RNA-seq Quality Control & Alignment</h3>
<p align="center">
  <img src="05_RNASeq_Galaxy/02_fastqc_summary.png" width="45%" alt="FastQC summary" />
  <img src="05_RNASeq_Galaxy/04_per_base_sequence_quality.png" width="45%" alt="Per base sequence quality" />
</p>
<p align="center">
  <img src="05_RNASeq_Galaxy/12_post_trim_FastQC_summary.png" width="45%" alt="Post-trim FastQC summary" />
  <img src="05_RNASeq_Galaxy/15_HISAT2_hg38_alignment.png" width="45%" alt="HISAT2 hg38 alignment" />
</p>

<h3 align="center">🧬 Functional Enrichment</h3>
<p align="center">
  <img src="06_Functional_Enrichment/go_bp_barplot.png" width="45%" alt="GO Biological Process" />
  <img src="06_Functional_Enrichment/kegg_barplot.png" width="45%" alt="KEGG pathways" />
</p>

</details>

> [!TIP]
> Each numbered folder has its own README explaining that step of the pipeline.

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 📁 Project Structure

<details>
<summary><b>📂 View folder layout (click to expand)</b></summary>
<br/>

```
HER2-Computational-Oncology-Portfolio-Updated/
├── 01_Protein_Preparation/      # HER2 structure preparation
├── 02_ADMET_Analysis/           # SwissADME drug-likeness results
├── 03_Molecular_Docking/        # PyRx docking of 14 phytochemicals
├── 04_Molecular_Dynamics/       # 100 ns GROMACS simulation
│   └── images/                  # RMSD, RMSF, Rg and SASA plots
├── 05_RNASeq_Galaxy/            # FastQC reports and HISAT2 alignment
├── 06_Functional_Enrichment/    # GO and KEGG enrichment results
└── README.md
```

</details>

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated.git
cd HER2-Computational-Oncology-Portfolio-Updated
```

**Requirements:** PyRx · GROMACS · access to a Galaxy server · Python 3

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 🗺️ Roadmap

- [x] HER2 protein preparation
- [x] ADMET profiling with SwissADME
- [x] Molecular docking of 14 phytochemicals and shortlisting of 5 candidates
- [x] 100 ns molecular dynamics simulation
- [x] RNA-seq quality control and hg38 alignment
- [x] GO and KEGG functional enrichment

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 👩‍🔬 Author

<div align="center">

**Waihida Yashmin**
MSc Biotechnology · SRM Institute of Science and Technology, Chennai

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/waihida-yashmin-3467bb230)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/waihida0406)

⭐ *If you find this project useful, consider giving it a star!*

</div>
