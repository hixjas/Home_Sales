# Home_Sales
Module 22

# PySpark Home Sales Analysis

This project demonstrates a comprehensive analysis of home sales data using PySpark in Google Colab. The analysis includes data caching, performance optimization, and comparison between different storage formats.

## Project Overview

The analysis performs the following operations:
1. Loads and preprocesses home sales data
2. Runs analytical queries to understand pricing patterns
3. Compares performance between cached, uncached, and parquet storage formats
4. Demonstrates Spark optimization techniques

## Prerequisites

- Google Colab environment
- Apache Spark 3.5.3
- Java JDK 11
- Python 3.x
- PySpark
- FindSpark package

## Installation

```bash
!apt-get update
!apt-get install openjdk-11-jdk-headless -qq > /dev/null
!wget -q https://archive.apache.org/dist/spark/spark-3.5.3/spark-3.5.3-bin-hadoop3.tgz
!tar xf spark-3.5.3-bin-hadoop3.tgz
!pip install -q findspark py4j
```


## Environment Setup
```import os
os.environ["JAVA_HOME"] = "/usr/lib/jvm/java-11-openjdk-amd64"
os.environ["SPARK_HOME"] = "/content/spark-3.5.3-bin-hadoop3"
os.environ['PYTHONPATH'] = f"{os.environ['SPARK_HOME']}/python:{os.environ['SPARK_HOME']}/python/lib/py4j-0.10.9.7-src.zip"
```

## Data Analysis Queries

The project includes these key analytical queries:

- Average price for 4-bedroom homes by year built

- Average price for 3-bedroom, 3-bath homes by year built

- Average price for homes with specific criteria (3 beds, 3 baths, 2 floors, ≥2000 sqft)

- Average price by view rating (filtered and sorted)

## Performance Optimization
The project demonstrates three data processing methods:

Uncached Data: Baseline performance

Cached Data: Improved performance through in-memory caching

Parquet Format: Optimized storage format for analytical queries

### Example output:

Performance Comparison:

- Uncached runtime: 1.0433 seconds
- Cached runtime:   0.0630 seconds
- Parquet runtime:  0.0391 seconds
