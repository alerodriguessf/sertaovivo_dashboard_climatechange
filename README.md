
# **Strategic Prioritization Index for Climate Adaptation in Brazil's Semi-Arid Region**

## **Executive Summary**

This project presents the design and implementation of a multi-criteria prioritization index and an interactive Power BI dashboard to guide the strategic allocation of a USD 60 million climate adaptation grant from the Brazilian Development Bank (BNDES). Tasked by the Special Advisory Office, this initiative aimed to create a data-driven framework to identify municipalities most vulnerable to climate change in Brazil's semi-arid region.

The core of this project was the development of a weighted scoring model based on official governmental data sources, incorporating socioeconomic vulnerability, climate risk, and food and water security indicators. The final deliverable—an interactive Power BI dashboard—translates this complex index into an intuitive decision-making tool, enabling policymakers to allocate infrastructure investments for water resilience with maximum impact and transparency.

## **Table of Contents**

1.  Business Context & Strategic Objective
2.  Methodology: The Prioritization Index
3.  Dashboard & Data Visualization
4.  Impact & Business Value
5.  Technologies Used
6.  Data Sources

---

## **Business Context & Strategic Objective**

The "Sertão Vivo" project, funded by BNDES, was established to enhance climate resilience for rural communities in Brazil's semi-arid Northeast, a region historically affected by severe droughts and climate-related challenges. With a significant grant to be distributed, the key challenge was to move beyond subjective decision-making and implement an equitable, evidence-based methodology for resource allocation.

The primary objective was to answer the critical question: **Which municipalities should be prioritized to receive investments, thereby maximizing the social and environmental impact of the grant?

This project directly addresses this challenge by creating a quantitative, transparent, and replicable system for ranking and selecting municipalities.

## **Methodology: The Prioritization Index**

A composite index was engineered to produce a final prioritization score for each municipality. The methodology, based on the official BNDES framework, involved a weighted combination of four key classificatory criteria.

### 1. Index Components & Scoring
Each municipality was scored on a scale of 0 to 4 for the following indicators:

* **Rural Poverty Incidence (IPR)**: Based on the percentage of rural households registered in Brazil's Unified Registry for Social Programs (CadÚnico) within poverty and extreme poverty brackets. A higher poverty rate results in a higher score.
* **Climate Vulnerability & Drought History (IVCS)**: Utilizes a climate vulnerability index ranging from "Very Low" to "Very High." Greater vulnerability corresponds to a higher score.
* **Food & Nutritional Security (ISAN)**: Measures the population's vulnerability to food insecurity. A higher vulnerability level (e.g., "Very High") receives a higher score.
* **Water Security Index (ISH)**: Assesses the availability and quality of water resources. Lower water security (rated from "Maximum" to "Minimum") results in a higher score, indicating greater need.

### 2. Weighting & Final Score Calculation
To align with the project's primary goal of addressing socioeconomic disparities, the criteria were assigned different weights. The Rural Poverty Incidence was given the highest importance.

* **Weights Applied**:
    * Rural Poverty (P1): **4** 
    * Climate Vulnerability (P2): **2** 
    * Food Security (P3): **2** 
    * Water Security (P4): **1** 

The final score for each municipality was calculated using the following weighted formula:
**Municipality Score = (4 × IPR) + (2 × IVCS) + (2 × ISAN) + (1 × ISH)**

### 3. Statistical Prioritization Tiers
The calculated scores for all municipalities formed an approximately normal distribution. This statistical property was leveraged to classify municipalities into four distinct priority tiers based on standard deviations from the mean (μ), ensuring a robust and statistically sound categorization.
* **Very High Priority**: Score > (μ + 1σ)
* **High Priority**: Score between μ and (μ + 1σ)
* **Medium Priority**: Score between (μ - 1σ) and μ
* **Low Priority**: Score < (μ - 1σ)

## **Dashboard & Data Visualization**

The calculated index and prioritization tiers were operationalized through the development of an interactive Power BI dashboard. This business intelligence tool was designed for strategic advisors and policymakers.

**Key Dashboard Features**:
* **Geospatial Visualization**: A map of Pernambuco's semi-arid region color-coded by the final priority tier, allowing for quick identification of critical zones.
* **Dynamic Filtering**: Users can filter municipalities by state, priority level, or individual index scores (e.g., show only municipalities with "Very High" climate vulnerability).
* **Detailed Drill-Down**: Selecting a municipality reveals its scores for each of the four criteria, providing a complete diagnostic view and justifying its final ranking.
* **Strategic Simulation**: The dashboard allows for simulating investment scenarios, calculating the overall impact score of a proposed project based on the number of families served in selected municipalities, using the official state-level scoring formula.

## **Impact & Business Value**

* **Data-Driven Governance**: Replaced subjective criteria with a transparent, quantitative framework, enhancing the legitimacy and efficiency of a USD 60 million public investment.
* **Strategic Resource Allocation**: Empowers decision-makers to direct funds towards areas with the highest empirically-measured need, maximizing the grant's impact on water resilience and poverty reduction.
* **Enhanced Transparency & Accountability**: Provides a clear, auditable trail for how and why investment decisions were made, fostering public trust.

## **Technologies Used**

* **Business Intelligence & Visualization**: Power BI
* **Data Analysis & Modeling**: Python (Pandas), Statistical Analysis (for distribution assessment)
* **Data Management**: Microsoft Excel

## **Data Sources**

The analysis was conducted using official, publicly available data from Brazilian government institutions, ensuring credibility and accuracy.

* **CadÚnico**: Brazilian Unified Registry for Social Programs 
* **AdaptaBrasil/MCTI**: Ministry of Science, Technology, and Innovation platform for climate vulnerability data
* **SISVAN/Ministry of Citizenship**: National Food and Nutrition Surveillance System 
* **ANA (National Water and Sanitation Agency)**: Data on water availability and quality
