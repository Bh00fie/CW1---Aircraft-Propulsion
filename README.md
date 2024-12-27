# Turboelectric Propulsion System Analysis

This repository contains Python scripts and Jupyter notebooks used for the analysis of a turboelectric propulsion system. The work is part of the **SESA6075 Aircraft Propulsion Coursework 1** at the University of Southampton. It focuses on analyzing the performance and efficiency of a STARC-ABL configuration, which includes generator fans (genFan) and a tail cone fan.

---

## Objectives

The key objectives of this coursework are:
1. Compute the thermodynamic and performance parameters of the turboelectric propulsion system.
2. Analyze the propulsive efficiency of the tail cone fan.
3. Investigate the effect of design variables like outer radius on system performance.
4. Use Python-based programming for efficient and accurate analysis.

---

## Repository Contents

- **`CW1_jupiter.ipynb`**: Jupyter Notebook with step-by-step calculations and visualizations.
- **`CW1.py`**: Python script implementing the computational framework for the analysis.
- **`SESA6075 Aircraft Propulsion CW1 - Abhinandan Thour.pdf`**: Final report documenting the results and insights.
- **`SESA6075 Assignment 1 2023(1).pdf`**: Assignment brief and requirements.
- **Images and Visualizations**: Figures illustrating the results.

---

## Visualizations

### 1. STARC-ABL Configuration
![STARC-ABL Configuration](Images/starc_abl_diagram.png)

### 2. Effect of Outer Radius on Propulsive Efficiency
![Propulsive Efficiency vs. Outer Radius](Images/prop_efficiency_vs_radius.png)

These figures illustrate the STARC-ABL propulsion system and the effect of design parameters on performance.

---

## How the Code Works

### Overview
The Python scripts compute key thermodynamic properties, mass flow rates, and velocities at various stages of the propulsion system, including:
- Flight velocity
- Fan inlet/outlet conditions
- Tail cone fan efficiency
- Overall thrust and power requirements

### Code Structure
1. **Inputs**: Includes material properties, boundary layer parameters, and efficiency values from the assignment brief.
2. **Calculations**:
   - Compute flight velocity using Mach number and atmospheric conditions.
   - Derive thermodynamic properties at each station (fan, LPC, HPC, HPT, LPT).
   - Calculate thrust and propulsive efficiency.
3. **Output**:
   - Key performance parameters such as net thrust, power, and efficiency.
   - Visualizations showing trends and system behavior.

### Example Calculation
#### Flight Velocity:
```python
vinf = Mcruise * np.sqrt(gammaAir * Rair * Tatm)
print(f'Flight velocity: {vinf:.2f} m/s')
```
```python
# Fan Outlet Conditions
T013 = T02 + (T02 / fan_efficiency) * ((fan_pr**((gamma_air-1)/gamma_air))-1)
P013 = P02 * fan_pr
```

