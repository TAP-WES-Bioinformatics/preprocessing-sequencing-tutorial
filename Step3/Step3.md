## Step 4 - Amplicon-Based Sequencing : Checking Read Counts and Depth

Once we have our mapped and trimmed reads, we then want to check the number of reads and the coverage depth to ensure our data is of good quality. 

```
samtools flagstat sample.sorted.bam
```
