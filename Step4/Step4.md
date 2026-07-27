## Step 4 - Shotgun Metagenomics : Adaptor and Quality Trimming

Unlike amplicon sequencing, shotgun metagenomics does not use targeted primers, so there is no primer trimming step. Instead, we trim off sequencing adaptors and low quality bases, and discard reads that are too short to be reliably mapped. The ```fastp``` command does adaptor detection and quality trimming for paired-end reads in a single step.

```
fastp \
  -i sample_R1.fastq.gz \
  -I sample_R2.fastq.gz \
  -o sample_trimmed_R1.fastq.gz \
  -O sample_trimmed_R2.fastq.gz \
  --detect_adapter_for_pe \
  --qualified_quality_phred 20 \
  --length_required 50 \
  --thread 8
```
