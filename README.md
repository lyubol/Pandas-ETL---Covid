# Pandas ETL project about Covid-19

## Overview

#### The project is extracting the most recent Covid-19 data, applying transformations to it and loading the files to an Azure Blob Storage. 

## Decription

#### This project consists of jupyter notebooks. 

### funcs.ipynb

#### funcs.ipynb contains functions that are used across all notebooks. It contains various functions including ones for data transformations, downloading files based on URL and uploading files to Azure Blob Storage.

### pipeline.ipynb 

#### pipeline.ipynb contains the execution flow. It runs all notebooks in a specific order and returns the results. This is the notebook the should be used to run the project and obtain the results.

### download_raw_datasets.ipynb

#### download_raw_datasets.ipynb is responsible for extracting the latest Covid-19 cases and vaccines information from the links provided inside the links.txt file. The files are being saved to the 'Raw' folder. New files are uploaded on a daily basis on the website.

### ETL_cases.ipynb

#### ETL_cases.ipynb reads the latest Covid-19 cases file from the 'Raw' folder, apply transformations to it and saves it to the 'Processed' folder and also to a 'Processed' container in Azure Blob Storage

