# preprocessing-sequencing-tutorial

Welcome to the tutorial for the preprocessing sequencing data component of the workshop!

Use the left sidebar to browse files, and click on them to open them in the file viewer.

You'll find each step of the tutorial as a numbered directory in the sidebar, starting with Step1. Each directory contains all the instructions and data needed for that step. Go ahead and cd into Step1 and open Step1.md to get started.

Steps 1-3 are for processing amplicon-based sequencing data, and Step 4 covers shotgun metagenomics.

Have fun!


# Running in GitHub Codespaces
This tutorial is designed to run in GitHub Codespaces. All dependencies are pre-installed in the container — no local installation required.

To launch a Codespace:

1. Click the green Code button at the top of this repository
2. Select the Codespaces tab
2. Click Create codespace on main

The container will build and open in your browser. This takes a few minutes the first time.

# Running Locally
If you prefer to run the tutorial locally, create a conda environment using the provided ```environment.yaml```:

```
conda env create -f environment.yaml
conda activate preprocessing-sequencing-tutorial
```

# What You'll Learn

## Step 1 - Amplicon-Based Sequencing: Mapping
- Mapping paired-end fastq reads to a reference genome with ```minimap2```
- Compressing mapped reads into a BAM file with ```samtools```

## Step 2 - Amplicon-Based Sequencing: Primer and Quality Trimming
- Trimming primer sequences and low-quality bases from mapped reads with ```ivar trim```

## Step 3 - Amplicon-Based Sequencing: Checking Read Counts and Depth
- Summarizing alignment statistics with ```samtools flagstat```
- Checking per-position coverage depth with ```samtools depth```

## Step 4 - Shotgun Metagenomics: Adaptor and Quality Trimming
- Trimming sequencing adaptors and low-quality bases from paired-end reads with ```fastp```

