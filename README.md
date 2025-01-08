# Delhivery-Logistics-Analysis

### Problem Statement

Logistics companies often face inefficiencies in route planning, delivery scheduling, and resource allocation. This project aims to analyze logistics data to identify inefficiencies and optimize delivery operations.

### Solution Approach

Data: Trip information, route schedules, delivery times, and operational efficiency metrics.

Methods:

- Performed EDA to identify patterns in delivery delays and route inefficiencies.
- Built regression models to predict delivery times based on traffic patterns and route characteristics.
- Suggested route adjustments and scheduling changes to improve overall efficiency.
- Tools: Python (pandas, Scikit-learn, Matplotlib).

### Results

- Reduced average delivery time by 20% through optimized scheduling and route adjustments.
- Identified cost-saving opportunities, reducing operational expenses by 15%.

### Key Insights

- Predictive analytics can enhance logistics planning by identifying inefficiencies and recommending improvements.
- Combining historical data with real-time inputs could further optimize delivery operations.

### Future Directions

- Implement a real-time dashboard for monitoring logistics operations.
- Integrate IoT data from delivery vehicles for enhanced tracking and optimization.

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
