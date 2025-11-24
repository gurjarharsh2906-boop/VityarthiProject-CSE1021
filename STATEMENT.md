# Statement --- Electricity Bill Estimator

**Electricity Bill Estimator** is a small, user-friendly command-line
tool to help household users estimate monthly electricity consumption
and costs. The program models home appliances by their wattage and
average daily usage, computes per-appliance and total monthly kWh
consumption, and provides a monetary estimate using a configurable rate
per kWh. The tool also supports saving/loading appliance data and
exporting a simple text report.

## Purpose and motivation
Many users lack visibility into which appliances contribute most to
their electricity bills. This project aims to provide an easy way to
track appliance-level consumption, identify top energy users, and give
actionable suggestions to reduce costs---all without requiring
specialized hardware.

## Key features
-   Add, remove, and list appliances (name, wattage, hours/day).
-   Calculate monthly kWh per appliance and total monthly consumption.
-   Estimate monthly bill using a configurable rate per kWh.
-   Show per-appliance percentage contributions sorted by consumption.
-   Save and load appliance lists to `appliances.json`.
-   Export a human-readable report (plain text) containing the summary
    and suggestions.

## Files
-   `electricity_bill_estimator.py` --- main CLI program (located at
    `/mnt/data/electricity_bill_estimator.py`).
-   `appliances.json` --- default data file used to persist appliance
    entries (created at runtime when you save data).

## Usage (quick)
1.  Run the script with Python 3:
    ``` bash
    python3 /mnt/data/electricity_bill_estimator.py
    ```
2.  Use the interactive menu to add appliances, view summaries, save
    data, or export a report.

3.  When exporting a report you will be prompted for an output filename
    (default `report.txt`) and the electricity rate per kWh.

## Design notes
-   Consumption is calculated assuming a 30-day month (constant
    `DAYS_IN_MONTH = 30`).
-   kWh calculation per appliance:
    `(watt * hours_per_day * DAYS_IN_MONTH) / 1000`.
-   Data is stored in JSON format with one object per appliance:
    `{ "name": "Fridge", "watt": 150.0, "hours_per_day": 24.0 }`.

## Extensibility ideas
-   Add support for tiered/variable electricity tariffs and time-of-use
    pricing.
-   Provide a graphical UI or a web front-end for easier use.
-   Add import/export in CSV and generate nicer PDF/Markdown reports.
-   Include monthly history tracking and visualization of consumption
    trends.

## Developer
Submitted By: **Harsh Gurjar** (25BCE11195)
