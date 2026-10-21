# Mapping Accident Trends in Maryland

An interactive D3.js dashboard that explores crash data from Montgomery County, Maryland, through six coordinated views.

**Live demo:** [add after Step 5]

![Dashboard screenshot](images/[screenshot-name].png)

## What it shows
- **Car clock:** crashes by time of day and vehicle type
- **Geospatial map:** crash density by ZIP code
- **Heatmap:** [what it compares]
- **Mosaic map:** [what it compares]
- **Pie chart matrix:** [what it compares]
- **Stacked bar / treemap:** [what it compares]

## My contribution
Group project for CSE 578 Data Visualization at Arizona State University (Fall 2024).
I designed and built the **mosaic map** view (`mosaicmap.js`), which shows [what it compares, e.g. how crash severity breaks down by weather and road condition], and integrated it into the main dashboard.
Teammates built the other five views and the data preprocessing pipeline.

Team: Aman, Anirudh Krishna, Ashutosh Dhopte, Harsh Chandak, Utkarsh Singh and Soumya Nagendra.

## Tech
D3.js, JavaScript, HTML/CSS, Node.js (Express) for data preprocessing

## Data
[Crash Reporting – Drivers Data](https://catalog.data.gov/dataset/crash-reporting-drivers-data), data.gov

## Run locally
1. Preprocess (optional; `final.csv` is already included): `npm install`, `npm run dev`, then open `http://localhost:5000/data-cleaning`
2. Serve the dashboard: `npx serve .` and open the printed URL
