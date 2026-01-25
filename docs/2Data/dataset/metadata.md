# Dataset Metadata Standards

This page explains how BNR-CVD datasets and scripts are named, how versions are managed, and how to complete the accompanying `.meta.yaml` metadata file.

---

## Dataset Filename Pattern

Each dataset name identifies what it contains, its privacy level, and the time period covered.

```
BNR-CVD-<CONTENT>-<TIER>-<YYYYMM>-v<VERSION>.dta
```

- `<YYYYMM>` – the **final month of data coverage** (not the creation date).  
- `<VERSION>` – uses semantic versioning (`v1.0`, `v2.0`, etc.).  

---

## Components and Allowed Values

| Component | Meaning | Allowed values | Description / When to use |
|---|---|---|---|
| `BNR-CVD` | Project and disease area | fixed | Always present. |
| `<CONTENT>` | Dataset type | `INDIV`, `AGGR`, `LINK` | **INDIV:** one row per event; full analytic dataset. <br> **AGGR:** aggregated or summarised dataset; no individual rows. <br> **LINK:** minimal internal linkage file used to connect records across years/sources (never distributed). |
| `<TIER>` | Privacy level | `FULL`, `DEID`, `ANON` | **FULL:** contains identifiers or quasi-identifiers; internal use only. <br> **DEID:** de-identified; no direct identifiers; used for approved research and reporting. <br> **ANON:** anonymised or aggregated; suitable for public release. |
| `<YYYYMM>` | Data coverage end month | e.g. `202312`, `202401` | Dataset includes data up to this month. |
| `v<VERSION>` | Release version. | `v1.0`, `v2.0` | Each number change represents a change to a dataset that has been previously released. |

---

## Examples

- Cumulative individual dataset (Dec 2023):  
  `BNR-CVD-INDIV-DEID-202312-v1.0.dta`
- Public aggregated dataset (mid-2026):  
  `BNR-CVD-AGGR-ANON-202606-v2.0.dta`
- Internal linkage file:  
  `BNR-CVD-LINK-FULL-202312-v1.0.dta`

---

## Versioning Rules

| Level | Example | When used |
|---|---|---|
| **Major** | `v2.0` | Structural change (variables, definitions, inclusion criteria). |
| **Minor** | `v1.1` | Added verified cases, late updates, or small analytic fixes. |
| **Patch** | `v1.0.1` | Cosmetic (labels only). |

> **Why both `<YYYYMM>` and version?**  
> The `YYYYMM` shows *coverage* (the period the data reach), while the `vX.X` tracks *updates* or corrections within that same period. This combination lets you know both **how far the data go** and **which iteration** of that coverage you’re using.

---

## Dataset Metadata

Each `.dta` file has a companion `.meta.yaml` file. This YAML file records the dataset’s identity and creation details, separate from the data itself.

A YAML file (short for “YAML Ain’t Markup Language”) is a simple, human-readable text format used to store structured data — like settings, metadata, or configurations — in a clear and consistent way. It’s important because it allows both humans and computers to easily read, share, and reuse information across systems, ensuring data documentation remains transparent, reproducible, and machine-actionable.

**Purpose:**

1. Records coverage, tier, and version for reproducibility.  
2. Enables automation — scripts can read metadata for reporting.  
3. Provides a simple audit trail and supports FAIR principles.  

---

### Metadata information contained in each YAML file

| Field | Description | Example |
|---|---|---|
| `title` | Plain-language title of dataset | `"BNR-CVD Individual Dataset (De-identified)"` |
| `identifier` | Filename stem (matches dataset) | `"BNR-CVD-INDIV-DEID-202312-v1.0"` |
| `description` | Short summary of what’s in the dataset | `"Confirmed cardiovascular events; cumulative through Dec 2023."` |
| `created` | Creation date (YYYY-MM-DD) | `"2025-01-15"` |
| `version` | Dataset version | `"1.0"` |
| `creator` | Dataset created by | `"Name of analyst"` |
| `coverage.temporal` | Period covered | `"2009-01 to 2023-12"` |
| `coverage.spatial` | Geographic coverage | `"Barbados"` |
| `data_tier` | Privacy tier (`FULL`, `DEID`, or `ANON`) | `"DEID"` |
| `format` | File format | `"Stata version 18 (.dta)"` |
| `source` | Original data sources | `"Hospital admissions (QEH) and death registration"` |
| `related_files` | Supporting `.do` or linkage files | `["bnrcvd-2009-2023-prep2-v1.0.do"]` |
| `contact` | Contact for access or clarification | `"ian.hambleton@uwi.edu"` |

---

### Example `.meta.yaml`

```yaml
title: "BNR-CVD Individual Dataset (De-identified)"
identifier: "BNR-CVD-INDIV-DEID-202312-v1.0"
description: "Confirmed cardiovascular events; cumulative through Dec 2023."
created: "2025-01-15"
version: "1.0"
coverage:
  temporal: "2009-01 to 2023-12"
  spatial: "Barbados"
data_tier: "DEID"
format: "Stata 18"
source: "Hospital admissions (QEH) and national death registration"
related_files:
  - "bnrcvd-2009-2023-prep2-v1.0.do"
  - "BNR-CVD-LINK-FULL-202312-v1.0.dta"
contact: "bnr@cavehill.uwi.edu"
```

---

### Creating YAML Files in Stata

Use the `bnryaml.ado` utility to generate metadata automatically from within Stata. Jump to [downloads](../../5Downloads/index.md) for more information.

Example `bnryaml` code:
```stata
local out "BNR-CVD-INDIV-DEID-202312-v1.0.dta"
bnryaml using "`out'", ///
    title("BNR-CVD Individual Dataset (De-identified)") ///
    version("1.0") ///
    created("2025-01-15") ///
    tier("DEID") ///
    temporal("2009-01 to 2023-12") ///
    spatial("Barbados") ///
    description("Confirmed cardiovascular events; cumulative through Dec 2023.") ///
    registry("CVD") ///
    content("INDIV") ///
    creator("Ian Hambleton, GA-CDRC") ///
    language("en") ///
    format("Stata 18") ///
    rights("Restricted – internal analytical use only") ///
    source("Hospital admissions (QEH) and death registration") ///
    contact("ian.hambleton@uwi.edu")
```

This creates a companion `.yml` file beside the dataset, ensuring consistent documentation for every data release.

<br/>
