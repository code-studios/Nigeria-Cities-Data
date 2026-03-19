================================================================
  DATASET DESCRIPTION
  File    : nigeria_cities_data.xlsx  +  state_json_files/
  Created : 2026-03-18  11:47:31
================================================================

TITLE
  Nigeria Cities Data — State-Level Geographic and
  Population Inventory

OVERVIEW
  This dataset is a comprehensive inventory of cities, towns,
  and settlements across 35 Nigerian states and the Federal
  Capital Territory (FCT). Each record represents a named
  settlement with its geographic coordinates, elevation, and
  population estimate.

  The data is provided in two formats:
    1. A single consolidated Excel workbook with one sheet
       per state and a master Summary sheet.
    2. Individual JSON files per state, preserved in the
       state_json_files/ subfolder.

FILE FORMAT
  Primary   : nigeria_cities_data.xlsx
               - Sheet "Summary" : one row per state with
                 aggregated statistics
               - Sheets [state name] : full city records
                 per state (auto-filter enabled)
  Secondary : state_json_files/ — 35 individual .json files,
               one per state, root-level arrays

SCHEMA
  Field      Type    Description
  ---------  ------  ----------------------------------------
  name       string  Settlement / city name
  what       string  Feature type (e.g. "city")
  region     string  Nigerian state or FCT name
  country    string  Country (Nigeria)
  lat        float   Latitude in decimal degrees (WGS84)
  long       float   Longitude in decimal degrees (WGS84)
  elev ft    int     Elevation above sea level (feet)
  pop est    int     Estimated population (0 = unpopulated
                     or data unavailable)

COVERAGE
  Geographic   : 35 Nigerian states + FCT
  Unit type    : Settlement-level point data
  Total records: 28,874
  Largest file : Borno (1,438 records)
  Smallest file: Ekiti (223 records)

  States included:
    Abia
    Adamawa
    Akwa Ibom
    Anambra
    Bauchi
    Bayelsa
    Benue
    Borno
    Cross River
    Delta
    Ebonyi
    Edo
    Ekiti
    Enugu
    Federal Capital Territory
    Gombe
    Imo
    Jigawa
    Kaduna
    Kano
    Katsina
    Kebbi
    Kogi
    Lagos
    Nasarawa
    Niger
    Ogun
    Ondo
    Oyo
    Plateau
    Rivers
    Sokoto
    Taraba
    Yobe
    Zamfara

  Note: 2 states not present in this release —
  Kwara and Rivers (files unavailable at time of compilation).

PRIVACY & SENSITIVITY ASSESSMENT
  PII present      : No
  Sensitive values : None — settlement-level geographic data
  Aggregation level: Place/settlement (not individual/household)
  Public release   : SUITABLE — fully public geographic
                     reference data

DATA SOURCE
  Open source / GitHub (exact repository unconfirmed).
  Data structure consistent with GeoNames.org export format.
  Coordinates use WGS84 decimal degrees.

INTENDED USE
  - Spatial clustering and K-means analysis of Nigerian
    urban settlement patterns
  - Transport accessibility and road network modelling
  - Population-weighted spatial analysis
  - Base layer for geographic information systems (GIS)
  - Urban planning and infrastructure research

LIMITATIONS
  - Population estimates may be outdated; year of estimate
    not specified in source data
  - Zero values in "pop est" may indicate missing data
    rather than truly uninhabited settlements
  - Elevation values in feet (not metres); convert if needed
  - 2 states (Kwara, Rivers) not included in this release
  - Settlement names may include transliterations or
    alternative spellings

LICENCE
  TRAMSYS LAB - https://tramsys-b0cc6.web.app/

CONTACT / MAINTAINER
  Eni Solomon Laughter - Chang'an University

================================================================
  END OF DESCRIPTION
================================================================
