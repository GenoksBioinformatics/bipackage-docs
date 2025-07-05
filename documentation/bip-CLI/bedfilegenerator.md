
__Usage__

```bash
bip bedfilegenerator [-h] --gene-list GENE_LIST [GENE_LIST ...] --bed-file-name BED_FILE_NAME --output-folder OUTPUT_FOLDER --whole-gene-list WHOLE_GENE_LIST [WHOLE_GENE_LIST ...] [--parsed-gtf-path PARSED_GTF_PATH] [--whole-gene-locs-path WHOLE_GENE_LOCS_PATH] [--cds] [--ref-folder REF_FOLDER]
```

__Options__

| Option                                        | Alias    | Required | Description                                                    |
|-----------------------------------------------|----------|----------|----------------------------------------------------------------|
| `-h, --help`                                  |          | No       | Show this help message and exit                               |
| `--gene-list GENE_LIST [GENE_LIST ...]`       | `-g`     | Yes      | Gene names to include.                                         |
| `--bed-file-name BED_FILE_NAME`               | `-b`     | Yes      | Name of the output BED file.                                   |
| `--output-folder OUTPUT_FOLDER`               | `-o`     | Yes      | Folder to save the output BED file.                           |
| `--whole-gene-list WHOLE_GENE_LIST [...]`     | `-w`     | Yes      | Whole gene names to include.                                   |
| `--parsed-gtf-path PARSED_GTF_PATH`           | `-p`     | No       | Path to Parsed GTF file.                                       |
| `--whole-gene-locs-path WHOLE_GENE_LOCS_PATH` | `-wglp`  | No       | Path to whole gene locs file.                                  |
| `--cds`                                       | `-c`     | No       | If used, use CDS features; otherwise use exon features.       |
| `--ref-folder REF_FOLDER`                     | `-rf`    | No       | Path to the folder for reference