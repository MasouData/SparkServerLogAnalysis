# SparkServerLogAnalysis

## Overview
This repository contains the project 'SparkServerLogAnalysis', a data-intensive application developed using Apache Spark for the course "Data Intensive Systems" at Utrecht University. The project involves analyzing server logs from a network provider to identify and group similar service tasks. The goal is to optimize the execution of service tasks by identifying small variations in similar processes and grouping them under a unique representation. This analysis can help in improving the efficiency of the server and provide valuable insights into the operation of the network provider. The project demonstrates the application of Big Data technologies in real-world scenarios.

## Project Workflow
The general idea of this project follows the Shingle -> MinHash -> LSH (Locality-Sensitive Hashing) approach. 

1. **Shingle**: This step involves transforming the server logs into a set of "shingles" or substrings. This helps in capturing the local structure of the server log data and enables the comparison of different logs.

2. **MinHash**: This step involves creating a "signature" for each server log using MinHash. This reduces the dimensionality of the data and makes it easier to compare different logs.

3. **LSH**: In this step, Locality-Sensitive Hashing is used to group similar server logs together. This allows us to identify and group similar service tasks.

## Code
The code for this project is written in Python and uses the PySpark library for processing large amounts of data. The code involves reading the server log data, preprocessing the data, transforming the data into shingles, creating MinHash signatures, and finally using LSH to group similar logs together. The code also includes the evaluation of the clustering results using the silhouette score.

## Running the Code
To run the code, you need to have PySpark installed. You can then run the script using a Spark session.

## Future Work
This project serves as a starting point for optimizing service tasks in a network provider. Future work could involve refining the shingling, MinHash, and LSH steps, trying out different parameters, and using additional data sources.
