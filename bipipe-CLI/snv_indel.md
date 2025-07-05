## USAGE

```bash
Usage: bipipe snv_indel [-h] [--config CONFIG] [--algotype ALGOTYPE]
                        [--index_fasta] [--aligner_threads ALIGNER_THREADS]
                        [--remove_all_duplicates]
                        [--remove_sequencing_duplicates]
                        [--use_gatk_mark_duplicates] [--use_dragen]
                        [--output_folder OUTPUT_FOLDER] [--run_name RUN_NAME]
                        [--ref_fasta REF_FASTA] [--ref_dict REF_DICT]
                        [--interval_list INTERVAL_LIST]
                        [--scatter_count SCATTER_COUNT]
                        [--germline_resource GERMLINE_RESOURCE]
                        [--index_image INDEX_IMAGE]
                        [--downsampling_stride DOWNSAMPLING_STRIDE]
                        [--panel_of_normals PANEL_OF_NORMALS]
                        [--variants_for_contamination VARIANTS_FOR_CONTAMINATION]
                        [--max_reads_per_alignment_start MAX_READS_PER_ALIGNMENT_START]
                        [--max_suspicious_reads_per_alignment_start MAX_SUSPICIOUS_READS_PER_ALIGNMENT_START]
                        [--max_population_af MAX_POPULATION_AF] [--lrom]
                        [--interval_padding INTERVAL_PADDING]
                        [--tumor_samples TUMOR_SAMPLES]
                        [--normal_samples NORMAL_SAMPLES]

```

## Example Config

```json
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


## CLI

```bash
Options:
  -h, --help            "show this help message and exit"
  --config CONFIG       "Path to the configuration file for the SNV/Indel pipeline."
  --algotype ALGOTYPE   "Algorithm type for BWA indexing."
  --index_fasta         "Whether to index the FASTA file."
  --aligner_threads ALIGNER_THREADS
                        "Number of threads for the aligner."
  --remove_all_duplicates
                        "Remove all duplicates."
  --remove_sequencing_duplicates
                        "Remove sequencing duplicates."
  --use_gatk_mark_duplicates
                        "Use GATK MarkDuplicates."
  --use_dragen          "Use DRAGEN."
  --output_folder OUTPUT_FOLDER
                        "Output folder for results."
  --run_name RUN_NAME   "Run name."
  --ref_fasta REF_FASTA
                        "Path to the reference FASTA file."
  --ref_dict REF_DICT   "Path to the reference dictionary file."
  --interval_list INTERVAL_LIST
                        "Path to the interval list file."
  --scatter_count SCATTER_COUNT
                        "Scatter count."
  --germline_resource GERMLINE_RESOURCE
                        "Path to the germline resource VCF."
  --index_image INDEX_IMAGE
                        "Path to the index image."
  --downsampling_stride DOWNSAMPLING_STRIDE
                        "Downsampling stride."
  --panel_of_normals PANEL_OF_NORMALS
                        "Panel of normals file."
  --variants_for_contamination VARIANTS_FOR_CONTAMINATION
                        "Variants for contamination file."
  --max_reads_per_alignment_start MAX_READS_PER_ALIGNMENT_START
                        "Max reads per alignment start."
  --max_suspicious_reads_per_alignment_start MAX_SUSPICIOUS_READS_PER_ALIGNMENT_START
                        "Max suspicious reads per alignment start."
  --max_population_af MAX_POPULATION_AF
                        "Max population allele frequency."
  --lrom                "Enable LROM."
  --interval_padding INTERVAL_PADDING
                        "Interval padding."
  --tumor_samples TUMOR_SAMPLES
                        "JSON string or path to tumor samples list."
  --normal_samples NORMAL_SAMPLES
                        "JSON string or path to normal samples list."

```