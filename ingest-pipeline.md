# Ingest Pipeline

The ingest pipeline moves data from the field to our public data server.

---

## 1. Steps

```mermaid
flowchart TD
    A[WGMS Data] --> B[Retrieve via API]
    B --> C[CSV Files]
    C --> D[Convert to NetCDF]
    D --> E[Generate datasets.xml]
    E --> F[Reload in ERDDAP]

