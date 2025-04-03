Quickstart
=====

Pre-requisites:

    * A Linux/Unix based OS

    * a fortran compiler (preferably gfortran), 
    
    * a fortran-OpenMP installation
    
    * a Python installation (if you want to use the pre-written post-processing scripts)
Now one can clone the github repository to use the code.

:code:`git clone git@github.com:astrojoanna/mcdust.git`

First run
+++++++++
#. Make the :code:`/setups/default` setup 
    :code:`make default`
#. Set the number of threads for OpenMP parallelisation.
    :code:`export OMP_NUM_THREADS=$OMP_NUM_THREADS`
#. Run the code
    :code:`cd setups/Setup1`
    :code:`./default setup.par`



