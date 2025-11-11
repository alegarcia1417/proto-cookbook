# Ale's Prototype Cookbook

<img src="thumbnails/thumbnail.png" alt="thumbnail" width="300"/>

[![nightly-build](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/cookbook-template/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/cookbook-template/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/475509405.svg)](https://zenodo.org/badge/latestdoi/475509405)


This Project Pythia Cookbook covers areas impacted by Hurricane Helene, looking at infrastructure and meteorological impacts, as well as an overview of social vulnerability and disaster declarations issued.

## Motivation

This cookbook works with csv datasets, Pandas DataFrames, GeoPandas, cleaning and isolating data, and visualizing data geographically over polygons. This  aims to teach how to conduct proper data analysis and plot data across polygons.

## Authors

[Alejandra Garcia](https://github.com/alegarcia1417)

### Contributors

<a href="https://github.com/ProjectPythia/cookbook-template/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/cookbook-template" />
</a>

## Structure

This cookbook is organized into two notebooks: visualizing presidential disaster declarations and physical impacts of Hurricane Helene AND visualizing the social vulnerability in counties impacted by Hurricane Helene.

### Notebook 1

This notebook imported two csv datasets and merged them to retain population, exposure, and recovery data for Hurricane Helene, as well as county geometry to be able to plot the statistical data as polygons. This notebook also spatially visualized the counties that issued a presidential disaster declaration during Hurricane Helene in 2024. This notebook also spatially mapped the distribution of customers who lost power during Hurricane Helene and the maximum observed wind swath during Hurricane Helene in each of the affected counties. ({cite:t}`Sawyer:2025`) ({cite:t}`US Army Corps of Engineers - Nashville District:2025`)

### Notebook 2

This notebook read in the helene_merged.csv we created in notebook1, but we also had to ensure that the geometry column was readable. We converted the MKT String to Shapely Geometry in order to convert helene_merged to a GeoDataFrame so the geometry column could be read as polygons. After that, this notebook plotted poverty level percentages using data from helene_merged as well as amount of people living in rural areas in the counties where Hurricane Helene led to a presidential disaster declaration.

## Running the Notebooks

You can either run the notebook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables the execution of a
[Jupyter Book](https://jupyterbook.org) in the cloud. The details of how this works are not
important for now. All you need to know is how to launch a Pythia
Cookbooks chapter via Binder. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon, (see figure below), and be sure to select
“launch Binder”. After a moment you should be presented with a
notebook that you can interact with. I.e. you’ll be able to execute
and even change the example programs. You’ll see that the code cells
have no output at first, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter).

Note, not all Cookbook chapters are executable. If you do not see
the rocket ship icon, such as on this page, you are not viewing an
executable book chapter.


### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

(Replace "cookbook-example" with the title of your cookbooks)

1. Clone the `https://github.com/ProjectPythia/cookbook-example` repository:

   ```bash
    git clone https://github.com/ProjectPythia/cookbook-example.git
   ```

1. Move into the `cookbook-example` directory
   ```bash
   cd cookbook-example
   ```
1. Create and activate your conda environment from the `environment.yml` file
   ```bash
   conda env create -f environment.yml
   conda activate cookbook-example
   ```
1. Move into the `notebooks` directory and start up Jupyterlab
   ```bash
   cd notebooks/
   jupyter lab
   ```
