# Facilitating Figures Creation For Performance Visualization

This repository contains scripts which aim to help make figures for parameter-tuning experiments.

Types of figures these scripts make:
* 3D bar chart showing performance (e.g. runtime) vs. parameter 1 and parameter 2
* 2D bar chart showing performance (e.g. runtime) vs. parameter 1, color-coded by parameter 2

## How to use this repository

### Data format

The notebook `make_plots_3Dbar_2DbarColor.ipynb` uses data stored in `.csv` format.
The `.csv` file should contain three columns:
The first row of the `.csv` file should be a header with the column names. The names in this row will be used for labeling plot axes.

#### Example data