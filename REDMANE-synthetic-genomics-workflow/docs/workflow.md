1. FASTQ Generation

Paired-end sequencing data were processed to generate multiple synthetic samples.

Each paired sample consisted of:

R1 reads
R2 reads
2. FASTQ Validation

The generated paired-end files were checked to ensure that the read counts were consistent between R1 and R2.

3. Reference Preparation

A chromosome 22 reference derived from GRCh38 was prepared for alignment.

4. Alignment

BWA-MEM was used to align paired-end reads against the chromosome 22 reference.

The alignment produced SAM files.

5. BAM Processing

SAM files were converted to BAM format.

The BAM files were then:

Sorted
Indexed

The resulting files consisted of sorted BAM files and BAI indexes.

6. Variant Calling

BCFtools was used for variant calling.

The process consisted of:

Sorted BAM
    ↓
bcftools mpileup
    ↓
BCF
    ↓
bcftools call
    ↓
VCF
7. Outputs

The workflow produced:

FASTQ
BAM
BAI
VCF

Large output files are stored externally rather than in this repository.