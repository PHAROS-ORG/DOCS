# Project Proposal: PHAROS

**Document ID:** PHAROS-DOC-PROPOSAL
**Version:** 0.0.1
**Status:** Draft
**Author:** Alexandros P. Liaskos
**Prepared For:** Project Collaborators and Reviewers
**Last Updated:** 16/9/2025

## Revision History

| Version | Date      | Author                  | Summary of Changes           |
| ------- | --------- | ----------------------- | ---------------------------- |
| 0.0.1   | 16/9/2025 | Alexandros P. Liaskos   | Initial draft of the document. |

## 1. Executive Summary

The field of Earth Observation faces a significant operational bottleneck: the complex, time-consuming, and often redundant manual effort required to transform raw satellite data into actionable scientific insights. Researchers in hydro-pyro hazard analysis repeatedly build custom, non-standardized workflows, hindering the pace of discovery and collaboration.

**PHAROS (Pyro-Hydro Hazard Analysis for Research with Open-source Sentinel data)** is proposed as a strategic initiative to solve this problem. It will be a suite of modular, open-source software components designed to operationalize and standardize the analysis of Sentinel satellite data for fire-related (Pyro) and water-related (Hydro) hazards.

By codifying validated research methodologies into accessible command-line tools, web applications, libraries, and APIs, PHAROS will directly serve the research community. This proposal outlines the project's vision, scope, technical architecture, and a detailed breakdown of its planned components. 

## 2. Introduction: The Problem

Researchers in environmental science and hazard analysis rely heavily on satellite imagery from programs like the Copernicus Sentinel mission. However, the path from raw data acquisition to validated analysis is fraught with challenges:

*   **High Barrier to Entry:** Processing satellite data requires specialized expertise in remote sensing, data science, and software development.
*   **Redundant Effort:** Research groups across the globe independently develop similar, bespoke scripts for fundamental tasks like data downloading, pre-processing, and calculating spectral indices.
*   **Lack of Standardization:** The absence of common tools leads to variations in methodology, making it difficult to compare or reproduce study results.
*   **Absence of reusable tools:** Promising research methodologies often remain as academic papers or one-off scripts, failing to transition into operational, reusable tools that benefit the wider community.

PHAROS is designed to bridge this gap, creating a foundational, open-source toolkit that empowers researchers to focus on novel scientific questions rather than repetitive data engineering.

## 3. The PHAROS Initiative: Our Solution

### 3.1. Project Goal

To provide a suite of open-source services to accelerate and operationalize satellite-based hydro-pyro hazard analysis for the research community.

### 3.2. Core Principles

*   **Open Source:** All code will be publicly available under permissive licenses to foster collaboration, transparency, and community contribution. The data sources will also be Free and Open-source (FOSS), like the Sentinel satellite imagery products.
*   **Modular:** Components are developed as independent, standalone tools to ensure maximum reusability and flexibility.
*   **Standardized:** The project enforces rigorous internal conventions for documentation, versioning, and development, ensuring a high-quality, consistent user experience. Additionally, the scientific methodologies utilized will be selected by their quality and acceptance by the scientific community.
*   **Researcher-Focused:** The tools are designed to directly codify and automate the complex analysis workflows currently performed manually by our target audience.

### 3.3. Scope

*   **Key Domains:** The project will focus on two critical hazard domains:
    *   **Pyro:** Fire-related hazards.
    *   **Hydro:** Water-related hazards.
*   **Data Source:** The primary data input will be imagery and products from the **Copernicus Sentinel** mission, accessed via the Copernicus Data Space Ecosystem (CDSE).

## 4. Proposed Components

The PHAROS suite is composed of specialized components, each addressing a specific step in the hazard analysis workflow. Some of the proposed ones are listed below:

### 4.1. Data Acquisition

*   **SatAcq (`PHAROS-COMP-DATACQ-SatAcq-CLI-PY`)**
    *   **Description:** A command-line tool for searching and downloading Sentinel satellite imagery via the CDSE.

### 4.2. Pyro Domain Components (Status: `PLAN-PROP`)

*   **BurnSev (`PHAROS-COMP-PYRO-BurnSev-CLI-PY`):** Assesses burn severity by calculating key spectral indices (e.g., dNBR) from pre- and post-fire Sentinel-2 imagery.
*   **SmokeDetect (`PHAROS-COMP-PYRO-SmokeDetect-CLI-PY`):** Detects active fires and smoke plumes using Sentinel-3 thermal data.
*   **BiomassExtract (`PHAROS-COMP-PYRO-BiomassExtract-CLI-PY`):** Estimates vegetation biomass from Sentinel-2 imagery for fuel load assessment.
*   **VegMoisture (`PHAROS-COMP-PYRO-VegMoisture-CLI-PY`):** Estimates vegetation water content from Sentinel-2 data to assess fire risk.
*   **FirePower (`PHAROS-COMP-PYRO-FirePower-CLI-PY`):** Calculates Fire Radiative Power (FRP) from Sentinel-3 data to measure fire intensity.
*   **SmokeTrack (`PHAROS-COMP-PYRO-SmokeTrack-CLI-PY`):** Analyzes smoke plumes from Sentinel-3 to assess air quality impacts.
*   **TempExtract (`PHAROS-COMP-PYRO-TempExtract-CLI-PY`):** Extracts land surface temperature from Sentinel-3 thermal data.

