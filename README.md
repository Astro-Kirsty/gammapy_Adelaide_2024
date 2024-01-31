![alt text](https://github.com/gammapy/gammapy-extra/blob/master/logo/gammapy_banner.png?raw=true)


# Hands-on workshop on VHE data analysis using Gammapy

This folder contains the analysis notebooks shown in the Gammapy hands on sessions for University of Adelaide and CTA-Oz

## Installation and set-up

These instructions assume that you have previously installed a version of [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) on your machine.

### Gammapy installation


We recommend that you install the latest version of gammapy as follows: 

```
curl -O https://gammapy.org/download/install/gammapy-1.1-environment.yml
conda env create -f gammapy-1.1-environment.yml
conda activate gammapy-1.1
```

OR with `pip`
```
python -m pip install gammapy[all]
```

### Download tutorials & associated data

To download the tutorials and associated datasets (necessary for the tutorials in this workshop)

```
gammapy download notebooks
gammapy download datasets
```

If using conda environment, set GAMMAPY_DATA with conda
```
conda env config vars set GAMMAPY_DATA=$PWD/gammapy-datasets/1.1
conda activate gammapy-1.1
```

else set with shell:
```
export GAMMAPY_DATA=$PWD/gammapy-datasets/1.1
```

### Check your installation

To check that the gammapy environment is working, open a new terminal and type

```
conda activate gammapy-1.1
gammapy info
```
To further check that you have correctly set up the data folder type

```
ipython
```

Then in the ipython window, type
```
from gammapy.data import DataStore
ds = DataStore.from_dir("$GAMMAPY_DATA/hess-dl3-dr1")
obs = ds.get_observations()
print(len(obs))
```

If the cells run without any error and prints `105`, **Congratulations! You have correctly set-up gammapy**

## Tutorials and timetable for the day

Session 1 - 1D spectral simulation


Session 2 - Simulation of sky maps

Lunch

Session 3 - Internal Science Data Challenge (Sabrina)

Session 4 - Producing 1D spectra

Session 5 - Producing skymaps through 3D analysis



