# Project Name: Vacuum Cleaner Simulation, ex3

## submitters
- Tomer Yihya 203596192
- Or Asheri 318506557

## Project Structure

The project consists of:
- **Main Application:** Compiles the main simulator executable.
- **Algorithms:** Two separate algorithms (`Algorithm_318506557_A` and `Algorithm_318506557_B`) implemented as shared objects (`.so` files).

## Prerequisites

Ensure that you have the following tools installed on your system:
- `g++`: GNU Compiler Collection to compile C++ code.
- `make`: A build automation tool to execute the commands in the Makefile.

## Build Instructions

Build the Main Application and Algorithms: 

Use the make command to compile the main application and both algorithms inside the project's main directory:
`make`

This command will:
Compile the `myrobot` executable using the source files specified in SOURCES.
Compile the `Algorithm_318506557_A.so` shared object using the source files specified in SOURCES_ALGO_A.
Compile the `Algorithm_318506557_B.so` shared object using the source files specified in SOURCES_ALGO_B.

Clean the Build: To remove all compiled files and clean the build directory, use: `make clean`
This command deletes the myrobot executable and both .so files (Algorithm_318506557_A.so and Algorithm_318506557_B.so).

In order to compile the files seperatly, use:
`make myrobot`
`make Algorithm_318506557_A.so`
`make Algorithm_318506557_B.so`


## The algorithms implementations are as following:
1. Algorithm_A:
Greedy algorithm, which always priotize the closest dirty coordinates to clean/explore. 

2. Algorithm_B:
An algorithm which moves in circuliar ways around the docking, which whenever encounters an obsticle it incriments its radius of its circle and whenever its relizes its trapped in a closed space becomes greedy.

Note:
We had another implementation which did an extensive usage with DFS, but in manners of results it wasn't better than the previous ones so we left it out.

