# TTC Subway Stops Analysis & Visualization

## Overview
This project processes and visualizes Toronto Transit Commission (TTC) stop data. It cleans raw transit data (`stops.csv`) by normalizing stop names, identifying core subway stations, and mapping individual platform stops to their respective parent stations based on geographic coordinates (latitude and longitude).

## Data Source
The `stops.csv` data is sourced from the official TTC Open Data portal: [TTC Routes and Schedules](https://open.toronto.ca/dataset/ttc-routes-and-schedules/).

## Key Features
* **Data Cleaning & Normalization:** Maps raw, messy stop names to canonical TTC station names (e.g., standardizing "1 Front St West Union Station" to "Union Station").
* **Geospatial Grouping:** Groups physically adjacent stops to determine `parent_station` and minimum `stop_id`s.
* **Line Mapping:** Automatically maps stations to their respective TTC Subway Lines (Line 1, 2, 4, 5, and 6) and handles interchange stations.
* **Interactive Visualization:** Uses `folium` to generate an interactive web map (`index.html`) featuring marker clustering, custom color-coded station markers, and drawn polylines representing the TTC subway routes. 
* **Export:** Outputs a cleaned, consolidated dataset (`processed_stations.csv`) ready for further spatial or transit analysis.

## Preview
You can view the interactive map of the generated TTC stations by opening the [index.html](index.html) file locally after running the notebook.


## Tech Stack
* Python
* Pandas
* Folium
* Regular Expressions (Regex)

## Getting Started

1. Ensure you have the required dependencies installed:
   ```bash
   pip install pandas folium
   ```
2. Download the `stops.csv` file from the [TTC Open Data portal](https://open.toronto.ca/dataset/ttc-routes-and-schedules/) and place it in the root directory.
3. Run the Jupyter Notebook (`sample.ipynb`) to process the data and generate the map.
4. Open the generated `index.html` file in your web browser to view the interactive map.
5. The cleaned data will be saved as `processed_stations.csv`.