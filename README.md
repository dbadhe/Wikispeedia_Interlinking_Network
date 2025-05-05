# Analyzing Wikipedia Paths and Network Structure

This project analyzes a dataset of user navigation paths on Wikipedia (from dataset from Wikilinks), focusing on the structure and properties of the networks formed by these paths. It investigates both completed and incomplete navigation sessions, as well as the overall network of links between articles.

## Overview

The goal of this project is to gain insights into how users navigate Wikipedia, identify key articles based on network centrality measures, and compare the characteristics of different types of navigation networks. The analysis involves:

* **Data Loading and Preprocessing:** 
Dataset - https://snap.stanford.edu/data/wikispeedia.html 
Reading and cleaning the provided TSV files containing article information, finished paths, and unfinished paths. This includes URL decoding of article titles and handling missing or incomplete data.
* **Network Construction:** Creating three distinct graph objects using the `igraph` package:
    * `g_fin`: A directed graph representing finished navigation paths.
    * `g_unfin`: A directed graph representing unfinished navigation paths.
    * `g_link`: An undirected graph representing the overall links between Wikipedia articles.
* **Network Analysis:** Calculating and comparing various network centrality measures (degree, closeness, betweenness) for each of the constructed graphs.
* **Visualization:** Generating box plots using `ggplot2` to compare the distributions of centrality measures across the different networks.
* **Shortest Path Analysis:** Calculating and analyzing the shortest path lengths in the finished paths network.

## Project Structure

The project likely contains the following files:

* `README.md`: This file, providing an overview of the project.
* `Wikipedia (1).Rmd`: The R Markdown file containing the code for data loading, preprocessing, network analysis, and visualization.
* `articles.tsv`: A tab-separated file containing Wikipedia article titles (likely URL-encoded).
* `paths_finished.tsv`: A tab-separated file containing completed user navigation paths.
* `paths_unfinished.tsv`: A tab-separated file containing incomplete user navigation paths.

## Getting Started

To run this analysis, you will need:

* **R:** The R programming language (version X.X.X or later).
* **RStudio:** An integrated development environment (IDE) for R (recommended).
* **The following R packages:**
    * `readr`
    * `utils`
    * `tidyr`
    * `igraph`
    * `tidyverse` (which includes `dplyr` and `ggplot2`)
    * `tidyselect`
    * `stringr`

### Installation

If you don't have these packages installed, you can install them in R using the following command:

```R
install.packages(c("readr", "utils", "tidyr", "igraph", "tidyverse", "tidyselect", "stringr"))