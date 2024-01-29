# Install viralrecon

1. First install nextflow
https://nf-co.re/docs/usage/installation

* Primero establecer los canales de instalación de bioconda:
```
conda config --add channels defaults
conda config --add channels bioconda
conda config --add channels conda-forge
```

* Después crear en el environment donde se va a instalar y activarlo:
```
conda create --name viralrecon
conda activate viralrecon
```

* Instalar propiamente nextflow:
```
conda install nextflow
```


Despues dentro de las pipelines de nextflow buscamos viral recon que es la que nos interesa.
https://nf-co.re/viralrecon/2.6.0
