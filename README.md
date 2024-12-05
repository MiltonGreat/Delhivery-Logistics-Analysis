# Delhivery-Logistics-Analysis

### Overview

This project analyzes logistics data provided by Delhivery, a leading logistics and supply chain services company in India. The dataset includes detailed trip information, route schedules, delivery times, and efficiency metrics. The goal is to identify inefficiencies in the logistics network, optimize delivery routes, and provide actionable insights for improving logistics performance.

### Project Goals

##### Exploratory Data Analysis (EDA):
- Analyze trip efficiency, route types, and performance metrics.
- Visualize trends in delivery times and distances.

##### Identify Inefficient Routes:
- Highlight routes with high inefficiency ratios.
- Explore reasons for inefficiencies (e.g., route type, distance, traffic).

##### Optimize Logistics:
- Use clustering and regression analysis to identify patterns.
- Propose actionable recommendations to improve efficiency.

### Dataset Description

The dataset contains information about logistics trips, including:

- Trip Details: route_type, trip_uuid, source_name, destination_name
- Time Metrics: od_start_time, actual_time, osrm_time
- Distance Metrics: actual_distance_to_destination, osrm_distance
- Performance Metrics: efficiency_ratio, segment_factor

### Key Features

- Trip Efficiency: Measures the ratio of actual time to OSRM-estimated time (efficiency_ratio).
- Route Optimization: Details of source and destination centers for each trip.
- Segment Analysis: Includes segment-specific actual time, OSRM time, and factors affecting delivery performance.

#### Visualizations

##### Distribution of Route Types:
- Most common routes: Carting.
- Insights on route performance and inefficiencies.

##### Distance vs. Trip Duration:
- Longer distances tend to correlate with higher inefficiencies.

##### Efficiency Ratio Distribution:
- Highlighted trips with efficiency ratios exceeding a threshold (e.g., 2.5).

### Key Analysis Results

The analysis identified routes with high inefficiency ratios, such as:

- Route: Khambhat_MotvdDPP_D (Gujarat) to Anand_Vaghasi_IP (Gujarat) with an efficiency_ratio of 2.59.
- Route: LowerParel_CP (Maharashtra) to Mumbai_Chndivli_PC (Maharashtra) with an efficiency_ratio of 4.18.

### Source

https://www.kaggle.com/datasets/devarajv88/delhivery-logistics-dataset/data
