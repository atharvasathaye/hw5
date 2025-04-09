---
layout: default
title: Homework 5
---

<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<style>
body {
  font-family: 'Segoe UI', sans-serif;
  max-width: 900px;
  margin: 2rem auto;
  padding: 1rem;
  background-color: #f7f9fb;
  color: #222;
}
h1, h2 {
  text-align: center;
}
.viz-container {
  margin: 2rem 0;
  background: #fff;
  padding: 1rem;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
button {
  padding: 0.5rem 1rem;
  font-size: 1rem;
  background-color: #3367d6;
  color: white;
  border: none;
  border-radius: 6px;
  margin-right: 1rem;
  cursor: pointer;
}
button:hover {
  background-color: #264f9c;
}
</style>

# Homework 5: Bigfoot Sightings Visualization

<div class="viz-container">
  <h2>Bigfoot Reports per Year</h2>
  <p>This bar chart shows how many Bigfoot sightings were reported each year. The color intensity helps highlight years with more reports.</p>
  <div id="chart1"></div>
</div>

<div class="viz-container">
  <h2>Bigfoot Sightings by Location and Season</h2>
  <p>This interactive map shows the location of sightings, color-coded by season. Use the legend to filter and explore seasonal patterns.</p>
  <div id="chart2"></div>
</div>

---

## Interactivity

The second chart uses Altair’s `selection_point` to allow filtering sightings by season. This helps make patterns easier to identify across the map.

---

## Resources

<a href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv">
  <button>The Data</button>
</a>

<a href="https://github.com/atharvasathaye/hw5/blob/main/Workbook.ipynb">
  <button>The Analysis</button>
</a>

<script>
vegaEmbed('#chart1', 'charts/bigfoot_reports_per_year.json', { actions: false });
vegaEmbed('#chart2', 'charts/bigfoot_map_interactive.json', { actions: false });
</script>
