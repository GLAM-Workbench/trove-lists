# Trove lists and tags

Jupyter notebooks to work with data from Trove's public lists and tags.

## Notebook topics

### Lists

* [**Convert a Trove list into a CSV file**](Convert-a-Trove-list-into-a-CSV-file.ipynb) – extracts list data from the Trove API and saves the results as CSV files (with separate files for newspaper articles and other resources); optionally save OCRd test, PDFs, and images of any listed newspaper articles.
* [**Harvest summary data from Trove lists**](Harvest-summary-data-from-lists.ipynb) – extract and analyse data from all public lists in Trove

### Tags

* [**Harvest public tags from Trove zones**](harvest-tags.ipynb) – assemble a dataset containing all public tags added to Trove
* [**Analyse public tags added to Trove**](analyse_tags.ipynb) – explore ways of analysing and visualising the complete dataset of public tags added to Trove resources

### Data files

* [trove-lists-2020-09-22.csv](https://github.com/GLAM-Workbench/trove-lists/blob/master/data/trove-lists-2020-09-22.csv) (harvested 22 September 2020) – basic metadata about all public lists
* [Trove public tags](https://doi.org/10.5281/zenodo.5094314) (Zenodo, zipped CSV, harvested 10 July 2021) – complete dataset of more than 8 million public tags
* [trove_tag_counts_20210710.csv](https://github.com/GLAM-Workbench/trove-lists/blob/master/trove_tag_counts_20210710.csv) (harvested 10 July 2021) – counts of individual tags

<!-- START RUN INFO -->

## Run these notebooks

There are a number of different ways to use these notebooks. Binder is quickest and easiest, but it doesn't save your data. I've listed the options below from easiest to most complicated (requiring more technical knowledge).

### Using Binder

[![Launch on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GLAM-Workbench/trove-lists/master/?urlpath=lab/tree/index.md)

Click on the button above to launch the notebooks in this repository using the [Binder](https://mybinder.org/) service (it might take a little while to load). This is a free service, but note that sessions will close if you stop using the notebooks, and no data will be saved. Make sure you download any changed notebooks or harvested data that you want to save.

### Using Reclaim Cloud

[![Launch on Reclaim Cloud](https://glam-workbench.github.io/images/launch-on-reclaim-cloud.svg)](https://app.my.reclaim.cloud/?manifest=https://raw.githubusercontent.com/GLAM-Workbench/trove-lists/master/reclaim-manifest.jps)

[Reclaim Cloud](https://reclaim.cloud/) is a paid hosting service, aimed particularly at supported digital scholarship in hte humanities. Unlike Binder, the environments you create on Reclaim Cloud will save your data – even if you switch them off! To run this repository on Reclaim Cloud for the first time:

* Create a [Reclaim Cloud](https://reclaim.cloud/) account and log in.
* Click on the button above to start the installation process.
* A dialogue box will ask you to set a password, this is used to limit access to your Jupyter installation.
* Sit back and wait for the installation to complete!
* Once the installation is finished click on the 'Open in Browser' button of your newly created environment (note that you might need to wait a few minutes before everything is ready).

See the GLAM Workbench for more details.

### Using Docker

You can use Docker to run a pre-built computing environment on your own computer. It will set up everything you need to run the notebooks in this repository. This is free, but requires more technical knowledge – you'll have to install Docker on your computer, and be able to use the command line.

* Install [Docker Desktop](https://docs.docker.com/get-docker/).
* Create a new directory for this repository and open it from the command line.
* From the command line, run the following command:  
  ```
  docker run -p 8888:8888 --name trove-lists -v "$PWD":/home/jovyan/work glamworkbench/trove-lists repo2docker-entrypoint jupyter lab --ip 0.0.0.0 --NotebookApp.token='' --LabApp.default_url='/lab/tree/index.md'
  ```
* It will take a while to download and configure the Docker image. Once it's ready you'll see a message saying that Jupyter Notebook is running.
* Point your web browser to `http://127.0.0.1:8888`

See the GLAM Workbench for more details.

### Setting up on your own computer

If you know your way around the command line and are comfortable installing software, you might want to set up your own computer to run these notebooks.

Assuming you have recent versions of Python and Git installed, the steps might be something like:

* Create a virtual environment, eg: `python -m venv trove-lists`
* Open the new directory" `cd trove-lists`
* Activate the environment `source bin/activate`
* Clone the repository: `git clone https://github.com/GLAM-Workbench/trove-lists.git notebooks`
* Open the new `notebooks` directory: `cd notebooks`
* Install the necessary Python packages: `pip install -r requirements.txt`
* Run Jupyter: `jupyter lab`

See the GLAM Workbench for more details.

<!-- END RUN INFO -->

## Cite as

See the GLAM Workbench or [Zenodo](https://doi.org/10.5281/zenodo.3521724) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  
If you think this project is worthwhile, you might like [to sponsor me on GitHub](https://github.com/sponsors/wragge?o=esb).
