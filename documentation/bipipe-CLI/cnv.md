## USAGE

```bash
bipipe cnv [--config CONFIG] **params
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
  "common_sites": "/PATH/TO/COMMON_SITES.interval_list",
  "pon": "/PATH/TO/PON.pon.hdf5",
  "blacklist_intervals": "/PATH/TO/BLACKLIST.interval_list",
  "minimum_base_quality": 30,
  "number_of_eigensamples": null,
  "minimum_total_allele_count_case": null,
  "minimum_total_allele_count_normal": null,
  "genotyping_homozygous_log_ratio_threshold": null,
  "genotyping_base_error_rate": null,
  "maximum_number_of_segments_per_chromosome": null,
  "kernel_variance_copy_ratio": null,
  "kernel_variance_allele_fraction": null,
  "kernel_scaling_allele_fraction": null,
  "kernel_approximation_dimension": null,
  "window_size": [8,16,32,64,128,256],
  "number_of_changepoints_penalty_factor": null,
  "minor_allele_fraction_prior_alpha": null,
  "number_of_samples_copy_ratio": null,
  "number_of_burn_in_samples_copy_ratio": null,
  "number_of_samples_allele_fraction": null,
  "number_of_burn_in_samples_allele_fraction": null,
  "smoothing_credible_interval_threshold_copy_ratio": null,
  "smoothing_credible_interval_threshold_allele_fraction": null,
  "maximum_number_of_smoothing_iterations": null,
  "number_of_smoothing_iterations_per_fit": null,
  "neutral_segment_copy_ratio_lower_bound": null,
  "neutral_segment_copy_ratio_upper_bound": null,
  "outlier_neutral_segment_copy_ratio_z_score_threshold": null,
  "calling_copy_ratio_z_score_threshold": null,
  "minimum_contig_length": null,
  "maximum_copy_ratio": null,
  "point_size_copy_ratio": null,
  "point_size_allele_fraction": null,
  "tumor_samples": [
    {
      "sample_id": "TUMOR_SAMPLE_ID",
      "r1": "/PATH/TO/TUMOR_R1.fastq.gz",
      "r2": "/PATH/TO/TUMOR_R2.fastq.gz"
    }
  ],
  "normal_samples": [
    {
      "sample_id": "NORMAL_SAMPLE_ID",
      "r1": "/PATH/TO/NORMAL_R1.fastq.gz",
      "r2": "/PATH/TO/NORMAL_R2.fastq.gz"
    }
  ]
}

```
This `cnv.json`  can be copied into the current working via

```shell
bipipe get-config cnv
```


## CLI

Parameters from the configuration file can be overwritten by the command line with the following parameters.

| Option                                           | Required | Description                                      |
|--------------------------------------------------|----------|--------------------------------------------------|
| `-h, --help`                                     | No       | Show this help message and exit                 |
| `--config CONFIG`                                | No       | Path to the configuration file for the CNV pipeline. |
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
| `--common_sites COMMON_SITES`                    | No       | Path to the common sites interval list.         |
| `--pon PON`                                      | No       | Panel of normals HDF5 file.                     |
| `--blacklist_intervals BLACKLIST_INTERVALS`      | No       | Path to blacklist intervals file.               |
| `--minimum_base_quality MINIMUM_BASE_QUALITY`    | No       | Minimum base quality.                            |
| `--number_of_eigensamples NUMBER_OF_EIGENSAMPLES` | No     | Number of eigensamples.                          |
| `--minimum_total_allele_count_case MINIMUM_TOTAL_ALLELE_COUNT_CASE` | No | Minimum total allele count (case). |
| `--minimum_total_allele_count_normal MINIMUM_TOTAL_ALLELE_COUNT_NORMAL` | No | Minimum total allele count (normal). |
| `--genotyping_homozygous_log_ratio_threshold GENOTYPING_HOMOZYGOUS_LOG_RATIO_THRESHOLD` | No | Genotyping homozygous log ratio threshold. |
| `--genotyping_base_error_rate GENOTYPING_BASE_ERROR_RATE` | No | Genotyping base error rate. |
| `--maximum_number_of_segments_per_chromosome MAXIMUM_NUMBER_OF_SEGMENTS_PER_CHROMOSOME` | No | Max segments per chromosome. |
| `--kernel_variance_copy_ratio KERNEL_VARIANCE_COPY_RATIO` | No | Kernel variance copy ratio. |
| `--kernel_variance_allele_fraction KERNEL_VARIANCE_ALLELE_FRACTION` | No | Kernel variance allele fraction. |
| `--kernel_scaling_allele_fraction KERNEL_SCALING_ALLELE_FRACTION` | No | Kernel scaling allele fraction. |
| `--kernel_approximation_dimension KERNEL_APPROXIMATION_DIMENSION` | No | Kernel approximation dimension. |
| `--window_size WINDOW_SIZE [WINDOW_SIZE ...]`    | No       | Window sizes.                                    |
| `--number_of_changepoints_penalty_factor NUMBER_OF_CHANGEPOINTS_PENALTY_FACTOR` | No | Changepoints penalty factor. |
| `--minor_allele_fraction_prior_alpha MINOR_ALLELE_FRACTION_PRIOR_ALPHA` | No | Minor allele fraction prior alpha. |
| `--number_of_samples_copy_ratio NUMBER_OF_SAMPLES_COPY_RATIO` | No | Number of samples (copy ratio). |
| `--number_of_burn_in_samples_copy_ratio NUMBER_OF_BURN_IN_SAMPLES_COPY_RATIO` | No | Burn-in samples (copy ratio). |
| `--number_of_samples_allele_fraction NUMBER_OF_SAMPLES_ALLELE_FRACTION` | No | Number of samples (allele fraction). |
| `--number_of_burn_in_samples_allele_fraction NUMBER_OF_BURN_IN_SAMPLES_ALLELE_FRACTION` | No | Burn-in samples (allele fraction). |
| `--smoothing_credible_interval_threshold_copy_ratio SMOOTHING_CREDIBLE_INTERVAL_THRESHOLD_COPY_RATIO` | No | Smoothing credible interval threshold (copy ratio). |
| `--smoothing_credible_interval_threshold_allele_fraction SMOOTHING_CREDIBLE_INTERVAL_THRESHOLD_ALLELE_FRACTION` | No | Smoothing credible interval threshold (allele fraction). |
| `--maximum_number_of_smoothing_iterations MAXIMUM_NUMBER_OF_SMOOTHING_ITERATIONS` | No | Max smoothing iterations. |
| `--number_of_smoothing_iterations_per_fit NUMBER_OF_SMOOTHING_ITERATIONS_PER_FIT` | No | Smoothing iterations