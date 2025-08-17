
# Engineering of Data Analysis: Assignment 2

This repository holds the solution for the second assignment in the "Engineering of Data Analysis" course. The project explores advanced data engineering topics, including performance analysis of data access patterns and the practical application of data privacy and anonymization techniques.

## Overview

-   **Goal:** To analyze the performance trade-offs of data locality and to implement and evaluate various data anonymization techniques. The project measures the impact of privacy-preserving methods on data utility for statistical analysis and machine learning tasks.
-   **Assignment Context:** This assignment transitions from foundational data processing to critical real-world concerns. It involves using specialized libraries to apply k-anonymity and differential privacy and assessing their effects on datasets used for health and socio-economic analysis.

## Key Analyses & Exercises

The assignment is divided into four main exercises, each tackling a different aspect of data engineering and privacy.

1.  **Local vs. Remote File Access:** This exercise benchmarks the performance of reading data from a local file within the Colab instance versus a remote file stored on Google Drive. The comparison is performed using both Pandas and Spark SQL to understand the I/O overhead in different frameworks.

2.  **Anonymization for Statistical Queries:** Using a heart disease dataset, this exercise explores the impact of k-anonymity on statistical utility. It compares results from:
    -   The original dataset.
    -   A dataset anonymized using a generic k-anonymity approach.
    -   A dataset anonymized using workload-aware k-anonymity (optimized for specific queries).
    The analysis focuses on how well group-based statistics are preserved after anonymization.

3.  **Anonymization for Correlation-Based Analysis:** This exercise investigates how anonymization affects machine learning models that rely on correlations between variables. Using a Life Expectancy dataset, a regression task is performed on three versions of the data:
    -   The original dataset.
    -   A workload-aware k-anonymized dataset (preserving key correlations).
    -   A dataset protected with differential privacy.

4.  **Advanced Machine Learning with Differential Privacy:** This exercise applies differential privacy to a custom machine learning task (e.g., classification, clustering). It involves implementing a model on both the original and the differentially private versions of a chosen dataset and systematically comparing the model's performance and accuracy to evaluate the utility-privacy trade-off.

## Technology Stack

This project leverages Python and Spark within a Google Colab environment, with a special focus on libraries designed for data privacy.

| Component                 | Technology / Library                                      | Purpose                                                                 |
| ------------------------- | --------------------------------------------------------- | ----------------------------------------------------------------------- |
| **Core Processing**       | Apache Spark, Pandas                                      | For distributed and single-core data processing and analysis.           |
| **Data Privacy**          | `anonymity-api`                                           | For implementing k-anonymity and workload-aware anonymization.          |
| **Data Privacy**          | `diffprivlib` (IBM Differential Privacy Library)          | For applying differential privacy to data and machine learning models.  |
| **APIs & Languages**      | Python, PySpark, Spark SQL                                | For writing data transformations and analytical queries.                |
| **Development Environment** | Google Colab, Jupyter Notebook                            | Interactive environment for executing code and documenting results.     |
| **Data Visualization**    | Matplotlib, Seaborn                                       | For creating plots to compare results and visualize data distributions. |

## Data Sources

This assignment utilizes several datasets to explore different analysis scenarios:

-   **NYC Taxi Data:** From the ACM DEBS 2015 Grand Challenge, used for performance testing in Exercise 1.
-   **Heart Disease Dataset:** A public dataset used in Exercise 2 to analyze the impact of anonymization on statistical health queries.
-   **Life Expectancy Dataset:** A WHO dataset from Kaggle, used in Exercise 3 to evaluate privacy techniques on regression tasks.
-   **Custom Dataset:** A user-provided dataset for Exercise 4 to demonstrate the application of differential privacy on a familiar ML problem.

## Setup and Execution

To run this project, open the `EoDA_2425_assignment2.ipynb` notebook in Google Colab.

**Prerequisites:**
-   A Google account with access to Google Drive.
-   The required datasets must be placed in a Google Drive folder accessible by the notebook.
-   The notebook is self-contained and installs all necessary libraries, including `pyspark`, `anonymity-api`, and `diffprivlib`, in the initial setup cells.

The notebook is intended to be run sequentially. Each exercise is clearly marked, and the final cells of each section contain a discussion of the results.

## Results and Discussion

All results, including performance measurements, statistical comparisons, model accuracy metrics, and visualizations, are generated and displayed directly within the Jupyter Notebook. Each exercise concludes with a "Results discussion" section that explains the findings and draws conclusions about the trade-offs between performance, privacy, and data utility.

---

_For all code, outputs, and detailed analysis, please refer to the main Jupyter Notebook file in this repository._
