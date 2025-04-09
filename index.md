# Homework 5: Bigfoot Sightings Visualization

## Bigfoot Reports per Year

This bar chart shows the number of Bigfoot sighting reports collected each year. I chose a bar chart because it's an effective way to compare frequency across discrete time units. I encoded the X-axis as ordinal years and the Y-axis as the count of reports. The color of the bars uses a sequential blue colormap to visually represent the magnitude of counts—darker bars indicate more reports.

To prepare this visualization, I converted the `date` column to datetime format and extracted the year. I filtered out records with missing or invalid year data. This plot is entirely new compared to Homework 5 and does not reuse any code or structure from it.

<iframe src="bigfoot_reports_per_year.json" width="100%" height="420"></iframe>

---

## Bigfoot Sightings by Season (Interactive Map)

This chart shows the geographic locations of Bigfoot sightings, using latitude and longitude. Each point is colored by the season the sighting occurred in. The use of color allows viewers to detect seasonal trends in sightings. The X and Y encodings correspond to longitude and latitude respectively, and color encodes the season.

I filtered out rows with missing geolocation data and used Altair's `selection_point` functionality to allow filtering by season via the legend. This improves clarity and makes it easier to focus on particular seasonal patterns. This plot is completely new and not reused from Homework 5.

<iframe src="bigfoot_map_interactive.json" width="100%" height="450"></iframe>

---

## Interactivity

The second visualization uses `selection_point` from Altair v5 to allow users to filter sightings by season. This interaction is bound to the legend, making it intuitive and seamless to explore patterns by season. This adds depth and clarity to the spatial distribution of sightings, especially when multiple seasons overlap geographically.

---

<div style="margin-top: 1.5em;">
  <a href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv" target="_blank">
    <button>The Data</button>
  </a>
  <a href="https://github.com/atharvasathaye/hw5/blob/main/Workbook.ipynb" target="_blank">
    <button>The Analysis</button>
  </a>
</div>
