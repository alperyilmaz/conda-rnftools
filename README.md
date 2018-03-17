# conda-rnftools

Dockerized version of [RNFtools](http://rnftools.readthedocs.io).

Citation for RNFtools:

> K. Břinda, V. Boeva, G. Kucherov. **RNF: a general framework to evaluate NGS read mappers**. Bioinformatics 32(1), pp. 136-139, 2016. [doi:[10.1093/bioinformatics/btv524](http://dx.doi.org/10.1093/bioinformatics/btv524)]

# how to use the Docker image

```bash
docker run --rm alperyilmaz/conda-rnftools rnftools --help
```

## accessing local folders

Assume that you placed `Snakefile` and genome files within `data` folder under current working directory. 

```bash
docker run --rm -v $(pwd)/data:/data alperyilmaz/conda-rnftools snakemake -s Snakemake
```
