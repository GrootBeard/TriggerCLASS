TriggerCLASS
==============================================
forked from CLASS by Julien Lesgourgues and Thomas Tram; see http://class-code.net and https://github.com/lesgourg/class_public

TriggerCLASS is a modification of CLASS that implements an instant phase transition triggered by a clock field and with adiabatic perturbations consistently included, as used to trigger the decay of an early dark energy component. As such, it describes the physics of the New Early Dark Energy (NEDE) and Hybrid Early Dark Energy model. The details of the implementation have been explained in the methodology part of https://arxiv.org/abs/2006.06686 and through many additional comments in the code tagged with "NEDE".

The version used for the publications ArXiv: 1910.10739, 2006.06686, 2009.00006 has been tagged with "NewEDEv3.0". 

Compiling TriggerCLASS and getting started
-----------------------------------

In order to install TriggerCLASS, clone the branch "NewEDEv3" in a new folder and follow the same steps as required for the installation of the base CLASS code detailed in https://github.com/lesgourg/class_public. Also see the Wiki page:

https://github.com/lesgourg/class_public/wiki/Installation

After compiling it, check that TriggerCLASS has been properly set up by running first
    
    ./class explanatory.ini

This corresponds to a standard LambdaCDM run. To check that the trigger component works correctly, type:

    ./class input/NewEDE.ini

This should result in a run with a non-vanishing fraction of NEDE. The output should provide a detailed account of the NEDE parameters.
The NewEDE.ini also explains the NEDE input parameters.

MCMC analysis
------

In order to perform a MCMC analysis, we recommend using MontePython, https://github.com/brinckmann/montepython_public, and follow their installation instructions. Our baseline MCMC run (as discussed in https://arxiv.org/abs/2006.06686) can be found under input/run_NEDE_base_wH0.param. To make it run, you first need to update MontePython with the files from the folder montepython_tree. In particular, this will update the data.py, needed to vary the fraction of NEDE and the log of the trigger mass directly. The corresponding covariance matrix and bestfit file can be found in the respective subfolders covmat and bestfit.

Support
-------

To get support, please open a new issue on

https://github.com/flo1984/TriggerClass

