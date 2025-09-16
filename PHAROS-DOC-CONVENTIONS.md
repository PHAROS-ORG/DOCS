# Document Management Conventions: PHAROS

**Document ID:** PHAROS-DOC-CONVENTIONS
**Version:** 0.0.1
**Status:** Draft
**Author:** Alexandros P. Liaskos
**Last Updated:** 16/9/2025

## Introduction

This document establishes the official conventions for creating, versioning, and managing all documentation within the PHAROS project. Adhering to these standards ensures that all project documents are consistent, discoverable, and clear, facilitating effective communication and project governance.

## Document ID Naming Convention

All official project documents must be assigned a unique Document ID following the convention below. This ID provides immediate context about the document's place within the project.

| Key/Part               | Description                                           | Currently Available Values                       |
| ---------------------- | ----------------------------------------------------- | ------------------------------------------------ |
| `[PROJECT_IDENTIFIER]` | The project identifier, static for all documents.     | `PHAROS`                                         |
| `[OBJECT_TYPE]`        | A static key indicating that the ID refers to a document. | `DOC`                                            |
| `[DOCUMENT_NAME]`      | A descriptive, abbreviated name for the document.     | `CHARTER`, `TECHNICAL_VISION`, `COMPONENT_SPECS`, etc. |

## Document Versioning Convention

Document versioning follows the Semantic Versioning (SemVer) format of `MAJOR.MINOR.PATCH`. This system is used to track the evolution of a document and the significance of its changes.

| Version Part | Rule                                                                                                                                              |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **MAJOR**    | Incremented for major, incompatible changes that significantly alter the document's scope or purpose (e.g., a complete rewrite of the Project Charter). A `0` indicates initial development or draft stages. |
| **MINOR**    | Incremented when new information or sections are added in a backward-compatible manner (e.g., adding a new component domain to the specifications). |
| **PATCH**    | Incremented for minor, backward-compatible fixes, such as correcting typographical errors, clarifying language, or fixing formatting.              |

### Lifecycle Stages:

- **Version 0.x.x:** The document is in its initial development phase (`Draft`, `In Review`). The content is subject to frequent and significant changes.
- **Version 1.0.0:** The first official, stable release of the document, considered `Active` and approved.

## Document Status Keys

Each document must be assigned a status key that reflects its current stage in the document lifecycle.

| Status Key | Lifecycle Stage | Description                                                                                                                   |
| ---------- | --------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `Draft`      | Initial         | The document is being created or is undergoing major revisions. It is not yet ready for formal review.                        |
| `In Review`  | Initial         | The document has been completed by the author and is now under review by stakeholders for feedback and approval.              |
| `Active`     | Stable          | The document has been reviewed, approved, and is considered the current, official version for the project.                    |
| `Superseded` | Post-Life       | The document has been replaced by a newer version or a different document. It is retained for historical purposes but is no longer in effect. |
| `Archived`   | Post-Life       | The document is no longer relevant to the project and is retired. It is kept for record-keeping only.                         |

## Revision History

All documents must include a "Revision History" table directly after the header. This table provides a changelog, making it easy to track modifications over time.

| Version | Date      | Author                  | Summary of Changes           |
| ------- | --------- | ----------------------- | ---------------------------- |
| 0.0.1   | 16/9/2025 | Alexandros P. Liaskos   | Initial draft of the document. |

## Document Control

-   **Storage:** All official project documentation will be stored and managed in a dedicated repository within the PHAROS GitHub Organization.
-   **Ownership:** The individual listed as the `Author` in the document header is the primary owner and is responsible for maintaining its content and accuracy.
-   **Approval Process:** A document transitions from `Draft` to `Active` status upon formal approval from the Project Lead or a majority of designated project stakeholders. The review process will be managed via GitHub pull requests or a similar tracked mechanism.