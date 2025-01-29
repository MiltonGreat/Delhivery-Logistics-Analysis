# Delhivery-Logistics-Analysis

## Overview

This project focuses on optimizing logistics delivery times and operational costs by analyzing route data from a logistics company. By identifying inefficiencies in trip durations and route allocation, we aim to reduce delivery times, improve route scheduling, and generate cost savings.

### Problem Statement

Logistics companies often face inefficiencies in route planning, delivery scheduling, and resource allocation. This project seeks to address these challenges by analyzing the provided dataset to identify inefficiencies and optimize delivery operations for better performance and cost-efficiency.

### Key Objectives:

1. **Optimize Delivery Time**: The goal is to reduce the average delivery time by 20% through optimized scheduling and route adjustments.
2. **Identify Cost-Saving Opportunities**: The project also focuses on identifying operational improvements that can reduce expenses by 15%.

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

### Solution Approach

#### 1. Data Preprocessing
- Missing values were handled by filling categorical columns with 'Unknown' and dropping rows with critical missing values.
- Essential numerical columns such as actual distance and time were retained for analysis.

#### 2. Data Analysis and Visualization
- Distribution analysis was done for trip durations, actual times, and efficiency ratios.
- Relationships between distance, time, and route type were explored through scatter plots and histograms.

#### 3. Efficiency Analysis
- Efficiency ratios were calculated by comparing actual times to OSRM estimated times.
- Inefficient routes were identified where the efficiency ratio exceeded a defined threshold (2), suggesting potential areas for optimization.

#### 4. Peak Hour Analysis
- The distribution of trips by hour of the day was analyzed to identify peak times and potential for scheduling optimization.

#### 5. Clustering for Route Optimization
- KMeans clustering was applied to route data using actual distance and time to categorize routes into groups for further analysis.
- Optimized route schedules were developed based on clustering results.

### Key Analysis Results

The analysis identified routes with high inefficiency ratios, such as:

- Route: Khambhat_MotvdDPP_D (Gujarat) to Anand_Vaghasi_IP (Gujarat) with an efficiency_ratio of 2.59.
- Route: LowerParel_CP (Maharashtra) to Mumbai_Chndivli_PC (Maharashtra) with an efficiency_ratio of 4.18.
- 
![screenshot-localhost_8888-2025 01 29-11_25_00](https://github.com/user-attachments/assets/0cf389a8-11a3-4d33-86c5-03f197e2dee1)

### Results

#### (1) **Can we reduce average delivery time by 20%?**
- **Current Average Delivery Time**: 416.93 minutes
- **Optimized Average Delivery Time**:  333.54 minutes (A reduction of 20%)

#### (2) **Can we identify cost-saving opportunities?**
- **Estimated Cost Savings from Optimization**: 14,146,282.07 units

These results demonstrate that through route optimization, significant reductions in both delivery time and operational expenses can be achieved.

### Future Directions

- The current analysis assumes the feasibility of the optimized route schedules in practice.
- Additional real-world factors such as weather conditions, road closures, and traffic patterns could further affect optimization outcomes.

### Source

Dataset: [Delhivery Logistics Analysis Dataset on Kaggle](https://www.kaggle.com/datasets/devarajv88/delhivery-logistics-dataset/data)
