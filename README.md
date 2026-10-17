# Logistics SLA & Delivery Performance Dashboard

An interactive dashboard for analyzing last-mile delivery performance and SLA compliance using the public LaDe dataset.

## Overview

This project explores delivery operations to identify potential bottlenecks, understand delay patterns, and support data-driven decision-making.

## Key Features

- Interactive KPI cards for delivery performance
- Pickup and Delivery SLA analysis
- City-level performance comparison
- Time-window and peak-hour analysis
- Delay pattern heatmaps
- Analysis of delivery distance, batching, and delivery sequence
- Interactive filters and CSV export
- Standalone HTML dashboard

## Technology Stack

- Python
- Pandas
- Plotly
- HTML
- CSS
- JavaScript

## Dataset

The project uses the public LaDe (Large-scale Last-mile Delivery) dataset.

Dataset repository: https://github.com/wenhaomin/LaDe

## Methodology

The analysis includes data validation, timestamp processing, operational duration calculations, SLA classification, and aggregation by city and time window.

SLA compliance is defined as:

- SLA Met: Actual duration is less than or equal to the SLA threshold.
- SLA Violated: Actual duration exceeds the SLA threshold.

Pickup and Delivery performance are evaluated separately.

## Running the Dashboard

The dashboard is generated as an HTML file that can be opened in a modern web browser.

Install the required Python dependencies and run the project's Python script using the input datasets and output arguments specified in the source code.

## Limitations

- The analysis is based on historical public data from China.
- Results depend on the selected SLA thresholds and data-cleaning rules.
- Observed associations do not necessarily imply causation.
- This project is an independent analytical demonstration, not a production monitoring system.

## Objective

To demonstrate how data processing, KPI design, and interactive visualization can transform raw logistics data into useful insights for operational analysis.

