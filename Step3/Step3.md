## Step 4 - Amplicon-Based Sequencing : Checking Read Counts and Depth

Once we have our mapped and trimmed reads, we then want to check the number of reads and the coverage depth to ensure our data is of good quality. 

```samtools flagstat``` summarizes the alignment statistics of a BAM file by reporting metrics such as total reads, mapped reads, properly paired reads, duplicates, and sequencing quality categories. This gives you some high level QC metrics to look at after mapping..

```
samtools flagstat sample_1.trimmed.bam
```

```samtools depth``` reports the read depth (coverage) at each position in a BAM file. Low coverage regions may produce less reliable variant calls.

```
samtools depth sample_1.trimmed.bam > sample_1_depth.txt
```

We can plot or manually inspect the contents of the ```*depth.txt``` file to visualize where our samples may have low coverage.
