# Technical Evidence and Verification

## Verification Method

The PBIX was treated as a read-only package. Its internal `Report/Layout` metadata was decoded to identify report pages, visual containers, visual types, titles and referenced fields. The `Connections` metadata was inspected only to classify the data-lineage type; private workspace, dataset and report identifiers are intentionally not reproduced here.

## File Integrity

- Intended repository path: `dashboard/Academic_Timetable_Dashboard.pbix`
- Size: `841,750` bytes
- SHA-256: `9f72cbf9bffae0b8f66ca8b9d0328da78e2ebea031c491e9f5760d967c457e10`

## Report Inventory

| Page | Count | Visual types |
|---|---:|---|
| MAIN | 4 | shape × 2; image × 2 |
| TIMETABLE | 13 | slicer × 5; card × 3; textbox × 2; shape × 1; image × 1; actionButton × 1 |
| ANALYSIS | 10 | slicer × 3; donutChart × 1; clusteredColumnChart × 1; treemap × 1; barChart × 1; table × 1; textbox × 1; actionButton × 1 |

**Total:** 3 pages and 27 visual containers.

## Verified Titles on the Analysis Page

- Department Distribution
- Theory vs Practical Hours
- Labs Offered
- Faculty Strength per Division
- Class Incharge Overview
- Filter by Year
- Filter by Department
- Filter by School

## Referenced Model Objects

- Model table: `MPSTME,SPTM,TEXTILE`
- Fields: `Total Faculty Mem.`, `Year`, `Department`, `SEM/Div`, `Total Labs`, `Total Subject`, `Link`, `Program`, `SCHOOL`, `LR.No`, `Pra.(Hr, Both Batch)`, `Theory (Hrs)`, `Labs Name`, `Class Incharge`

## Data-Lineage Evidence

The PBIX contains a remote-artifact connection to a Power BI Service semantic model. The report layout is present locally, while live values and refresh behaviour may depend on access to the original workspace and dataset.

## Interpretation Boundary

This evidence proves the presence and structure of the report. It does not prove that the connected dataset is current, complete or publicly distributable. Numerical claims should be made only after opening the report with authorised data access and documenting the observation date and filter context.
