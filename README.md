# project-1

<img src= airline_cover.jpg width="800">


# Airline Routes - Season

This repository analyzes airline passenger trends over time, focusing on changes correlated to seasons.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Visualization](#visualization)

## Project Overview

This project explores the trends and effects of seasons in airline passengers traveling to various cities. The analysis includes:
- Visual of passenger numbers overall and in 5-year intervals.
- Popular destinations each season.
- Popular routes each season.
- Animated bar chart of city popularity across seasons.

## Dataset

The dataset used in this project contains the following columns:
- `Year`: The year each flight took place.
- `Departure City`: The cities the passengers were leaving from.
- `Destination City`: The cities the passengers are traveling to.
- `Passengers`: The number of passengers recorded in each interval.
- `Fare`: The average fare of each flight that took place.
- `Departure State`: The states the passengers were leaving from.
- `Destination State`: The states the passengers are traveling to.
- `Season`: The season each flight took place: Winter, Spring, Summer, Fall
- `Flights`: The total number of flights from one city to another
- `5 Year Interval`: The time intervals (e.g., 1990-1995, 1995-2000) that the passenger data is organized into.

The data is stored in a CSV file and is loaded into the Jupyter Notebook for analysis.

## Installation

To run this project locally:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/george-aristides/project-1.git
   cd project-1
   
2. **Run in Jupyter Notebook:**

   jupyter notebook Airline.ipynb
   
4. **Necessary Installs**
    ```python
    import pandas as pd
    import re
    import seaborn as sns
    import matplotlib.pyplot as plt
    import plotly.express as px
    from geopy.geocoders import Nominatim
    import time

## Usage

After the dataset it loaded it is broken into 4 sections:

1. Inital breakdown of the data.
2. Customizing and narrowing down the data to fit our specific needs.
3. Analysis of the data to answer any specific questions.
4. Visualizations of the data acquired.

## Visualization

<img src= city_popularity_over_time.png width="800">

Visualization of the top 10 most popular citites over 5 year intervals starting from 1990 to 2020

