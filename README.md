# Golf Ball Trajectory Simulation 

This repository simulates the flight of a golf ball under various physical conditions using Python. The goal is to explore how different forces—gravity, drag, wind, and spin-induced lift—affect the ball's trajectory. The project includes visualizations, numerical solvers (RK4 and `solve_ivp`), and performance comparisons to better understand real-world golf ball dynamics.

## Project Contributions

**A. Rohan S. Kumar Rskumar2@illinois.edu**
I worked on the majority of the code that set up the golf ball trajectory simulation in section (2) as well as the
results and discussion in section (4). In addition to these technical aspects, I worked on the Introduction, Results and
Discussion, as well as the References. I worked on 32% of the project, including edits and time spent writing and
formatting the paper.

**B. Luke H. McNamara Lukem4@illinois.edu**
I worked on the introduction and the mathematical derivation. I interacted with ChatGPT to help find a topic that
worked for everyone but also fell within the requirements of the report. Additionally, I helped format the Latex document
and the nomenclature. I worked on 32% of the project, which includes formatting and writing the report.

**C. Ella M. Young Ellamy2@illinois.edu**
I worked on the collection of data and writing section (4), and I worked on creating figures and justification for
section (3) of the requirements for this project. In addition to this, I worked on the abstract, the conclusion, and
formatting of the code in GitHub (organization and markdown explanations). I worked on 36% of the project, including
edits and time spent writing the paper.

## Project Motivation

Golf ball flight is a rich application of physics, involving fluid dynamics, force modeling, and numerical integration. This simulation aims to:

- Build a physically sound model of golf ball flight.
- Compare different launch angles and optimize for distance.
- Study the effects of spin (Magnus lift) and wind on trajectory.
- Experiment with different numerical methods like RK4 and `solve_ivp`.

## Key Features

- **No-spin Baseline Model**: Includes drag, wind, and gravity.
- **Spin Model**: Adds spin-induced Magnus lift with exponential spin decay.
- **RK4 Implementation**: Custom Runge-Kutta method to compare with `solve_ivp`.
- **Angle Optimization**: Finds the optimal launch angle for maximum carry distance.
- **Realistic Course Visualization**: Includes green, grass, and bunkers on a 2D plot.

## Assumptions

- Steady, incompressible airflow.
- Constant drag coefficient (Cd = 0.25).
- Constant mass and radius of the golf ball.
- Wind is steady and acts in the horizontal plane only.
- Magnus lift modeled from y-axis backspin.
- Spin decays exponentially over time.
- Earth curvature and rotation are ignored.

## Technologies

- Python 3
- NumPy
- Matplotlib
- SciPy

## Simulations Included

1. **Baseline Trajectory (No Spin)**  
   Gravity + Drag + Wind

2. **Optimal Launch Angle Estimation**  
   Angle sweep to find the best angle for a hole-in-one.

3. **Trajectory With Spin and Lift**  
   Adds backspin and Magnus lift to make the flight more realistic.

4. **Custom RK4 Solver**  
   Implements a manual RK4 integrator and compares it to `solve_ivp`.

5. **RK4 Accuracy Analysis**  
   Visualizes error trends for different time steps to guide step-size selection.

## Results

- Adding spin increases carry distance and height due to Magnus lift.
- Wind direction significantly skews the lateral position.
- RK4 matches `solve_ivp` closely when step size is ≤ 0.05.
- Optimal angle for a 100-yard carry (without spin) is ~28°.

