# RRS-001 | Sugarcane Bagasse Steam Pasteurization

[← Research Lab](https://github.com/atmblaise/research-lab) | [↑ Profile](https://github.com/atmblaise) | [Development Lab →](https://github.com/atmblaise/development-lab)

---

**Integrated experimental and computational investigation of steam pasteurization of sugarcane bagasse through material characterization, transient thermal modelling, condensation analysis, and process simulation.**

**Research Status:** Engineering prototype developed

**Study Type:** Integrated Engineering Study

**Research Domain:** Process Engineering · Heat Transfer · Biomass Processing · Process Simulation

---

## Project Summary

RRS-001 investigates the engineering behaviour and process requirements of steam pasteurization of shredded sugarcane bagasse for applications including mushroom substrate preparation.

The study integrates experimental characterization, heat-transfer analysis, transient mathematical modelling, process simulation, and engineering evaluation into a single computational workflow.

A central challenge addressed by the study is the variability of reported thermophysical properties for sugarcane bagasse. Moisture content, bulk density, compaction, fibre composition, particle structure, and measurement methodology can substantially influence the thermal properties used in engineering calculations.

To establish representative process-design parameters, an experimental characterization programme was conducted under different material conditions. The resulting thermal and physical properties were processed and incorporated into transient heating models describing the evolution of bagasse temperature during steam treatment.

Two condensation regimes were subsequently investigated to examine the influence of condensate behaviour on predicted pasteurization performance. The resulting mathematical models were implemented computationally and integrated with DWSIM process simulations using custom unit operations and IronPython scripting.

The study therefore connects experimentally measured material behaviour with process-level simulation and engineering analysis.

The repository contains the experimental data, processed datasets, mathematical models, simulation models, computational workflows, engineering calculations, results, and publication materials supporting the study.

The work is presented as a research and engineering-development study. The models and prototype require further validation under controlled and industrial-scale operating conditions before the results can be considered representative of commercial pasteurization systems.

---

## Project Origin & Academic Outcome

RRS-001 originated as a final-year Chemical Engineering research project undertaken collaboratively by **Blaise Atambo** and **Moses Chai**, under the supervision of **Dr. Godfrey Kabungo**.

The project was successfully completed, defended, and awarded a **First Class grade** as part of the undergraduate Chemical Engineering programme.

Following its academic completion, the work is being reconstructed and extended as an engineering research repository. The objective of this transition is to preserve the underlying experimental data, computational models, engineering calculations, simulation workflows, and technical findings in a reproducible form suitable for further research and publication.

The repository therefore represents the transition of the work from an **undergraduate research project into a structured engineering research artifact**.

---

# Current Status

* Experimental characterization of sugarcane bagasse completed.
* Thermal and physical properties determined for multiple material conditions.
* Representative process-design basis established.
* Heat-transfer analysis completed.
* Transient heating model developed.
* Alternative condensation regimes formulated.
* Mathematical models implemented computationally.
* DWSIM process simulation developed using custom unit operations and IronPython.
* Steam-flowrate sensitivity analysis performed.
* Engineering prototype developed.
* Simulation results generated for a range of steam-flow conditions.
* Research repository being reconstructed for reproducibility and publication.
* Integrated engineering manuscript under development.

The current repository should be regarded as an evolving research artifact. Results, datasets, models, and documentation will be progressively reorganized and verified as part of the publication process.

---

# Research Question

The study investigates the following engineering question:

> **How can experimentally characterized thermophysical properties and transient process modelling be integrated to evaluate the steam requirements and thermal performance of a sugarcane bagasse pasteurization process?**

The investigation additionally examines:

* how material condition affects the thermal basis used for process modelling;
* how condensation behaviour influences predicted heating performance;
* how steam flowrate affects the time required to reach the target pasteurization temperature;
* and how computational process simulation can support engineering design of a biomass steam-treatment system.

---

# Engineering Problem

Steam pasteurization of lignocellulosic biomass involves coupled heat and mass-transfer phenomena. Steam entering a biomass bed can condense and release latent heat while simultaneously altering the moisture content and thermal properties of the material.

Reliable engineering design therefore requires an appropriate representation of:

* material thermophysical properties;
* biomass temperature evolution;
* steam condensation;
* latent and sensible heat transfer;
* moisture accumulation;
* steam consumption;
* and process operating conditions.

Published thermophysical properties for sugarcane bagasse exhibit substantial variability. Direct use of a single literature value can therefore introduce uncertainty into heat-transfer and process-design calculations.

RRS-001 addresses this uncertainty through experimental characterization followed by computational modelling and process simulation.

---

# Research Objectives

The study was developed around the following objectives:

1. Experimentally characterize the physical and thermophysical properties of sugarcane bagasse relevant to steam pasteurization.
2. Establish a representative material basis for engineering calculations.
3. Develop transient thermal models describing bagasse heating under steam treatment.
4. Formulate alternative representations of steam condensation and condensate behaviour.
5. Implement the mathematical models computationally.
6. Integrate the models with DWSIM through custom unit operations and IronPython scripting.
7. Evaluate the influence of steam flowrate on predicted pasteurization time.
8. Analyse the resulting process behaviour and identify model limitations.
9. Establish an engineering basis for further prototype development and experimental validation.

---

# Research Workflow

```text
                    INDUSTRIAL APPLICATION
                           │
                           ▼
                  Engineering Problem
                           │
                           ▼
                     Literature Review
                           │
                           ▼
              Experimental Characterization
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
        Moisture       Density      Thermal Properties
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                  Engineering Design Basis
                           │
                           ▼
                  Heat Transfer Analysis
                           │
                           ▼
                Transient Thermal Model
                           │
                  ┌────────┴────────┐
                  ▼                 ▼
          No Deposition       Deposition
             Model              Model
                  │                 │
                  └────────┬────────┘
                           ▼
                    DWSIM Integration
                           │
                           ▼
                 Steam Flow Sensitivity
                           │
                           ▼
                 Engineering Evaluation
                           │
                           ▼
                 Prototype Development
                           │
                           ▼
                Validation & Publication
```

---

# Repository Structure

```text
RRS-001-Sugarcane-Bagasse-Steam-Pasteurization/
│
├── README.md
├── LICENSE
├── CITATION.cff
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── metadata/
│
├── notebooks/
│
├── models/
│   ├── thermal/
│   ├── condensation/
│   └── process/
│
├── dwsim/
│   ├── flowsheets/
│   ├── scripts/
│   └── documentation/
│
├── engineering/
│   ├── calculations/
│   ├── assumptions/
│   └── design_basis/
│
├── results/
│   ├── experimental/
│   ├── model/
│   ├── simulation/
│   └── figures/
│
├── documentation/
│
├── references/
│
└── paper/
    ├── manuscript/
    ├── figures/
    ├── tables/
    └── supplementary/
```

The repository structure separates experimental evidence, computational models, simulation files, engineering calculations, generated results, and publication materials.

---

# Experimental Characterization

Experimental characterization was conducted to establish the material properties required for thermal and process modelling.

The investigated properties include:

| Property               | Engineering relevance            |
| ---------------------- | -------------------------------- |
| Thermal conductivity   | Internal heat-transfer modelling |
| Specific heat capacity | Sensible-energy calculations     |
| Moisture content       | Material and energy balance      |
| Bulk density           | Bed and process calculations     |

Characterization was performed for different material conditions, including:

* wet uncompacted bagasse;
* wet compacted bagasse;
* dry uncompacted bagasse;
* dry compacted bagasse.

The resulting datasets are retained separately from processed datasets to preserve the distinction between experimental measurements and derived engineering quantities.

---

# Process Design Basis

The experimental results were evaluated to establish a representative material condition for process modelling.

The selected design basis represents the material condition considered most representative of the intended steam-pasteurization application.

The design-basis dataset is documented separately from the complete experimental dataset so that the effect of material-condition selection can be independently evaluated.

---

# Heat Transfer Analysis

Heat-transfer analysis was performed to establish the appropriate modelling framework for steam heating of the biomass bed.

A Biot number analysis was conducted to evaluate the relative importance of internal conduction and external heat-transfer resistance.

The analysis informed:

* characteristic length selection;
* lumped versus distributed modelling assumptions;
* heat-transfer methodology;
* representative biomass dimensions;
* and the subsequent transient thermal model.

All assumptions and correlations used in the heat-transfer calculations are intended to be explicitly documented in the engineering calculation files and manuscript methodology.

---

# Mathematical Model

A transient energy-balance framework was developed to describe the temperature evolution of the bagasse during steam treatment.

The model accounts for the thermal contribution of steam condensation and the sensible heating of the biomass.

The model framework includes:

* biomass sensible heating;
* steam condensation;
* latent heat transfer;
* steam enthalpy;
* temperature evolution;
* condensation rate;
* and, where applicable, condensate accumulation.

The mathematical formulation is implemented computationally so that the governing equations can be reproduced independently of the DWSIM flowsheet.

---

# Condensation Models

Two representations of condensate behaviour were investigated.

## Model A — Condensation Without Deposition

The first formulation assumes that steam condenses and transfers its latent heat to the biomass without accumulation of condensate within the modelled biomass mass.

Primary state variables include:

* bagasse temperature;
* steam temperature;
* condensation rate;
* steam quality;
* condensed mass.

Under this formulation, the bagasse mass remains constant.

---

## Model B — Condensation With Deposition

The second formulation allows condensed water to accumulate within the biomass system.

The model therefore couples heat and mass transfer through:

* condensation;
* moisture accumulation;
* changing biomass-system mass;
* latent heat transfer;
* and steam outlet flowrate.

This formulation was developed to investigate the influence of condensate deposition on predicted pasteurization behaviour.

---

# Computational Implementation

The mathematical models were implemented computationally and subsequently integrated into DWSIM.

The computational workflow provides a separation between:

1. experimental data;
2. engineering-property selection;
3. mathematical formulation;
4. numerical solution;
5. process simulation;
6. result extraction;
7. engineering analysis.

This separation is intended to improve reproducibility and allow individual parts of the model to be independently inspected and validated.

---

# DWSIM Process Simulation

DWSIM was used as the process-simulation environment for evaluating the steam-pasteurization system.

Custom unit-operation logic was implemented using IronPython.

The simulation framework includes:

* steam inlet conditions;
* biomass heating;
* condensation;
* heat transfer;
* steam outlet behaviour;
* temperature tracking;
* condensate tracking;
* and process-level result extraction.

Simulation files and scripts are maintained separately from generated outputs.

---

# Steam Flowrate Sensitivity Analysis

Steam flowrate was investigated over approximately:

**0.1–200 kg/h**

For each investigated flowrate, the simulation was executed until the modelled biomass reached the target temperature of **75°C**.

The primary performance indicator was:

> **Time required for the modelled biomass to reach 75°C.**

Additional simulation outputs include temperature, condensation, steam quality, condensate accumulation, and outlet-flow behaviour.

The complete simulation dataset is retained to allow the sensitivity analysis to be reproduced rather than presenting only selected operating points.

---

# Reference Results

The current simulation results include the following representative values:

| Steam Flowrate | No Deposition | Deposition |
| -------------: | ------------: | ---------: |
|       0.1 kg/h |       32.91 h |    34.00 h |
|       0.5 kg/h |       25.75 h |    28.56 h |
|         2 kg/h |       16.01 h |    18.00 h |
|         4 kg/h |       10.31 h |    12.22 h |
|         6 kg/h |        6.88 h |     8.19 h |
|         8 kg/h |        5.15 h |     6.11 h |
|        10 kg/h |        4.13 h |     4.86 h |
|        12 kg/h |       12.64 h |     4.17 h |
|        14 kg/h |       13.53 h |     3.67 h |
|        16 kg/h |       14.54 h |     3.33 h |
|        18 kg/h |       15.71 h |     3.06 h |
|        20 kg/h |       17.06 h |     2.92 h |
|        50 kg/h |       25.63 h |     2.64 h |
|       100 kg/h |       21.99 h |     2.50 h |
|       150 kg/h |       18.86 h |     2.36 h |
|       200 kg/h |       16.43 h |     2.36 h |

These values are presented as **current reference simulation results**, not as experimentally validated performance predictions.

The apparent non-monotonic behaviour observed in the no-deposition model at higher steam flowrates is retained as part of the research record. Its origin requires further numerical and physical investigation before the model can be used to infer an optimum operating region.

---

# Engineering Interpretation

The results demonstrate that the representation of condensate behaviour has a substantial influence on predicted pasteurization performance.

The deposition model generally predicts shorter heating times as steam flowrate increases because condensed water contributes additional thermal energy while simultaneously increasing the moisture associated with the biomass system.

The no-deposition model exhibits unexpected non-monotonic behaviour at higher steam flowrates. This behaviour is not interpreted as evidence of a physical optimum without further investigation.

Possible sources requiring examination include:

* numerical formulation;
* time-stepping behaviour;
* energy-balance implementation;
* steam-quality calculations;
* condensation correlations;
* heat-transfer assumptions;
* boundary-condition treatment;
* and DWSIM implementation effects.

This behaviour therefore forms part of the model-verification work required before publication.

---

# Prototype Development

The computational investigation was accompanied by development of a working engineering prototype for steam treatment of shredded sugarcane bagasse.

The prototype provides a physical basis for future validation of the computational model.

The research pathway is therefore:

```text
Experimental Material Characterization
                ↓
        Mathematical Model
                ↓
       Process Simulation
                ↓
       Engineering Design
                ↓
      Physical Prototype
                ↓
     Experimental Validation
```

The prototype should not be interpreted as an industrially validated production system.

---

# Engineering Assumptions

The current model includes assumptions concerning:

* representative material condition;
* steam operating pressure;
* steam saturation;
* heat-transfer coefficients;
* thermophysical properties;
* biomass geometry;
* steam-flow behaviour;
* condensation behaviour;
* and temporal numerical integration.

Each assumption will be documented together with its source, justification, applicability, and potential influence on model uncertainty.

---

# Model Verification and Validation

The research distinguishes between **verification** and **validation**.

### Verification

Verification addresses whether the implemented computational model correctly represents the intended mathematical formulation.

Planned verification activities include:

* energy-balance checks;
* mass-balance checks;
* limiting-case tests;
* timestep sensitivity;
* conservation checks;
* independent Python calculations;
* and comparison between computational implementations.

### Validation

Validation addresses whether the model adequately represents physical bagasse pasteurization behaviour.

Validation requires additional experimental measurements under controlled steam-treatment conditions.

The current repository should therefore not be interpreted as providing a fully validated industrial process model.

---

# Data Integrity and Reproducibility

Research data are organized according to their origin and processing state.

```text
Raw Experimental Data
        ↓
Data Processing
        ↓
Processed Dataset
        ↓
Engineering Parameters
        ↓
Mathematical Model
        ↓
Simulation
        ↓
Generated Results
        ↓
Publication Figures / Tables
```

Raw measurements should remain unchanged.

Derived datasets should contain documented processing steps.

Generated results should be reproducible from the underlying data and model implementation wherever practical.

---

# Engineering Software

The study uses:

* **DWSIM** — process simulation;
* **IronPython** — custom DWSIM unit-operation implementation;
* **Python** — numerical modelling and data analysis;
* **Microsoft Excel** — experimental data processing and engineering calculations.

The computational workflow is being progressively consolidated toward reproducible, script-based analysis.

---

# Limitations

The current study has several limitations:

* Experimental measurements contain finite measurement uncertainty.
* Thermophysical properties may vary with moisture, temperature, compaction, and material structure.
* The present model does not fully resolve spatial temperature gradients within the biomass bed.
* Steam distribution through the biomass bed is not explicitly resolved.
* Pressure drop is not currently modelled.
* Moisture gradients are simplified.
* Some thermophysical properties are treated as constant within individual simulations.
* The current model has not been validated against a comprehensive experimental heating dataset.
* The observed high-flow non-monotonic behaviour of the no-deposition formulation requires further investigation.
* Industrial-scale performance has not been demonstrated.

These limitations define the scope of the current study rather than invalidating the engineering analysis.

---

# Planned Research Development

The next development stages are:

1. Audit and standardize all experimental datasets.
2. Establish complete data provenance and metadata.
3. Quantify experimental uncertainty.
4. Independently verify the mathematical models.
5. Investigate the high-flow non-monotonic model behaviour.
6. Reproduce all DWSIM results from clean inputs.
7. Generate publication-quality figures and tables.
8. Compare model predictions against available experimental observations.
9. Identify the minimum additional experiments required for model validation.
10. Prepare the integrated engineering manuscript.
11. Package the final dataset and computational workflow for reproducibility.

---

# Publication

The repository is being developed as the computational and data foundation for a publishable engineering study.

The intended manuscript will integrate:

* experimental characterization;
* thermophysical-property analysis;
* heat-transfer modelling;
* condensation modelling;
* DWSIM process simulation;
* steam-flow sensitivity;
* model verification;
* engineering interpretation;
* and prototype implications.

The publication will distinguish experimentally established results from model-derived predictions and clearly document uncertainty, assumptions, and limitations.

---

# Related Workspaces

* [Research Lab](https://github.com/atmblaise/research-lab)
* [Development Lab](https://github.com/atmblaise/development-lab)
* [Engineering Technologies](https://github.com/atmblaise/engineering-technologies)
* [Publications](https://github.com/atmblaise/publications)

---

# Navigation

[← Research Lab](https://github.com/atmblaise/research-lab) | [↑ Profile](https://github.com/atmblaise) | [Development Lab →](https://github.com/atmblaise/development-lab)
