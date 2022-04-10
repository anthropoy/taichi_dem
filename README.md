# DEM (Discrete Element Modelling) in Taichi
In this project, we have a built a basic DEM solver using Taichi HPC programming language. By letting Taichi do the heavy lifting in GPU processing at the backend and with Python has the front-end, it has enabled users to write high performance solvers in only hundreds of lines of Python code. 

Taichi is platform agnostic and supports various backends, CPU, CUDA, Vulkan and even Apple's Metal. More information of Taichi can be found in this gihub repo https://github.com/taichi-dev/taichi.

## DEM Implementation Summary
In around 300 lines of Python code, it includes a simple hash grid, solver and rendering. 

The contact model is a linear spring model with linear viscous elastic rolling friction model. Particles are rendered using Taichi's built-in rendering engine. 

## Setup
The main dependency is only the Taichi Python module. Note that Taichi only support Python 3.7 to 3.9. Taichi requirement is 0.9.0 and above.

```
python -m pip install taichi
```
To run the demo example, it's just simply

```
python dem_gui_demo.py
```
The example demo shows the collapse of a column of 72K particles. Although particle cohesion has not been added yet, but due to rolling friction, it eventually forms a pile.

