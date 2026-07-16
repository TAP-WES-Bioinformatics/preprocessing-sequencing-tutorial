## Step 1 - Amplicon-Based Sequencing : Mapping

After performing sequencing, we should have our data in fastq.gz (a compressed fastq file) format. This file type contains the raw sequencing reads that we will need to align to our reference genome, as well as information on the quality of each sequenced base. Note for paired end sequencing, we will often have two separate fastq.gz files for each run, corresponding to forward and reverse reads.

We will then map these read to a reference genome using the tool minimap2 and pass it to samtools to compress it into a bam file. The output mapped, compressed reads are unsorted and unindexed.

```
minimap2 \
    -ax sr \
    reference.fasta \
    sample_R1.fastq.gz sample_R2.fastq.gz \
| samtools view -b -o sample.bam
```
