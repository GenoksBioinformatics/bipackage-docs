## USAGE

```bash
bipipe snv_indel [--config CONFIG] **params
```

## Example Config File

```json title="snv_indel.json"
{
  "algotype": "bwtsw",
  "index_fasta": false,
  "aligner_threads": 40,
  "remove_all_duplicates": true,
  "remove_sequencing_duplicates": false,
  "use_gatk_mark_duplicates": true,
  "use_dragen": false,
  "output_folder": "/PATH/TO/OUTPUT/FOLDER",
  "run_name": "RUN_NAME",
  "ref_fasta": "/PATH/TO/REFERENCE/genome.fa",
  "ref_dict": "/PATH/TO/REFERENCE/genome.dict",
  "interval_list": "/PATH/TO/INTERVAL_LIST.interval_list",
  "scatter_count": 48,
  "germline_resource": "/PATH/TO/GERMLINE_RESOURCE.vcf.gz",
  "index_image": "/PATH/TO/INDEX_IMAGE.img",
  "downsampling_stride": null,
  "panel_of_normals": null,
  "variants_for_contamination": null,
  "max_reads_per_alignment_start": null,
  "max_suspicious_reads_per_alignment_start": null,
  "max_population_af": null,
  "lrom": true,
  "interval_padding": 100,
  "tumor_samples": [
    {
      "sample_id": "TUMOR_SAMPLE_ID",
      "r1": "/PATH/TO/TUMOR_R1.fastq.gz",
      "r2": "/PATH/TO/TUMOR_R2.fastq.gz"
    },
    {
      "sample_id": "TUMOR_SAMPLE_ID1",
      "r1": "/PATH/TO/TUMOR_R1.fastq.gz",
      "r2": "/PATH/TO/TUMOR_R2.fastq.gz"
    },
    {
      "sample_id": "TUMOR_SAMPLE_ID2",
      "r1": "/PATH/TO/TUMOR_R1.fastq.gz",
      "r2": "/PATH/TO/TUMOR_R2.fastq.gz"
    }
  ],
  "normal_samples": [
    {
      "sample_id": "NORMAL_SAMPLE_ID",
      "r1": "/PATH/TO/NORMAL_R1.fastq.gz",
      "r2": "/PATH/TO/NORMAL_R2.fastq.gz"
    },
    {
      "sample_id": "NORMAL_SAMPLE_ID1",
      "r1": "/PATH/TO/NORMAL_R1.fastq.gz",
      "r2": "/PATH/TO/NORMAL_R2.fastq.gz"
    },
    {
      "sample_id": "NORMAL_SAMPLE_ID2",
      "r1": "/PATH/TO/NORMAL_R1.fastq.gz",
      "r2": "/PATH/TO/NORMAL_R2.fastq.gz"
    }
  ]
}
```
This `snv_indel.json`  can be copied into the current working via

```shell
bipipe get-config snv_indel
```


## CLI

Parameters from the configuration file can be overwritten by the command line with the following parameters.

| Option                                           | Required | Description                                      |
|--------------------------------------------------|----------|--------------------------------------------------|
| `-h, --help`                                     | No       | Show this help message and exit                 |
| `--config CONFIG`                                | No       | Path to the configuration file for the SNV/Indel pipeline. |
| `--algotype ALGOTYPE`                            | No       | Algorithm type for BWA indexing.                |
| `--index_fasta`                                  | No       | Whether to index the FASTA file.                |
| `--aligner_threads ALIGNER_THREADS`              | No       | Number of threads for the aligner.              |
| `--remove_all_duplicates`                        | No       | Remove all duplicates.                           |
| `--remove_sequencing_duplicates`                 | No       | Remove sequencing duplicates.                    |
| `--use_gatk_mark_duplicates`                     | No       | Use GATK MarkDuplicates.                         |
| `--use_dragen`                                   | No       | Use DRAGEN.                                      |
| `--output_folder OUTPUT_FOLDER`                  | No       | Output folder for results.                       |
| `--run_name RUN_NAME`                            | No       | Run name.                                        |
| `--ref_fasta REF_FASTA`                          | No       | Path to the reference FASTA file.               |
| `--ref_dict REF_DICT`                            | No       | Path to the reference dictionary file.          |
| `--interval_list INTERVAL_LIST`                  | No       | Path to the interval list file.                 |
| `--scatter_count SCATTER_COUNT`                  | No       | Scatter count.                                   |
| `--germline_resource GERMLINE_RESOURCE`          | No       | Path to the germline resource VCF.              |
| `--index_image INDEX_IMAGE`                      | No       | Path to the index image.                         |
| `--downsampling_stride DOWNSAMPLING_STRIDE`      | No       | Downsampling stride.                             |
| `--panel_of_normals PANEL_OF_NORMALS`            | No       | Panel of normals file.                           |
| `--variants_for_contamination VARIANTS_FOR_CONTAMINATION` | No | Variants for contamination file.           |
| `--max_reads_per_alignment_start MAX_READS_PER_ALIGNMENT_START` | No | Max reads per alignment start.       |
| `--max_suspicious_reads_per_alignment_start MAX_SUSPICIOUS_READS_PER_ALIGNMENT_START` | No | Max suspicious reads per alignment start. |
| `--max_population_af MAX_POPULATION_AF`          | No       | Max population allele frequency.                 |
| `--lrom`                                         | No       | Enable LROM.                                     |
| `--interval_padding INTERVAL_PADDING`            | No       | Interval padding.                                |
| `--tumor_samples TUMOR_SAMPLES`                  | No       | JSON string or path to tumor samples list.      |
| `--normal_samples NORMAL_SAMPLES`                | No       | JSON string or path to normal samples list.     |