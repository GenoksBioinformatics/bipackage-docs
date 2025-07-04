

__Usage__

```bash
bip downsample [-h] --sample_id SAMPLE_ID --r1 R1 --r2 R2 --out-path OUT_PATH --reference REFERENCE
               [--threads THREADS] [--remove-all-dups] [--remove_seq_dups] [--use-gatk-md]
               [--strategy STRATEGY] [--keep KEEP]
```

__Options__

| Option                      | Alias | Required | Description                      |
|-----------------------------|-------|----------|----------------------------------|
| `-h, --help`                |       | No       | Show this help message and exit |
| `--sample_id SAMPLE_ID`     | `-s`  | Yes      | Sample ID.                       |
| `--r1 R1`                   | `-r1` | Yes      | Path to R1 fastq file.          |
| `--r2 R2`                   | `-r2` | Yes      | Path to R2 fastq file.          |
| `--out-path OUT_PATH`       | `-o`  | Yes      | Output path for the results.     |
| `--reference REFERENCE`     | `-r`  | Yes      | Path to the reference genome.    |
| `--threads THREADS`         | `-t`  | No       | Number of threads to use.        |
| `--remove-all-dups`         | `-ra` | No       | Remove all duplicates            |
| `--remove_seq_dups`         | `-rs` | No       | Remove sequencing duplicates     |
| `--use-gatk-md`             | `-ug` | No       | Use GATK MarkDuplicatesSpark     |
| `--strategy STRATEGY`       | `-st` | No       | Downsampling strategy            |
| `--keep KEEP`               | `-k`  | No       | How much read to keep? Give a ratio