### 4.3. Hydro Domain Components (Status: `PLAN-PROP`)

*   **FloodMap (`PHAROS-COMP-HYDRO-FloodMap-CLI-PY`):** Maps flood extent using Sentinel-1 SAR imagery, ideal for all-weather monitoring.
*   **WaterDepth (`PHAROS-COMP-HYDRO-WaterDepth-CLI-PY`):** Estimates water depth in shallow water bodies using Sentinel-2 optical imagery.
*   **RainEstimate (`PHAROS-COMP-HYDRO-RainEstimate-CLI-PY`):** Estimates precipitation rates from Sentinel-1 SAR data.
*   **EvapTrans (`PHAROS-COMP-HYDRO-EvapTrans-CLI-PY`):** Calculates evapotranspiration for drought analysis using Sentinel-2 imagery.
*   **SlopeStability (`PHAROS-COMP-HYDRO-SlopeStability-CLI-PY`):** Analyzes slope stability for landslide susceptibility mapping.
*   **ErosionRisk (`PHAROS-COMP-HYDRO-ErosionRisk-CLI-PY`):** Maps soil erosion potential using the RUSLE model with Sentinel-2 and DEM data.

## 5. Technical Vision & Architecture

PHAROS will be built on a modern, flexible, and maintainable technical foundation.

*   **Modular Architecture:** Each component will be developed in its own repository within a central PHAROS GitHub Organization. This allows for independent versioning, issue tracking, and development.
*   **Multiple Software Types:** To serve diverse use cases, components will be delivered in various forms:
    *   **`CLI` (Command-Line Interface):** For easy integration into scripts and automated workflows.
    *   **`LIB` (Library):** For programmatic use within researchers' custom Python applications.
    *   **`API` (Web API):** For network-based access and integration into larger systems.
    *   **`WEB` / `SPA` (Web Applications):** For providing user-friendly graphical interfaces for specific workflows.
*   **Primary Technology Stack:** The initial focus for CLI and library components will be **Python**, leveraging its extensive scientific computing ecosystem. Web components will utilize TypeScript, Next.js, and Nest.js.

## 6. Project Governance & Management

To ensure the long-term success and quality of the project, PHAROS has established a clear set of governance conventions (see `PHAROS-DOC-CONVENTIONS`).

*   **Standardized Naming:** All documents and components use a consistent ID system for immediate identification and clarity (e.g., `PHAROS-DOC-CHARTER`, `PHAROS-COMP-PYRO-BurnSev-CLI-PY`).
*   **Semantic Versioning:** Document and component versions will follow the `MAJOR.MINOR.PATCH` standard to clearly communicate the nature of changes.
*   **Lifecycle Management:** All assets have defined status keys (e.g., `Draft`, `Active`, `PLAN-PROP`, `DEV-WIP`) to track their progress from ideation to retirement.
*   **Automated Governance:** The project leverages internal utilities, such as **DocGen (`PHAROS-UTIL-GOV-DocGen-CLI-PY`)**, to automate the creation of standardized documentation, reinforcing our commitment to consistency and quality.

## 7. Benefits and Impact

The successful implementation of PHAROS will provide transformative benefits to the research community:

*   **Accelerates Discovery:** By automating foundational analysis, researchers can achieve results in hours or days, not weeks or months.
*   **Eliminates Redundant Effort:** Provides a common, reliable toolkit, freeing up valuable researcher time for novel science.
*   **Enhances Reproducibility:** Standardized components ensure that analyses are consistent, transparent, and more easily reproduced by peers.
*   **Lowers the Barrier to Entry:** Enables students, junior researchers, and scientists from adjacent fields to effectively utilize complex satellite data.
*   **Fosters an Open-Source Community:** Creates a collaborative ecosystem for developing and sharing state-of-the-art hazard analysis tools.

## 8. Next Steps

We request formal approval of this project proposal. Upon approval, we will proceed with the following actions:

1. Working on the development of the proposed/planned components, as well as advance the list of planned components with new ideas.

We are confident that the PHAROS project will become an invaluable asset to the Earth Observation community, fundamentally improving how we analyze and respond to environmental hazards.