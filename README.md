# VityarthiProject-CSE1021
# Electricity Bill Estimator

*A Python-based Command Line Utility for Computing Monthly Electricity
Consumption, Generating Reports, and Analyzing Appliance-wise Energy
Usage.*

 ## Project Overview

The **Electricity Bill Estimator** is a Python CLI tool designed to help
users estimate their monthly electricity bill. Users can add appliances,
define wattage and usage hours, and the program calculates total kWh,
estimated bill, appliance-wise breakdown, and exports reports.

## Key Features

-   Add / Remove appliances\
-   Accurate monthly kWh calculation\
-   Bill estimation using custom rate\
-   Percentage-based consumption breakdown\
-   JSON-based data persistence\
-   Exportable detailed report

## Architecture & Design

### Appliance Class

-   Holds name, wattage, and daily usage\
-   Computes monthly kWh\
    \### Estimator Class
-   Manages appliances\
-   Calculates totals and bill\
-   Saves/loads JSON\
-   Exports report

## How It Works

Monthly kWh formula:

    kWh = (Watt × Hours × 30) / 1000

## Installation

    git clone https://github.com/YOUR-USERNAME/YOUR-REPO.git
    cd YOUR-REPO
    python electricity_bill_estimator.py

## Usage Guide

Menu-driven system allowing users to add, list, remove appliances,
estimate bills, and export reports.

## Sample Input/Output

Example bill estimation:

    Total monthly consumption: 45.00 kWh
    Estimated bill: ₹360.00

## File Structure

    .
    ├── electricity_bill_estimator.py
    ├── appliances.json
    └── README.md

## Data Storage Format

Stored in `appliances.json`:

``` json
[
  {"name": "Fan", "watt": 75, "hours_per_day": 8}
]
```

## Future Enhancements

-   GUI version\
-   Graphical reports\
-   Cloud syncing\
-   Energy-saving recommendations

## Author

**Harsh Gurjar**\
Roll Number: 25BCE11195\
Date: 23 Nov 2025
