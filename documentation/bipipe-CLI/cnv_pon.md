## USAGE

```bash
bipipe cnv_pon [--config CONFIG] **params
```


## Example Config File

```json title="cnv_pon.json"
{
  "output_folder": "/PATH/TO/OUTPUT/FOLDER",
  "ref_fasta": "/PATH/TO/REFERENCE/genome.fa",
  "ref_dict": "/PATH/TO/REFERENCE/genome.dict",
  "interval_list": "/PATH/TO/INTERVAL_LIST.interval_list",
  "pon_id": "PON_ID",
  "normal_bams": [
    "/PATH/TO/NORMAL1.bam",
    "/PATH/TO/NORMAL2.bam",
    "/PATH/TO/NORMAL3.bam"
  ],
  "gc_correction": true,
  "bin_length": 10000,
  "blacklist_intervals": "/PATH/TO/BLACKLIST.interval_list",
  "padding": 250,
  "do_impute_zeros": true,
  "number_of_eigensamples": 20,
  "feature_query_lookahead": 1000000,
  "minimum_interval_median_percentile": 10.0,
  "maximum_zeros_in_sample_percentage": 5.0,
  "maximum_zeros_in_interval_percentage": 5.0,
  "extreme_sample_median_percentile": 2.5,
  "extreme_outlier_truncation_percentile": 0.1,
  "maximum_chunk_size": 16777216

}
```


This `cnv_pon.json`  can be copied into the current working via

```shell
bipipe get-config cnv_pon
```



## CLI

Parameters from the configuration file can be overwritten by the command line with the following parameters.

| Option                                           | Required | Description                                      |
|--------------------------------------------------|----------|--------------------------------------------------|
| `-h, --help`                                     | No       | Show this help message and exit                 |
| `--config CONFIG`                                | No       | Path to the configuration file for the PON pipeline. |
| `--output_folder OUTPUT_FOLDER`                  | No       | Output folder for results.                       |
| `--ref_fasta REF_FASTA`                          | No       | Path to the reference FASTA file.               |
| `--ref_dict REF_DICT`                            | No       | Path to the reference dictionary file.          |
| `--interval_list INTERVAL_LIST`                  | No       | Path to the interval list file.                 |
| `--pon_id PON_ID`                                | No       | Panel of Normals ID.                            |
| `--normal_bams NORMAL_BAMS [NORMAL_BAMS ...]`    | No       | List of normal BAM files.                       |
| `--gc_correction`                                | No       | Enable GC correction.                           |
| `--bin_length BIN_LENGTH`                        | No       | Bin length.                                     |
| `--blacklist_intervals BLACKLIST_INTERVALS`      | No       | Path to blacklist intervals file.              |
| `--padding PADDING`                              | No       | Padding value.                                  |
| `--do_impute_zeros`                              | No       | Impute zeros.                                   |
| `--number_of_eigensamples NUMBER_OF_EIGENSAMPLES` | No     | Number of eigensamples.                         |
| `--feature_query_lookahead FEATURE_QUERY_LOOKAHEAD` | No   | Feature query lookahead.                        |
| `--minimum_interval_median_percentile MINIMUM_INTERVAL_MEDIAN_PERCENTILE` | No | Minimum interval median percentile. |
| `--maximum_zeros_in_sample_percentage MAXIMUM_ZEROS_IN_SAMPLE_PERCENTAGE` | No | Maximum zeros in sample percentage. |
| `--maximum_zeros_in_interval_percentage MAXIMUM_ZEROS_IN_INTERVAL_PERCENTAGE` | No | Maximum zeros in interval percentage. |
| `--extreme_sample_median_percentile EXTREME_SAMPLE_MEDIAN_PERCENTILE` | No | Extreme sample median percentile. |
| `--extreme_outlier_truncation_percentile EXTREME_OUTLIER_TRUNCATION_PERCENTILE` | No | Extreme outlier truncation percentile. |
| `--maximum_chunk_size MAXIMUM_CHUNK_SIZE`        | No       | Maximum chunk size. |