# Facilitating Figures Creation For Performance Visualization

This repository contains a script which aims to help make figures for parameter-tuning experiments involving two parameters.

Types of figures this script makes:
* 3D bar chart showing performance (e.g. runtime) vs. parameter 1 and parameter 2
* 2D bar chart showing performance (e.g. runtime) vs. parameter 1, color-coded by parameter 2
* Heat map showing performance (e.g. runtime) for grid defined by parameter 1 and parameter 2

## How to use this repository

The main script is `make_plots_3Dbar_2DbarColor.ipynb`. This script should be modified with the path for the data file. After this modification, running all the code cells will produce both figures listed above.

It can also be optionally modified to 1) switch which parameter appears on the x-axis for each of the three figures, and 2) display parameter values in decreasing order rather than increasing order for each of the two bar charts. Comments in the second code-cell guide how these modifications can be made.

### Data format

The notebook `make_plots_3Dbar_2DbarColor.ipynb` uses data stored in `.csv` format.
The `.csv` file should contain three columns: one for paramter 1 values, one for parameter 2 values, and one for performance values.
The first row of the `.csv` file should be a header with the column names. The names in this row will be used for labeling plot axes.

#### Example data

| PAR  | BSIZE | Execution Time (s) |
| ---- | ----- | ------------------ |
| 8    | 64    | 12.3               |
| 8    | 128   | 45                 |
| 16   | 64    | 67.8               |
| 16   | 128   | 90.1               |
| 32   | 64    | 2                  |
| 32   | 128   | 34.5               |

The data in the table above should be stored in the format below:

PAR,BSIZE,Execution Time (s)\
8,64,12.3\
8,128,45\
16,64,67.8\
16,128,90.1\
32,64,2\
32,128,34.5

### Example figures

#### 3D bar chart

By default, the first column will be graphed on the x-axis (the front-facing axis), and the second column will be graphed on the y-axis (the side-facing axis). 
The figure below shows the 3D bar chart produced from the example data above.
![3D bar chart for example data](/readme_images/3D_bar_chart_example.JPG)


#### 2D bar chart

By default, the first column will be graphed on the x-axis, and the second column will be displayed using colors.
The figure below shows the 2D bar chart produced from the example data above.
![2D bar chart for example data](/readme_images/2D_bar_chart_example.JPG)

#### Heatmap

By default, the first column will be plotted across the x-axis, and the second column will be plotted across the y-axis.
The figure below shows the heatmap produced from the example data above.
![heatmap for example data](/readme_images/heatmap_example.JPG)