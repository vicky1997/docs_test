Input and Output files
============
Input
++++++
There are two required input files to run a simulation with mcdust, setup.par and prepocs.opt. The details are each file are explained below.

Input file 1: setup.par
-----------------------

This is the file to specify the simulation parameters. The parameters to be entered in the file are written below

number_of_particles_per_cell  - Number of particles in a cell          
number_of_radial_zones  -  Number of radial grids            
number_of_vertical_zones -  Number of vertical grids                 
steps_between_outputs  - Number of iterations between outputs                   
time_between_outputs_[yrs] - time duration between outputs               
maximum_time_of_simulation_[yrs]  - simulation time in yrs
minimum_radius_[AU] - inner radial boundary of the simulation in AU                      
maximum_radius_[AU] - outer radial boundary of the simulation in AU                      
monomer_radius_[cm] - radius of the particle monomers in cm                      
material_density_[g/cm3] - internal density of the particles in g/cm3                 
dmmax  -                                    
evaporation_radius_[AU] - radius inside which particles will not be tracked anymore                  
dust_to_gas_ratio - the dust to gas ratio in the disk                        
fragmentation_velocity_[cm/s] - fragmentation velocity of the particles            
alpha - the alpha turbulence value to specifiy the strength of the turbulence in the disk                                   
sigma_gas_[g/cm2] - the gas surface density at 1 AU                        
temperature_[K]  - the temperature in K at 1 AU                         
erosion_mass_ratio - mass ratio condition to trigger erosion                     
data_directory - directory name to write the data  


If the values for the parameters are not entered in the file, the default values will be taken as specified in the parameters.f90 file. New parameters can be added to the simulation vial the parameters.f90 file.


Input file 2: preprocs.opt
--------------------------
This file specifies the regions of the code to be compiled based on compiler options. The current compiler options are listed

VERTICALMODEL: activate this to setup a 1D vertical model
TRANSPORT: activate dust transport
VERTSETTLING: activate vertical settling of particles
RADRIFT: activate radial drift of particles
COLLISIONS: activate dust coagulation
EROSION: activate erosion as a collision outcome
AUXDATA: write timestep data
RESTART: restart a simulation from a snapshot


Output
++++++

The output files are of the hdf5 file format with the extension .h5. Each snapshot has its own file and can accessed in outputs directory.

Each data file contains the properties of each representative particle. The properties that are stored in the default version are given below.
.. code-block

To add new properties to be written, one can add the same in the hdf5output.f90 file.
