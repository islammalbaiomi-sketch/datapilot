# DataPilot V1 — Data Operations Workspace

Open `index.html` in Chrome or Edge. No server or installation needed.

Features: CSV and XLSX import (first worksheet), trim whitespace, remove duplicate rows by selected key, missing-value rules, US-format slash date normalization, numeric normalization, original/cleaned preview, undo preview, CSV export, and offline XLSX export with two worksheets (Cleaned Data and Audit Report).

Quick test:
1. Import `sample_messy_data.csv`.
2. Select duplicate key `order_id`, leave cleaning rules on, click Apply & preview.
3. Verify one duplicate removed, dates standardized, numeric values normalized.
4. Export Excel + audit, open in Microsoft Excel, check both sheets.
5. Choose Remove rows with blanks and re-apply, then Restore original.

Notes: All data stays in the browser session; no server upload. Maximum 30,000 rows / 80 columns for responsive previews. Only first 100 rows shown in preview, but all cleaned rows exported. XLSX import uses browser ZIP decompression and supports typical XLSX worksheet cell types, but advanced formulas, formatting, merged cells and Excel date serial conversion are not preserved. CSV parser supports quoted commas and line breaks. Date parsing is ISO or US mm/dd/yyyy; unrecognized values are retained and counted. This is a portfolio-grade local data utility, not a production ETL pipeline.
