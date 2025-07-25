## USAGE

```bash
bipipe bwa_dedup [--config CONFIG] **params
```

## Example Config File

```json title="bwa_dedup.json"
{
  "ref_fasta": "/PATH/TO/REFERENCE/genome.fa",
  "bed_file": "/PATH/TO/TARGETS.bed",
  "out_path": "/OUTPUT/DIRECTORY",
  "r1": "/PATH/TO/SAMPLE_R1.fastq.gz",
  "r2": "/PATH/TO/SAMPLE_R2.fastq.gz",
  "sample_name": "SAMPLE_ID",
  "at": "bwtsw",
  "threads": 40,
  "remove_dups": false,
  "remove_seq_dups": false,
  "use_md": false
}
```

This `bwa_dedup.json`  can be copied into the current working via

```shell
bipipe get-config bwa_dedup
```

## CLI

Parameters from the configuration file can be overwritten by the command line with the following parameters.

| Option                | Required | Description                                                    |
|-----------------------|----------|----------------------------------------------------------------|
| `-h, --help`          | No       | Show this help message and exit                               |
| `--config CONFIG`     | No       | Path to the configuration file for the bwa_dedup_sp_qc_mosdepth pipeline. |
| `--ref_fasta REF_FASTA` | No     | Path to the reference FASTA file.                             |
| `--bed_file BED_FILE` | No       | Path to the BED file for coverage analysis.                   |
| `--at AT`             | No       | Algorithm type for BWA indexing (default is 'bwtsw').         |
| `--out_path OUT_PATH` | No       | Output directory for results.                                  |
| `--r1 R1`             | No       | Path to the first read FASTQ file.                            |
| `--r2 R2`             | No       | Path to the second read FASTQ file.                           |
| `--sample_name SAMPLE_NAME` | No | Sample identifier for output files.                           |
| `--threads THREADS`   | No       | Number of threads to use for processing.                      |
| `--remove_dups`       | No       | Whether to remove all duplicates (default is False).          |
| `--remove_seq_dups`   | No       | Whether to remove sequencing duplicates (default is False).   |
| `--use_md`            | No       | Whether to use MarkDuplicatesSpark (default is False).        |