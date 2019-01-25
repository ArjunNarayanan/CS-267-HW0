# Homework 0 - CS 267 - Applications of Parallel Computers - Arjun Narayanan
## My Bio
My academic and professional interests are broadly in the field of simulation and scientific computing. I developed an interest in this field during my masters in Civil and Environmental Engineering at Stanford University. I took courses on mechanics (solids and fluids), numerical methods (finite difference, explicit/implicit schemes), and the finite element method. For my research, I implemented an isogeometric finite element method which uses Bezier basis functions, and applied it to study high order PDEs of non-linear elasticity arising from higher-gradient formulaitons. Subsequently, I worked at Siemens Corporate Technology (2016-2017) as a research engineer. I used simulation to improve product design of various industrial machines, primarily for the Power & Gas division. I also implemented multi-scale analysis methods to aid with Design for Additive Manufacturing.

I am a PhD student in the department of Mechanical Engineering at UC Berkeley. I develop finite element methods to study solid-solid phase transformations that are relevant to geophysics. Through CS 267, I want to learn how I can reduce the compute time of my finite element simulations. I am also interested in computational geometry and would like to learn parallel algorithms that will be relevant to this field.

## Multi-physics phase field simulations
Phase field simulations are a popular class of numerical methods used to simulate microstructure evolution. These include transient phenomenon like solidification, dendrite growth, and phase transformations. (See Chen 2002 for an overview of the method.) At its heart, the phase field method aims to study the evolution of __order parameters__. Order parameters may be used as an indicator to represent, for example, various chemical species in a chemical reaction, differing phases of a material undergoing phase transition, damaged or fractured regions in a material that is failing. Often, it is necessary to couple these evolution equations with other physics -- for example thermomechanics.

We will specifically examine the __MARMOT__ numerical framework which is based on Idaho National Laboratory's Multiphysics Object-Oriented Simulation Environment (__MOOSE__). See Tonks et al 2012 for details.

### The need for parallelism


## Bibliography
Chen, Long-Qing. "Phase-field models for microstructure evolution." Annual review of materials research 32, no. 1 (2002): 113-140.

Tonks, Michael R., Derek Gaston, Paul C. Millett, David Andrs, and Paul Talbot. "An object-oriented finite element framework for multiphysics phase field simulations." Computational Materials Science 51, no. 1 (2012): 20-29.
