### Demultiplexing frogs description ###

Split by samples the reads in function of inner barcode.

### Build the image ###

`docker build -t demultiplex:1.1.0 .`

### Command example execution ###

`docker run -it --rm -v <path_data>:/root -w /root demultiplex:1.1.0 demultiplex.py --input-R1 test.fastq --input-barcode index.tsv`
