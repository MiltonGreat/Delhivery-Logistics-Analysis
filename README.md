# Delhivery Logistics Analysis

## Overview

**In logistics, on-time delivery isn't just a metric—it's the foundation of customer trust and operational predictability.** This project conducts a comprehensive performance audit of a major logistics network, treating delivery data as the vital signs of supply chain health. We move beyond descriptive analytics to diagnose systemic vulnerabilities, identify failure patterns, and provide the intelligence needed to build a more resilient and predictable delivery ecosystem. While 75% of deliveries arrive on-time, the 25% that don't represent critical vulnerabilities in your routing strategy and operational execution.

### Logistics Problem: The Hidden Costs of Delivery Variance

A logistics network optimized only for average performance hides critical risks in its variance. Key vulnerabilities identified include:

- Predictability Risk: Indirect routes show 2.5x higher time deviation than direct routes, creating unreliable customer experiences.
- Capacity Planning Risk: 60-minute evening deliveries vs. 40-minute morning deliveries indicate systemic bottlenecks during peak hours.
- Network Integrity Risk: Extreme outliers (e.g., 180-minute deliveries for 10km routes) signal fundamental process breakdowns or data quality issues.

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

### Approach: The Logistics Network Diagnostic Framework

We applied a multi-layered governance framework to audit the delivery network's resilience and predictability.

1. **The Network Resilience Stress Test**

Route Vulnerability Analysis: We identified that indirect routes (25% deviation) aren't just slower—they're fundamentally unpredictable. This variance represents a critical weakness in service reliability that customers experience directly.

Temporal Bottleneck Detection: The 50% increase in delivery times during late afternoon isn't random noise—it's evidence of systematic capacity constraints that require strategic intervention, not just operational patience.

2. **The Performance & Predictability Audit**

Service Level Governance: The 75.23% on-time rate is a baseline, not a celebration. A governed network would establish tiered service levels with specific targets for different route types and time windows.

Outlier Analysis as Quality Control: The detection of extreme outliers (5000km deliveries) is treated as a data integrity and process compliance issue. These aren't statistical anomalies—they're symptoms of broken processes.

3. **The Operational Intelligence Framework**

Efficiency Ratio Analysis: The efficiency_ratio (actual time vs. OSRM estimated time) serves as a real-world calibration metric. Consistent overruns indicate either poor routing estimates or operational constraints not captured by the algorithm.

Segment Performance Mapping: By analyzing source-destination pairs, we identified specific corridors where performance consistently degrades, enabling targeted infrastructure investments.

### Audit Results & Strategic Recommendations

- Route Reliability	- Indirect routes show 25% deviation vs. 10% for direct routes	HIGH RISK. Prioritize route optimization and establish separate service level agreements for indirect routes.
- Temporal Capacity	- Evening deliveries take 50% longer than morning deliveries	OPERATIONAL BOTTLENECK. Implement dynamic pricing or capacity allocation to smooth demand peaks.
- Network Integrity	- 2.66% of deliveries have significant delays (>50% deviation)	CRITICAL ALERT. Launch root cause analysis program for delayed deliveries with executive oversight.
- Data Quality - Extreme outliers in distance and time metrics	SYSTEMIC ISSUE. Implement data validation gates at trip creation to prevent garbage data.

### Conclusion: Building the Predictable Logistics Network

This audit demonstrates that delivery performance is not a random outcome but a predictable result of network design, capacity planning, and process discipline.

The logistics network is efficient at scale but fragile at the edges. The high on-time percentage masks predictable patterns of failure that, if addressed systematically, could elevate overall network reliability from good to exceptional.

### Source

Dataset: [Delhivery Logistics Analysis Dataset on Kaggle](https://www.kaggle.com/datasets/devarajv88/delhivery-logistics-dataset/data)
