Dust dynamics
=============

The transport of dust particles is determined the disk properties (radial drift, settling) and the turbulence levels of the disk (diffusion).
We briefly explain the different components of the dust velocites in this section. For further detail we refer the reader to Drazkowska et al 2013.

Radial velocity
+++++++++++++++

The radial advection velocity is given by,

.. math:: 

    v^r_d = \frac{v_g}{1 + \mathrm{St}^2} + \frac{2v_\eta}{\mathrm{St} + \mathrm{St}^{-1}}

The above equation takes into account radial drift of dust particles due to the differences in dust and gas radial and azimuthal velocities.

The radial diffusion is implemented as a random kick on the particle distributions as in Ciesla 2010 and Zsom et al 2011. 

Vertical velocity
+++++++++++++++++
In the vertical direction, settling of the dust particles due to the gravity of the central star is of importance. This is given by,

.. math:: 

    v_z = -z\Omega_K \mathrm{St}]

The diffusion in the vertical direction is implemented in the same way as in the radial direction as turbulent kicks.

Advection timestep
++++++++++++++++++

