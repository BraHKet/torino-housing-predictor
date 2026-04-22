# Turin Housing Predictor

![Turin Housing](https://via.placeholder.com/1200x300?text=Turin+Housing+Predictor)

Real estate market intelligence and investment opportunity analysis for Turin's housing market.

**Created by:** Lorenzo Rizzo

---

## Table of Contents

1. [Project Overview](#project-overview)
2. [Research Question](#research-question)
3. [Project Workflow](#project-workflow)
4. [Data Structure](#data-structure)
5. [Interactive Dashboards](#interactive-dashboards)
   - [Market Overview by District](#market-overview-by-district)
   - [Student Housing Investment Opportunities](#student-housing-investment-opportunities)
6. [Video Tutorials](#video-tutorials)
7. [Dashboard Features](#dashboard-features)
8. [How to Use the Dashboards](#how-to-use-the-dashboards)
9. [Technologies Used](#technologies-used)
10. [Next Steps](#next-steps)

---

## Project Overview

This project provides comprehensive market intelligence for Turin's real estate sector through interactive data visualization and exploratory analysis. The work transforms raw property data into actionable insights for investors, buyers, and real estate professionals.

By analyzing over 1,300 property listings, the project reveals market patterns, pricing dynamics, and investment opportunities across Turin's neighborhoods.

---

## Research Question

**How can we understand Turin's real estate market through exploratory analysis of property features and geographic location?**

This question drives our analysis to uncover market patterns, identify investment opportunities, and provide data-driven insights for decision-making in the city's housing sector.

---

## Project Workflow

### 1. Data Collection

Real property data was collected from Immobiliare.it using a web scraper (Google Web Scraper extension).

**Dataset Specifications:**
- Total listings: 1,388 property records
- Data collection method: Automated web scraping across multiple pages
- Time to collect: Approximately 1 hour of scraping
- Data freshness: March 2026

**Data Includes:**
- Property types (apartments, bilocales, studios)
- Location details (district, address, street number)
- Physical characteristics (size, rooms, bathrooms)
- Energy efficiency ratings and consumption data
- Listing metadata (update dates, direct links, descriptions)
- Image URLs and property descriptions
- Amenities information (elevators, balconies, etc.)

---

### 2. Data Cleaning & Preprocessing

The raw dataset contained numerous inconsistencies and redundancies that required systematic cleaning and standardization.

All the steps used in this process are described in detail in the notebook of the repository [Jupyter Notebook](https://github.com/BraHKet/torino-housing-predictor/blob/main/notebooks/Main_Notebook_Immobiliare.ipynb).
<br>
<br>


<p align="center">
  <img src="https://i.imgur.com/qpvStMX.png" width="45%"/>
  <img src="https://i.imgur.com/1BzhrSa.png" width="42.2%"/>
</p>

---

### 3. Exploratory Data Analysis

The cleaned dataset serves as the foundation for comprehensive exploratory analysis, revealing market patterns and relationships.

**Analysis Components:**

- Price distribution analysis across all districts
- Correlation between property size and market pricing
- Impact assessment of property characteristics (rooms, bathrooms, amenities)
- Temporal trends in listing updates and market activity
- Energy efficiency class distribution and implications
- Geographic clustering patterns and neighborhood analysis
- Property type segmentation and market representation
- District-level market positioning and competitiveness

---

### 4. Interactive Dashboards

Multiple interactive dashboards were developed using Tableau to present findings in an accessible and actionable format for different stakeholder needs.

---

## Data Structure

This is the final cleaned file used to create the Dashboards in Tableau [Final Clean CSV for Tableau](https://github.com/BraHKet/torino-housing-predictor/blob/main/notebooks/data/TABLEAU/file_TABLEAU_V6(quartieri_standard).csv)
<br><br>

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `energy_class` | String | Energy efficiency rating (A-G) |
| `tipo_immobile` | String | Property type classification |
| `via` | String | Street name |
| `civico` | String | Street number |
| `quartiere` | String | District/neighborhood name (raw) |
| `citta` | String | City name |
| `lat` | Float | Latitude coordinate |
| `lon` | Float | Longitude coordinate |
| `dist_metro_m` | Float | Distance to nearest metro station (meters) |
| `minuti_metro` | Float | Walking time to nearest metro (minutes) |
| `dist_tram_m` | Float | Distance to nearest tram stop (meters) |
| `minuti_tram` | Float | Walking time to nearest tram (minutes) |
| `dist_bus_m` | Float | Distance to nearest bus stop (meters) |
| `minuti_bus` | Float | Walking time to nearest bus stop (minutes) |
| `distanza_ospedale_m` | Float | Distance to nearest hospital (meters) |
| `ospedale_piu_vicino` | String | Nearest hospital name |
| `tempo_piedi_ospedale_min` | Float | Walking time to nearest hospital (minutes) |
| `distanza_universita_m` | Float | Distance to nearest university (meters) |
| `universita_piu_vicino` | String | Nearest university name |
| `tempo_piedi_universita_min` | Float | Walking time to nearest university (minutes) |
| `distanza_stazione_m` | Float | Distance to nearest train station (meters) |
| `stazione_piu_vicino` | String | Nearest train station name |
| `tempo_piedi_stazione_min` | Float | Walking time to nearest train station (minutes) |
| `distanza_asilo_m` | Float | Distance to nearest nursery school (meters) |
| `asilo_piu_vicino` | String | Nearest nursery school name |
| `tempo_piedi_asilo_min` | Float | Walking time to nearest nursery school (minutes) |
| `distanza_scuola_elementare_m` | Float | Distance to nearest primary school (meters) |
| `scuola_elementare_piu_vicino` | String | Nearest primary school name |
| `tempo_piedi_scuola_elementare_min` | Float | Walking time to nearest primary school (minutes) |
| `distanza_scuola_media_m` | Float | Distance to nearest middle school (meters) |
| `scuola_media_piu_vicino` | String | Nearest middle school name |
| `tempo_piedi_scuola_media_min` | Float | Walking time to nearest middle school (minutes) |
| `distanza_scuola_superiore_m` | Float | Distance to nearest high school (meters) |
| `scuola_superiore_piu_vicino` | String | Nearest high school name |
| `tempo_piedi_scuola_superiore_min` | Float | Walking time to nearest high school (minutes) |
| `data_aggiornamento` | String | Last listing update timestamp |
| `numero_locali` | Integer | Number of rooms |
| `size_m2` | Float | Property size in square meters |
| `Bathrooms` | Integer | Number of bathrooms |
| `floor` | String | Floor number |
| `price` | Float | Property price in EUR |
| `Balcony` | String | Balcony presence |
| `coefficient` | Float | Price adjustment coefficient |
| `elevator_final` | String | Elevator availability |
| `esposizione` | String | Property sun exposure |
| `infissi_vetro` | String | Window glass type |
| `infissi_materiale` | String | Window frame material |
| `luxury_score` | Float | Computed luxury score |
| `quartiere_pulito` | String | Standardised district/neighborhood name |

---

## Interactive Dashboards

---

### Market Overview by District

Comprehensive analysis of the Turin housing market across all neighborhoods.

![Market Overview Dashboard](https://via.placeholder.com/1000x600?text=Market+Overview+Dashboard)

#### Analysis Metrics:

**Property Inventory**
Number of listings

**Price per Square Meter**
Cost efficiency comparison

**Price by Property Type**
Pricing segmentation for apartments, bilocales, and other property categories

**Average Property Size**
Mean square meters by district for comparative analysis

**Average Price by District**
Overall pricing rankings and market positioning

#### Dashboard Features:

- Interactive filtering by district, price range, and property type
- Trend identification across districts

#### Ideal For:

- General market research and analysis

[Tableau Dashboard Link](https://public.tableau.com/views/PrezziimmobiliareTorino/PrezziImmobiliareTorino?:language=it-IT&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

### Student Housing Investment Opportunities

Specialized analysis for real estate investors targeting the student rental market in Turin.

![Student Housing Investment Dashboard](https://via.placeholder.com/1000x600?text=Student+Housing+Investment+Dashboard)

#### Investment Scoring Framework:

The dashboard combines two key metrics to identify the best investment opportunities in Turin's student housing market.

**Investment Score**

A comprehensive metric evaluating multiple critical factors:

- **Property Price** - Acquisition cost and market value positioning
- **Location Quality** - Neighborhood desirability and urban development
- **Public Transportation** - Proximity to transit hubs and accessibility
- **University Proximity** - Distance to major educational institutions
- **Neighborhood Quality** - Overall area amenities, safety, and infrastructure

**Gross ROI**

Expected rental yield calculation based on:

- Property acquisition cost
- Average student rental rates in the district
- Market demand and expected occupancy rates
- Operating and maintenance cost estimations

#### Combined Opportunity Score

A unified metric combining both Investment Score and Gross ROI to rank properties by overall investment potential for student housing.

#### Dashboard Features:

- **Comprehensive Property Ranking** - Individual assessment of every listing
- **District Heat Maps** - Identify high-opportunity neighborhoods at a glance
- **ROI Projections** - Estimated returns based on historical market data
- **Risk Assessment** - Market volatility and demand stability analysis
- **Location Analysis** - University proximity and transportation accessibility
- **Comparative Filtering** - Customize analysis by budget, location, and ROI targets
- **House-by-House Opportunity Assessment** - Detailed individual property evaluation

#### Ideal For:

- Real estate investors exploring Turin's student housing sector
- Property managers seeking high-yield rental opportunities
- Portfolio diversification and investment planning
- Student housing market specialists and institutional investors

[Access the Investment Dashboard](INSERT_DASHBOARD_2_LINK)

---

## Video Tutorials

### Student Housing Investment Dashboard Tutorial

[![Student Housing Investment Dashboard](https://img.youtube.com/vi/YOUR_YOUTUBE_VIDEO_ID/maxresdefault.jpg)](https://www.youtube.com/watch?v=YOUR_YOUTUBE_VIDEO_ID)

**Duration:** XX minutes

**Tutorial Contents:**

- Dashboard interface navigation and layout overview
- Interactive filtering by investment criteria and preferences
- Interpreting the Investment Score methodology
- Analyzing ROI projections and expected returns
- Identifying top investment opportunities in your target areas
- Comparing different districts and neighborhoods
- Exporting analysis data for further research and presentations

[Watch on YouTube](https://www.youtube.com/watch?v=YOUR_YOUTUBE_VIDEO_ID)

---

## Dashboard Features

### General Capabilities

All dashboards include the following interactive features:

**Filtering & Customization**
- Filter by district, price range, property type, size
- Dynamic updates reflecting selected criteria
- Multiple simultaneous filter combinations

**Data Visualization**
- Interactive charts and graphs
- Heat maps for geographic analysis
- Comparative views and trend visualization
- Exportable visualizations for presentations

**Data Export**
- Download filtered data to CSV or Excel
- Export charts and visualizations
- Generate custom reports for stakeholders

**Navigation & Interaction**
- Drill-down capabilities for detailed analysis
- Hover tooltips with detailed information
- Cross-filtering between visualization elements
- Responsive design for desktop and tablet viewing

---

## How to Use the Dashboards

### Market Overview Dashboard

1. Access the dashboard using the provided link
2. Browse all neighborhoods using the interactive district selector
3. Compare property types and pricing across areas
4. Analyze average metrics by neighborhood
5. Identify pricing patterns and market leaders
6. Export insights for market research reports

**Use Cases:**
- Identify neighborhoods with best price-per-square-meter
- Compare average prices across districts
- Understand property type distribution
- Support market entry decisions with data

### Investment Opportunity Dashboard

1. Open the specialized investment analysis dashboard
2. Define your investment criteria using available filters:
   - Budget range and price limits
   - Target location/district preferences
   - Expected ROI threshold
3. Review the Investment Score for each property
4. Analyze gross ROI projections and market opportunity
5. Consult the video tutorial for detailed workflow guidance
6. Export property lists and analysis for due diligence

**Use Cases:**
- Identify best value properties in target locations
- Compare investment opportunities across districts
- Assess ROI potential for student housing
- Screen properties based on multiple criteria
- Build investment opportunity shortlists

### General Navigation Tips

- Use filters to customize views based on your specific criteria
- Hover over data points for detailed information and tooltips
- Leverage drill-down functionality to explore neighborhood details
- Share dashboards with stakeholders for collaborative analysis
- Export insights and reports for external presentations and meetings
- Refresh dashboards periodically to see updated market data

---

## Technologies Used

**Data Collection:**
- Web Scraper (Google Browser Extension)

**Data Processing & Analysis:**
- Python programming language
- Pandas for data manipulation and analysis
- NumPy for numerical computing
- Regular expressions for data parsing and cleaning

**Data Storage:**
- Excel spreadsheets for initial data management
- SQL databases for structured data storage and queries

**Data Visualization:**
- Tableau for interactive dashboards and business intelligence

---

## Next Steps

**Short Term:**
- Gather user feedback on dashboard usability
- Refine filtering and visualization options
- Optimize dashboard performance

**Medium Term:**
- Implement real-time data updates from Immobiliare.it
- Expand analysis to include rental market data
- Add historical price trend analysis
- Develop automated alert system for investment opportunities

**Long Term:**
- Expand to other Italian real estate markets
- Integrate additional data sources (census, transportation, education)
- Develop comprehensive market comparison tools
- Build investor community platform

---

## Documentation

**Project Repository:**
[github.com/BraHKet/torino-housing-predictor](https://github.com/BraHKet/torino-housing-predictor)

**Data Analysis Notebook:**
[View the complete exploratory analysis notebook](https://github.com/BraHKet/torino-housing-predictor/blob/main/notebooks/Main_Notebook_Immobiliare.ipynb)

---

This project demonstrates a complete end-to-end data analysis workflow, from raw data acquisition through exploratory analysis and interactive visualization. The Tableau dashboards provide actionable market intelligence for real estate professionals, investors, and anyone seeking to understand Turin's dynamic housing market.

The focus on interactive exploration and investment opportunity assessment enables stakeholders to make data-driven decisions with confidence.

**Created by:** Lorenzo Rizzo
