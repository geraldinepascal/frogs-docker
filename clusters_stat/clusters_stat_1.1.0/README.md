### Clustering frogs description ###

Process some metrics on clusters.

### Build the image ###

`docker build -t clusters_stat:1.1.0 .`

### Command example execution (help) ###

`docker run -it --rm -v <path_data>:/root -w /root clusters_stat:1.1.0 clusters_stat.py -i example.biom -o example_summary.out`
