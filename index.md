<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Homework 5: Bigfoot Visualizations</title>
  <script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
  <script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      margin: 2rem auto;
      max-width: 900px;
      padding: 1rem;
      background: #f7f9fb;
      color: #222;
    }
    h1 {
      text-align: center;
    }
    .viz-container {
      margin: 2rem 0;
    }
    iframe, .vega-embed {
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 0.5rem;
      background: white;
    }
    button {
      padding: 0.5rem 1rem;
      font-size: 1rem;
      margin-right: 1rem;
      background-color: #3367d6;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
    }
    button:hover {
      background-color: #264f9c;
    }
  </style>
</head>
<body>

  <h1>Homework 5: Bigfoot Sightings Visualization</h1>

  <div class="viz-container">
    <h2>Bigfoot Reports per Year</h2>
    <p>This bar chart shows how many Bigfoot sightings were reported each year. The color intensity helps highlight higher frequency years.</p>
    <div id="chart1"></div>
  </div>

  <div class="viz-container">
    <h2>Bigfoot Sightings by Location and Season</h2>
    <p>This interactive map shows the locations of sightings, colored by season. Use the legend to filter by season.</p>
    <div id="chart2"></div>
  </div>

  <h3>Resources</h3>
  <p>
    <a href="https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv">
      <button>The Data</button>
    </a>
    <a href="https://github.com/atharvasathaye/hw5/blob/main/Workbook.ipynb">
      <button>The Analysis</button>
    </a>
  </p>

  <script>
    vegaEmbed('#chart1', 'bigfoot_reports_per_year.json', {actions: false});
    vegaEmbed('#chart2', 'bigfoot_map_interactive.json', {actions: false});
  </script>
</body>
</html>
