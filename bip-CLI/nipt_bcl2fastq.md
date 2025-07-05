__Usage__

```bash
bip nipt_bcl2fastq [-h] --folders FOLDERS [FOLDERS ...] --part PART --names NAMES [NAMES ...]
                   --output-folder OUTPUT_FOLDER [--num-readers NUM_READERS] [--num-writers NUM_WRITERS]
                   [--num-processors NUM_PROCESSORS] [--compression-level COMPRESSION_LEVEL] --bcl-path
                   BCL_PATH --source-path SOURCE_PATH
```

__Options__

| Option                                        | Alias  | Required | Description                                    |
|-----------------------------------------------|--------|----------|------------------------------------------------|
| `-h, --help`                                  |        | No       | Show this help message and exit               |
| `--folders FOLDERS [FOLDERS ...]`             | `-f`   | Yes      | NIPT folders.                                  |
| `--part PART`                                 | `-p`   | Yes      | NIPT Part number.                              |
| `--names NAMES [NAMES ...]`                   | `-n`   | Yes      | Fastq sample names - For example 24B3043312.  |
| `--output-folder OUTPUT_FOLDER`               | `-o`   | Yes      | Path to the output Fastq folder.              |
| `--num-readers NUM_READERS`                   | `-r`   | No       | Number of readers.                             |
| `--num-writers NUM_WRITERS`                   | `-w`   | No       | Number of writers.                             |
| `--num-processors NUM_PROCESSORS`             | `-np`  | No       | Number of processors.                          |
| `--compression-level COMPRESSION_LEVEL`       | `-cl`  | No       | Compression level.                             |
| `--bcl-path BCL_PATH`                         | `-b`   | Yes      | Path to the BCL folder.                        |
| `--source-path SOURCE_PATH`                   | `-s`   | Yes      | Path to