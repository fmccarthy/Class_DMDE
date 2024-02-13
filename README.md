CLASS_DMDE: Cosmic Linear Anisotropy Solving System for dark matter-dark energy scattering
==============================================

Authors: Alex Lague, Fiona McCarthy, Colin Hill, Mathew Madhavacheril

This is a fork of the Einstein-Boltzmann solver CLASS v3 (https://lesgourg.github.io/class_public/class.html), written by Julien Lesgourgues, Thomas Tram, Nils Schoeneberg, et al.; refer to the original repository for the README of CLASS, including installation instructions.

This code was described in Lague et al arXiv:2024.XXXX . Please cite this paper, along with the original CLASS citations, if you use the code.



Differences with respect to CLASS
-----------------------------------

In addition to the standard parameters of CLASS, there is no an additional parameter Gamma_DMDE that can be read in the input file. This is in the explanatory.ini file. If you read this in, use_ppf must be set to 'no' and w0_fld must be greater than -1 (as in explanatory.ini)


 
