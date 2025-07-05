## USAGE

```bash
Usage: bipipe bwa_dedup [-h] [--config CONFIG] [--ref_fasta REF_FASTA]
                        [--bed_file BED_FILE] [--at AT] [--out_path OUT_PATH]
                        [--r1 R1] [--r2 R2] [--sample_name SAMPLE_NAME]
                        [--threads THREADS] [--remove_dups]
                        [--remove_seq_dups] [--use_md]
```


## Example Config



```json
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

```python
Options:
  -h, --help            "show this help message and exit"
  --config CONFIG       "Path to the configuration file for thebwa_dedup_sp_qc_mosdepth pipeline."
  --ref_fasta REF_FASTA 
                        "Path to the reference FASTA file."
  --bed_file BED_FILE   "Path to the BED file for coverage analysis."
  --at AT               "Algorithm type for BWA indexing (default is 'bwtsw')."
  --out_path OUT_PATH   "Output directory for results."
  --r1 R1              " Path to the first read FASTQ file."
  --r2 R2               "Path to the second read FASTQ file."
  --sample_name SAMPLE_NAME
                        "Sample identifier for output files."
  --threads THREADS     "Number of threads to use for processing."
  --remove_dups         "Whether to remove all duplicates (default is False)."
  --remove_seq_dups     "Whether to remove sequencing duplicates (default is False)."
  --use_md              "Whether to use MarkDuplicatesSpark (default is False)."
```