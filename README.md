# ceres
A set of routines for processing data of echelle spectrographs

Author: Rafael Brahm (rbrahm@astro.puc.cl)

# About the code
The principal goal of the CERES routines is the developement of fully automated pipelines for the reduction, extraction and analysis of echelle data. CERES currently counts with dedicated pipelines for eleven different instruments, which are included in the repository: APO3.5m/ARCES, CAHA2.2m/CAFE, Euler1.2m/Coralie, DuPont2.5m/Echelle, MPG2.2m/FEROS, ESO1.0m/FIDEOS, ESO3.6m/HARPS, KECK10m/HIRES, MAGELLAN6.5m/MIKE, MALLEGAN6.5m/PFS, PUC0.5m/PUCHEROS. These processing recipes can be used as reference for developing pipelines for new instruments. A detailed decription of the structure and performance of these pipelines can be found in [Brahm et al 2016](http://adsabs.harvard.edu/abs/2016arXiv160705792B). The standard output of the pipelines is a cube fits with the optimally extracted, wavelength calibrated and instrumetal drift corrected spectrum for each of the science images. Additionally, CERES includes routines for the computation of precise radial velocities and bisector spans via the cross-correlation method, and an automated algorithm to obtain a relatively precise guess of the atmospheric parameters of the observed star.

# Usage
In order to run one of the pipelines, you have to be in the CERES directory where the pipeline lives and run the correspondig python pipe code followed by the path to the raw data. For example in the case of the FEROS pipeline you have to enter:

    $ cd ceres/feros
    $ python ferospipe.py /path/to/the/raw/data/to/be/processed

Additionally you can add some options to the command in order to modify some of the processing steps. The allowed options are:

    -avoid_plot     this option will prevent the code to generate a pdf file with the plot of the computed CCF

    -dirout     path to the directory where the reductions will be placed. The default path will be a
                new directory with the same name that the input directory but followed by a '_red' suffix.
                
    -do_class   this option will allow the code to perform the estimation of the atmospheric parameters.
    
    
    



