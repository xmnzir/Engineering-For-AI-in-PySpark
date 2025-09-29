# Engineering-For-AI-in-PySpark
A PySpark-based data pipeline for cleaning, enriching, and summarising NYC Taxi trip data. The project processes raw taxi trip records, joins them with NYC zones, computes profitability metrics, and ranks zones by trip activity and performance, while also benchmarking execution times across dataset sizes.
NYC Taxi Trips Analysis Pipeline



📖 Overview

This project implements a distributed data pipeline using PySpark to process the NYC Taxi Trips dataset. It demonstrates key steps in big data processing:

Data Cleaning – Removing invalid trips and outliers.

Feature Engineering – Enriching trip data with zone information and profitability metrics.

Zone Summarisation – Aggregating results per zone and ranking zones based on key performance indicators.

Performance Measurement – Recording execution times across datasets of different sizes and formats.

📂 Inputs


NYC Taxi Trips dataset – Contains records of trips with fields such as:

Distance,
Number of passengers,
Origin zone,
Destination zone,
Total cost (fare charged to customer),
NYC Zones dataset – Contains metadata about NYC zones (used to join with trip data).




🛠️ Development Notes

Implemented entirely with pyspark.sql API.

Uses vectorised operations where possible for performance.

Custom UDFs are applied when required for feature engineering.

Execution time measured via Spark actions (collect, take).

Initial pipeline developed for small ("S") dataset, then scaled for larger datasets.


🚀 How to Run

Load datasets into Spark.

Implement tasks using the provided function skeletons.

Run the final pipeline (already assembled at the end of the notebook).

View execution times in the Spark output logs.


📊 Output

Cleaned and enriched trip dataset.

Per-zone summary statistics.

Top 10 zone rankings by:

Trip volume,
Profitability,
Passenger count,
Execution time benchmarks.
