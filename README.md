# Museum of Modern Art (MoMA) Artist Dataset Analysis
## Structure

This notebook presents the complete workflow followed during the preparation, cleaning, enrichment, and analysis of the Museum of Modern Art (MoMA) artist dataset.

The notebook is organised into the following sections:

1. Project Description
2. Research Purpose
3. Data Origin
4. Research Questions
5. Workflow
   - Data Access
   - Selection / Sampling
   - Cleaning / Preprocessing
   - Enrichment / Linking
   - Analysis
   - Visualisation
   - Archiving & Sharing
6. Results
7. Key Findings

## Project Description

The objective of this project is to prepare and analyse metadata describing artists included in the Museum of Modern Art (MoMA) Collection. The dataset contains demographic information about artists, including their names, nationalities, gender, and birth and death years.

The project follows a complete data processing workflow, beginning with data acquisition and ending with dataset preparation for enrichment using Wikidata. The analysis focuses on improving data quality, identifying missing information, and preparing the dataset for semantic linking.

## Research Purpose

The primary purpose of this research is to evaluate the completeness and quality of the Museum of Modern Art artist metadata and prepare it for enrichment using external knowledge sources such as Wikidata.

The project demonstrates a typical digital humanities workflow consisting of data cleaning, metadata enhancement, entity resolution, and descriptive analysis.

## Data Origin

The dataset used in this project originates from the Museum of Modern Art (MoMA) Collection and contains metadata describing artists represented in the collection.

The dataset includes the following variables:

- Artist ID
- Name
- Nationality
- Gender
- Birth Year
- Death Year

These metadata provide the basis for analysing artist demographics and supporting future semantic enrichment using Wikidata.

## Research Questions

The project seeks to answer the following research questions:

1. How complete is the metadata describing artists in the MoMA Collection?
2. Which artists contain incomplete demographic information?
3. Which artists have complete metadata suitable for semantic enrichment?
4. Can missing metadata be supplemented through Wikidata?
5. How can entity resolution improve the quality of cultural heritage datasets?


## Workflow
### 1. Data Access

The original dataset (artists.csv) was imported into Python using the pandas library.

The dataset was inspected to understand its structure, variables, dimensions, and overall completeness before further processing.

### 2. Selection / Sampling

The complete dataset was used for analysis without sampling.

Several subsets of the original dataset were generated automatically during preprocessing:

- artists_all_fields_complete.csv
- artists_likely_alive.csv
- artists_missing_any_field.csv

These subsets support different stages of the data preparation process.

### 3. Cleaning / Preprocessing

The dataset was cleaned by identifying missing values across the key metadata fields.

The preprocessing stage included:

- inspecting dataset structure
- generating descriptive statistics
- identifying missing values
- separating complete records
- separating incomplete records
- identifying artists who are likely still living (birth year ≥ 1960 and no recorded death year)

The cleaned datasets were exported as new CSV files for reproducibility.

### 4. Enrichment / Linking

The cleaned dataset was prepared for semantic enrichment using Wikidata.

Additional metadata columns were added:

- wikidata_id
- enhanced_birth_year
- match_status

The matching process searches Wikidata using the artist's name and applies disambiguation based on:

- occupation
- nationality
- birth year
- death year
- gender

Each artist is assigned one of three statuses:

- matched
- uncertain
- not_found

This process improves metadata quality while reducing incorrect entity matches.

### 5. Analysis

Descriptive statistical analysis was performed using pandas.

The analysis included:

- dataset dimensions
- missing value counts
- descriptive statistics
- frequency distributions
- completeness assessment

These statistics provide an overview of the quality and characteristics of the dataset.

### 6. Visualisation

Visualisation will be used to present the characteristics of the dataset through charts and summary tables.

Possible visualisations include:

- artist nationality distribution
- gender distribution
- birth year timeline
- missing data overview
- completeness comparison

These visualisations assist in interpreting the cleaned and enriched dataset.

### 7. Archiving & Sharing
All generated datasets were saved as CSV files to ensure reproducibility.

The complete project, including notebooks, datasets, and documentation, is maintained using Git and GitHub for version control and collaborative development.

The following files were generated during the project:

- artists_statistics.csv
- artists_all_fields_complete.csv
- artists_likely_alive.csv
- artists_missing_any_field.csv
- artists_prepared_for_wikidata.csv
- artists_enhanced_wikidata.csv

### 8. Results

The preprocessing workflow successfully separated the original dataset into multiple subsets representing complete records, incomplete records, and artists with potentially missing death information.

The preparation for Wikidata enrichment introduced additional metadata fields required for entity resolution and semantic linking.

The resulting datasets provide a cleaner and more structured foundation for future analysis and metadata enhancement.





# Openproject-SoSe-2026
Creating the first repository for Open Scholarship in History and the Humanities: Resources, Tools, and Methods for Research Implementation 02-04-0130-ue SoSe 2026

## Project description: 
#### Museum of Modern Art Collection
Getting the list of the artist who have and are contributing to the Modern Art. 

## Data Origin Note Source: 
#### https://www.kaggle.com/datasets/momanyc/museum-collection?select=artists.csv
### Date accessed: 11.05.2026
### License: 
#### https://creativecommons.org/publicdomain/zero/1.0/ 
## Description: 
The Museum’s website features 72,706 artworks from 20,956 artists. The artworks dataset contains 130,262 records, representing all of the works that have been accessioned into MoMA’s collection and cataloged in our database. It includes basic metadata for each work, including title, artist, date, medium, dimensions, and date acquired by the Museum. Some of these records have incomplete information and are noted as “not curator approved.”

## What has already been done to the data: 
The artworks dataset contains 130,262 records, representing all of the works that have been accessioned into MoMA’s collection and cataloged in our database. The artists dataset contains 15,091 records, representing all the artists who have work in MoMA's collection and have been cataloged in our database. It includes basic metadata for each artist, including name, nationality, gender, birth year, and death year.

# Museum of Modern Art (MoMA) Collection Analysis

## Research Questions

This project aims to explore the Museum of Modern Art (MoMA) Collection dataset in order to answer the following research questions:

1. What are the demographic characteristics of artists represented in the MoMA collection?
2. Which nationalities appear most frequently in the dataset?
3. What is the gender distribution of artists in the collection?
4. How are birth years and death years distributed across artists?
5. Are there observable historical patterns in the representation of artists over time?

## Dataset Description

The dataset used in this project is the Museum of Modern Art (MoMA) Collection dataset.

The dataset contains metadata about artists included in the collection, including:

- Artist ID
- Name
- Nationality
- Gender
- Birth Year
- Death Year

These metadata attributes help answer the research questions by allowing statistical analysis of:
- artist demographics,
- historical representation,
- nationality distribution,
- gender representation,
- and lifespan patterns.

## Statistical Analysis

The Python code in the notebook is used to generate descriptive statistics for the dataset.

The analysis includes:
- loading the dataset with pandas,
- displaying dataset structure,
- identifying missing values,
- generating descriptive statistics,
- and exporting the statistical summary into the DATA folder.

The outputs are displayed directly in the notebook and saved as a CSV file for documentation and reproducibility purposes.
