# LMPC Autonomous Racing

This repository evaluates the performance and learning efficiency of a **Learning Model Predictive Control (LMPC)** framework within a simulated autonomous racing environment on the **Yoshi Circuit**.

## Project Overview
The primary goal of this project was to test how the LMPC framework adapts to changing environmental conditions and track disturbances while optimizing the learning process to reach benchmark speeds faster.

## Key Features
* **Learning Optimization**: Implemented a decaying weighted cost on lateral error during early training laps. This strategy significantly reduced the number of iterations required to reach benchmark lap times.
* **Environmental Disturbances**: Integrated a stochastic **Wind Model** (Gaussian distribution) and longitudinal/lateral **aerodynamic drag** terms into the vehicle dynamics to evaluate controller robustness.
* **Adaptive Friction Control**: Engineered a friction-aware subsystem that allows the controller to detect and adapt to sudden changes in road conditions, such as **surprise ice**. The system adjusts peak wheel forces and dynamics based on real-time friction look-ups.



## Results
* **Baseline Performance**: Reached a best lap time of **25.90 seconds** through iterative learning of terminal costs and constraints.
* **Robustness**: Maintained stability and adapted trajectories when encountering wind and variable friction zones.
* **Efficiency**: Increased the learning rate using weighted costs, achieving faster lap times in significantly fewer iterations compared to unweighted baseline tests.

## Team
* **Wanangwa Nyasulu**: Friction Model and Adaptive Control
* **Zhuoran Dong**: Wind Model and Aerodynamics
* **Marina Nelson**: Weighted Cost Model and Performance Optimization

## Acknowledgments
Original LMPC developers: Ugo Rosolia, Charlott Vallon, Francesco Borrelli, and Luigi Glielmo.
