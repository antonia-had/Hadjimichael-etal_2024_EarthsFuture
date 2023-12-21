_your zenodo badge here_

# Hadjimichael-etal_2024_EarthsFuture

**Multi-actor, multi-impact scenario discovery of consequential narrative storylines for human-natural systems planning**

Antonia Hadjimichael<sup>1, 2\*</sup>, Patrick M. Reed <sup>3</sup>, Julianne D. Quinn <sup>4</sup>, Chris R. Vernon <sup>5</sup>, Travis Thurber <sup>5</sup>

<sup>1 </sup> Department of Geosciences, The Pennsylvania State University, State College, PA, USA\
<sup>2 </sup> Earth and Environmental Systems Institute (EESI), The Pennsylvania State University, State College, PA, USA\
<sup>3 </sup> School of Civil and Environmental Engineering, Cornell University, Ithaca, NY, USA
<sup>4</sup> Department of Engineering Systems and Environment, University of Virginia, Charlottesville, VA, USA
<sup>5</sup> Atmospheric Sciences \& Global Change, Pacific Northwest National Laboratory, Richland, WA, USA

\* corresponding author:  hadjimichael@psu.edu

## Abstract
Scenarios have emerged as valuable tools in managing complex human-natural systems, but the traditional approach of limiting focus on a small number of predetermined scenarios can inadvertently miss consequential dynamics, extremes, and diverse stakeholder impacts. Exploratory modeling approaches have been developed to address these issues by exploring a wide range of possible futures and identifying those that yield consequential vulnerabilities. However, vulnerabilities are typically identified based on aggregate robustness measures that do not take full advantage of the richness of the underlying dynamics in the large ensembles of model simulations and can make it hard to identify key dynamics and/or narrative storylines that can guide planning or further analyses. This study introduces the FRamework for Narrative Scenarios and Impact Classification (FRNSIC; pronounced ``forensic''): a scenario discovery framework that addresses these challenges by organizing and investigating consequential scenarios using hierarchical classification of diverse outcomes across actors, sectors, and scales, while also aiding in the selection of narrative storylines, based on system dynamics that drive consequential outcomes. We present an application of this framework to the Upper Colorado River Basin, focusing on decadal droughts and their water scarcity implications for the basin’s diverse users and its obligations to downstream states through Lake Powell. We show how FRNSIC can explore alternative sets of impact metrics and drought dynamics and use them to identify narrative drought storylines, that can be used to inform future adaptation planning.

## Journal reference
Hadjimichael, A., Reed, P.M., Quinn, J.D, Vernon, C.R., Thurber, T., Multi-actor, multi-impact scenario discovery of consequential narrative storylines for human-natural systems planning. _Earth's Future_ (in review)

## Data reference

### Input data
Hadjimichael, A., Reed, P. M., Quinn, J. D., Vernon, C. R., & Thurber, T. (2023). Data for Hadjimichael et al. - Multi-actor, multi-impact scenario discovery (Version v1) [Data set]. MSD-LIVE Data Repository. https://doi.org/10.57931/2205512

To download this data, follow the instructions provided on the MSD-LIVE page. 

## Contributing modeling software
| Model | Version | Repository Link | DOI |
|-------|---------|-----------------|-----|
| StateMod | 15.0 | https://github.com/OpenCDSS/cdss-app-statemod-fortran | - |

## Reproduce my experiment

1. Install all package dependencies listed in environment.yml using `conda env create --file environment.yml`
2. Activate environment using `conda activate Hadjimichael-etal_2024_EarthsFuture`
3. Create directory `/xdd_parquet_flow` under `/data`
4. Download and install the supporting input data required to perform the analysis from [Input data](#input-data) and save under `../data/xdd_parquet_flow`
4. Go through the following notebooks in the `workflow` directory to re-create these results:

| Script Name                                  | Description                                                                                 | How to Run                                  |
|----------------------------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------|
| `classify_naturalized_streamflows-drought.ipynb` | Script to perform drought classification for historic and synthetic streamflows (Fig. 3)    | Execute notebook |
| `streamflow_distribution_changes.ipynb`      | Script for drought classification across rolling windows (Figs. 4, S1-3)                    | Execute notebook |
| `hive_plots_drought_impacts-history.ipynb`     | Script to generate hive plot and storyline for historically-informed conditions (Figs. 8-9) | Execute notebook |
| `hive_plots_drought_impacts-history.ipynb`     | Script to generate hive plot and storyline for historically-informed conditions (Figs. 8-9) | Execute notebook |

4. Download and unzip the output data from my experiment [Output data](#output-data)
5. Run the following scripts in the `workflow` directory to compare my outputs to those from the publication

| Script Name | Description | How to Run |
| --- | --- | --- |
| `compare.py` | Script to compare my outputs to the original | `python3 compare.py --orig /path/to/original/data.csv --new /path/to/new/data.csv` |

## Reproduce my figures
Use the scripts found in the `figures` directory to reproduce the figures used in this publication.

| Script Name | Description | How to Run |
| --- | --- | --- |
| `generate_figures.py` | Script to generate my figures | `python3 generate_figures.py -i /path/to/inputs -o /path/to/outuptdir` |
