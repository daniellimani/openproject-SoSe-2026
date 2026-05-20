# Openproject-SoSe-2026
Creating the first repository for Open Scholarship in History and the Humanities: Resources, Tools, and Methods for Research Implementation 02-04-0130-ue SoSe 2026

## Project description: 
#### Museum of Modern Art Collection
Getting the list of the artist who have and are contributing to the Modern Art. 

## Data Origin Note Source: 
#### https://www.kaggle.com/datasets/momanyc/museum-collection?select=artists.csv
### Date accessed: 05.11.2026
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
