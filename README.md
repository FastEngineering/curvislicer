# Caution, this software can generate inappropriate trajectories for your printer that can damage it.

Results using OSQP can vary from the one using Gurobi.

To have the same **quality and speed** as presented at the **SIGGRAPH 2019 conference**, use the dedicated branch (**Siggraph2019**). This branch can only work with Gurobi optimizer.

# How to use it
## Prerequisites:

### IceSL
Install the latest version of IceSL (It's a slicer, with a small added feature to work with curvislice)

Once installed, move the folder "Curvy" into the folder
*windows:* **%appdata%/IceSL/icesl-printers/fff/**
*linux:* **?/icesl-printers/fff/**

### CMake
Download and install the last CMake version.

## Download, build and run

### Download
**git clone --recurse-submodules --remote-submodules https://github.com/mfx-inria/curvislicer.git**

It will download other repositories as:
	SolverWrapper (to be able to switch between Gurobi and OSQP).
	OSQP
	LibSL-small


### Build

By default, only OSQP solver will be used. If you want to use Gurobi instead, you'll have to enable the cmake flag "BUILD_WITH_GRB" and choose the "GRB_VERSION".


### Run

On Windows, run:
curvislice.bat [printer_name] [stl_filename]
On Linux, run:
curvislice.sh [printer_name] [stl_filename]