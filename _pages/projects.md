---
permalink: /projects/
title: "projects"
---

## FSAE Cooling Loop
**Highlander Racing** | UC Riverside | March 2024 – Present

![Cooling Loop Render](/assets/images/FINALLLRENDER.png)

Led analysis, design, and testing of a liquid-cooling loop for a Formula SAE Electric racecar. Managed thermal requirements for motor and inverter while meeting FSAE rules constraints and packaging limitations.

### Analysis
Built a MATLAB thermal simulation workflow modeling motor/inverter heat generation and radiator dissipation to predict coolant temperatures throughout a dynamic race lap.

- Calculated pressure drops (major and minor losses) using Swamee-Jain equation/Colebrooke-White Iterative Solver.
- Validated flow rate requirements → collaborated with EE team to implement a custom 97.4% efficient 21V boost converter to meet 8 LpM target
- Developed empirical test methods to validate flow rates, cavitation thresholds, and loop volume

![Thermal Simulation Results](/assets/images/matlab_thermal.png)
*Placeholder: MATLAB output showing coolant temperature vs. lap time*

### Design
Designed the complete cooling architecture with focus on serviceability and compact packaging.

- Created 3D-printed pump mounts and sheet metal mounting tabs in SolidWorks
- Managed CAD assembly integration with full vehicle (suspension, chassis, battery pack)
- Produced GD&T-compliant manufacturing drawings for machine shop fabrication

![CAD Assembly](/assets/images/cooling_cad_assembly.png)
*Placeholder: Isometric view showing cooling loop integrated with chassis*

### Testing & Controls
Instrumented the system with thermocouples and Hall-Effect flow meter to log data and verify simulation predictions.

- Bench-tested loop for leaks, flow rate verification, pump performance
- Implemented embedded fan control system on Arduino Uno R3 using custom PWM curves for six 36W fans—significantly reduced power draw while maintaining optimal temperatures

![Testing Setup](/assets/images/cooling_bench_test.png)
*Placeholder: Photo of bench test setup with instrumentation*

### Team Leadership
Scaled the Cooling Subteam from 2 to 11 members (4x typical annual intake). Standardized documentation by implementing FFMEA and assembly manuals to ensure knowledge transfer across graduation cycles.

---

## Personal Projects

### Strava Route Planner (R'Cycle Co-Op)
**Status**: Ongoing | [GitHub](#)

Built a Python-based cycling route planner that generates bike loops using ~5,000 miles of personal Strava data. Most routing tools optimize for speed or distance—this optimizes for air quality and UV exposure to reduce health impacts from exercising in industrial corridors.

![Route Generation Example](/assets/images/strava_routes.png)
*Placeholder: Map showing generated routes overlaid with air quality data*

**Current Features**:
- Route generation from personal ride history using Strava API
- Loop creation algorithm for discovering new areas
- GPX export for navigation

**In Progress**:
- Integration with EPA AirNow API for real-time PM2.5 data
- UV index overlay to minimize sun exposure during peak hours
- Route scoring system balancing distance, air quality, and shade coverage

**Technical Stack**: Python (NumPy, Pandas, Matplotlib), Strava API, Folium for mapping

**Motivation**: Riding through Riverside's industrial corridors means exposure to PM2.5 levels that regularly exceed EPA thresholds. A 10-mile route through freight zones vs. residential areas can mean a 40% difference in particulate exposure.

---

### Home Energy Dashboard
**Status**: Complete (2025) | [GitHub](#)

Created a modular home energy simulation and dashboard modeling HVAC, appliances, EV charging, and solar PV for a 3-bedroom house. The goal: identify system-level optimization opportunities that aren't obvious from individual component behavior.

![Energy Dashboard Interface](/assets/images/energy_dashboard_ui.png)
*Placeholder: Screenshot of dashboard showing energy flows*

**Features**:
- Season-aware cost, load, and solar generation profiles
- Interactive sliders for real-time control (HVAC setpoints, EV charge timing)
- Analytics for peak load, subsystem energy shares, and solar offset
- Actionable efficiency recommendations

![Sankey Diagram](/assets/images/energy_sankey.png)
*Placeholder: Sankey diagram showing energy flows between solar, grid, HVAC, EV, and household loads*

**Key Findings**:
- HVAC pre-cooling before ToU peak rates saves ~$15/month in summer
- Shifting EV charging to solar production hours reduces grid draw by 40%
- Solar offset maximization requires coordinating appliance schedules with generation curves

**Technical Stack**: Python (Pandas, Matplotlib), modular simulation architecture, Jupyter notebooks for analysis

**Next Steps**: Add predictive modeling using weather forecasts to automate HVAC scheduling and EV charge timing.

---

## Utthunga Internship Projects (Summer 2025)

### Thermal Simulation & Design Optimization
Performed thermal simulation and design optimization for electronic enclosures:

- **Fanless Automotive ECU**: Used Altair SimLab to analyze MOSFET temperatures and recommend cooling improvements
- **HART Simulator Enclosure**: Refined sheet metal design in SolidWorks for manufacturability and thermal performance

![Thermal Simulation Results](/assets/images/utthunga_thermal.png)
*Placeholder: SimLab temperature contour plot*

### Python Diagnostic Tools

**Pump Performance Classifier**:
- Created a parametric tool for generating pump performance curves
- Built a 96%-accurate classifier using synthetic sensor data to predict OK/Warning/Failure states
- Enables predictive maintenance before catastrophic pump failure

**Heat Exchanger Analysis Tool**:
- Automated heat exchanger design calculations using LMTD and ε-NTU methods
- Modular Python architecture for rapid parameter sweeps
- Reduced manual calculation effort for thermal design iterations

**Technical Stack**: Python (NumPy, SciPy, scikit-learn), synthetic data generation for ML training

---

## Robotics

### FIRST Robotics Competition Team 256 (President, 2019-2023)

Led subteams in designing, fabricating, and assembling competition robots for FRC. Managed team operations through COVID-19 by implementing sub-team structure, which improved member retention to 90% and restored technical skills pipeline.

- Taught Fusion 360 and machine shop safety to 25+ members
- Oversaw mechanical design, fabrication, and assembly processes
- Coordinated cross-functional teams (mechanical, electrical, programming, business)

![FRC Robot](/assets/images/frc_robot.png)
*Placeholder: Photo of competition robot or team at event*

**Skills Developed**: Project management, technical mentorship, CAD/CAM workflows, systems integration

---
