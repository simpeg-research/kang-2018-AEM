**[summary](#summary) | [contents](#contents) | [usage](#usage) | [running the notebooks](#running-the-notebooks) | [issues](#issues) | [citation](#citation) | [license](#license)**

# Feasibility of induced polarization effects in time-domain airborne EM data

[![Build Status](https://travis-ci.org/simpeg-research/heagy-2018-AEM.svg?branch=master)](https://travis-ci.org/simpeg-research/heagy-2018-AEM)
[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/simpeg-research/heagy_2018_AEM/master)
[![License](https://img.shields.io/github/license/simpeg-research/heagy-2018-AEM.svg)](https://github.com/simpeg-research/heagy-2018-AEM/blob/master/LICENSE)
[![SimPEG](https://img.shields.io/badge/powered%20by-SimPEG-blue.svg)](http://simpeg.xyz)

Notebooks and python scripts to reproduce the figures shown in
"[Feasibility of induced polarization effects in time-domain airborne EM data](/aem_workshop_2018_kang_seogi.pdf),"
submitted to the AEM 2018 workshop.


<iframe width="560" height="315" src="https://www.youtube.com/embed/hebXfwISnh0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/Hkrplu6f8co" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


## Summary

The potential for extracting and interpreting induced polarization (IP) data from air- borne surveys is now broadly recognized. There is, however, still considerable discussion about the conditions under which the technique can provide knowledge about the sub- surface and thus, its practical applications. Foremost among these is whether, or under what conditions, airborne IP can detect chargeable bodies at depth. To investigate, we focus on data obtained from a coincident loop time-domain system. Our analysis is expedited by using a stretched exponential rather than a Cole-Cole model to represent the IP phenomenon. Our paper begins with an example that illuminates the physical understanding about how negative transients (the typical signature of the airborne IP) can be generated. The effects of the background conductivity are investigated and this shows that a moderately conductive and chargeable target in a resistive host is an ideal scenario for generating strong IP signals. We then address the important topic of estimating the maximum depth of the chargeable target that can generate nega- tive transients. Lastly, some potential chargeable earth materials are discussed and their typical IP time-domain features are analyzed. The results presented in this paper can be reproduced and further explored by accessing the provided Jupyter notebooks.

## Contents

There are 4 notebooks in this repository:

- [TEM_VerticalConductor_2D_forward.ipynb](/notebooks/TEM_VerticalConductor_2D_forward.ipynb) : runs a forward simulation of an airborne electromagnetic simulation over a conductive plate. This notebook was used to generate figures 1-4 in the abstract
- [TEM_VerticalConductor_1D_stitched_inversion.ipynb](/notebooks/TEM_VerticalConductor_1D_stitched_inversion.ipynb) : Using the forward simulated data from the previous notebook, we run 1D inversions over the plate (Figure 5 in the abstract).
- [TEM_VerticalConductor_2D_inversion_load.ipynb](/notebooks/TEM_VerticalConductor_2D_inversion_load.ipynb) : This notebook loads the 2D inversion results over the plate (Figure 6 in the abstract). The 2D inversion was run using the script [2dinv_smooth.py](/notebooks/2d_inv_smooth/2dinv_smooth.py).
- [TEM_VerticalConductor_parametric_inversion_load.ipynb](/notebooks/TEM_VerticalConductor_parametric_inversion_load.ipynb) : This notebook loads the 2D parametric inversion inversion results (Figure 7 in the abstract). The 2D parametric inversion was run using the script [2dinv_parametric.py](/notebooks/2d_inv_parametric/2d_inv_parametric.py) .

In addition, there are two notebooks used for demos in the workshop [3D EM Modelling and Inversion with Open Source Resources](https://courses.geosci.xyz/aem2018):

- [TEM_VerticalConductor_2D_forward.ipynb](/demo_notebooks/TEM_VerticalConductor_2D_forward.ipynb) : runs a forward simulation of an airborne electromagnetic simulation over a conductive plate. Similar to that in the notebooks directory.
- [TDEM_1D_inversion.ipynb](/demo_notebooks/TDEM_1D_inversion.ipynb): In this notebook, we run a 1D inversion for a single airborne time domain EM sounding

## Usage

Dependencies are specified in [requirements.txt](/requirements.txt)

```
pip install -r requirements.txt
```

To run the notebooks locally, you will need to have python installed,
preferably through [anaconda](https://www.anaconda.com/download/) .

You can then clone this repository. From a command line, run

```
git clone https://github.com/simpeg-research/kang-2018-AEM.git
```

Then `cd` into the `kang-2018-AEM` directory:

```
cd kang-2018-AEM
```

To setup your software environment, we recommend you use the provided conda environment

```
conda env create -f environment.yml
source activate aem-environment
```


alternatively, you can install dependencies through pypi

```
pip install -r requirements.txt
```

You can then launch Jupyter

```
jupyter notebook
```

Jupyter will then launch in your web-browser.

## Running the notebooks

Each cell of code can be run with `shift + enter` or you can run the entire notebook by selecting `cell`, `Run All` in the toolbar.

<img src="https://raw.githubusercontent.com/simpeg-research/heagy-2018-emcyl/revisions/figures/cell_run_all.png" width=80% align="middle">

For more information on running Jupyter notebooks, see the [Jupyter Documentation](https://jupyter.readthedocs.io/en/latest/)

## Issues

Please [make an issue](https://github.com/simpeg-research/kang-2018-AEM/issues) if you encounter any problems while trying to run the notebooks.

## Citation

If you build upon or use these examples in your work, please cite:

Kang, S., Oldenburg, D. W., and Heagy, L. J.(2018). Feasibility of induced polarization effects in time-domain airborne EM data.

```
@inproceedings{kang2018,
author = {Kang, Seogi and Oldenburg, Douglas W. and Heagy, Lindsey J.},
booktitle = {7th International Workshop on Airborne Electromagnetics},
keywords = {induced Polarization, airborne electromagnetic, time-domain},
title = {{Feasibility of induced polarization effects in time-domain airborne EM data}},
year = {2018}
}
```

## License
These notebooks are licensed under the [MIT License](/LICENSE) which allows academic and commercial re-use and adaptation of this work.
