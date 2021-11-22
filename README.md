# WRR_UpwellingLakeTahoe2018_NumericalSimulations
2021WR030666_Valbuena_etal_3D_Flow_Structures_During_Upwelling_Events_in_Lakes_of_Moderate_Size.

This repository contains the following:

1 "LakeTahoeUpwelling2018" contains the Si3D files needed to reproduce numerical results.
	
	1.1 "h" is the bathymetry file used (100 m x 100 m)
	1.2 "si3d_init.txt" is the temperature profile used as the initial condition in the water column
	1.3 "si3d_layer.txt" is the description of the vertical resolution of the numerical simulation
	1.4 "surfbc.txt" is the time series surface boundary conditions used in the numerical simulations
	1.5 "si3d_inp.txt" is the main file of Si3D where parameters controlling the numerical simulations are specified
	1.6 "psi3d_20-11-12" compiled executable psi3d file to run numerical simulations.

2 "NodeTimeSeries" contains the numerical results of vertical profiles at locations of interest (i.e., sites for calibration and validation of the numerical model). 
	
	2.1 "tfx_y.txt" files of sites at locations x, y of the model's bathymetry grid
	2.2 "LocationSites.txt" indicates the locations x, y of sites used for numerical calibration and validation. Columns "idx" and "idy" align to files tfx_y.txt

3 The Version of the Si3D source code used.

To reproduce the numerical outputs presented within the manuscript submitted to the Water Resources Research journal, the user must run the compiled executable file "psi3d_20-11-12" within the folder "LakeTahoeUpwelling2018". Execution of the file will run the numerical simulations for the period of study and will reproduce the results provided within the "NodeTimeSeries" folder along with a 3D binary file "ptrack_hydro.bnr" containing the numerical outputs for the whole domain. Finally, a binary file "plain_2" containing the outputs at the surface of the lake is generated after running the numerical model. 

To read the 3D binary file "ptrack_hydro.bnr" produced by the numerical model, the script "Si3DtoParaview.m" can be used to create vtk files that can be read and viewed using the OpenSource software Paraview.
