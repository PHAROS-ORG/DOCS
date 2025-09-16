# Component Specifications: PHAROS

**Document ID:** PHAROS-DOC-COMPONENT_SPECS
**Version:** 0.0.1
**Status:** Draft
**Author:** Alexandros P. Liaskos
**Last Updated:** 16/9/2025

## Revision History

| Version | Date      | Author                  | Summary of Changes           |
| ------- | --------- | ----------------------- | ---------------------------- |
| 0.0.1   | 16/9/2025 | Alexandros P. Liaskos   | Initial draft of the document. |

## Introduction

This document provides a detailed specification for each currently proposed component within the PHAROS project suite.

## Component ID Naming Convention

| Key/Part               | Description                                                  | Currently Available Values                         |
| ---------------------- | ------------------------------------------------------------ | -------------------------------------------------- |
| `[PROJECT_IDENTIFIER]` | The project identifier, static for all components.           | `PHAROS`                                           |
| `[OBJECT_TYPE]`        | A static key indicating that the ID refers to a component.   | `COMP`                                             |
| `[DOMAIN]`             | The functional domain the component belongs to.              | `DATACQ`, `PYRO`, `HYDRO`                            |
| `[COMPONENT_NAME]`     | The specific, abbreviated name of the component.             | `SatAcq`, `BurnSev`, `FloodMap`, `WaterDepth`, …     |
| `[SOFTWARE_TYPE]`      | The type of the component software.                          | `CLI`, `LIB`, `API`, `WEB`, `SPA`                      |
| `[LANGUAGE]`           | A two-letter abbreviation for the primary programming language. | `PY`, `JS`, `TS`                                     |

## Component Status Keys

| Status Key   | Lifecycle Stage         | Description                                                                      |
| ------------ | ----------------------- | -------------------------------------------------------------------------------- |
| `PLAN-PROP`  | Planning & Initial      | **Proposed:** The component is a suggested idea, awaiting approval.              |
| `PLAN-PLND`  | Planning & Initial      | **Planned:** The component is approved and scheduled for development.            |
| `PLAN-DRFT`  | Planning & Initial      | **Draft:** Initial specifications or requirements are being written.             |
| `DEV-WIP`    | Active Development      | **Work In Progress:** The component is actively being coded.                     |
| `DEV-REVW`   | Active Development      | **In Review:** The component is undergoing code or functional review.            |
| `DEV-TEST`   | Active Development      | **Testing:** The component is with Quality Assurance (QA) for validation.        |
| `DEV-ALPHA`  | Active Development      | **Alpha:** A pre-release version is available for internal testing.              |
| `DEV-BETA`   | Active Development      | **Beta:** A pre-release version is available for limited external testing.       |
| `STABLE-ACTV`| Completed & Stable      | **Active:** The component is stable, tested, and ready for production use.       |
| `STABLE-RLSD`| Completed & Stable      | **Released:** The component has been officially deployed in a formal project release. |
| `EOL-DEPR`   | Post-Life (End of Life) | **Deprecated:** Superseded by a new component but kept for backward compatibility. |
| `EOL-RETD`   | Post-Life (End of Life) | **Retired:** The component is no longer supported, maintained, or in use.        |

## Data Acquisition Components

### SatAcq:

-   **Component ID:** `PHAROS-COMP-DATACQ-SatAcq-CLI-PY`
-   **Status:** `DEV-ALPHA`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** A tool for searching and downloading satellite imagery from Sentinel via the Copernicus Data Space Ecosystem (CDSE) OData API.

## Pyro Domain Components

### BurnSev:

-   **Component ID:** `PHAROS-COMP-PYRO-BurnSev-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** A Python-based tool for burn severity assessment using pre-fire and post-fire Sentinel-2 imagery. Calculates spectral indices (NBR, dNBR, RdNBR) and produces standardized burn severity classifications.

### SmokeDetect:

-   **Component ID:** `PHAROS-COMP-PYRO-SmokeDetect-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Detects active fires and smoke using Sentinel-3 SLSTR thermal data, implementing hotspot and thermal anomaly algorithms.

### BiomassExtract:

-   **Component ID:** `PHAROS-COMP-PYRO-BiomassExtract-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Estimates vegetation biomass from Sentinel-2 imagery for fuel load assessment.

### VegMoisture:

-   **Component ID:** `PHAROS-COMP-PYRO-VegMoisture-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Estimates vegetation water content from Sentinel-2 imagery for fire risk assessment.

### FirePower:

-   **Component ID:** `PHAROS-COMP-PYRO-FirePower-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Calculates Fire Radiative Power (FRP) from Sentinel-3 SLSTR for fire intensity assessment.

### SmokeTrack:

-   **Component ID:** `PHAROS-COMP-PYRO-SmokeTrack-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Analyzes smoke plumes from Sentinel-3 SLSTR to assess air quality impact.

### TempExtract:

-   **Component ID:** `PHAROS-COMP-PYRO-TempExtract-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Extracts land surface temperature from Sentinel-3 SLSTR.

## Hydro Domain Components

### FloodMap:

-   **Component ID:** `PHAROS-COMP-HYDRO-FloodMap-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Maps flood extent using Sentinel-1 SAR imagery through backscatter analysis and change detection.

### WaterDepth:

-   **Component ID:** `PHAROS-COMP-HYDRO-FloodMap-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Estimates water depth in shallow water bodies using Sentinel-2 optical imagery.

### RainEstimate:

-   **Component ID:** `PHAROS-COMP-HYDRO-RainEstimate-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Estimates precipitation rates from Sentinel-1 SAR imagery.

### EvapTrans:

-   **Component ID:** `PHAROS-COMP-HYDRO-EvapTrans-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Calculates evapotranspiration using SEBAL/METRIC algorithms for drought analysis and Sentinel-2 imagery.

### SlopeStability:

-   **Component ID:** `PHAROS-COMP-HYDRO-SlopeStability-CLI-PY`
-   **Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Analyzes slope stability for landslide susceptibility mapping using DEMs and Sentinel-2 imagery.

### ErosionRisk:

-   **Component ID:** `PHAROS-COMP-HYDRO-ErosionRisk-CLI-PY`
**Status:** `PLAN-PROP`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** Maps soil erosion potential using the RUSLE model, DEMs and Sentinel-2 imagery.
