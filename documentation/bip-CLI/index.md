
__Usage__
```bash
bip [command] **params
```

| Command                      | Alias   | Description |
|------------------------------|---------|-------------|
| `bam_counts`                 |         | Get counts from BAM file. |
| `compile_bam_stats`          | `cbs`   | Complies BAM stats to CSV. |
| `bedfilegenerator`           | `bfg`   | Generate and sort BED files from a parsed GTF file. |
| `panelgenequery`             | `pgq`   | Using an intersected bedfile, produces a file with gene presence information. |
| `downsample`                 |         | Pipeline to map, deduplicate, and downsample sequencing reads. |
| `fastq_read_counter`         | `frc`   | Count reads from FASTQ file. |
| `fastqvalidate`              | `fqv`   | Validate fastq files in a given directory using `fastQValidator`. |
| `merge_it`                   | `mff`   | Merge FASTQ files. |
| `undetermined_demultiplexer` | `ud`    | Filter undetermined FASTQ files for multiple samples using index information. |
| `remove_undetermined_fastq`  | `ruf`   | Remove undetermined FASTQ files (recursively) from a directory. |
| `is_mounted`                 |         | Check if a given path is a mounted server. |
| `mount_server`               |         | Mount a server. |
| `check_reconnect`            |         | Check reconnects. |
| `md5sumchecker`              | `md5sc` | Check md5sum of a file. |
| `check_gzip_validity`        | `cgv`   | Check a compressed file validity. |
| `nipt_bcl2fastq`             | `nb2f`  | Run bcl2fastq conversion for multiple BCL folders. |

__Options__

| Option           | Description                       |
|------------------|-----------------------------------|
| `-h, --help`     | Show this help message and exit   |
| `--version, -v`  | Show version                      |