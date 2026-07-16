## Step 4 - Shotgun Metagenomics : Adaptor and Quality Trimming


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
