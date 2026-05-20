# Wildfire Mapping
Project of SDS210

This project analyzes recent wildfire activity in Campeche, southern Mexico, using interactive web mapping techniques. Wildfire detections are retrieved dynamically through the FirePing API and visualized using Python and Folium. The project focuses on how wildfire activity changes over a 7-day period and how Fire Radiative Power (FRP) can be effectively represented through cartographic visualization techniques. The study area is located in the state of Campeche in southern Mexico near the Gulf of Mexico.

## Objective
The goal of this project is to create an interactive wildfire map that allows users to:
- visualize wildfire detections over a time,
- identify areas with high wildfire intensity,
- explore spatial clustering of wildfire events,
- and analyze daily wildfire activity within the monitoring period.

The visualization emphasizes Fire Radiative Power (FRP) values using a continuous color gradient. Interactive popups provide additional information for each wildfire detection, including:
- date,
- time,
- confidence level,
- FRP value,
- and satellite source.

Marker clustering is used to improve readability in areas with dense wildfire detections.

## Data Source
Wildfire data were retrieved from:
https://fireping.net/

To access the API:
1. Create a free FirePing account
2. Generate an API key
3. Choose monitoring coordinates and radius
4. Request wildfire detections using the API

API limitations for the free version:
- Maximum monitoring radius: 25 km
- Maximum temporal range: 7 days (168 hours)
- Maximum number of detections: 1000

The project was developed using the coordinates:

- Latitude: 19.038
- Longitude: -90.683

The code can be adapted to any other location with wildfire activity.

## Background map
The project uses the CartoDB dark basemap:
CartoDB.PositronOnlyLabels
Source: https://leaflet-extras.github.io/leaflet-providers/preview/

A dark basemap was chosen because it improves contrast and visibility for dense wildfire detections and FRP color gradients.

## Data Storage:
Wildfire detections retrieved from the API are converted into CSV files and stored locally in:
data/processed/

This improves reproducibility and allows the map to be recreated without repeatedly requesting live API data.

The repository currently contains wildfire datasets collected on:
- 08 May 2026
- 16 May 2026

## Technologies Used
- Python
- Pandas
- Folium
- Branca
- Requests
- Jupyter Notebook / VS Code

## Setup Instructions: Exactly what software and libraries are required to run the code (e.g., pointing to an environment.yml or requirements.txt file).
This project requires a specific spatial software stack. To recreate the environment:
1. Ensure you have Conda installed.
2. Run: `conda env create -f environment.yml`


