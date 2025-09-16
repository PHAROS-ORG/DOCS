# Utility Specifications: PHAROS

**Document ID:** PHAROS-DOC-UTILITY_SPECS
**Version:** 0.0.1
**Status:** Draft
**Author:** Alexandros P. Liaskos
**Last Updated:** 16/9/2025

## Revision History

| Version | Date      | Author                  | Summary of Changes           |
| ------- | --------- | ----------------------- | ---------------------------- |
| 0.0.1   | 16/9/2025 | Alexandros P. Liaskos   | Initial draft of the document. |

## Introduction

This document provides a detailed specification for each utility developed for the PHAROS project. Utilities are defined as tools, scripts, or other software assets that support project development, management, or governance, but are not part of the core scientific analysis suite delivered to the target audience.

The naming convention for Utility IDs is defined in `PHAROS-DOC-CONVENTIONS`.

## Governance & Management Utilities

This domain includes internal tools designed to support project management, enforce standards, and facilitate project governance.

### DocGen:

-   **Utility ID:** `PHAROS-UTIL-GOV-DocGen-CLI-PY`
-   **Status:** `DEV-ALPHA`
-   **Type:** CLI Application
-   **Language:** Python
-   **Description:** A command-line utility that generates standardized .docx project documents from a Python-based content template. It ensures all official documentation adheres to the PHAROS formatting conventions, promoting consistency and reducing manual effort.
-   **Dependencies:** `python-docx` library.