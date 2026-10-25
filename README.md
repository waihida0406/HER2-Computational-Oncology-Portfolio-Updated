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

- **Molecular Docking**: virtual screening of 14 phytochemicals against HER2 using PyRx
- **ADMET Profiling**: drug-likeness and pharmacokinetics evaluated with SwissADME
- **Shortlisting**: top 5 candidates selected on binding affinity and ADMET properties
- **Molecular Dynamics**: 100 ns GROMACS simulation of the HER2–ligand complex to assess stability

</details>

<details>
<summary><b>🧪 Transcriptomics (click to expand)</b></summary>
<br/>

- **Quality Control**: FastQC assessment across 9 quality metrics
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

<!-- Upload your figures to a "results" folder and keep the file names below the same, or change them to match. -->

<details open>
<summary><b>🖼️ Figures (click to expand/collapse)</b></summary>
<br/>

<p align="center">
  <img src="results/docking_pose.png" width="45%" alt="Docking pose" />
  <img src="results/rmsd.png" width="45%" alt="RMSD plot" />
</p>
<p align="center">
  <img src="results/rmsf.png" width="45%" alt="RMSF plot" />
  <img src="results/kegg_enrichment.png" width="45%" alt="KEGG enrichment" />
</p>

</details>

> [!TIP]
> Start with the `results/` folder for a quick look at the key findings.

<p align="right"><a href="#-her2-computational-oncology-portfolio">⬆ Back to top</a></p>

---

## 📁 Project Structure

<!-- Edit the folder names below to match the folders actually in this repo. -->

<details>
<summary><b>📂 View folder layout (click to expand)</b></summary>
<br/>

```
HER2-Computational-Oncology-Portfolio-Updated/
├── docking/          # Ligand files, PyRx outputs, binding scores
├── admet/            # SwissADME results
├── md_simulation/    # GROMACS inputs and analysis plots
├── rna_seq/          # FastQC reports, alignment stats, enrichment results
├── results/          # Final figures and tables
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

<!-- Add only the next steps you actually plan, as unticked "- [ ]" lines. -->

- [x] Molecular docking of 14 phytochemicals
- [x] ADMET profiling and shortlisting of 5 candidates
- [x] 100 ns molecular dynamics simulation
- [x] RNA-seq alignment and GO/KEGG enrichment

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

