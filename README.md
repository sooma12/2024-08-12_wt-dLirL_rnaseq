# 2024-08-12_wt-dLirL_rnaseq

## Sample prep

Samples were prepared by MWS 24 July, 2024 following Geisinger lab protocol

Sent 30 uL of 100 ng/uL RNA to SeqCenter

## Initial QC

Gzipped fastq files were downloaded to Geisinger Lab desktop, then uploaded to Discovery.  

md5sums of gzipped files were checked using `check_md5sums.py`

Files were gunzipped.  

FastQC was used to check read quality and verify adapter trimming.

## Alignment

Bowtie2-build was run using parameters in config for 17978-mff genome, including plasmids.

Constructed sample sheet using script 2.  Afterwards, manually adjusted sample names for MSA9, 11, and 13 to append _dlirL to each for ease of processing later.

Modifications were made to bowtie2 array script as follows:

1. --array=1-6%7
2. --ntasks=6
3. --output=/work/geisingerlab/Mark/rnaSeq/2024-08-12_wt-dLirL_rnaseq/logs/%x-%A-%a.log 
4. --error=/work/geisingerlab/Mark/rnaSeq/2024-08-12_wt-dLirL_rnaseq/logs/%x-%A-%a.err 
5. --mail-user=soo.m@northeastern.edu

