# Force-fields-for-metal-cations

## Introduction
******************
We have developed force field parameters for the metal cations Li+, Na+, K+, Cs+, Mg2+, Ca2+, Sr2+, and Ba2+ in combination with the TIP3P water model.
Our optimized parameters simultaneously reproduce thermodynamic and kinetic properties of aqueous solutions (hydration free energy, activity derivative and water exchange rate from the first hydration shell).
Our optimized parameters aim to capture the role of different cations in all-atom molecular dynamics simulations of biological processes including ion specific binding and ion binding kinetics.


## Quick start guide
******************
Our parameters are optimized for the TIP3P water model.
The parameters work in combination with all protein and RNA force fields (e.g. amber14sb.ff).
All parameter sets here are to be used with the Lorentz-Berthelot combination rule (otherwise modifications are required).
Note that we have chosen unique names for the optimized parameters to avoid errors in overwriting atom names:
* CXY - Cl
* LIO - Li
* NIO - Na
* KIO - K
* CIO - Cs
* Mg2 - MG
* Ca2 - CA
* Sr2 - SR
* Ba2 - BA

To get started: Replace the standard ion names in your .gro file by our unique names.
Modify the given topology file according to your system. The topology file includes the optimized force field parameters via ffions.itp and ions.itp


## Example: 0.5 molar MgCl2
******************
Folder contains all files for an MD simulation of 0.5 molar MgCl2 solution with GROMACS.
Initial coordinates are given in out.gro.
To create a .tpr file for energy minimization type: gmx grompp -f mdout.mdp -c out.gro -p topol.top

## Citation
******************
If you use our optimized parameters for metal cations please cite:
S. Mamatkulov and N. Schwierz, J. Chem. Phys., 148, 074504 (2018)
https://doi.org/10.1063/1.5017694


Implementation has been tested by Nadine Schwierz and Sergio Cruz-Leon.
USE AT YOUR OWN RISK!!
