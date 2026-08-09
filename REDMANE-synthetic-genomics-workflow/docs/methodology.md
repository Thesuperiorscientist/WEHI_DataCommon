
---

# 4. `docs/methodology.md`

```markdown
# Methodology

## 1. Input Data

Genome in a Bottle HG005 paired-end whole-genome sequencing data were used as the starting material.

## 2. Synthetic FASTQ Generation

The paired-end sequencing reads were divided into multiple synthetic samples.

Five synthetic samples were generated.

The pairing between R1 and R2 was maintained throughout the process.

## 3. Read Validation

Read counts were checked to ensure that paired-end files remained synchronized.

## 4. Reference Genome

The original plan was to use the complete GRCh38 reference genome.

Due to computational memory limitations, chromosome 22 was selected as the working reference.

## 5. Alignment

BWA-MEM was used to align the paired-end reads to the reference.

```text
R1 + R2 + reference
        ↓
      BWA-MEM
        ↓
       SAM
        ↓
        BAM
        ↓
        Sorted BAM
        ↓
        BAI
        Sorted BAM
        ↓
        bcftools mpileup
        ↓
        BCF
        ↓
        bcftools call
        ↓
        VCF