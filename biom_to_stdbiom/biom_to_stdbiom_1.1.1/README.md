### Converter tool frogs description ###

Converts a FROGS BIOM in fully compatible BIOM.

### Build the image ###

`docker build -t biom_to_stdbiom:1.1.1 .`

### biom_to_stdbiom example execution (help) ###

`docker run -v <data_path>:/root -w /root biom2stdbiom:1.1.1 biom_to_stdBiom.py -b example.biom`
