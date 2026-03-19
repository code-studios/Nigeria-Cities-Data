# 🇳🇬 Nigeria Cities Data
### State-Level Geographic and Population Inventory

> **File:** `nigeria_cities_data.xlsx` + `state_json_files/`  
> **Created:** 2026-03-18 · 11:47:31 UTC

---

## Overview

A comprehensive inventory of cities, towns, and settlements across **35 Nigerian states** and the **Federal Capital Territory (FCT)**. Each record represents a named settlement with its geographic coordinates, elevation, and population estimate.

The dataset is available in two formats:

| # | Format | Description |
|---|--------|-------------|
| 1 | **Excel Workbook** | Single consolidated `.xlsx` file with one sheet per state and a master `Summary` sheet |
| 2 | **JSON Files** | Individual `.json` files per state, stored in the `state_json_files/` subfolder |

---

## File Structure

```
nigeria_cities_data.xlsx
│
├── Sheet: Summary          ← one row per state with aggregated statistics
└── Sheet: [State Name]     ← full city records per state (auto-filter enabled)

state_json_files/
└── *.json                  ← 35 individual files, one per state (root-level arrays)
```

---

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `name` | `string` | Settlement / city name |
| `what` | `string` | Feature type (e.g. `"city"`) |
| `region` | `string` | Nigerian state or FCT name |
| `country` | `string` | Country (`Nigeria`) |
| `lat` | `float` | Latitude in decimal degrees (WGS84) |
| `long` | `float` | Longitude in decimal degrees (WGS84) |
| `elev ft` | `int` | Elevation above sea level (feet) |
| `pop est` | `int` | Estimated population (`0` = unpopulated or data unavailable) |

---

## Coverage

| Attribute | Value |
|-----------|-------|
| **Geographic scope** | 35 Nigerian states + FCT |
| **Unit type** | Settlement-level point data |
| **Total records** | 28,874 |
| **Largest file** | Borno — 1,438 records |
| **Smallest file** | Ekiti — 223 records |

<details>
<summary><strong>View all included states (35 + FCT)</strong></summary>

<br>

| | | | |
|---|---|---|---|
| Abia | Adamawa | Akwa Ibom | Anambra |
| Bauchi | Bayelsa | Benue | Borno |
| Cross River | Delta | Ebonyi | Edo |
| Ekiti | Enugu | **Federal Capital Territory** | Gombe |
| Imo | Jigawa | Kaduna | Kano |
| Katsina | Kebbi | Kogi | Lagos |
| Nasarawa | Niger | Ogun | Ondo |
| Oyo | Plateau | Rivers | Sokoto |
| Taraba | Yobe | Zamfara | |

</details>

> **⚠️ Note:** 2 states are absent from this release — **Kwara** and **Rivers** — as source files were unavailable at the time of compilation.

---

## Intended Use

This dataset is suitable for, but not limited to:

- 📍 Spatial clustering and K-means analysis of Nigerian urban settlement patterns
- 🚦 Transport accessibility and road network modelling
- 📊 Population-weighted spatial analysis
- 🗺️ Base layer for geographic information systems (GIS)
- 🏙️ Urban planning and infrastructure research

---

## Data Source

Open source / GitHub *(exact repository unconfirmed)*.  
Data structure is consistent with **[GeoNames.org](https://www.geonames.org/)** export format.  
Coordinates use the **WGS84** decimal degrees standard.

---

## Privacy & Sensitivity Assessment

| Attribute | Status |
|-----------|--------|
| PII present | ✅ None |
| Sensitive values | ✅ None |
| Aggregation level | Place / settlement *(not individual / household)* |
| Public release | ✅ **SUITABLE** — fully public geographic reference data |

---

## Limitations

- Population estimates may be **outdated** — year of estimate not specified in source data
- Zero values in `pop est` may indicate **missing data** rather than truly uninhabited settlements
- Elevation values are in **feet**, not metres — convert if needed (`ft × 0.3048 = m`)
- **2 states** (Kwara, Rivers) are not included in this release
- Settlement names may include **transliterations** or alternative spellings

---

## Licence

**TRAMSYS LAB** — [https://tramsys-b0cc6.web.app/](https://tramsys-b0cc6.web.app/)

## Maintainer

**Eni Solomon Laughter** — Chang'an University
