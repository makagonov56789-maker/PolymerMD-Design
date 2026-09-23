**_Automated molecular-dynamics workflow for polymer property prediction and computational materials design_**

PolymerMD-Design is a computational workflow for building atomistic polymer models, performing molecular-dynamics simulations, automatically extracting thermophysical and mechanical properties, and developing a foundation for inverse polymer design.

The project combines **_RDKit, RadonPy, GAFF2 and LAMMPS_** with automated post-processing and data-driven materials design.

The project is built around the Python scientific-computing ecosystem.

**_Core:_**

- **_Python_** — workflow automation and computational analysis
- **_NumPy_** — numerical computation and array-based data processing
- **_SciPy_** — scientific computing, optimization, regression, and statistical analysis
- **_Pandas_** — tabular data processing and property datasets
 
**_Molecular modelling:_**

- _**RDKit**_ — molecular representations, SMILES processing, and cheminformatics
- **_RadonPy_** — atomistic polymer model generation and molecular-dynamics preparation

**_Data analysis and visualization:_**

- **_Matplotlib_** — scientific visualization
- **_Jupyter Notebook_** — interactive analysis and reproducible computational workflows
 
**_Molecular dynamics:_**
 
- **_LAMMPS_** — classical molecular-dynamics simulations
- **_GAFF2_** — force-field parameterization for molecular simulations

**_Materials:_**
- **_Ultem_**
- **_Extem_**
- **_PEEK_**
- **_PEKK_**

_**The calculated properties include:**_

- glass-transition temperature (Tg);
- Young's modulus;
- Poisson's ratio;
- shear modulus;
- thermal conductivity;
- temperature-dependent volumetric behaviour.

The **_central_** idea is to connect **_molecular structure_** with **_macroscopic polymer properties_** through a reproducible computational workflow:

**_Molecular structure
       →
Polymer model generation
       →
Force-field assignment
       →
Molecular dynamics
       →
Automated property extraction
       →
Property dataset_**

The **_current_** version of the project focuses on _atomistic_ modelling, _molecular-dynamics_ simulations, and _automated extraction_ of polymer properties.

The long-term objective is to extend this workflow with _machine-learning_ models capable of learning _structure–property_ relationships and, ultimately, to develop an _inverse-design_ pipeline:

**_Property dataset
       →
Machine-learning model
       →
Target properties
       →
Candidate polymer structures
       →
MD validation
       →
Updated property dataset_**

This would enable computational screening of polymer structures according to target combinations of properties rather than relying exclusively on trial-and-error experimental development.

_**Computational workflow**_

**_1. Molecular representation_**

Polymer repeat units are represented using molecular graph representations and SMILES.

RDKit is used for molecular manipulation and structure preparation.

RadonPy is used for polymer model construction and preparation of atomistic systems.

**_2. Molecular dynamics_**

The generated structures are converted into LAMMPS-compatible systems and simulated using classical molecular dynamics.

The workflow includes:

- initial structure generation;
- energy minimization;
- relaxation;
- equilibration;
- production simulations;
- temperature-dependent simulations;
- mechanical deformation;
- thermal-property calculations.

**_3. Automated property extraction_**

Simulation output is processed automatically rather than relying on manual inspection.

For example, glass-transition temperature is obtained from the temperature dependence of the simulated volume using several fitting strategies, including piecewise regression and robust loss functions.

Mechanical properties are extracted from simulated stress-strain curves using automated identification of the appropriate deformation region.

Thermal conductivity is evaluated using direct thermal-gradient approaches.
