# RRS-001 Sugarcane Bagasse Steam Pasteurization

[← Research Lab](https://github.com/atmblaise/research-lab) | [↑ Profile](https://github.com/atmblaise) | [Development Lab →](https://github.com/atmblaise/development-lab)

---

**Experimental characterization, mathematical modelling, and DWSIM based process simulation of a steam pasteurization process for sugarcane bagasse.**

## Project Summary

RRS-001 investigates the engineering design of a steam pasteurization process for sugarcane bagasse intended for mushroom cultivation. The project integrates experimental material characterization, heat transfer analysis, mathematical modelling, and process simulation to evaluate steam based pasteurization under representative operating conditions.

Published thermophysical properties of sugarcane bagasse exhibit considerable variability, making direct application of literature values unsuitable for reliable process design. To establish representative engineering parameters, an experimental characterization programme was undertaken to determine thermal conductivity, specific heat capacity, moisture content, and bulk density under multiple material conditions.

The experimentally determined properties were incorporated into transient mathematical models and implemented in DWSIM using custom unit operations and IronPython scripts. Two condensation regimes were investigated to evaluate the influence of condensate behaviour on process performance through steam flowrate sensitivity analysis.

This repository documents the engineering methodology, computational models, simulation files, and supporting documentation developed during the project. It should be regarded as a process design and engineering analysis study rather than a validated industrial pasteurization system.

---

# Engineering Problem

Steam pasteurization is widely used to prepare lignocellulosic biomass for mushroom cultivation by reducing competing microorganisms while preserving beneficial microbial activity. Reliable process design depends on representative thermophysical properties and accurate prediction of heat transfer within the biomass bed.

Published material properties for sugarcane bagasse vary considerably due to differences in moisture content, compaction, fibre composition, and experimental methods. These inconsistencies introduce uncertainty into engineering calculations and process simulations.

This project addresses that challenge by experimentally characterizing the material and integrating the measured properties into a process simulation framework suitable for engineering analysis.

---

# Objectives

The objectives of this study were to:

* Experimentally determine the thermophysical properties of sugarcane bagasse.
* Select representative engineering properties for process design.
* Develop transient heat transfer and condensation models.
* Implement the governing equations in DWSIM using custom unit operations.
* Investigate condensation behaviour through two modelling approaches.
* Evaluate process performance across a range of steam flowrates.
* Document the engineering methodology for future development and validation.

---

# Engineering Workflow

```text
Industrial Problem

↓

Literature Review

↓

Experimental Characterization

↓

Heat Transfer Analysis

↓

Mathematical Modelling

↓

Process Simulation

↓

Sensitivity Analysis

↓

Engineering Evaluation
```

---

# Repository Structure

```text
bagasse_pasteurization/
│   .gitignore
│   LICENSE
│   README.md
│   tree.txt
│
├── data
│   ├── processed_experimental_data
│   ├── raw_data_processing
│   └── raw_experimental_data
│
├── dwsim
│   ├── IronPython_scripts
│   └── simulation_flowsheets
│
├── engineering_documentation
│
├── reference_simulation_outputs
│
└── results
```

---

# Experimental Characterization

An experimental programme was conducted to determine engineering properties required for process modelling.

Measured properties included:

| Property               | Engineering Application     |
| ---------------------- | --------------------------- |
| Thermal Conductivity   | Heat transfer modelling     |
| Specific Heat Capacity | Energy balance calculations |
| Moisture Content       | Material characterization   |
| Bulk Density           | Process design calculations |

Material characterization was performed under:

* Wet uncompacted bagasse
* Wet compacted bagasse
* Dry uncompacted bagasse
* Dry compacted bagasse

Following statistical comparison, **wet uncompacted bagasse** was selected as the process design basis because it most closely represents industrial mushroom substrate preparation.

---

# Heat Transfer Analysis

A Biot number analysis was performed to evaluate the relationship between internal conduction resistance and external convection resistance during steam heating.

The analysis supported:

* Thermal modelling assumptions
* Representative bagasse dimensions
* Heat transfer methodology
* Process design decisions

Supporting calculations are available within the engineering documentation.

---

# Mathematical Modelling

Transient mass and energy balances were developed to describe steam heating of the biomass bed.

The model incorporates:

* Sensible heat transfer
* Latent heat released during condensation
* Condensation rate estimation
* Steam quality evolution
* Time dependent bagasse temperature prediction

---

# Condensation Regimes

Two engineering models were developed to evaluate uncertainty associated with condensate behaviour.

## Condensation Without Deposition

Assumptions:

* Steam condenses.
* Latent heat is transferred to the biomass.
* Condensed water does not accumulate.
* Bagasse mass remains constant.

Outputs include:

* Bagasse temperature
* Steam temperature
* Condensation rate
* Steam quality
* Condensed mass

---

## Condensation With Deposition

Assumptions:

* Steam condenses.
* Condensed water accumulates within the biomass bed.
* Bagasse mass increases during operation.
* Heat and mass transfer are fully coupled.

Additional outputs include:

* Dynamic bagasse mass
* Steam outlet flowrate reduction

---

# DWSIM Implementation

The mathematical models were implemented in DWSIM through custom unit operations developed using IronPython.

Simulation components include:

* DWSIM flowsheets
* IronPython scripts
* Spreadsheet interfaces
* Reference simulation outputs

The simulation tracks:

* Bagasse temperature
* Steam temperature
* Condensation rate
* Steam quality
* Steam outlet flowrate
* Condensed mass
* Dynamic bagasse mass

---

# Sensitivity Analysis

Steam flowrate sensitivity analysis was performed over a range of approximately **0.1 kg/h to 200 kg/h**.

Each simulation:

* specified the inlet steam flowrate
* executed until the bagasse reached 75°C
* recorded pasteurization time
* exported simulation results for analysis

---

# Results

The principal performance indicator was the time required for the biomass to reach the target pasteurization temperature of **75°C**.

| Steam Flowrate (kg/h) | No Deposition (h) | Deposition (h) |
| --------------------: | ----------------: | -------------: |
|                   0.1 |             32.91 |          34.00 |
|                   0.5 |             25.75 |          28.56 |
|                     2 |             16.01 |          18.00 |
|                     4 |             10.31 |          12.22 |
|                     6 |              6.88 |           8.19 |
|                     8 |              5.15 |           6.11 |
|                    10 |              4.13 |           4.86 |
|                    12 |             12.64 |           4.17 |
|                    14 |             13.53 |           3.67 |
|                    16 |             14.54 |           3.33 |
|                    18 |             15.71 |           3.06 |
|                    20 |             17.06 |           2.92 |
|                    50 |             25.63 |           2.64 |
|                   100 |             21.99 |           2.50 |
|                   150 |             18.86 |           2.36 |
|                   200 |             16.43 |           2.36 |

---

# Engineering Discussion

The study demonstrates how experimentally determined material properties can improve engineering confidence during process design and simulation.

The condensation deposition model generally predicted shorter pasteurization times at higher steam flowrates because condensed water contributed additional thermal energy and increased moisture within the biomass bed.

The no deposition model exhibited non monotonic behaviour at higher steam flowrates. Although this behaviour was not fully investigated during the project, it represents an important area for future model refinement and validation.

---

# Engineering Software

The project was developed using:

* DWSIM
* IronPython
* Microsoft Excel
* Custom DWSIM Unit Operations

---

# Repository Contents

The repository includes:

* Experimental datasets
* Data processing spreadsheets
* DWSIM simulation files
* IronPython scripts
* Engineering documentation
* Reference simulation outputs
* Process analysis results

---

# Model Assumptions

* Wet uncompacted bagasse represents the design basis.
* Steam pressure remains constant.
* Condensation occurs under saturation conditions.
* Heat transfer coefficients are estimated using Nusselt correlations.
* Material properties remain constant during each simulation.
* Steam flowrate remains constant throughout operation.

---

# Limitations

Current limitations include:

* Experimental uncertainty in measured properties.
* No industrial scale validation.
* Pressure drop not included.
* Steam distribution within the biomass bed not modelled.
* Spatial moisture gradients neglected.
* Unresolved behaviour within the no deposition model at higher flowrates.

---

# Future Work

Future development may include:

* Industrial scale validation.
* Distributed heat and moisture transfer models.
* Pressure drop modelling.
* Additional experimental characterization.
* Standalone Python simulation framework.
* Process optimization studies.

---

# Related Workspaces

* [Research Lab](https://github.com/atmblaise/research-lab)
* [Development Lab](https://github.com/atmblaise/development-lab)
* [Engineering Technologies](https://github.com/atmblaise/engineering-technologies)
* [Publications](https://github.com/atmblaise/publications)

---

# Navigation

[← Research Lab](https://github.com/atmblaise/research-lab) | [↑ Profile](https://github.com/atmblaise) | [Development Lab →](https://github.com/atmblaise/development-lab)
