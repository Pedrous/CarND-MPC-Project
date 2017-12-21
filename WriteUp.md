### Compiling

The code can be compiled by using `cmake` and `make`.

---
### Implementation

#### The Model

The model has four states and it has two actuators

##### Timestep (dt) and number of steps (N)

The timestep 0.1 was used because it seemeed to function well and also because it was the same as the latency 100 ms so there was really no need to control more frequently. The number of steps was chosen to 20, 10 and 15 steps were also tried but there was not much difference. Maybe 20 steps gives a little bit smoother trajectory with high speeds and I tried to optimize a high speed.

##### Polynomial fitting and MPC preprocessing

The reference trajectory points are first transformed to car coordinates and then the polynomial is fitted to car coordinates. Then the state is calculated for one step ahead before inputting the state to MPC. Also the speed is calculated from mph to m/s.

##### Model Predictive Control With Latency

The latency is tackled by calculating the future state values one step ahead and inputting them to the MPC solver. 

---
### Simulation

With the trained values no tyre leaves the drivable portion of the road.
