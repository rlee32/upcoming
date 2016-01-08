Simulation in OpenFOAM  

All code can be found at:  
https://github.com/rlee32/openfoam_tutorials/tree/master/this_project  

DESCRIPTION:  


OUTLINE:
-Create mesh in Gmsh.
-Convert the mesh and change the boundary file.  
-Run the simulation and view post-processed results.  

COMMANDS:  
gmsh mesh/main.geo -3 -o test.msh  
gmshToFoam test.msh -case case  
# Modify boundary file  


This tutorial was run successfully on:  
-Ubuntu 14.04 64-bit  
-OpenFOAM 3.0.0  
-Gmsh 2.11  