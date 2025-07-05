__Usage__

```bash
bip undetermined_demultiplexer [-h] --sample_sheet SAMPLE_SHEET --input_r1 INPUT_R1 --input_r2 INPUT_R2
                               --output_dir OUTPUT_DIR --json_output JSON_OUTPUT [--threads THREADS]
```

__Options__

| Option                          | Alias  | Required | Description                                          |
|---------------------------------|--------|----------|------------------------------------------------------|
| `-h, --help`                    |        | No       | Show this help message and exit                     |
| `--sample_sheet SAMPLE_SHEET`   | `-s`   | Yes      | Path to the sample sheet CSV file.                  |
| `--input_r1 INPUT_R1`           | `-r1`  | Yes      | Path to the undetermined R1 FASTQ.gz file.          |
| `--input_r2 INPUT_R2`           | `-r2`  | Yes      | Path to the undetermined R2 FASTQ.gz file.          |
| `--output_dir OUTPUT_DIR`       | `-o`   | Yes      | Directory to store the filtered FASTQ files.        |
| `--json_output JSON_OUTPUT`     | `-j`   | Yes      | Path to output JSON file for sample target indices. |
| `--threads THREADS`             | `-t`   | No       | Number of threads to use (default: 4).              |