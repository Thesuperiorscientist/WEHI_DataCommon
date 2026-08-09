# Synthetic Genomic Data Workflow

A computational genomics workflow developed during the WEHI RCP Discovery Internship for generating and processing synthetic genomic datasets from Genome in a Bottle (GIAB) sequencing data.

The workflow demonstrates the transformation of paired-end sequencing data through multiple genomic data representations:

**FASTQ → BAM → VCF**

## Project Overview

The project explored the generation of synthetic genomic datasets at three levels:

1. Raw sequencing data — FASTQ
2. Processed alignment data — BAM
3. Variant data — VCF

Genome in a Bottle (GIAB) HG005 whole-genome sequencing data were used as the starting dataset.

Five synthetic paired-end samples were generated and subsequently processed through alignment, BAM processing, and variant calling.

## Workflow

GIAB HG005
    │
    ▼
Paired-end FASTQ
    │
    ▼
Synthetic sample generation
    │
    ▼
FASTQ validation
    │
    ▼
BWA-MEM alignment
    │
    ▼
SAM
    │
    ▼
BAM
    │
    ▼
Sorted BAM + BAI
    │
    ▼
BCFtools mpileup
    │
    ▼
BCF
    │
    ▼
BCFtools call
    │
    ▼
VCF

Data
Input
        Genome in a Bottle (GIAB)
        Sample: HG005
        Whole-genome sequencing
        Paired-end reads

Generated datasets
        Synthetic FASTQ files
        BAM files
        Sorted BAM files
        BAM index files
        VCF files

Large genomic datasets are not stored directly in this GitHub repository. See Data Availability.

Tools
Python
Jupyter Notebook
Bash
WSL / Ubuntu
BWA
Samtools
BCFtools
My Contribution

During the project, I worked on the computational processing and documentation of the synthetic genomic data workflow.

My work included:

Generating synthetic paired-end FASTQ samples
Validating paired-end read counts
Preparing a GRCh38 chromosome 22 reference
Performing BWA-MEM alignment
Converting SAM files to BAM
Sorting and indexing BAM files
Performing variant calling with BCFtools
Validating generated VCF files
Documenting computational constraints and workflow decisions


Computational Limitation

    The initial plan involved using the complete GRCh38 reference genome. Due to available system memory, full-genome indexing was not practical in the working environment.
    The workflow was therefore adapted to use chromosome 22 from GRCh38 as a computationally manageable demonstration reference.
    Consequently, this workflow should not be interpreted as a whole-genome analysis.


Documentation

Project Overview
Workflow
Methodology
Technical Diary
Limitations
Data Availability
Archive

The project documentation is associated with the Zenodo record:

https://zenodo.org/records/19081661

Citation

If using this repository, please refer to the associated Zenodo record and project documentation.
