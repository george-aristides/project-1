# project-1

<img src= 'airline_cover.jpg' width="800">


# Airline Routes - Major Events

This repository analyzes airline passenger trends over time, focusing on sudden and unpredictable changes via major events.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)

## Project Overview

This project explores the trends and effects of seasons in airline passengers traveling to various cities. The analysis includes:
- Breaking down the original dataset for major events.
- Mapping each airport to the map of USA using airport ID.
- Animated maps showing a heatmap of each airport and the passengers traveling through them per quarter.

## Dataset

The dataset is from: https://www.kaggle.com/datasets/oleksiimartusiuk/all-airline-fight-routes-in-the-us

## Installation

To run this project locally:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/george-aristides/project-1.git
   cd project-1
   
2. **Run in Jupyter Notebook:**
   jupyter notebook major-events-maharath.ipynb
   
3. **Necessary Installs**
    ```python
    import pandas as pd
    import hvplot.pandas
    import re
    import matplotlib
    import matplotlib.pyplot as plt
    import geopandas as gpd
    import plotly.express as px
    from plotly.subplots import make_subplots
    import os
    import imageio
    from geopy.geocoders import Nominatim
    import time
    
## Usage

After the dataset it loaded it is broken into 4 sections:

1. Basic Setup Code: Inital breakdown of the data.
2. Geomapping: Creates mapping data for the dataframes.
3. Saving the files: Output the animated maps as gifs (DNW)
4. Background code: Nominatim API and extract state functions for other branches.

## Visualization

<img src= 'Departure 2008-2011.gif' width="800">

Visualization of the top 10 most popular citites over 5 year intervals starting from 1990 to 2020

