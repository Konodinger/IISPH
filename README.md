This is the main repository for an IGR202 project at Télécom Paris.
The project is to implement a fluid simulation method called IISPH in a 2D environment, and to visualize it with a simple representation using the glfw library.

You can find the paper used for the implementation of IISPH at `doc/Implicit_Incompressible_SPH.pdf`. There is also a report of the details of the method as well as the improvements I made at `doc/IISPH_report_BERGER_Jonas.pdf`.

Most of the code for the visualization and a part of the simulation comes from a TP of SPH implementation from Télécom Paris.
The specificities of the IISPH can be found in the methods computing the intermediate velocity, the d_ii and a_ii coefficient, and the intermediate density.

## Initialisation

The code is initialized with specific coordinates for the wall (which are stationary particles) and the fluid particles. It can be found in the `initScene()` method in `src/main.cpp`. You can modify the display to your preferences, but beware of the collision and the off-grid particles! A few exemples of wall display can be found in comments in the method, you can try those by placing the fluid accordingly.

## Exemples

You can find in the `exemples` folder a few videos illustrating different tests made with the simulation. There is also a `README.md` document detailing what the videos represen.

## Build

The code uses the ***glad*** and ***glfw*** libraries, which are already on the repository. However, those are for a Windows 10+ computer, so you may need to reinstall it on your own computer if you use another OS (or if the project doesn't compile).
It also uses the ***openMP*** libraries. It is not mandatory for the execution, but you may want to use it since it really fasten the computations.

You can build the executable by entering this command in your terminal:

```bash
cmake -B build
```
If, like me, you use *MinGW* for cmake compilation, you may need to specify it with the flag `-G "MinGW Makefiles"`.

Then, in the `build/` folder, enter this command:

```bash
cmake --build .
```

## Run

You can now run the code simply by executing the `tpSph.exe` file. A window should open with the simulation in a grid. You can start and stop the simulation by pressing **P**, and quit the program by pressing **Q**. For a detail of the different options of the simulation, you can check the help section by pressing **H**.
