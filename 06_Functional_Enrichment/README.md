# 🧬 Functional Enrichment Analysis of HER2-Associated Genes

## 📌 Overview

This project focuses on the **functional enrichment analysis of HER2-associated genes** to identify important biological processes, cellular components, molecular functions, and biological pathways associated with the selected gene set.

Gene Ontology (GO) and Kyoto Encyclopedia of Genes and Genomes (KEGG) enrichment analyses were performed to interpret the biological significance of the identified genes.

This analysis provides a functional and pathway-level perspective of the molecular mechanisms associated with **HER2-positive breast cancer** and forms the functional bioinformatics component of the **HER2 Computational Oncology Portfolio**.

---

## 🎯 Objectives

The main objectives of this project were to:

* Perform functional enrichment analysis of HER2-associated genes.
* Identify significantly enriched Gene Ontology (GO) terms.
* Analyze enriched Biological Process (BP) categories.
* Identify associated Cellular Components (CC).
* Identify enriched Molecular Functions (MF).
* Identify significantly enriched KEGG pathways.
* Visualize enrichment results using bar plots.
* Summarize enrichment results using result tables.
* Interpret the biological relevance of enriched functions and pathways in the context of HER2-positive breast cancer.

---

# 🔬 Analysis Workflow

```text
HER2-Associated Gene Set
          ↓
Functional Enrichment Analysis
          ↓
       GO Analysis
          ↓
 ┌────────┼─────────┐
 ↓        ↓         ↓
BP       CC        MF
 ↓        ↓         ↓
Biological Cellular Molecular
Processes Components Functions
          ↓
    KEGG Pathway
      Analysis
          ↓
   Visualization
          ↓
Biological Interpretation
```

---

# 1️⃣ Gene Ontology (GO) Enrichment Analysis

Gene Ontology enrichment analysis was performed to determine which biological functions were overrepresented among the HER2-associated genes.

GO analysis was evaluated under three major categories:

### Biological Process (BP)

Describes the biological processes or larger cellular activities in which the genes participate.

Examples include:

* Cellular processes
* Biological regulation
* Signaling-related processes
* Metabolic processes
* Response to stimuli

### Cellular Component (CC)

Describes the cellular locations or structures where the gene products are found.

Examples include:

* Cytoplasm
* Nucleus
* Plasma membrane
* Protein complexes
* Intracellular compartments

### Molecular Function (MF)

Describes the molecular-level activities performed by gene products.

Examples include:

* Protein binding
* ATP binding
* Enzyme activity
* Receptor activity
* Molecular signaling activities

---

# 2️⃣ GO Biological Process (BP)

The GO Biological Process analysis identifies biological processes that are significantly enriched within the HER2-associated gene set.

### GO Biological Process Bar Plot

![GO Biological Process Bar Plot](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_bp_barplot.png)

### GO Biological Process Results Table

![GO Biological Process Results](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_bp_table.png)

These results provide an overview of the biological processes potentially associated with the selected HER2-related genes.

---

# 3️⃣ GO Cellular Component (CC)

GO Cellular Component analysis identifies the cellular structures and compartments associated with the HER2-associated gene set.

### GO Cellular Component Bar Plot

![GO Cellular Component Bar Plot](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_cc_barplot.png)

### GO Cellular Component Results Table

![GO Cellular Component Results](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_cc_table.png)

The enriched cellular components provide insight into the cellular locations where the associated gene products may function.

---

# 4️⃣ GO Molecular Function (MF)

GO Molecular Function analysis identifies the molecular activities associated with the HER2-associated genes.

### GO Molecular Function Bar Plot
![GO Molecular Function Bar Plot](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_mf_barplot.png)

### GO Molecular Function Results Table
![GO Molecular Function Results](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/go_mf_table.png)


These results provide information about the molecular activities potentially contributing to HER2-associated cellular functions.

---

# 5️⃣ KEGG Pathway Enrichment Analysis

KEGG pathway enrichment analysis was performed to identify biological signaling and metabolic pathways significantly associated with the HER2-related gene set.

KEGG provides pathway-level information that helps connect individual genes to broader biological mechanisms.

### KEGG Enrichment Bar Plot

![KEGG Enrichment Bar Plot](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/kegg_barplot.png)

### KEGG Enrichment Results Table

