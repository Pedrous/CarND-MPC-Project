### Compiling

The code can be compiled by using `cmake` and `make`.

---
### Implementation

#### The Model

The model has four states and it has two actuators

#### Timestep (dt) and N

#### Polynomial fitting and MPC preprocessing

The reference trajectory points are first transformed to car coordinates and then the polynomial is fitted to car coordinates. 

#### Model Predictive Control With Latency

The algorithm is the same as thaught in the lessons, and the twiddle is used to optimize the values.

---
### Simulation

With the trained values no tyre leaves the drivable portion of the road.
