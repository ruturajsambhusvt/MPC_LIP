# MPC_LIP
The main.m file needs to be run. The real height parameter 
needs to be changed to see the robustness. The desired_vel 
needs to be changed to change the step size and hence speed.

List of the functions

-applyAction - used to apply action in closed loop discrete dynamics

-applyActionODE - used to apply action in closed loop continuous ODE 

-Dynamics - get the dynamics based on real height 

-getCOMTargetTrajectory- get the target COM positions from the step size 
extrapolation

-getCOMTargetTrajectory_Footholds - get the target COM trajectories as the
average of the contacting footsteps

-getContactMatrix - gets the contact matrix for the problem.

-getDomainIndicator - return which domain number the current time step belongds to

-getDynamics - gets the discrete and continuous dynamics for controller design

-getFootHolds - designs the foot holds to track the required step size

-getForceFeet - gets the Force data in format required by the animator

-getInputs - obtains primarily the inputs to be applied to the system, also

provides more parameters  such as C_lambda, equalities, feet, lambda, contact indicstor
and matrix of contact indicators with lambdas in place of 1

-getQP - gets the cost function H,f and equality and inequality matrices that need to 
be fed into the qp solvers

-getTargetTrajectory - obtains the LIP state target trajectory having all velocity targets
as zero

-plotResults - Plots the results 