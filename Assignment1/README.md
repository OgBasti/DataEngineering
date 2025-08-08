# Engineering of Data Analysis: Assignment 1

This repository contains the Jupyter Notebook for the first assignment of the "Engineering of Data Analysis" course. The project involves analyzing the large-scale NYC Taxi dataset from the ACM DEBS 2015 Grand Challenge, with a focus on comparing the performance and implementation styles of different data processing and machine learning frameworks.

**Authors:**
- **Student num:** `TBC` **; Name:** `TBC`
- **Student num:** `TBC` **; Name:** `TBC`

## Overview

- **Goal:** To implement and evaluate solutions for a series of data analysis and machine learning tasks using various high-performance computing frameworks. The core objective is to compare the runtimes and methodologies of Pandas, Spark (SQL and Pandas API), and NVIDIA RAPIDS (cuDF and cuML).
- **Assignment Context:** The project leverages the well-known ACM DEBS 2015 Grand Challenge dataset. It addresses practical questions such as calculating driver earnings, identifying popular routes, and optimizing taxi rank locations through clustering.

## Key Analyses & Exercises

The assignment is structured around four main exercises, each designed to test different aspects of data engineering and analysis:

1.  **Simple Aggregations:** Compute the total earnings for each taxi driver. This task is used as a benchmark to compare the raw performance of:
    -   Pandas (single-core, in-memory)
    -   Spark Pandas API (distributed)
    -   Spark SQL (distributed)
    -   cuDF (GPU-accelerated)

2.  **UDF Performance Analysis:** Measure and contrast the performance of a Spark SQL query that uses a native Python User-Defined Function (UDF) against an equivalent query written using only standard Spark SQL functions. This demonstrates the performance overhead associated with UDFs.

3.  **Frequent Route Identification:** Find the 20 most frequent taxi routes with a trip distance above a defined threshold. The solution involves creating a spatial grid to group pickup and dropoff locations and is implemented using both Spark SQL and the Spark Pandas API.

4.  **Taxi Rank Placement with Clustering:** Use K-Means clustering to identify optimal locations for taxi ranks based on pickup density. This exercise compares the performance and implementation of three different machine learning libraries:
    -   scikit-learn (traditional CPU-based)
    -   cuML (GPU-accelerated)
    -   Spark MLlib (distributed)

## Technology Stack

This project utilizes a range of tools to compare different data processing paradigms. The entire analysis is conducted within a Google Colab environment with GPU acceleration enabled.

| Component                 | Technology / Library                                      | Purpose                                                                |
| ------------------------- | --------------------------------------------------------- | ---------------------------------------------------------------------- |
| **Core Processing**       | Apache Spark, Pandas                                      | Foundational engines for distributed and single-core data processing.  |
| **APIs & Languages**      | Python, PySpark, Spark SQL, Pandas API on Spark           | For writing data transformations and analytical queries.               |
| **GPU Acceleration**      | NVIDIA RAPIDS (cuDF, cuML)                                | For high-performance, GPU-accelerated data manipulation and ML.        |
| **Machine Learning**      | Spark MLlib, cuML, Scikit-learn                           | For implementing K-Means clustering across different frameworks.       |
| **Development Environment** | Google Colab, Jupyter Notebook                            | Interactive environment with free access to GPU hardware.              |
| **Data Visualization**    | Matplotlib                                                | For plotting heatmaps and scatter plots to visualize results.          |

## Data Source

The dataset is from the **ACM DEBS 2015 Grand Challenge**, containing taxi trip records from New York City. The data is provided in different sizes (`tiny`, `sample`, `full`) to allow for scalable testing and development.

-   **Source Link:** The data is hosted on Google Drive and accessed via a mounted drive in the Colab environment.
-   **Schema:** Key fields include pickup/dropoff times and coordinates, trip duration, distance, and fare details.

## Setup and Execution

To run this analysis, open the `EoDA_2425_assignment1.ipynb` notebook in a Google Colab environment.

**Prerequisites:**
- A Google account with access to Google Drive.
- In Colab, set the hardware accelerator to **GPU** (`Edit > Notebook settings > T4 GPU`).

The notebook handles its own setup by running installation scripts for all required dependencies, including:
- `pyspark`
- `gdown` for file handling
- `rapidsai-csp-utils` for installing RAPIDS libraries (cuDF, cuML)

The notebook is designed to be executed cell-by-cell. The `FILENAME` variable can be adjusted to switch between the tiny, sample, and full datasets for performance comparisons.

## Results and Discussion

The results, including performance timings, code outputs, and visualizations, are documented within the Jupyter Notebook under each exercise. A detailed discussion follows each exercise, explaining the code's rationale and analyzing the performance differences observed between the tested frameworks.

---

_For all code, detailed implementation, and query results, please see the main Jupyter Notebook file in this repository._

---

_For all code, detailed implementation, and query results, please see the main Jupyter Notebook file in this repository._



