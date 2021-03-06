# Using a Structured Mesh to Simulate a Converging-Diverging Nozzle in OpenFOAM  

All code can be found at:  
https://github.com/rlee32/openfoam_tutorials/tree/master/CDNozzle  

## Description  
Here we simulate subsonic and supersonic inviscid flow in a 
converging-diverging nozzle using a structured axisymmetric mesh 
written in Gmsh. 
The flow starts subsonic at the inlet, and becomes supersonic after passing 
through the throat. 
We compare the simulation results with experimental measurements found at: 
http://www.grc.nasa.gov/WWW/wind/valid/cdv/cdv.html  
Centerline pressure values and Mach numbers are extracted via the 'sample'
utility.   

## Outline  
-Describe how to generate a structured mesh in Gmsh.
-Convert the mesh and change the boundary file.  
-Run the simulation and view comparisons.  
-Sample Mach number and pressure along the centerline axis using sampleDict.  

## Commands
gmsh mesh.geo -3 -o test.msh  
gmshToFoam test.msh -case case  
changeDictionary  
sonicFoam > log  
./residuals log  
sample -latestTime  

## Software
-Ubuntu 14.04 64-bit  
-OpenFOAM 3.0.0  
-Gmsh 2.12  