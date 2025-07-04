## USAGE

```bash
Usage: bipipe gatk_gcnv [-h] [--config CONFIG] [--input_json INPUT_JSON]
                        [--output_dir OUTPUT_DIR] [--exome_loc EXOME_LOC]
                        [--genome_fasta GENOME_FASTA] [--ref_dict REF_DICT]
                        [--contig_pp CONTIG_PP]
                        [--class_coherence_length CLASS_COHERENCE_LENGTH]
                        [--cnv_coherence_length CNV_COHERENCE_LENGTH]
                        [--min_contig_length MIN_CONTIG_LENGTH]
                        [--p_active P_ACTIVE] [--p_alt P_ALT]
                        [--interval_psi_scale INTERVAL_PSI_SCALE]
                        [--sample_psi_scale SAMPLE_PSI_SCALE]

```

## Example Config

```json
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


## CLI

```bash
Options:
  -h, --help            "show this help message and exit"
  --config CONFIG       "Path to the configuration file for the GATK GCNV pipeline."
  --input_json INPUT_JSON
                        "Paths to input bams (JSON file)"
  --output_dir OUTPUT_DIR
                        "Path to output directory"
  --exome_loc EXOME_LOC
                        "Path to exome BED file"
  --genome_fasta GENOME_FASTA
                        "Path to genome FASTA file"
  --ref_dict REF_DICT   "Path to reference dictionary file"
  --contig_pp CONTIG_PP
                        "Path to contig ploidy prior file"
  --class_coherence_length CLASS_COHERENCE_LENGTH
                        "Class coherence length"
  --cnv_coherence_length CNV_COHERENCE_LENGTH
                        "CNV coherence length"
  --min_contig_length MIN_CONTIG_LENGTH
                        "Minimum contig length"
  --p_active P_ACTIVE   "Prior probability of treating an interval as CNV-active"
  --p_alt P_ALT         "Total prior probability of alternative copy-number states"
  --interval_psi_scale INTERVAL_PSI_SCALE
                        "Typical scale of interval-specific unexplained variance"
  --sample_psi_scale SAMPLE_PSI_SCALE
                        "Typical scale of sample-specific correction to the unexplained variance"
```