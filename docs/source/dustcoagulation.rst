Dust coagulation
================

Dust coagulation in :code:`mcdust` is done with a Monte Carlo approach rather than solving the Smoluchowski equation. We briefly explain the method here.
For details we refer the reader to Drazkowksa et al 2013 and Zsom and Dullemond 2008. We follow representative particles and follow their evolution rather than tracking every single particle and its evolution. These :math:`n` representative particles statistically represent :math:`N` physical particles (:math:`n << N`).
For eg, the representative particle :math:`i` shares identical properties with :math:`N_i` physical particles. 
The total mass of physical particles in one swarm (:math:`M_{\mathrm{swarm}}`) is given by,

.. math:: 

    M_{\mathrm{swarm}} = m_i N_i,

where :math:`m_i` is the mass of the representative particle :math:`i`. The fundamental assumption here is that :math:`M_{\mathrm{swarm}}` is the same for every swarm and is a constant that does not change with time. This means that if a particle grows (:math:`m_i` increases),
the number of particles it represents reduces (:math:`N_i`). This is a statistical effect and not a physical effect.  

Collisions
++++++++++
In this framework, we assume that the representative particles themselves do not collide with each other (the collisions between the representative particles are too rare). The representative particles collide with physical (non-representative) particles whose history we do not track. We track only the representative particle and its evolution.

To perform a collision we choose a representative particle :math:`i` and a physical particle which represented by representative particle :math:`k`. The probability of a collision between particle :math:`i` and particle :math:`k` is given by,

.. math:: 

    r_{ik} = \frac{N_k K_{ik}}{V},

where V is the cell volume and :math:`K_{ik}` is the coagulation kernel which is given by,

.. math:: 

    K_{ik} = \Delta v_{ik} \sigma_{ik},

with :math:`\sigma_{ik}` being the geometric cross-section for the collision and :math:`\Delta v_{ik}` being the relative velocity between particle :math:`i` and :math:`k`. 




Collisional Outcomes
--------------------
In the standard model the collisional outcomes are sticking, fragmentation and erosion. The outcomes are decided based on the relative velocities of the particles.
If the relative velocities are below a threshold velocity then we perform sticking. This threshold is the fragmentation velocity :math:`v_{\mathrm{frag}}` which is an input parameter for :code:`mcdust`.
If the relative velocities are above the fragmentation velocity then there are two outcomes erosion and fragmentation depending on the mass ratio of the particles.

Sticking
^^^^^^^^

Fragmentation & Erosion
^^^^^^^^^^^^^^^^^^^^^^^



Collision Optimization
----------------------

Adaptive Grid
+++++++++++++
In order to 

Relative velocity
+++++++++++++++++
