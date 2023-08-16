# GenBank Genomic FNA Downloader

Use this tool to retrieve genomic `.fna` files from GenBank using accession or assembly numbers.

## Table of Contents
- [Overview](#overview)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Example](#example)
- [Disclaimer](#disclaimer)
- [Contributing](#contributing)

## Overview

This script facilitates the fetching of genomic `.fna` files hosted on GenBank's FTP servers using provided accession or assembly numbers. This tool is invaluable for researchers and bioinformaticians who frequently deal with genomic sequences and need a streamlined way to retrieve specific `.fna` files from GenBank.

## Requirements

- NCBI's Entrez Direct command-line tools. Installation instructions are available [here](https://www.ncbi.nlm.nih.gov/books/NBK179288/).

## Installation

1. Clone this repository:
   ```sh
   git clone https://github.com/ryu1013/accession_to_genbank_link.git
   ```

2. Navigate to the cloned directory:
   ```sh
   cd accession_to_genbank_link
   ```

3. Make it executable:
   ```sh
   chmod +x accession_to_genbank_link.py
   ```

3. Ensure you have the required tools and dependencies installed.

## Usage

Execute the script directly from the command line:

```sh
./accession_to_link_converter.py -i INPUT_FILE [-o OUTPUT_FILE]
```

### Parameters:

- `-i` or `--input`: Path to the input file containing the accession or assembly numbers. One number per line.
- `-o` or `--output`: Path to the output file where the resulting HTTPS links will be saved (default: `results.tsv`).

## Example

Given an input file `accessions.txt`:

```
JSPI01
JAJLMS000000000
GCA_000258785.1
```

The resulting `results.tsv` might look like:

```
Accession        Link
JSPI01           https://ftp.ncbi.../GCA_000779275.1_ASM77927v1_genomic.fna.gz
JAJLMS000000000  https://ftp.ncbi.../GCA_023705435.1_ASM2370543v1_genomic.fna.gz
GCA_000258785.1  https://ftp.ncbi.../GCA_000258785.1_genomic.fna.gz
```

(Note: The actual links can vary based on the FTP server's structure and specific accession numbers.)

## Disclaimer

- Always ensure you have the necessary permissions to download data.
- The FTP server structure or URL format might change. Ensure tool compatibility with the current NCBI FTP structure.

## Contributing

If you'd like to contribute, please fork the repository and use a feature branch. Pull requests are warmly welcomed.
