
LRL_edesigner_core

eDESIGNER is an algorithm used to enumerate comprehensively DNA encoded library designs and select the ones giving a minimum number of library members that fulfill at the same time a pre-defined heavy atom distribution profile.

edesigner_core is a suit of scripts written in python. We have used eDESIGNER with the following dependencies: python 3.6.5, rdkit 2017.09.3, pandas 0.23.4 and numpy 1.15.1. All other modules are custom written and provided within the package. The scripts were run in a linux workstation with 8 processors running redhat enterprise linux version 7.6.

There are four main python scritps in the package: e_bbt_creator.py, e_designer.py, lib_designer.py and lib_design_interpreter. These scripts are run through bash wrapper scripts named: run_e_bbt_creator.sh, run_e_designer.sh, run_lib_designer.sh and run_lib_design_interpreter.sh. Any of these scripts creates the folder system required for the suit to run when they are executed. Scripts are typically executed without passing arguments, all required parameters are red from a set of configuration files that must have been placed in the folder "resources". Examples of parameters files are provided but must be edited by users to connect properly with their source building block files.

run_e_bbt_creator.sh is the first script to be run, every time that the user wants to use a different building block set. Once this script is run, a new folder is created within the folder "comps". The name of the folder has the format YYYYMMDD taken from the date the script is run. If the script is run twice in the same day the folder is overwritten. Then, the name of this folder must be introduced in the path.par file so the rest of the scripts can use the building blocks placed in that folder. The rest of the scripts can be run now (in the order that is indicated above). Final results will be placed in the folder "results"
