This folder contains:

 - *Result.mp4*: the first working implementation of the IISPH model.
 - *SPH_Result.mp4*: a comparison with an implementation of the SPH model, a basic method of fluid simulation.
 - *Overpressure.mp4*: a crash test, where the simulation crash at the last frame. The yellow particle at the end has infinite pressure because it doesn't have any neighbor. When he finally have one at last frame, infinite pressure force causes the crash. (This video was made to illustrate a very specific configuration of crash, which is now fixed)
 - *Overpressure_grav.mp4*: same, but in order to better see the issue, I reversed the gravity on the right side of the grid (same intensity, but goes up). There are a few yellow particles, this time.
 - *Result_boundary.mp4*: an implementation of a new boundary handling method.
 - *Result_grav.mp4*: reversing gravity gave cool effects, so I kept a video of it on a working simulation.
 - *Result_obstacle.mp4*: a simulation with 4*24x24 particles, and an obstacle. Notice how the fluid arrange well near the obstacle.
 - *Result_pipes1.mp4*: a simulation with a few pipes, in order to see how the liquid flows.
 - *Result_pipes2.mp4*: quite the same but I rearranged the pipes in order to observe the first industrial law of thermodynamics (here, velocity * [pipe width] is a constant).
 - *Result_Upipe.mp4*: a simulation with a U pipe, in order to see how the liquid reaches a state of equilibrium.