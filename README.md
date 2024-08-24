# Sea-Level-Dynamics

# Climate Change Data Analysis and Visualization Project

This project is dedicated to analyzing climate change data to predict future sea level rises based on various environmental factors. It combines data analysis and a dynamic Shiny dashboard to facilitate interactive data exploration and visualization.

## Table of Contents
- [Project Overview](#project-overview)
- [Data](#data)
- [Installation](#installation)
- [Usage](#usage)
- [Data Analysis](#data-analysis)
- [Shiny Dashboard](#shiny-dashboard)
- [Results](#results)

## Project Overview

The Climate Change Data Analysis and Visualization Project aims to predict future sea level rise using historical climate data. The project is divided into two main components:
1. **Data Analysis**: Utilizing statistical methods like linear regression to identify relationships between various environmental factors and sea level rise.
2. **Shiny Dashboard**: An interactive web application for users to explore the data, visualize trends, and download customized datasets.

## Data

The dataset (`climate_change_data.csv`) contains historical climate records, including:
- **Date**: The observation date.
- **Temperature**: Global temperature data (°C).
- **CO2 Emissions**: Atmospheric CO2 levels (ppm).
- **Sea Level Rise**: Sea level rise data (mm).
- **Precipitation**: Global precipitation data (mm).
- **Humidity**: Global humidity levels (%).
- **Wind Speed**: Wind speed data (m/s).

## Installation

To run this project, install R and the following packages: `tidyverse`, `lubridate`, `ggplot2`, `dplyr`, `corrplot`, `shiny`, and `leaflet`.

## Usage

### Data Analysis

The data analysis component focuses on processing and analyzing the climate data to derive insights and predict future trends. Key steps include:

1. **Data Preprocessing**: 
   - Conversion of the `Date` column to a date format.
   - Handling missing values to ensure data integrity.
   - Normalization of data to facilitate accurate analysis.

2. **Exploratory Data Analysis (EDA)**:
   - **Correlation Plot**: A correlation matrix visualization to understand the relationships between different variables like temperature, CO2 emissions, sea level rise, etc. This plot helps in identifying the strength and direction of relationships, which is crucial for modeling.

3. **Model Training**:
   - **Linear Regression**: The project employs linear regression to model the relationship between sea level rise and other environmental factors such as temperature, CO2 emissions, precipitation, humidity, and wind speed. The model is then used to predict future sea level rises based on projected environmental changes.

4. **Prediction**:
   - **Future Data Projections**: The project generates future projections of environmental data and predicts the corresponding sea level rises. This step is critical for understanding the potential impact of climate change on sea levels over time.

### Shiny Dashboard

The Shiny dashboard provides an interactive interface for exploring the climate data. It allows users to filter the data, visualize trends, and download customized datasets. Here’s a breakdown of the dashboard’s features:

#### User Interface (UI)

- **Title Panel**: The title "Environmental Dashboard" is prominently displayed at the top.
- **Sidebar Panel**: This section allows users to:
  - Select a date range to filter the data.
  - Choose a specific country and location type (Urban or Rural) to focus the analysis.
  - Select a specific environmental measurement (e.g., Temperature, CO2 Emissions, Sea Level Rise, Humidity) to visualize.
  - Download the filtered dataset in CSV format.

#### Main Panel

- **Main Plot**: Displays a time series plot of the selected environmental measurement over the chosen date range. This visualization helps users understand trends over time and identify any significant changes or patterns.
  
- **Summary Table**: Provides key statistical summaries (Mean, Median, Standard Deviation) for the selected measurement. This table gives users a quick overview of the central tendency and variability in the data.

- **Interactive Map**: Using Leaflet, the dashboard renders an interactive map with markers representing sample locations. This map feature is particularly useful for visualizing geographic variations in environmental data.

#### Visualizations in Detail

1. **Time Series Plot**:
   - A line plot showing the trend of a selected environmental measurement (e.g., Temperature, CO2 Emissions, Sea Level Rise, or Humidity) over the chosen time period. This plot allows users to track changes over time, providing insights into long-term trends and anomalies.

2. **Correlation Plot**:
   - A heatmap of correlations between different environmental variables. Each cell in the matrix shows the correlation coefficient between two variables, with the color intensity representing the strength of the correlation. This visualization is key for understanding how different factors like temperature and CO2 emissions are interrelated.

3. **Summary Statistics**:
   - A tabular representation of the mean, median, and standard deviation for the selected measurement, giving users a concise summary of the data's central tendency and spread.

4. **Interactive Map**:
   - A geographical visualization using Leaflet, where users can see the distribution of environmental data across different locations. The map is interactive, allowing users to zoom in and out and click on markers to view more details about specific locations.

### Running the Application

To run the Shiny dashboard, load the application in your R environment and explore the different features to analyze the climate data.

## Results

The project successfully models and predicts future sea level rises based on historical data. The results highlight the relationships between various environmental factors and their impact on sea levels. Through the Shiny dashboard, users can interactively explore these relationships, generate visualizations, and download filtered data for further analysis.

