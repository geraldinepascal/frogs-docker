### Filtering tools frogs description ###

Filters OTUs on several criteria.

### Build the image ###

`docker build -t filters:1.2.0 .`

### Command example execution ###

`docker run -it --rm -v <path_data>:/root -w /root filters.py --input-biom example.biom --input-fasta db.fasta -a`
