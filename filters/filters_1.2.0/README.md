### Filtering tools frogs description ###

Filters OTUs on several criteria.

### Build the image ###

`docker build -t filters:1.2.0 .`

### Command example execution ###

`docker run -it --rm -v <path_data>:/root -w /root  demultiplex:1.2.0 demultiplex.py --input-R1 test.fastq --input-barcode index.tsv`
