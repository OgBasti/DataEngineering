# Engineering of Data Analysis: Assignment 1

This repository contains the solution for the first assignment in the "Engineering of Data Analysis" course, developed by the students listed below. The project focuses on processing and analyzing a large-scale dataset using distributed computing with Apache Spark.

## Overview

-   **Goal:** The primary objective of this assignment is to implement a scalable data processing solution to answer a series of analytical queries on a large trip dataset. The project demonstrates proficiency in using Apache Spark for data ingestion, transformation, and analysis.
-   **Assignment Context:** The analysis is based on the **ACM DEBS 2015 Grand Challenge**, which involves real-time analysis of New York City taxi trip records. This project provides batch-processing solutions to the challenge questions using Spark's powerful distributed computing capabilities.

## Main Data Features

The dataset consists of records representing taxi trips in New York City. The key features of the data include:

| Feature                   | Description                                                 |
| ------------------------- | ----------------------------------------------------------- |
| medallion                 | An anonymized license identifier for the taxi.              |
| hack_license              | An anonymized license identifier for the driver.            |
| pickup_datetime           | Timestamp for the start of the trip.                        |
| dropoff_datetime          | Timestamp for the end of the trip.                          |
| trip_time_in_secs         | The total duration of the trip in seconds.                  |
| trip_distance             | The distance of the trip in miles.                          |
| pickup_longitude / latitude | Geographic coordinates for the pickup location.             |
| dropoff_longitude / latitude| Geographic coordinates for the dropoff location.            |
| payment_type              | The method of payment (e.g., cash, credit card).            |
| fare_amount               | The base fare for the trip.                                 |
| total_amount              | The total amount paid, including tolls and surcharges.      |

## Workflow & Analysis

The core of this assignment is implemented in the Jupyter Notebook, following a structured workflow:

1.  **Environment Setup:** Initialize a Spark session and configure the environment for distributed data processing, potentially within a cloud environment like Google Colab with GPU acceleration.
2.  **Data Loading:** Ingest the large taxi trip dataset (in formats like CSV or Parquet) into a Spark DataFrame.
3.  **Data Cleaning & Transformation:** Perform necessary data cleaning, such as handling null values, correcting data types, and parsing timestamps. New features, like trip duration or speed, may be engineered to support the analysis.
4.  **Query Implementation:** Address the specific analytical questions from the assignment using Spark SQL and DataFrame API operations. This includes performing complex aggregations, joins, and window functions to derive insights.
5.  **Results Presentation:** The results for each query are calculated and presented directly within the notebook, showcasing the final output of the analysis.

## Technology Stack

| Component               | Technology / Tool                                         | Purpose                                                     |
| ----------------------- | --------------------------------------------------------- | ----------------------------------------------------------- |
| **Core Processing Engine**| Apache Spark                                            | For distributed data processing, transformations, and analytics. |
| **Language & API**      | Python, PySpark                                           | The primary language and library for interacting with Spark. |
| **Development Environment**| Jupyter Notebook / Google Colab                         | An interactive environment for developing and documenting the analysis. |
| **Machine Learning (Optional)** | Spark MLlib                                       | Used for any predictive modeling or machine learning tasks. |

## Data Source

The data for this assignment is from the **ACM DEBS 2015 Grand Challenge**, which focuses on real-time event processing for large data streams. The dataset contains details of over 1.5 billion taxi trips in New York City during 2013.

-   **Source:** [ACM DEBS 2015 Grand Challenge Website](http://www.debs2015.org/call-grand-challenge.html)
-   **Citation:** The data is a publicly available dataset commonly used for big data processing benchmarks and academic exercises.

## Results

The Jupyter notebook provides the complete code, step-by-step transformations, and final answers for each of the analytical questions posed in the assignment. The solutions demonstrate the efficient use of Spark to query and extract meaningful information from a large-scale, real-world dataset.

---

_For all code, detailed implementation, and query results, please see the main Jupyter Notebook file in this repository._



