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


![Thermal lag](https://github.com/Shissors/Automated-Climate-Niche-Diagnostic-tool/blob/main/TL.png)

Thermal Lag Plot, shows the occurences of tigers at this temperature (max avg temperature) based on past and present observations. The change in density means that the tigers at present are found at higher temperature regions.

![Precipitation lag](https://github.com/Shissors/Automated-Climate-Niche-Diagnostic-tool/blob/main/AL.png)

Precipitation Lag Plot, shows the occureneces of tigers at locations with annual rainfall (avg annual rainfall) based on past and present observations. The change in density indicates their movement to more drier regions.

![KDL](https://github.com/Shissors/Automated-Climate-Niche-Diagnostic-tool/blob/main/KDL.png)

Kernel Density Map, shows the relationship between max temp and annual rainfall. The clusters show occurences of tigers at that temperature and rainfall. They occupied two different climatic niches. 

![MAP](https://github.com/Shissors/Automated-Climate-Niche-Diagnostic-tool/blob/main/newplot%20(1).png)

Geographical Temporal map showing the distribution of Tiger occurences and the max annual temperature at that region where the observeances were recorded. 




