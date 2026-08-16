# RNA-Seq Analysis of HER2-Positive Breast Cancer Using Galaxy

## Overview

This project demonstrates an RNA-Seq data analysis workflow for HER2-positive breast cancer using the **Galaxy platform**. The analysis includes raw sequencing quality assessment, preprocessing and quality trimming, post-trimming quality control, and alignment of RNA-Seq reads to the human **hg38 reference genome**.

The workflow was performed using publicly available sequencing data and is part of the **HER2 Computational Oncology Portfolio**.

---

## Objectives

* Assess the quality of raw RNA-Seq sequencing data.
* Identify sequencing quality issues and adapter contamination.
* Perform quality trimming and preprocessing.
* Evaluate sequencing quality after trimming.
* Align the processed reads to the human **hg38 reference genome**.
* Document the complete RNA-Seq preprocessing and alignment workflow.

---

## Dataset

**Data type:** RNA-Seq
**Organism:** *Homo sapiens*
**Reference genome:** Human hg38
**Analysis platform:** Galaxy
**Data source:** NCBI Sequence Read Archive (SRA)

The sequencing data were imported into Galaxy in FASTQ format and used as the starting point for downstream analysis.

---

## RNA-Seq Analysis Workflow

```text
Raw FASTQ Data
      ↓
FASTQC – Raw Read Quality Assessment
      ↓
Quality Trimming / Adapter Removal
      ↓
FASTQC – Post-Trimming Quality Assessment
      ↓
HISAT2 Alignment
      ↓
Human hg38 Reference Genome
      ↓
Aligned RNA-Seq Reads
```

---

## 1. Raw Data Upload

The RNA-Seq FASTQ dataset was uploaded to the Galaxy platform for analysis.

**Screenshot:**
`01_galaxy_upload.png`

---

## 2. Raw Read Quality Assessment

FASTQC was used to evaluate the quality of the raw sequencing reads.

The following quality parameters were examined:

* Per-base sequence quality
* Per-sequence quality scores
* Per-base sequence content
* Per-sequence GC content
* Sequence duplication levels
* Overrepresented sequences
* Per-base N content
* Sequence length distribution

### FASTQC Results

**FASTQC Summary:**
`02_fastqc_summary.png`

**Basic Statistics:**
`03_basic_statistics.png`

**Per-base Sequence Quality:**
`04_per_base_sequence_quality.png`

**Per-sequence Quality:**
`05_per_sequence_quality.png`

**Per-base Sequence Content:**
`06_per_base_sequence_content.png`

**Per-sequence GC Content:**
`07_per_sequence_gc_content.png`

**Sequence Duplication Levels:**
`08_sequence_duplication_levels.png`

**Overrepresented Sequences:**
`09_overrepresented_sequences.png`

**Per-base N Content:**
`10_per_base_n_content.png`

**Sequence Length Distribution:**
`11_sequence_length_distribution.png`

---

## 3. RNA-Seq Preprocessing

Quality trimming was performed to remove low-quality bases and sequencing adapter contamination from the raw reads.

The objective of preprocessing was to improve the quality of reads before genome alignment.

### Post-Trimming Quality Control

FASTQC was performed again after trimming to evaluate the improvement in sequencing quality.

**Post-trimming FASTQC Summary:**
`12_post_trim_FastQC_summary.png`

**Post-trimming Per-base Quality:**
`13_post_trim_per_base_quality.png`

**Post-trimming Adapter Content:**
`14_post_trim_adapter_content.png`

---

## 4. Alignment to Human Genome

The processed RNA-Seq reads were aligned to the **human hg38 reference genome** using **HISAT2**.

HISAT2 is a splice-aware aligner designed for efficient alignment of RNA-Seq reads to reference genomes.

**HISAT2 Alignment Result:**
`15_HISAT2_hg38_alignment.png`

---

## Tools Used

| Tool             | Purpose                                   |
| ---------------- | ----------------------------------------- |
| Galaxy           | RNA-Seq workflow and analysis             |
| FASTQC           | Quality assessment of sequencing reads    |
| Quality Trimming | Removal of low-quality bases and adapters |
| HISAT2           | Alignment of RNA-Seq reads                |
| hg38             | Human reference genome                    |
| NCBI SRA         | Public sequencing data source             |

---

## Key Outcomes

* Raw RNA-Seq data quality was assessed using FASTQC.
* Sequencing quality metrics were evaluated before preprocessing.
* Adapter and low-quality sequences were removed during preprocessing.
* Post-trimming quality was evaluated using FASTQC.
* Processed RNA-Seq reads were successfully aligned against the human **hg38 reference genome using HISAT2**.
* The workflow provides a reproducible foundation for downstream RNA-Seq analysis.

---

## Project Structure

```text
05_RNASeq_Galaxy/
│
├── 01_galaxy_upload.png
├── 02_fastqc_summary.png
├── 03_basic_statistics.png
├── 04_per_base_sequence_quality.png
├── 05_per_sequence_quality.png
├── 06_RNA_Seq_Preprocessing_and_Alignment_Using_Galaxy
├── 06_per_base_sequence_content.png
├── 07_per_sequence_gc_content.png
├── 08_sequence_duplication_levels.png
├── 09_overrepresented_sequences.png
├── 10_per_base_n_content.png
├── 11_sequence_length_distribution.png
├── 12_post_trim_FastQC_summary.png
├── 13_post_trim_per_base_quality.png
├── 14_post_trim_adapter_content.png
├── 15_HISAT2_hg38_alignment.png
└── README.md
```

---

## Significance

RNA-Seq analysis enables genome-wide investigation of gene expression patterns in cancer. In the context of HER2-positive breast cancer, transcriptomic analysis can help identify differentially expressed genes, altered biological pathways, and potential molecular biomarkers.

This project demonstrates practical experience in **NGS data quality control, RNA-Seq preprocessing, genome alignment, and Galaxy-based bioinformatics workflows**.

---

## Future Scope

The processed and aligned RNA-Seq data can be used for downstream analyses such as:

* Gene quantification
* Differential gene expression analysis
* Volcano plot generation
* Heatmap analysis
* GO enrichment analysis
* KEGG pathway analysis
* Identification of potential biomarkers
* Integration with HER2-related molecular findings

---

## Skills Demonstrated

**Bioinformatics:** RNA-Seq Analysis • NGS Data Analysis • Quality Control • Sequence Preprocessing • Genome Alignment

**Tools:** Galaxy • FASTQC • HISAT2 • NCBI SRA

**Reference:** Human hg38 Genome

**Application:** HER2-Positive Breast Cancer / Computational Oncology
