# AMC Calf Nasopharyngeal Microbiome & AMR Analysis

This repository contains all processed data and reproducible R workflows used for the analysis of the calf nasopharyngeal microbiome and antimicrobial resistance (AMR) profiles under simulated waste-milk β-lactam exposure.  

All outputs included in this repository are generated directly from the analysis scripts to ensure full reproducibility of the associated manuscript.

---

## Repository Structure

**amr/**  
Processed AMR outputs, including:
- Decontaminated ARG tables  
- Alpha and beta diversity results  
- CLR-transformed matrices  
- Resistance class summaries  
- Mixed-effects model (LMM) outputs  
- PERMANOVA results  

**taxonomic/**  
Processed taxonomic outputs, including:
- Kraken2/Bracken taxonomic tables  
- Phyloseq objects  
- Decontamination results  
- Alpha and beta diversity outputs  
- Mixed-effects model (LMM) results  
- PERMANOVA results  

**data/**  
Metadata and RDS input files used to construct phyloseq objects  

**scripts/**  
RMarkdown workflows for:
- Taxonomic analysis  
- AMR analysis  

---

## Analysis Workflows

### Taxonomic Analysis (Kraken2 → Bracken → phyloseq)
- Kraken2 classification and Bracken abundance estimation  
- Phyloseq object construction  
- Prevalence-based decontamination  
- Alpha diversity analysis (mixed-effects models)  
- Beta diversity analysis (CLR transformation, Aitchison distance)  
- PERMANOVA with repeated measures  
- Relative abundance summaries and compositional visualization  

**Script:** `scripts/AMC-Stats_Tax.Rmd`

---

### AMR Gene Analysis (AMR++)
- ARG detection using AMR++ (MEGARes database)  
- Prevalence-based decontamination  
- Filtering of low-read samples  
- Alpha diversity analysis (mixed-effects models)  
- Beta diversity analysis (CLR transformation)  
- Resistance class aggregation  
- Heatmap visualization  
- PERMANOVA with repeated measures  

**Script:** `scripts/AMR-Stats_AMC.Rmd`

---

## Reproducibility

All CSV and RDS files in the `amr/` and `taxonomic/` directories are generated directly from the scripts in this repository.  

No manual post-processing steps were performed.

---

## Data Availability

**NCBI BioProject:** PRJNA1347079
