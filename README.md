# AMC Calf Nasopharyngeal Microbiome & AMR Analysis

This repository contains all processed data and R scripts used for the calf nasopharyngeal microbiome and antimicrobial resistance (AMR) analysis.  
All outputs are included to support full reproducibility for the associated manuscript.

## Repository Structure

**amr/**  
Processed AMR outputs (decontamination results, alpha/beta diversity summaries, CLR matrices, resistance class summaries, PERMANOVA)

**taxonomic/**  
Processed taxonomic outputs (Kraken2/Bracken tables, phyloseq objects, alpha/beta diversity summaries, PERMANOVA)

**data/**  
Metadata and RDS input files used to build phyloseq objects

**scripts/**  
RMarkdown analysis scripts for both taxonomic and AMR workflows

## Analysis Workflows

### Taxonomic Analysis (Kraken2/Bracken → phyloseq)
- Kraken2/Bracken taxonomic profiling  
- Construction of phyloseq objects  
- Decontamination  
- Alpha and beta diversity  
- PERMANOVA  
- Relative abundance summaries  

Script: `scripts/AMC-Stats_Tax.Rmd`

### AMR Gene Analysis (AMR++)
- Antimicrobial resistance gene detection  
- Filtering and decontamination  
- Alpha and beta diversity  
- CLR transformation  
- Resistance class summarization  
- Heatmap and PERMANOVA outputs  

Script: `scripts/AMR-Stats_AMC.Rmd`

## Reproducibility

All exported CSV and RDS files in the `amr/` and `taxonomic/` folders are generated directly from the scripts in this repository.

BioProject: PRJNA1347079
