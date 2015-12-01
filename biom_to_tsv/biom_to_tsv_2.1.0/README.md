### Converter tool frogs description ###

Converts a BIOM file in TSV file.

### Build the image ###

`docker build -t biom_to_tsv:2.1.0 .`

### biom_to_tsv example execution (help) ###

`docker run -it --rm -v <path_data>:/root biom_to_tsv:2.1.0 biom_to_tsv.py -b /root/example.biom`