![KEGG Enrichment Results](https://raw.githubusercontent.com/waihida0406/HER2-Computational-Oncology-Portfolio-Updated/master/06_Functional_Enrichment/kegg_table.png)

The enriched pathways provide a broader view of the biological signaling networks potentially involved in HER2-associated cancer biology.

---

# 📊 Results Summary

The functional enrichment analysis generated results across four major analysis categories:

| Analysis              | Output                        |
| --------------------- | ----------------------------- |
| GO Biological Process | Enriched biological processes |
| GO Cellular Component | Enriched cellular locations   |
| GO Molecular Function | Enriched molecular functions  |
| KEGG                  | Enriched biological pathways  |

The enrichment results were visualized using bar plots and summarized using result tables for easier interpretation.

---

# 🧬 Biological Relevance to HER2-Positive Breast Cancer

HER2 is an important receptor involved in cellular signaling, proliferation, survival, and cancer progression.

Functional enrichment analysis helps move beyond individual genes by identifying groups of genes participating in common biological processes and signaling pathways.

The GO and KEGG analyses therefore provide a systems-level perspective of the biological functions associated with the HER2-related gene set.

Such analyses can help investigate:

* Cancer-associated biological processes
* Signaling mechanisms
* Cellular components involved in tumor biology
* Molecular functions associated with disease progression
* Important signaling pathways
* Candidate biomarkers
* Potential therapeutic targets

---

# 📈 Visualization

The enrichment results were visualized using bar plots to facilitate interpretation and comparison of significantly enriched functional categories.

The following visualizations were generated:

### Gene Ontology

* GO Biological Process
* GO Cellular Component
* GO Molecular Function

### KEGG

* KEGG Pathway Enrichment

Corresponding result tables were also generated for each enrichment category.

---

# 🛠️ Tools and Resources

| Tool / Resource          | Purpose                                          |
| ------------------------ | ------------------------------------------------ |
| R                        | Functional enrichment analysis and visualization |
| Bioconductor             | Bioinformatics and enrichment analysis           |
| Gene Ontology            | Functional classification and enrichment         |
| KEGG                     | Biological pathway enrichment                    |
| HER2-associated gene set | Input for functional analysis                    |

---

# 📁 Project Structure

```text
06_Functional_Enrichment/
│
├── 06_Functional_Enrichment_of_HER2_Associated_Genes
│
├── go_bp_barplot.png
├── go_bp_table.png
│
├── go_cc_barplot.png
├── go_cc_table.png
│
├── go_mf_barplot.png
├── go_mf_table.png
│
├── kegg_barplot.png
├── kegg_table.png
│
└── README.md
```

---

# 🔑 Key Outcomes

This project demonstrated the application of functional enrichment analysis to HER2-associated genes.

### Major outcomes include:

* Functional classification of HER2-associated genes using Gene Ontology.
* Identification of enriched Biological Process terms.
* Identification of enriched Cellular Component terms.
* Identification of enriched Molecular Function terms.
* Identification of enriched KEGG pathways.
* Visualization of enrichment results using bar plots.
* Generation of tables containing enrichment results.
* Biological interpretation of gene functions and pathways in the context of HER2-associated cancer biology.

---

# 🔮 Future Scope

The functional enrichment analysis can be further extended by:

* Performing pathway-level network analysis.
* Constructing gene–pathway interaction networks.
* Identifying hub genes within enriched pathways.
* Integrating enrichment results with differential gene expression data.
* Comparing enriched pathways between cancer and normal samples.
* Integrating GO/KEGG results with molecular docking findings.
* Integrating transcriptomic results with molecular dynamics and structural analysis.
* Identifying potential biomarkers and therapeutic targets associated with HER2-positive breast cancer.

---

# 💡 Significance of the Project

Functional enrichment analysis provides an important bridge between **gene-level findings and biological interpretation**.

In this portfolio, the analysis complements the structural and computational investigation of HER2 by providing a functional and pathway-level perspective.

Together with protein preparation, ADMET analysis, molecular docking, molecular dynamics, and RNA-Seq analysis, this project contributes to an integrated **computational oncology workflow for studying HER2-positive breast cancer**.

---

# 💻 Skills Demonstrated

### Bioinformatics

* Functional Enrichment Analysis
* Gene Ontology Analysis
* KEGG Pathway Analysis
* Gene Set Interpretation
* Biological Data Visualization
* Pathway-Based Biological Interpretation

### Computational Biology

* HER2-associated gene analysis
* Cancer pathway analysis
* Functional annotation
* Systems-level interpretation

### Tools

* R
* Bioconductor
* Gene Ontology
* KEGG

---

# 📌 Portfolio Context

This project is **Project 6 of the HER2 Computational Oncology Portfolio**.

The overall portfolio combines multiple computational approaches:

1. **Protein Preparation of HER2**
2. **ADMET Analysis of Phytochemicals**
3. **Molecular Docking against HER2**
4. **100 ns Molecular Dynamics Simulation**
5. **RNA-Seq Analysis using Galaxy**
6. **Functional Enrichment of HER2-Associated Genes**

This project represents the **functional bioinformatics and pathway analysis component** of the portfolio.


