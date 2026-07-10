# Academic Timetable & Institutional Workload Dashboard | Power BI

> A three-page reporting experience that moves from navigation, to timetable lookup, to institutional workload analysis.

[![Power BI](https://img.shields.io/badge/Microsoft-Power%20BI-F2C811?logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![Portfolio Project](https://img.shields.io/badge/Project-Portfolio-blue)](https://github.com/sagar-grv/academic-timetable-dashboard-powerbi)
[![Verification](https://img.shields.io/badge/Report-Verified-success)](docs/technical-evidence.md)

## Why This Project Exists

Academic schedules are usually stored as wide tables or static documents. That makes a simple question—*Which programme, division, laboratory or faculty group is affected?*—slow to answer. This report turns the timetable into an interactive lookup experience and then connects it to a management-level workload view.

## Analytical Story

The report follows a **lookup-to-management** sequence:

1. **Orient the user** — the `MAIN` page provides a clear entry point and visual navigation.
2. **Find the exact timetable context** — the `TIMETABLE` page combines school, department, programme, year and semester/division filters with KPI cards and a timetable link.
3. **Explain institutional workload** — the `ANALYSIS` page compares department distribution, theory versus practical hours, laboratories, faculty strength and class-in-charge responsibility.

This sequence supports two audiences without forcing them into the same view: students or staff who need a schedule, and academic administrators who need operational context.

## Verified Project Evidence

The supplied PBIX was inspected in read-only mode by parsing its internal `Report/Layout` and connection metadata. No dashboard values were invented or inferred from screenshots.

| Evidence | Verified value |
|---|---:|
| Power BI pages | **3** |
| Visual containers | **27** |
| Dashboard file size | **841,750 bytes** |
| SHA-256 | `9f72cbf9bffae0b8f66ca8b9d0328da78e2ebea031c491e9f5760d967c457e10` |
| Data connection | Power BI Service remote semantic model |

### Page and Visual Inventory

| Page | Visuals | Verified visual types |
|---|---:|---|
| MAIN | 4 | `shape` × 2, `image` × 2 |
| TIMETABLE | 13 | `slicer` × 5, `card` × 3, `textbox` × 2, `shape` × 1, `image` × 1, `actionButton` × 1 |
| ANALYSIS | 10 | `slicer` × 3, `donutChart` × 1, `clusteredColumnChart` × 1, `treemap` × 1, `barChart` × 1, `table` × 1, `textbox` × 1, `actionButton` × 1 |

Full proof is available in [`docs/technical-evidence.md`](docs/technical-evidence.md) and [`evidence/report-inventory.json`](evidence/report-inventory.json).

## Verified Analytical Components

- Department Distribution
- Theory vs Practical Hours
- Labs Offered
- Faculty Strength per Division
- Class Incharge Overview
- Filters for Year, Department and School
- Additional timetable filters for programme and semester/division

## Referenced Data Fields

`SCHOOL`, `Department`, `Program`, `Year`, `SEM/Div`, `LR.No`, `Theory (Hrs)`, `Pra.(Hr, Both Batch)`, `Total Labs`, `Labs Name`, `Total Subject`, `Total Faculty Mem.`, `Class Incharge`, `Link`

## Data Lineage and Privacy Boundary

The PBIX is connected to a remote Power BI Service semantic model. Refreshing or exploring live values may require access to the original workspace and dataset. The file also contains embedded institutional images/logos; these should be reviewed for publication permission before screenshots are posted publicly.

For that reason, this repository proves the report structure, visual inventory, field references and file integrity, but does not publish unsupported numerical findings or private connection identifiers.

## Skills Demonstrated

Power BI • education analytics • interactive filtering • KPI design • report navigation • workload analysis • data storytelling • responsible data publication

## Repository Structure

```text
.
├── dashboard/          # Power BI artefact when uploaded
├── docs/               # Story, evidence and publication notes
├── evidence/           # Machine-readable inventory and checksum
├── screenshots/        # Exported report images after privacy review
├── LINKEDIN_POST.md
├── LICENSE
└── README.md
```

## How to Review

1. Review the story and evidence documents in this repository.
2. Download `dashboard/Academic_Timetable_Dashboard.pbix` when present.
3. Open it in Microsoft Power BI Desktop.
4. Move through `MAIN` → `TIMETABLE` → `ANALYSIS`.
5. Reconnect to the semantic model only with authorised access.
6. Verify the downloaded file against `evidence/SHA256SUMS.txt`.

## Evidence Limitations

GitHub cannot render PBIX files. Structural metadata and cryptographic hashes therefore serve as reproducible proof until privacy-reviewed screenshots are added. The repository deliberately separates **what is verified in the artefact** from **what would require live data access**.

## Author

**Sagar Gurav**  
AI/ML and Data Analytics Student
