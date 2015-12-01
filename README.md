# Command to test tools

##  TOOL biom_to_stdbiom
docker run -v $(pwd):/root -w /root biom2stdbiom:1.1.1 biom_to_stdBiom.py -b example.biom

##  TOOL biom_to_tsv
docker run -it --rm -v $(pwd):/root biom_to_tsv:2.1.0 biom_to_tsv.py -b /root/example.biom

##  TOOL clusters_stat
docker run -v $(pwd):/root -w /root clusters_stat:1.4.0 clusters_stat.py -i example.biom -o example_summary.out

##  TOOL demultiplex
docker run -it --rm -v $(pwd):/root -w /root demultiplex:1.1.0 demultiplex.py --input-R1 test.fastq --input-barcode index.tsv

##  TOOL filters
docker run -it --rm -v $(pwd):/root -w /root filters:1.1.0 filters.py --input-biom example.biom --input-fasta db.fasta -a 0.5

##  TOOL upload_tar







