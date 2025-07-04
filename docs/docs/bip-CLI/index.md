
```bash
bip --help
```

```bash
Usage: bip [-h] [--version]
           {bam_counts,compile_bam_stats,cbs,bedfilegenerator,bfg,panelgenequery,pgq,downsample,fastq_read_counter,frc,fastqvalidate,fqv,merge_it,mff,undetermined_demultiplexer,ud,remove_undetermined_fastq,ruf,is_mounted,mount_server,check_reconnect,md5sumchecker,md5sc,check_gzip_validity,cgv,nipt_bcl2fastq,nb2f}
           ...

BIpackage CLI

Positional Arguments:
  {bam_counts,compile_bam_stats,cbs,bedfilegenerator,bfg,panelgenequery,pgq,downsample,fastq_read_counter,frc,fastqvalidate,fqv,merge_it,mff,undetermined_demultiplexer,ud,remove_undetermined_fastq,ruf,is_mounted,mount_server,check_reconnect,md5sumchecker,md5sc,check_gzip_validity,cgv,nipt_bcl2fastq,nb2f}
    bam_counts          "Get counts from BAM file."
    compile_bam_stats (cbs)
                        "Complies BAM stats to CSV."
    bedfilegenerator (bfg)
                        "Generate and sort BED files from a parsed GTF file."
    panelgenequery (pgq)
                        "Using an intersected bedfile, produces a file with gene presence information."
    downsample          "Pipeline to map, deduplicate, and downsample sequencing reads."
    fastq_read_counter (frc)
                        "Count reads from FASTQ file."
    fastqvalidate (fqv)
                        "Validate fastq files in a given directory using`fastQValidator`."
    merge_it (mff)      "Merge FASTQ files."
    undetermined_demultiplexer (ud)
                        "Filter undetermined FASTQ files for multiple samples using index information."
    remove_undetermined_fastq (ruf)
                        "Remove undetermined FASTQ files (recursively) from a directory."
    is_mounted          "Check if a given path is a mounted server."
    mount_server        "Mount a server."
    check_reconnect     "Check reconnects."
    md5sumchecker (md5sc)
                        "Check md5sum of a file."
    check_gzip_validity (cgv)
                        "Check a compressed file validity."
    nipt_bcl2fastq (nb2f)
                        "Run bcl2fastq conversion for multiple BCL folders."

Options:
  -h, --help            "show this help message and exit"
  --version, -v         "Show version"
```