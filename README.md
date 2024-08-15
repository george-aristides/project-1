# project-1

![airline_cover (1)](https://github.com/user-attachments/assets/a8b5cae3-7eb7-4c3e-be98-95c461eb3e7c)



# Airline Routes - Unpredicted events and their impacts on flight routes in the US

This repository analyzes unpredicted events and their impacts on flight routes, focusing on major events in the US from 2001-2023

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Visualization](#visualization)

## Project Overview

This project analyzes unpredicted events and their impacts on flight routes. The analysis includes:
- Scatter plot maps of airports in the US
- The airport density of travel from origin to destination from years of 2012-2015 and 2016-2023
- Analyzes flight routes during the time of Hurricane Sandy and Covid-19
  

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
   Unpredicted events and their impacts on flight routes .ipynb
   
3. **Necessary Installs**
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

<img width="810" alt="Screenshot 2024-08-15 at 5 52 39 PM" src="https://github.com/user-attachments/assets/d55e1f3c-b66b-4148-99b4-38d05e626132">


