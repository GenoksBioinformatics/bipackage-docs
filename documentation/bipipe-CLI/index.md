# BIPackage Pipelines CLI

__Usage__

```bash
bipipe [-h] [--version] {bwa_dedup,gatk_gcnv,cnv_pon,snv_indel,cnv,get-config} ...
```

__Positional Arguments__

| Command     | Description                                           |
|-------------|-------------------------------------------------------|
| `bwa_dedup` | Run the bwa_dedup_sp_qc_mosdepth pipeline.           |
| `gatk_gcnv` | Run the GATK GCNV pipeline.                          |
| `cnv_pon`   | Run the Panel of Normals (PON) pipeline.             |
| `snv_indel` | Run the SNV/Indel pipeline.                          |
| `cnv`       | Run the CNV pipeline.                                 |
| `get-config`| Get examples pipeline configurations in json format. |

__Options__

| Option        | Description                           |
|---------------|---------------------------------------|
| `-h, --help`  | Show this help message and exit      |
| `--version`   | Show program's version              |