# Puskesmas Distribution Analysis in Jakarta, Indonesia

## Project Overview

This project explores the distribution and data quality of public community health centers (*Pusat Kesehatan Masyarakat* or Puskesmas) across Jakarta, Indonesia, using publicly available data from the Jakarta Provincial Government's open data portal.

The analysis focuses on regional distribution, geographic coordinates, and the completeness and consistency of facility contact information. The objective is to demonstrate how a relatively simple government dataset can be transformed into structured findings using exploratory data analysis (EDA).

## Objectives

This project aims to:

- Examine the distribution of recorded Puskesmas facilities across Jakarta's administrative regions.
- Identify potential data quality issues, including duplicate records, missing values, and inconsistent contact information.
- Explore the geographic distribution of facilities using longitude and latitude coordinates.
- Identify additional data requirements for a more comprehensive assessment of primary healthcare accessibility.

## Dataset

**Source:** Satu Data Jakarta — Jakarta Provincial Government

**Dataset:** [Healthcare Facilities — Community Health Centers (Puskesmas)](https://ws.jakarta.go.id/gateway/DataPortalSatuDataJakarta/1.0/satudata?kategori=dataset&tipe=detail&url=data-fasilitas-kesehatan-pusat-kesehatan-masyarakat-puskesmas)

**Recorded data period:** 2025

The provided dataset contains 44 records and 10 columns covering facility identification, administrative location, contact information, website information, and geographic coordinates.

Key variables include:

| Variable | Description |
|---|---|
| `id_puskesmas` | Facility identifier |
| `nama_puskesmas` | Name of the health center |
| `wilayah_puskesmas` | Administrative region |
| `alamat_puskesmas` | Facility address |
| `no_telepon` | Contact telephone number |
| `email` | Contact email address |
| `website_puskesmas` | Website information |
| `longitude_puskesmas` | Geographic longitude |
| `latitude_puskesmas` | Geographic latitude |
| `periode_data` | Data reporting period |

The unit of analysis is the facility record as provided by the source. The exact classification of each facility should be confirmed against the source metadata.

## Research Questions

1. How are recorded Puskesmas facilities distributed across Jakarta's administrative regions?
2. Which regions have the highest and lowest numbers of recorded facilities?
3. Are there potential data quality issues in facility identifiers, coordinates, and contact information?
4. How can geographic coordinates be used to explore the spatial distribution of facilities?
5. What additional data are required to assess whether healthcare facilities are distributed in line with population needs?

## Tools and Technologies

- **Python** — Data analysis
- **Pandas** — Data manipulation and cleaning
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Google Colab** — Cloud-based analysis environment

## Methodology

### 1. Data Loading and Inspection

Load the source file into Python and inspect its dimensions, column names, data types, and basic structure.

### 2. Data Quality Assessment

Assess data completeness and consistency by checking:

- Missing values across relevant columns.
- Duplicate records and facility identifiers.
- Duplicate facility names requiring verification.
- Numeric data types and coordinate plausibility.
- Basic email formatting and website URL consistency.

Formatting checks are used as preliminary indicators and do not establish whether contact information is active or accessible.

### 3. Data Cleaning

Standardize text fields, remove unnecessary whitespace, convert numeric fields to appropriate data types, and create validation flags for coordinates and contact information.

The original data should be retained separately so that cleaning decisions remain transparent and reproducible.

### 4. Exploratory Data Analysis

Aggregate facility records by administrative region and calculate each region's share of the total recorded facilities.

Use descriptive statistics and visualizations to examine regional differences and explore geographic coordinates.

### 5. Data Visualization

Create visualizations to communicate the findings, including:

- A bar chart showing recorded facilities by administrative region.
- A coordinate scatter plot showing the geographic distribution of facilities.
- Summary tables highlighting data quality issues.
- Contact information quality summaries.

### 6. Interpretation and Recommendations

Interpret the results within the limits of the available data. Identify further datasets needed to assess healthcare accessibility, such as population counts, facility capacity, healthcare personnel, and travel time.

## Preliminary Findings

Based on the initial examination of the provided file:

- The dataset contains 44 facility records for the recorded 2025 period.
- The initial regional aggregation shows 10 records each for East Jakarta and South Jakarta, 8 each for Central Jakarta and West Jakarta, 6 for North Jakarta, and 2 for the Thousand Islands Regency.
- Geographic coordinates provide a basis for exploring facility locations.
- Contact information requires validation beyond simple completeness checks or formatting rules.

These results describe the records in the provided dataset. They should not be interpreted as evidence that one region has better or worse healthcare access than another.

## Limitations

This analysis has several limitations:

- The dataset represents a single recorded period and does not support time-series analysis.
- Facility counts alone do not measure healthcare accessibility, service quality, or service capacity.
- The number of residents served by each facility cannot be determined without compatible population data.
- Geographic coordinates do not directly measure travel time or actual service coverage.
- Contact formatting checks cannot confirm whether an email address or website is operational.
- The classification and coverage of the listed facilities should be verified against the official source metadata.

## Potential Next Steps

Future analysis could be expanded by integrating:

1. Population data by district or subdistrict.
2. Administrative boundary data for geographic mapping.
3. Healthcare personnel and service capacity indicators.
4. Road networks or estimated travel times to facilities.

These additions could support a more meaningful assessment of population-to-facility ratios and geographic accessibility.

## Repository Structure

```text
puskesmas-distribution-analysis/
├── README.md
├── Analisis_Puskesmas_DKI_Jakarta.ipynb
├── data/
│   └── README.md
├── analysis/
│   └── data_dictionary.md
├── dashboard/
│   └── dashboard_preview.png
└── insights/
    └── key_findings.md
```

The structure above is a suggested organization for the project. Include only files and folders that actually exist in the repository.

## Author

**Andra Anwar**

Data Analytics Portfolio Project

