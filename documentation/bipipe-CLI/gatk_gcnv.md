## USAGE

```bash
bipipe gatk_gcnv [--config CONFIG] **params

```

## Example Config File

```json title="gatk_gcnv.json"
{
  "input_json": "/PATH/TO/INPUT.json",
  "output_dir": "/PATH/TO/OUTPUT_DIR",
  "exome_loc": "/PATH/TO/EXOME_LOC.bed",
  "genome_fasta": "/PATH/TO/REFERENCE/genome.fa",
  "ref_dict": "/PATH/TO/REFERENCE/genome.dict",
  "contig_pp": "/PATH/TO/CONTIG_PLOIDY_PRIORS.tsv",
  "class_coherence_length": "10000",
  "cnv_coherence_length": "10000",
  "min_contig_length": "46709983",
  "p_active": "0.01",
  "p_alt": "0.000001",
  "interval_psi_scale": "0.001"
}
```
This `gatk_gcnv.json`  can be copied into the current working via

```shell
bipipe get-config gatk_gcnv
```


## CLI

Parameters from the configuration file can be overwritten by the command line with the following parameters.

| Option                                    | Required | Description                                                           |
|-------------------------------------------|----------|-----------------------------------------------------------------------|
| `-h, --help`                              | No       | Show this help message and exit                                      |
| `--config CONFIG`                         | No       | Path to the configuration file for the GATK GCNV pipeline.           |
| `--input_json INPUT_JSON`                 | No       | Paths to input bams (JSON file)                                      |
| `--output_dir OUTPUT_DIR`                 | No       | Path to output directory                                              |
| `--exome_loc EXOME_LOC`                   | No       | Path to exome BED file                                                |
| `--genome_fasta GENOME_FASTA`             | No       | Path to genome FASTA file                                             |
| `--ref_dict REF_DICT`                     | No       | Path to reference dictionary file                                     |
| `--contig_pp CONTIG_PP`                   | No       | Path to contig ploidy prior file                                      |
| `--class_coherence_length CLASS_COHERENCE_LENGTH` | No | Class coherence length                                           |
| `--cnv_coherence_length CNV_COHERENCE_LENGTH` | No | CNV coherence length                                                 |
| `--min_contig_length MIN_CONTIG_LENGTH`   | No       | Minimum contig length                                                 |
| `--p_active P_ACTIVE`                     | No       | Prior probability of treating an interval as CNV-active              |
| `--p_alt P_ALT`                           | No       | Total prior probability of alternative copy-number states            |
| `--interval_psi_scale INTERVAL_PSI_SCALE` | No       | Typical scale of interval-specific unexplained variance              |
| `--sample_psi_scale SAMPLE_PSI_SCALE`     | No       | Typical scale of sample-specific correction to the unexplained variance |