Logistics SLA & Delivery Performance Dashboard
An interactive analytics dashboard for exploring last-mile delivery performance, SLA compliance, and operational bottlenecks using the public LaDe (Large-scale Last-mile Delivery) dataset.
The project transforms raw logistics data into actionable insights, helping identify when and where delivery delays occur and which operational factors may be associated with SLA violations.
Project Overview
Last-mile delivery performance depends on multiple factors, including pickup delays, delivery distance, order batching, courier workload, and time of day.
This project provides an interactive dashboard to investigate these factors, compare Pickup and Delivery SLA performance, and identify potential areas for operational improvement.
Dataset: LaDe — Large-scale Last-mile Delivery Dataset
Key Features
Interactive KPI Cards: Monitor delivery volume, average processing times, and SLA compliance.
Pickup & Delivery SLA Analysis: Examine pickup and delivery performance separately.
Dynamic Filters: Explore results by city, day, two-hour time window, and SLA threshold.
Temporal Analysis: Identify peak hours and time periods associated with higher SLA violation rates.
City-Level Comparison: Compare logistics performance across cities.
Time Heatmap: Discover recurring delay patterns across days and time windows.
Geographical Visualization: Explore potential problem areas using a schematic map.
Operational Factor Analysis: Investigate relationships between SLA performance and factors such as acceptance time, delivery distance, batch size, and delivery sequence.
Time-Window Playback: Explore how performance changes throughout the day.
CSV Export: Export filtered results for further analysis.
Technology Stack
Python — Data processing and dashboard generation
Pandas — Data cleaning and transformation
Plotly — Interactive charts and visualizations
HTML, CSS, JavaScript — Dashboard interface and interactions
Git & GitHub — Version control and project sharing
Data Source
The project uses the publicly available LaDe dataset, which contains large-scale last-mile delivery records collected in China between May and October 2022.
The dataset provides information about delivery operations, including timing, courier assignments, order characteristics, and pickup and delivery activities.
Dataset repository: https://github.com/wenhaomin/LaDe
Data Preparation
The data preparation process includes:
Loading and validating the source data.
Cleaning records and handling invalid or incomplete observations.
Preparing timestamps and deriving time-based features.
Calculating operational durations and SLA indicators.
Preparing separate datasets for Pickup and Delivery analysis.
Aggregating metrics by city, day, and time window.
In the analyzed dataset, 1,003,534 input records were reduced to 974,610 retained records, with 28,924 records excluded during data preparation. These figures describe the processed dataset used in this project.
SLA Definition
SLA compliance is evaluated by comparing an observed operational duration against a defined time threshold.
For an order with a valid duration:
SLA Met: Actual duration ≤ SLA threshold
SLA Violated: Actual duration > SLA threshold
The SLA threshold depends on the operational stage and the assumptions used in the analysis. In particular, the Delivery SLA threshold is configurable, so results should be interpreted in the context of the selected definition.
Pickup and Delivery SLA rates are calculated separately to avoid combining different operational stages into a single metric.
Key Analytical Questions
This dashboard is designed to answer questions such as:
Which cities and time windows have the highest SLA violation rates?
How does delivery performance change throughout the day?
Are delays concentrated during specific days or peak hours?
How are batch size, delivery sequence, and distance associated with delivery performance?
Which operational segments may deserve further investigation?
Does the pattern of Pickup SLA violations differ from Delivery SLA violations?
How to Run
The dashboard is generated as a standalone HTML file that can be opened in a web browser.
If you have the project source files and the required input datasets, run the following command from your project directory:
python lade_sla_visual_refresh.py delivery.csv pickup.csv output
Replace delivery.csv and pickup.csv with the paths to your delivery and pickup datasets, and replace output with the desired output location or filename according to the script's configuration.
Open the generated HTML file in a modern web browser to explore the dashboard.
Note: The command assumes that the Python dependencies are installed and that the input files follow the expected dataset structure. Check the source script for any additional requirements.
Important Notes & Limitations
This project is an independent analysis of public LaDe data. It does not represent actual operational performance or internal systems of SnappBox or any other delivery company.
The dataset reflects historical logistics operations in China; findings should not be generalized to other markets without further validation.
The geographical visualization is schematic and should not be interpreted as an exact operational map.
Correlation between operational variables does not establish causation.
SLA results depend on the selected thresholds, data-cleaning rules, and assumptions.
The dashboard is intended for exploratory analysis and operational decision support, not as a production monitoring system.
Project Objective
The goal of this project is to demonstrate how raw logistics data can be transformed into an interactive analytical tool for monitoring SLA performance, identifying operational bottlenecks, and supporting data-driven decision-making.
The project combines data preparation, KPI design, exploratory data analysis, and interactive visualization in a single dashboard.

Author: ArefeSharifi
Dataset: LaDe — GitHub Repository
