<h1 align="center">Turin Housing Investments</h1>
<br>

<p align="center">
  <img src="https://i.imgur.com/DaUNWta.png" width="25%"/>
</p>
<br><br>
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

# Market Overview by District

Comprehensive analysis of the Turin housing market across all neighborhoods.
<br><br>

<p align="center">
  <img src="https://i.imgur.com/2mo3nMQ.png" width="80%"/>
</p>

<br><br>
#### Analysis Metrics:

- **Property Inventory**
Number of listings

- **Price per Square Meter**
Cost efficiency comparison

- **Price by Property Type**
Pricing segmentation for apartments, bilocales, and other property categories

- **Average Property Size**
Mean square meters by district for comparative analysis

- **Average Price by District**
Overall pricing rankings and market positioning

#### Dashboard Features:

- Interactive filtering by district, price range, and property type
- Trend identification across districts

[Tableau Dashboard Link](https://public.tableau.com/views/PrezziimmobiliareTorino/PrezziImmobiliareTorino?:language=it-IT&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

---

# Student Housing Investment Opportunities

Specialized analysis for real estate investors targeting the student rental market in Turin.

<br><br>

<p align="center">
  <img src="https://i.imgur.com/82tpJrG.png" width="80%"/>
</p>

<br><br>

#### Investment Scoring Framework:

The dashboard combines two key metrics to identify the best investment opportunities in Turin's student housing market.

**Investment Score**

A comprehensive metric evaluating multiple critical factors:

- **Property Price** - Acquisition cost and market value positioning
- **Locals** - Number of rentable rooms in the property
- **Public Transportation** - Proximity to transit hubs and accessibility
- **University Proximity** - Distance to major educational institutions
- **Property Quality** - Overall quality of property

**Gross ROI**

Expected rental yield calculation based on:

- Property acquisition cost
- Average student rental rates in Turin 
- Market demand and expected occupancy rates
- Operating and maintenance cost estimations

#### Combined Opportunity Score

A unified metric combining both Investment Score and Gross ROI to rank properties by overall investment potential for student housing.

#### Dashboard Features:

- **Comprehensive Property Ranking** - Individual assessment of every listing
- **District Heat Maps** - Identify high-opportunity neighborhoods at a glance
- **ROI Projections** - Estimated returns
- **Location Analysis** - University proximity and transportation accessibility
- **House-by-House Opportunity Assessment** - Detailed individual property evaluation

#### Ideal For:

- Real estate investors exploring Turin's student housing sector
- Property managers seeking high-yield rental opportunities
- Student housing market specialists and institutional investors

[Access the Investment Dashboard](https://public.tableau.com/views/IndagineinvestimentiimmobiliariTorino/DashboardInvestimenti?:language=it-IT&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

## Video Tutorials

### Student Housing Investment Dashboard Tutorial

<p align="center">
  <a href="https://www.youtube.com/watch?v=qeyRn1bU6_U&t=99s">
    <img src="https://img.youtube.com/vi/qeyRn1bU6_U/0.jpg" width="70%"/>
  </a>
</p>

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

**Data Visualization:**
- Tableau for interactive dashboards and business intelligence

---

## Next Steps

**Short Term:**
- Careful calibration of score weights
- Gather user feedback on dashboard usability
- Refine filtering and visualization options
- Optimize dashboard performance

**Medium Term:**
- Implement real-time data updates
- Expand analysis to include rental market data
- Add historical price trend analysis
- Develop automated alert system for investment opportunities

**Long Term:**
- Expand to other Italian real estate markets
- Integrate additional data sources (census, transportation, education)
- Develop comprehensive market comparison tools
- Build investor community platform
  

