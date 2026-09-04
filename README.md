[README.md](https://github.com/user-attachments/files/31821676/README.md)
# Indian Agricultural Crop Yield Dashboard

An interactive Excel dashboard analyzing crop yield patterns across Indian states — built with real PivotTables, PivotCharts, and slicers to support data-driven agricultural planning.

## Overview

Agriculture employs over 50% of India's population, and understanding yield patterns across states, crops, seasons, and irrigation types is critical for effective policy-making and agribusiness planning. This project takes a raw dataset of Indian crop yield records and transforms it into an interactive dashboard that lets you explore performance by state, crop, season, irrigation type, geographic zone, and year — all filterable in real time.

## Dataset

- **500 records** spanning **2010–2022**
- **7 states**: Bihar, Haryana, Karnataka, Maharashtra, Punjab, Uttar Pradesh, West Bengal (3 districts each)
- **6 crops**: Wheat, Rice, Maize, Cotton, Pulses, Sugarcane
- **3 seasons**: Kharif, Rabi, Zaid
- **4 irrigation types**: Canal, Borewell, Drip, Rainfed

| Column | Description |
|---|---|
| Crop ID | Unique identifier for each crop entry |
| State / District | Location of cultivation |
| Year / Season | Year of observation; crop season |
| Crop Name | Wheat, Rice, Maize, Cotton, Pulses, Sugarcane |
| Area (Hectares) | Land area cultivated |
| Production (Tonnes) | Total crop production |
| Yield (Kg/Ha) | Derived metric: Production ÷ Area |
| Irrigation Type | Canal, Borewell, Drip, Rainfed |
| Fertilizer Type / Used (Kg) | Fertilizer category and quantity applied |
| Rainfall (mm) | Total rainfall during the crop season |
| Soil Type | Black, Red, Alluvial, Laterite, Sandy |
| Temperature (Celsius) | Average temperature during the crop period |

## What's in the Workbook

| Sheet | Contents |
|---|---|
| `Raw_data` | Original, untouched dataset |
| `Cleaned_data` | Cleaned data plus two derived columns: **Zone** (North/South/East/West, mapped from State) and **Yield Category** (High/Medium/Low) |
| `pivot_analysis` | Six PivotTables — State, Crop Name, Season, Irrigation Type, Zone, Year — each with Average Yield and Sum of Production |
| `Dashboard` | KPI cards, six PivotCharts, and four cross-connected slicers |

## Dashboard Features

- **KPI cards**: Total Records, Total Production, Average Yield, Total Area
- **6 PivotCharts**: Average Yield by State, Production Share by Crop, Average Yield by Season, Average Yield by Irrigation Type, Average Yield by Zone, Yield Trend Over Years
- **4 interactive slicers**: State, Season, Crop Name, Irrigation Type — connected to all six PivotTables, so any selection filters the entire dashboard at once
- **Conditional formatting**: color scale on Yield, data bars on Production for at-a-glance scanning

## Key Findings

- **Karnataka** posted the highest average yield (4,265.96 Kg/Ha); **Haryana** the lowest (3,753.19 Kg/Ha)
- **Cotton** led total production share (19%); **Rice** had the smallest share (14%)
- **Rabi** season outperformed **Zaid** on average yield (4,213 vs. 3,749 Kg/Ha)
- **Canal** and **Borewell** irrigation both clearly beat **Rainfed** on yield
- Yield trended without a clear sustained direction from 2010–2022, peaking in 2018 and dipping lowest in 2015

## Process

1. **Data Understanding** — reviewed structure and meaning of each field
2. **Data Cleaning** — checked for duplicates (none found), blanks (none found), and inconsistent text values across State, Crop Name, Season, Irrigation Type, Soil Type (none found)
3. **Data Transformation** — added Zone (INDEX/MATCH lookup) and Yield Category (nested IF) columns; validated Yield against Production ÷ Area
4. **Dashboard Development** — built native PivotTables and PivotCharts, added KPI cards, wired up slicers via Report Connections

## How to Use

1. Download `Agricultural_Crop_Yield_Dashboard.xlsx`
2. Open in Excel (2013 or later required for slicers)
3. Go to the **Dashboard** tab
4. Click any slicer value (e.g. a state or season) to filter all charts and KPIs simultaneously
5. Use the clear-filter icon on a slicer to reset

## Tools Used

- Microsoft Excel — PivotTables, PivotCharts, Slicers, Conditional Formatting, INDEX/MATCH, nested IF

## Repository Contents

```
├── Agricultural_Crop_Yield.csv              # Raw source dataset
├── Agricultural_Crop_Yield_Dashboard.xlsx   # Final Excel workbook
└── README.md
```

## License

This project uses a synthetic/sample agricultural dataset for educational and portfolio purposes.
