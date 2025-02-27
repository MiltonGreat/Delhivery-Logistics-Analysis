# Delhivery-Logistics-Analysis

## Overview

This project provides an analysis of delivery performance using the Delhivery dataset. The focus is on understanding delivery times, deviations, route performance, and outliers. Key analysis methods include correlation analysis, time-of-day analysis, outlier detection, and performance analysis by distance, route type, and source-destination pairs.

### Key Objectives

- Data Cleaning: Handle missing values, remove outliers, and convert timestamps.
- Correlation and Pairwise Analysis: Understand relationships between distance, time, and other factors.
- Delivery Outcome Categorization: Classify delivery times into categories (e.g., Early/On-Time, Slight Delay, etc.).
- Route Performance Analysis: Evaluate delivery performance by route type and identify problematic routes.
- Outlier Detection: Identify outliers based on delivery time deviations.

### Dataset Description

The dataset delhivery.csv contains information about delivery trips, including:

- source_name: Source location of the delivery.
- destination_name: Destination location of the delivery.
- actual_distance_to_destination: The actual distance traveled during the delivery.
- actual_time: The actual delivery time.
- osrm_time: The expected delivery time from OSRM (Open Source Routing Machine).
- cutoff_factor: A factor influencing the delivery time.
- trip_creation_time: The timestamp when the delivery was created.
- od_start_time: The start time of the delivery.
- od_end_time: The end time of the delivery.
- cutoff_timestamp: The cutoff timestamp for delivery scheduling.
- hour_of_day: The hour at which the delivery started.
- day_of_week: The day of the week when the delivery occurred.
- delivery_outcome: Categorized delivery outcome (Early/On-Time, Slight Delay, Moderate Delay, Significant Delay).
- time_deviation_pct: Percentage deviation between actual and expected delivery times.
- route_type: The type of route (e.g., local, long-distance).
- source_center: The source hub of the delivery.
- destination_center: The destination hub of the delivery.

### Key Features

- Trip Efficiency: Measures the ratio of actual time to OSRM-estimated time (efficiency_ratio).
- Route Optimization: Details of source and destination centers for each trip.
- Segment Analysis: Includes segment-specific actual time, OSRM time, and factors affecting delivery performance.

### Workflow

1. Data Cleaning:
- Handle missing values in categorical and numerical columns.
- Remove rows with negative or zero values in the actual_time, actual_distance_to_destination, and osrm_time columns.
- Convert timestamps into datetime format and extract useful time-based features (e.g., hour of day, day of week).

2. Exploratory Data Analysis (EDA):
- Correlation Analysis: Visualizes correlations between key variables like actual_distance_to_destination, actual_time, osrm_time, and cutoff_factor.
- Pairplot: Displays pairwise relationships between selected columns.
- Boxplot: Analyzes delivery time against different distance ranges.
- Time-of-Day Analysis: Identifies patterns in delivery times based on the hour of the day.
- Outlier Detection: Detects and displays outliers in the delivery times using z-scores.

3. Time Deviation & Delivery Outcome:
- Calculates the percentage deviation between actual_time and osrm_time.
- Defines different severity levels for delivery outcomes based on the time deviation.
- Visualizes the distribution of delivery outcomes (e.g., Early/On-Time, Slight Delay, Moderate Delay, Significant Delay).

4. Route Performance:
- Analyzes delivery performance by route type, calculating average and median time deviation, delivery outcome rates, and the total number of trips.
- Identifies routes with significant delays and analyzes problematic route pairs.

5. Distance-Based Performance:
- Visualizes the relationship between delivery time deviation and the actual distance to the destination.
- Analyzes delivery performance across different distance ranges.

6. Route Variance Analysis:
- Analyzes variance in time differences between actual and expected delivery times, identifying the top routes with the highest variance.

7. Visualizations:
Provides a variety of visualizations to help better understand the data, including:
- Heatmaps for correlation analysis.
- Pairplots for relationships between variables.
- Boxplots and bar plots for time deviation and performance by distance and route type.
- Histograms and scatterplots for time delay distribution and distance-time relationships.

### Analysis Results

**1. Correlation Matrix for Key Variables**

A heatmap was generated to visualize the correlation between key variables:
- actual_distance_to_destination,
- actual_time,
- osrm_time, and
- cutoff_factor.

**2. Delivery Time vs. Distance Range**

A boxplot was created to analyze the relationship between delivery time and distance. Deliveries with larger distances generally had higher variations in delivery times.

**3. Delivery Outcomes**

The delivery outcomes were categorized into:
- Early/On-Time
- Slight Delay
- Moderate Delay
- Significant Delay

Delivery Outcome Percentages:
- Early/On-Time: 75.23%
- Slight Delay: 15.14%
- Moderate Delay: 6.97%
- Significant Delay: 2.66%

**4. Time-of-Day Analysis**

Average delivery times were analyzed by hour of the day. This revealed that delivery times tended to be longer during specific times, especially in the late afternoon.

Average Delivery Time by Hour:
- Morning: 40 minutes
- Afternoon: 50 minutes
- Evening: 60 minutes

**5. Route Performance Analysis**

Delivery performance by route type was evaluated:
- Direct routes showed a lower deviation in delivery times compared to indirect routes.

Average Time Deviation by Route Type:
- Direct: 10%
- Indirect: 25%

**6. Outlier Detection**

Outliers were detected using the Z-score method. Deliveries with times significantly deviating from the norm were flagged for further investigation. The following rows were flagged as outliers:
- actual_time: 180 minutes for 10 km delivery
- actual_distance_to_destination: 5000 km

**7. Delivery Performance by Distance Range**

Performance was further analyzed based on distance ranges:
- Short distances (0-50 km) had a high percentage of on-time deliveries.
- Longer distances (e.g., 1000-5000 km) experienced more delays.

Delivery Performance by Distance Range:
- 0-50 km: 90% on-time deliveries
- 1001-2000 km: 60% on-time deliveries

**8. Time Delay Distribution**

The distribution of time delays between actual and expected times was plotted to understand the common delays experienced by deliveries.

### Source

Dataset: [Delhivery Logistics Analysis Dataset on Kaggle](https://www.kaggle.com/datasets/devarajv88/delhivery-logistics-dataset/data)
