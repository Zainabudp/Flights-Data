Plane Finder: A Real-Time Flight Tracking Script
Overview
This project provides a real-time flight tracking system that identifies airplanes flying over a specified location. The script utilizes APIs to fetch live flight data and visualizes aircraft movements using data analysis and mapping techniques.

How to run the code
- If the script contains a Colab link, simply click on it or copy-paste the URL into your browser.
- This will open the notebook in Google Colab, an interactive cloud-based environment.

Purpose & Features
The primary aim of this project is to:
- Retrieve real-time aircraft data using APIs.
- Determine the location of flights above a specific airport (Paris CDG in this case).
- Display flight details such as origin, latitude, longitude, and direction.
- Generate a bar chart analyzing flights by their origin country.
- Provide a visual map representation of flight locations.

How It Works
- Import Required Libraries
- urllib.request, json: Fetch flight data from APIs.
- matplotlib.pyplot, seaborn: Data visualization.
- folium: Generate interactive maps.
- pandas, numpy: Data manipulation and analysis.
- ssl: Handle HTTPS requests securely.
- Obtain Airport Location (Latitude & Longitude)
- The script queries https://www.airport-data.com/api/ap_info.json?iata=CDG to get latitude & longitude of Paris CDG Airport.
- Fetch Real-Time Flight Data
- Retrieves live flight data from https://opensky-network.org/api/states/all.
- Extracts relevant details like:
- Flight Name
- Origin Country
- Latitude & Longitude
- Position Relative to Observer
- Calculate Distance & Direction
- Converts latitude and longitude using predefined formulas to determine the flight's visibility direction (NE, NW, SE, SW).
- Analyze & Display Flight Data
- Loop through flights and print details.
- Determine how many planes are flying above the chosen location.
- Data Visualization
- Creates a bar chart using seaborn to display the number of flights per origin country.
- Saves the chart as Flights.png.

Potential Enhancements
- Integrate Folium maps for real-time flight visualization.
- Expand location tracking beyond Paris CDG.
- Improve flight data filtering to include altitude and speed metrics

