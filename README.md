# Mapping Accident Trends and Patterns in Maryland

An interactive D3.js dashboard that tells a data-driven story about traffic crashes in Montgomery County, Maryland: when they happen, where, under what conditions, and how severe they are.

**Live demo:** [add link after enabling GitHub Pages]

![Dashboard overview](images/[screenshot-name].png)

## Views
- **Mosaic chart:** lighting conditions vs. injury severity. Shows that poor light at dawn and dusk is linked to higher injury rates.
- **Stacked bar chart:** crashes across light and weather conditions, split by driver fault. Click a bar to open the treemap.
- **Treemap:** breaks crashes down by weather condition and severity (size = frequency, color = severity).
- **Car-in-a-clock:** collision direction mapped onto a clock face, with a spider chart comparing frequency and injury severity, filterable by vehicle type.
- **Geospatial map:** crash hotspots and severity by ZIP code.
- **Pie chart matrix:** injury severity by vehicle model year and brand origin.

## My contribution
Group project for CSE 578 Data Visualization at Arizona State University (Fall 2024).

I designed and built the **mosaic chart** (`mosaicmap.js`), which shows how lighting conditions relate to injury severity, using the Photino D3 Components mosaic-plot API with custom color encoding, tooltips and interactive filtering. I also integrated it into the main dashboard (`index.html`).

Team: Anirudh Iyengar Kaniyar Narayana Iyengar, Aman Bhaiji Jain, Ashutosh Prakash Dhopte, Harsh Nitinkumar Chandak and Soumya Nagendra.

## Data
[Crash Reporting – Drivers Data](https://catalog.data.gov/dataset/crash-reporting-drivers-data), Montgomery County, MD (Automated Crash Reporting System).

Preprocessing (Node.js + Express): filtered incomplete records, mapped crash coordinates to ZIP-code regions with GeoJSON, sampled every 5th record to keep the dataset small while staying representative, and exported the result to `final.csv`.

## Tech
D3.js, JavaScript, jQuery, HTML/CSS · Node.js, Express, csvtojson, json-2-csv · Turf.js and RBush for geospatial work · GitHub Pages

## Run locally
1. Preprocessing (optional; `final.csv` is already included): `npm install`, then `npm run dev`, then open `http://localhost:5000/data-cleaning`
2. Serve the dashboard: `npx serve .` and open the URL it prints
