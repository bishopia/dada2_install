# How to build dada2 environment
##### not the most straighforward install, here's how i've been doing it.

### in your home directory, download and install miniconda3
```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
bash Miniconda3-latest-Linux-x86_64.sh
```

### install mamba in your base environment
```
conda install mamba -c conda-forge
```

### create new conda environment, put it in a place with all your other conda environments and where there is lots of spaces (e.g. data, not home or scratch)
```
mamba create --prefix /gpfs/home/ibishop/data/ibishop/condas/dada2
```
### activate
```
conda activate /gpfs/home/ibishop/data/ibishop/condas/dada2
```
### install r then devtools
```
mamba install -c conda-forge r-base=4.0
mamba install -c conda-forge r-devtools=2.4.2
```

### start R
```
R
```

### load libraries and install via dada2 via github
```
library("devtools")
devtools::install_github("benjjneb/dada2", ref="v1.16")
```

### check version
```
packageVersion("dada2")
help(package="dada2")
```
