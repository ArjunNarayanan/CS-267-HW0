# Homework 0 - CS 267 - Applications of Parallel Computers - Arjun Narayanan
## My Bio
My academic and professional interests are broadly in the field of simulation and scientific computing. I developed an interest in this field during my masters in Civil and Environmental Engineering at Stanford University. I took courses on mechanics (solids and fluids), numerical methods (finite difference, explicit/implicit schemes), and the finite element method. For my research, I implemented an isogeometric finite element method which uses Bezier basis functions, and applied it to study high order PDEs of non-linear elasticity arising from higher-gradient formulations. Subsequently, I worked at Siemens Corporate Technology (2016-2017) as a research engineer. I used simulation to improve product design of various industrial machines, primarily for the Power & Gas division. I also implemented multi-scale analysis methods to aid with Design for Additive Manufacturing.

I am a PhD student in the department of Mechanical Engineering at UC Berkeley. I develop finite element methods to study solid-solid phase transformations that are relevant to geophysics. Through CS 267, I want to learn how I can reduce the compute time of my finite element simulations. I am also interested in computational geometry and would like to learn parallel algorithms that will be relevant to this field.

## Multi-physics phase field simulations
Phase field simulations are a popular class of numerical methods used to simulate microstructure evolution. These include transient phenomenon like solidification, dendrite growth, and phase transformations. (See Chen 2002 for an overview of the method.) At its heart, the phase field method aims to study the evolution of _order parameters_. Order parameters may be used as an indicator to represent, for example, various chemical species in a chemical reaction, differing phases of a material undergoing phase transition, damaged or fractured regions in a material that is failing. Often, it is necessary to couple these evolution equations with other physics -- for example heat transfer and mechanics.

We will specifically examine the capabilities and application of the Multiphysics Object-Oriented Simulation Environment [MOOSE](https://mooseframework.inl.gov/) developed by the Idaho National Laboratory (INL). MOOSE is built on several well known and well tested numerical libraries including the finite element framework [libMesh](http://libmesh.github.io/) and the [PETSc](https://www.mcs.anl.gov/petsc/) and [Trilinos](https://github.com/trilinos/Trilinos) suites. Thus, MOOSE has been designed with scalability and parallelization in mind. MOOSE supports both shared memory and distributed memory parallelism. INL has developed several specialized modules for various classes of problems, including thermo-mechanics (BISON), geo-mechanics (FALCON), phase-field (MARMOT) among others. (For a more detailed list please see [this presentation](https://mooseframework.inl.gov/static/media/uploads/docs/main.pdf).) INL users regularly perform large scale simulations using MOOSE on their supercomputer FALCON which ranks 361 on the top500 list as of 2018.

## Application: Temperature dependent stability of Al-Cu alloys
In Shower et al 2018, phase field simulations were performed using the MOOSE framework to understand the stability regimes of precipitate strengthened Al-Cu alloys. Commercial Al-Cu alloys are strengthened by the presence of high aspect ratio disc shaped precipitates of Al<sub>2</sub>Cu. At elevated temperatures, phase transformations cause these precipitates to grow, with a reduction in aspect ratio. This results in a significant deterioration (~60%) in strength and hardness of the alloy. 



## Bibliography
Chen, Long-Qing. "Phase-field models for microstructure evolution." Annual review of materials research 32, no. 1 (2002): 113-140.

Tonks, Michael R., Derek Gaston, Paul C. Millett, David Andrs, and Paul Talbot. "An object-oriented finite element framework for multiphysics phase field simulations." Computational Materials Science 51, no. 1 (2012): 20-29.

Shower, Patrick, James R. Morris, Dongwon Shin, Balasubramaniam Radhakrishnan, Lawrence L. Allard, and Amit Shyam. "Temperature-dependent stability of θ′-Al2Cu precipitates investigated with Phase Field simulations and experiments." Materialia (2018): 100185.
