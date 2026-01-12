# Automated Climate Niche Diagnostic Tool

A series of tools that combines occurence and climate data to calculate Useful metrics and uses plots for data analysis

## Getting Started

Before starting the program, you would need the following packages installed: Pandas, yaml,xarray, rioxarray, seaborn, matplotlib, plotly express, Scikit learn, scipy.

### The packages can be installed from here using pip or using singularity

If using pip
```
pip install -r requirements.txt
```
Using Singularity with the AMCN.def
```
sudo singularity build AMCN.sif AMCN.def
```

You would also require a a GBIF occurence file that you get [here](https://www.gbif.org/) and CHELSEA climate data which you get [here](https://www.chelsa-climate.org/)

Keep the gbif installation as a zip file itself. For the CHELSEA data, use the text file that you get from the downloads website should have the name like:"envidats3path.txt" or something similar.

### Installing

You can use the config files (.yaml) files to change the parameters. Like the input path and output path, etc. Then run the jupyter notebooks (Note: in future, versions I am planning to make this into one big NF pipeline)



## Running the Pipeline

Modify config.yaml
Run the gbif_unzip.ipynb 
Check the log
Modify config_chelsea.yaml
Run the Chelsea_unzip.ipynb
Check the log
Modify the config_metrics.yaml
Check the Output


## Output Plots


![The Read Depth Plot, showing the Position of Sequence (POS) on X axis and Read Depth (DP) on the Y axis, higher depth -> better coverage -> better quality](https://github.com/Shissors/Varaint-Calling-Pipeline/blob/main/read_depth.png)

The Read Depth Plot, showing the Position of Sequence (POS) on X axis and Read Depth (DP) on the Y axis, higher depth -> better coverage -> better quality

![The variant plot, shows SNPs and INDELs along the genome. The quality on the Y axis and POS on the X axis. Higher quality -> More reliable result](https://github.com/Shissors/Varaint-Calling-Pipeline/blob/main/variant.png)


The variant plot, shows SNPs and INDELs along the genome. The quality on the Y axis and POS on the X axis. Higher quality -> More reliable result

