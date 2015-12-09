### Affiliation tools frogs description ###

Process some metrics on taxonomies.

### Build the image ###

`docker build -t affiliations_stat:1.1.0 .`

### Command example execution ###

`docker run -it --rm -v <path_data>:/root -w /root affiliations_stat.py -h`
