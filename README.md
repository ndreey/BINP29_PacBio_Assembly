# BINP29 PacBio Long Read Assembly Excersice


## Program versions

```
sra-tools               3.0.1
fastqc                  0.12.1

```


## Setting up the data

```
# Folder to store raw data
mkdir 00_RAW

# Download the SRR reads
fasterq-dump SRR13577846 --threads 10 --progress --outdir 00_RAW/
```

## Quality Control
From the FastQC report we see that everything is in order.
The quality is above 36 and the peak is at phred score of 92.
```
# Folder to store FastQC report
mkdir 01_QC

# Run FastQC
fastqc -o 01_QC -f fastq -t 10 00_RAW/SRR13577846.fastq
```


