# Pandas ETL project about Covid-19
#### Created by: Lyubomir Lirkov / lyubomir.lirkov@gmail.com
#### Created date: November 2021

## Overview

#### The project is extracting the most recent Covid-19 data, applying transformations to it and loading the files to an Azure Blob Storage. 

## Decription

#### This project consists of jupyter notebooks. Files that are updated on a daily basis are being downloaded to obtain the latest Covid-19 cases and vaccines information. This data is then transformed and saved to Azure Blob Storage. Later it is combined with countries information (e.g population, density, life expectency) to produce visualisations. The whole process is controlled by the 'pipeline' notebook, which executes all other notebooks in particular order. All results are visible within the 'pipeline' notebook, when it gets executed.

### funcs.ipynb

#### funcs.ipynb contains functions that are used across all notebooks. It contains various functions including ones for data transformations, downloading files based on URL and uploading files to Azure Blob Storage.

### pipeline.ipynb 

#### pipeline.ipynb contains the execution flow. It runs all notebooks in a specific order and returns the results. This is the notebook the should be used to run the project and obtain the results.

### download_raw_datasets.ipynb

#### download_raw_datasets.ipynb is responsible for extracting the latest Covid-19 cases and vaccines information from the links provided inside the links.txt file. The files are being saved to the 'Raw' folder. New files are uploaded on a daily basis on the website.

### ETL_cases.ipynb

#### ETL_cases.ipynb reads the latest Covid-19 cases file from the 'Raw' folder, apply transformations to it and saves it to the 'Processed' folder and also to a 'Processed' container in Azure Blob Storage

### ETL_vaccines.ipynb

#### ETL_vaccines.ipynb reads the latest Covid-19 vaccines file from the 'Raw' folder, apply transformations to it and saves it to the 'Processed' folder and also to a 'Processed' container in Azure Blob Storage

### ETL_countries.ipynb 

#### ETL_countries.ipynb downloads transforms countries data, which is later used in combination with Covid-19 data for data analysis. An example is population data, which helps to find the ratio of new cases to population and compare different countries.

### merge_processed_datasets.ipynb 

#### merge_processed_datasets.ipynb is merging the transformed Covid-19 cases and vaccines data into one file, which is later used for data analysis.

### data_analysis.ipynb

#### data_analysis.ipynb contains data analysis and visualisations, which provide useful insides. All produced visualisations are visible when pipeline.ipynb is executed. 