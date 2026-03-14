# Earthquake Dashboard

A real-time earthquake monitoring dashboard that displays live data from the USGS (United States Geological Survey) Earthquake API. This interactive web application provides visualizations, maps, and filters to explore recent seismic activity.

## Features

- **Live Data**: Fetches real-time earthquake data from USGS feeds (past 24 hours, 7 days, or 30 days).
- **Interactive Map**: Displays earthquake locations on a Leaflet map with magnitude-based markers.
- **Charts and Graphs**: 
  - Bar chart showing earthquake frequency over time.
  - Pie chart categorizing earthquakes by magnitude classes.
- **Filters**:
  - Minimum magnitude filter.
  - Country/region filter (extracted from location data).
  - Year filter (for historical data).
- **Real-time Updates**: Automatically checks for new earthquakes every minute and notifies with toast messages.
- **Responsive Design**: Works on desktop and mobile devices using Bootstrap.

## Technologies Used

- **HTML/CSS/JavaScript**: Core web technologies.
- **Chart.js**: For creating interactive charts.
- **Leaflet.js**: For the interactive map.
- **Bootstrap 5**: For responsive UI components.
- **USGS Earthquake API**: Source of earthquake data (https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php).

## How to Run

### Option 1: Open Directly in Browser
1. Download or clone the repository.
2. Open `earthquake_dashboard.html` in your web browser.
3. The dashboard will load and display live data.

### Option 2: Serve Locally (Recommended for Development)
1. Ensure you have Python installed (Python 3.x).
2. Open a terminal in the project directory.
3. Run: `python -m http.server 8000`
4. Open your browser and go to `http://localhost:8000/earthquake_dashboard.html`

The local server allows for proper loading of resources and avoids CORS issues.

## Data Source

This dashboard uses data from the USGS Earthquake Hazards Program, which provides real-time earthquake information. The data includes:
- Magnitude
- Location (latitude, longitude, place description)
- Depth
- Time of occurrence

For more information, visit: https://earthquake.usgs.gov/

## Filters Explanation

- **Magnitude Filter**: Shows only earthquakes above the selected minimum magnitude.
- **Country Filter**: Filters earthquakes based on the country/region mentioned in the location string. Note: This is parsed from the USGS place field, which may not always be a country (e.g., "California" instead of "USA").
- **Year Filter**: Filters by the year of the earthquake event. Useful for historical analysis within the selected time range.

## Contributing

Feel free to fork this repository and submit pull requests for improvements or bug fixes.

## License

This project is open source and available under the [MIT License](LICENSE).

## Disclaimer

This dashboard is for informational purposes only. Earthquake data is provided by the USGS and may not be real-time in all cases. Always refer to official sources for critical earthquake information and safety guidelines.