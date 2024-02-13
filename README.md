CLASS_DMDE: Cosmic Linear Anisotropy Solving System for dark matter-dark energy scattering
==============================================

Authors: Alex Laguë, Fiona McCarthy, Colin Hill, Mathew Madhavacheril

This is a fork of the Einstein-Boltzmann solver CLASS v3 (https://lesgourg.github.io/class_public/class.html), written by Julien Lesgourgues, Thomas Tram, Nils Schoeneberg, et al.; refer to the original repository for the README of CLASS, including installation instructions.

This code was described in Lague et al arXiv:2024.XXXX . Please cite this paper, along with the original CLASS citations, if you use the code.

All modifications are indicated with either 
```
// FMcC DMDE edit 
// end FMcC DMDE edit
```
or
```
// AL modif 
```
.



Differences with respect to CLASS
-----------------------------------

In addition to the standard parameters of CLASS, there is no an additional cosmological parameter Gamma_DMDE that controls the size of the coupling between dark energy and dark matter perturbations. The value of this can be read in in the input file. This can be seen in the explanatory.ini file. If you read this in,it is neccesary to set:

```
'fluid_equation_of_state': 'CLP',
'gauge':'newtonian',
'use_ppf':False,
'w0_fld': XXX
```
where XXX>-1.

-----------------------------------
Additionally, there are modifications to the nonlinear hmcode computation as described in Laguë et al. If you use 

```
'Gamma_DMDE': xxx
'non_linear': 'hmcode'
```
for xxx>0, the modified non-linear model will be used. These include both incorporation of the DMDE model as well as some updates to the CLASS hmcode implementation; to use this with LCDM set Gamma_DMDE to a very small positive number. If 'non_linear' is set to 'halofit', even with non-zero Gamma_DMDE, the standard LCDM halofit fitting functions will be used. 
 
