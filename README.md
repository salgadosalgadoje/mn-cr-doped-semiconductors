# Mn- and Cr-Doped Diluted Magnetic Semiconductors

This repository contains three Jupyter notebooks and corresponding Python
scripts for exploring temperature-dependent magnetic and thermodynamic
quantities in Diluted Magnetic Semiconductors (DMSs).

## Theoretical basis

The project combines two complementary models:

- A theoretical framework for Fe-doped GaSb (`Ga_{1-x}Fe_xSb`) with `Fe³⁺`
  ions, used to study the magnetic and thermodynamic behavior of the
  semiconductor host.
- A consolidated model for the magnetic properties of Mn-doped wurtzite AlN
  (`Al_{1-x}Mn_xN`), covering the relevant temperature-dependent behavior and
  transition trends in the Mn-containing system.
- A comparative study of Mn-doped AlN, GaN, and GaSb, using wurtzite
  structures for AlN and GaN and a zinc-blende structure for GaSb. The model
  assumes `S = 5/2` and compares Curie temperature across concentrations, plus
  reduced magnetization and magnon heat capacity for `x = 5%`. The heat-capacity
  curves also compare concentrations from 5% to 8%.

Together, these studies provide calculations for Curie-temperature trends,
reduced magnetization curves, and heat-capacity profiles.

## What the simulations calculate

Using low-temperature magnon and exchange-based models, the notebooks calculate
and plot:

- Curie temperature as a function of dopant concentration.
- Heat-capacity trends over temperature.
- Reduced magnetization curves, `M_s(T) / M_s(0)`, over the relevant
  temperature range.

The model uses Heisenberg-like exchange descriptions and long-wavelength magnon
approximations to capture the qualitative temperature dependence of the
magnetic response.

## Repository contents

```text
figures/
  01_Curie_Temperature_vs_Concentration.png
  02_Heat_Capacity_vs_Temperature.png
  03_Reduced_Magnetization_vs_Temperature.png
  04_Tc_vs_Mn_Concentration.png
  05_Reduced_Magnetization.png
  06_Heat_Capacity.png
  07_Tc_vs_Mn_Concentration.png
  08_Reduced_Magnetization.png
  09_Heat_Capacity_AlN_Mn.png
  10_Heat_Capacity_GaN_Mn.png
  11_Heat_Capacity_GaSb_Mn.png
  12_Combined_Dashboard.png
notebooks/
  01-Theoretical_Framework_(Ga_{1-x}Fe_xSb).ipynb
  02-Consolidated_Theoretical_Model_of_the_Magnetic_Properties_of_Al_{1-x}Mn_xN_(Wurtzite).ipynb
  03-Theoretical_Comparative_Study_AlN.ipynb
src/
  01-Theoretical_Framework_(Ga_{1-x}Fe_xSb).py
  02-Consolidated_Theoretical_Model_of_the_Magnetic_Properties_of_Al_{1-x}Mn_xN_(Wurtzite).py
  03-Theoretical_Comparative_Study_AlN.py
requirements.txt
```

## Setup

Use Python 3.9 or later. From the repository root, install the dependencies:

```powershell
python -m pip install -r requirements.txt
```

## Run the notebooks

Start Jupyter from the repository root:

```powershell
python -m jupyter notebook
```

Open a notebook in the `notebooks/` directory and run its cells in order:

- `notebooks/01-Theoretical_Framework_(Ga_{1-x}Fe_xSb).ipynb`
- `notebooks/02-Consolidated_Theoretical_Model_of_the_Magnetic_Properties_of_Al_{1-x}Mn_xN_(Wurtzite).ipynb`
- `notebooks/03-Theoretical_Comparative_Study_AlN.ipynb`

## Run the Python scripts

Run the scripts from the `src` folder. They save their figures to the
repository's `figures` directory:

```powershell
Set-Location src
python "01-Theoretical_Framework_(Ga_{1-x}Fe_xSb).py"
python "02-Consolidated_Theoretical_Model_of_the_Magnetic_Properties_of_Al_{1-x}Mn_xN_(Wurtzite).py"
python "03-Theoretical_Comparative_Study_AlN.py"
```

The scripts also open plots interactively when the selected Matplotlib backend
supports graphical windows.

## Figures

### Curie temperature versus Fe concentration

![Curie temperature versus Fe concentration](figures/01_Curie_Temperature_vs_Concentration.png)

### Heat capacity versus temperature

![Heat capacity versus temperature](figures/02_Heat_Capacity_vs_Temperature.png)

### Reduced magnetization versus temperature

![Reduced magnetization versus temperature](figures/03_Reduced_Magnetization_vs_Temperature.png)

### Curie temperature versus Mn concentration

![Curie temperature versus Mn concentration](figures/04_Tc_vs_Mn_Concentration.png)

### Reduced magnetization

![Reduced magnetization](figures/05_Reduced_Magnetization.png)

### Heat capacity

![Heat capacity](figures/06_Heat_Capacity.png)

### Comparative Curie temperature versus Mn concentration

The comparison includes Mn-doped AlN, GaN, and GaSb.

![Comparative Curie temperature versus Mn concentration](figures/07_Tc_vs_Mn_Concentration.png)

### Comparative reduced magnetization at 5% Mn

![Comparative reduced magnetization at 5% Mn](figures/08_Reduced_Magnetization.png)

### Heat capacity: AlN:Mn

![Heat capacity of AlN:Mn](figures/09_Heat_Capacity_AlN_Mn.png)

### Heat capacity: GaN:Mn

![Heat capacity of GaN:Mn](figures/10_Heat_Capacity_GaN_Mn.png)

### Heat capacity: GaSb:Mn

![Heat capacity of GaSb:Mn](figures/11_Heat_Capacity_GaSb_Mn.png)

### Comparative dashboard

The dashboard combines Curie-temperature trends, reduced magnetization, and
heat-capacity curves for all three materials.

![Combined comparative dashboard](figures/12_Combined_Dashboard.png)
