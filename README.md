# BCOR_ITD_ext
BCOR_ITD_ext is a perl script for detecting, annotating, and quantifying BCOR-ITDs (within exon 15) in paired-end NGS data.

## Version 1.0 (modified from FLT3_ITD_ext v1.1)
Type "perl BCOR_ITD_ext.pl" for usage and options 
Input: bamfile or fastq files (R1 and R2)
1. This script is intended for DNA NGS, however may be applied to RNA NGS (flag -rna) by extracting reads from a reduced locus within exon 15 to avoid spliced reads

Before running perl script for first time:
1. Create a bwa index for the BCOR target locus from the provided fasta file ("bwa index -p BCOR_dna_e15 BCOR_dna_e15.fa") and modify script to provide path of the index if necessary (variable $refindex).
2. Download following software tools as needed and add to path (or modify script with paths): bwa, samtools, sumaclust, fgbio, bbduk, bedtools, java, picard.

## License
[MIT](https://choosealicense.com/licenses/mit/)
