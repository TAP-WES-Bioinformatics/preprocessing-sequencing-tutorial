## Step 2 - Amplicon Based Sequencing: Primer and Quality Trimming

In amplicon-based sequencing, primer anneal to the DNA/RNA in order to amplify the genetic material during PCR. Prior to doing any data analysis, we remove the primer sequence by trimming. Additionally, we trim off low quality bases, and remove reads of a short length. The ```ivar trim``` command does both primer and quality trimming at the same time.

```
ivar trim
```
