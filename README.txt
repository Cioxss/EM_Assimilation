The purpose of the following files are as follows:

create_realizations/create_realizations.py:
Example of a sequential Gaussian simulation script to make Gaussian reservoir models based on probably distributions and sample data.

calculate_efields.py:
This is the file to create Figure 1 and Figure 2 of the paper. It is primarily used to calculate and save the electric field responses
for the ensemble. 
Requires a porosity and permeability ensemble as given by create_realizations.py

plot_moments.py:
This loads and calculates the moments of the electric fields and temperature profiles. Used to generate Figures 3 and 4.
Uses the created files containing the electric field responses from from calculate_efields.

model_esmda.py:
A reservoir model class file for DARTS with a few small adaptations to make it work with ESMDA. Other existing DARTS reservoirs
files should be able to be used as long as they have a way of taking a vector containing the porosity or permeability data and a
way to convert between them each other in the class file.

main.py:
Main data assimilation file script. Calculates the prior, posterior, reference, and intermediate iteration results.
Requires a porosity and permeability ensemble as given by create_realizations.py

main_plotting.py:
Plots the data gotten from main.py. Used for Figure 5.

utils.py:
Some extra functions used in main.py to make main.py more readable.

dap_well_like:
Folder containing example porosity and permeability data text files which were used as the prior ensemble. 
Generated by create_realizations/create_realizations.py.

