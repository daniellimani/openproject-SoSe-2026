# Museum of Modern Art (MoMA) Artist Metadata Enrichment using Wikidata

## Project Overview

This project investigates the completeness of metadata describing artists in the Museum of Modern Art (MoMA) collection and demonstrates how open knowledge graphs can enrich missing information.

Using Python, Jupyter Notebook, GitHub, and the Wikidata SPARQL endpoint, the project identifies artists with incomplete metadata, performs entity matching, and enriches missing Birth Year and Death Year values where reliable matches are found.

The project follows the principles of **Open Scholarship** by ensuring transparency, reproducibility, and version control throughout the research workflow.

---

# Repository Structure

```text
openproject-SoSe-2026/

│
├── data/
│   ├── artists.csv
│   ├── artists_statistics.csv
│   ├── artists_all_fields_complete.csv
│   ├── artists_missing_dates.csv
│   ├── artists_prepared_for_wikidata.csv
│   └── data_artists_enriched.csv
│
├── notebook/
│   ├── create_update_notebook.ipynb
│   ├── Data_enrichment.ipynb
│   └── Results_Analysis.ipynb
│
├── README.md
└── .gitignore
```

---

# Project Description

The objective of this project is to prepare, clean, analyse, and enrich metadata describing artists included in the Museum of Modern Art (MoMA) collection.

The workflow begins with data preparation and descriptive statistics, followed by metadata enrichment using Wikidata and concludes with quantitative analysis measuring the effectiveness of the enrichment process.

---

# Research Purpose

The purpose of this research is to evaluate the completeness of the Museum of Modern Art artist metadata and investigate whether missing Birth Year and Death Year information can be recovered through semantic enrichment using Wikidata.

The project demonstrates a complete Digital Humanities workflow including:

- Data Cleaning
- Metadata Preparation
- Entity Matching
- Semantic Enrichment
- Data Analysis
- Visualisation
- Open Research Documentation

---

# Data Origin

**Dataset**

Museum of Modern Art (MoMA) Artist Dataset

Source:

https://www.kaggle.com/datasets/momanyc/museum-collection

Date accessed:

11 May 2026

License:

Creative Commons CC0 1.0 Public Domain

https://creativecommons.org/publicdomain/zero/1.0/

---

# Dataset Description

The original dataset contains metadata describing artists represented in the Museum of Modern Art collection.

Variables include:

- Artist ID
- Name
- Nationality
- Gender
- Birth Year
- Death Year

Original dataset size:

**15,091 artists**

---

# Research Questions

This project investigates the following research questions:

1. How complete is the metadata describing artists in the Museum of Modern Art collection?

2. Which artists contain incomplete demographic information?

3. Can missing Birth Year and Death Year values be enriched using Wikidata?

4. How effective is entity matching when enriching cultural heritage metadata?

5. What proportion of artists can be successfully linked to Wikidata?

---

# Workflow

## 1. Data Access

The original dataset (`artists.csv`) was imported into Python using the **pandas** library.

The dataset structure, variables and missing values were inspected before any preprocessing.

---

## 2. Selection / Sampling

The complete dataset was analysed without sampling.

Several subsets were automatically generated during preprocessing:

- artists_statistics.csv
- artists_all_fields_complete.csv
- artists_missing_dates.csv
- artists_prepared_for_wikidata.csv

---

## 3. Cleaning / Preprocessing

The preprocessing stage included:

- Inspecting the dataset
- Checking missing values
- Identifying incomplete metadata
- Separating complete records
- Exporting reproducible datasets

No original records were removed from the dataset.

---

## 4. Enrichment / Linking

Metadata enrichment was performed using the **Wikidata SPARQL Endpoint**.

The notebook queried Wikidata for every artist contained in:

`artists_prepared_for_wikidata.csv`

The enrichment process compared available metadata using:

- Name
- Nationality
- Gender

When a reliable match was found, the following metadata were added:

- Wikidata ID
- Birth Year (if missing)
- Death Year (if missing)
- Match Status
- Source

The workflow classified every artist as:

- matched
- uncertain
- not_found

---

## 5. Analysis

The enriched dataset was analysed to evaluate:

- Metadata completeness
- Number of successful matches
- Birth Years recovered
- Death Years recovered
- Match success rate
- Remaining missing metadata

---

## 6. Visualisation

Visualisations include:

- Entity matching results
- Metadata completeness before and after enrichment
- Birth Year recovery
- Death Year recovery
- Gender distribution
- Nationality distribution
- Birth Year timeline

---

## 7. Archiving & Sharing

The complete workflow was documented using:

- Jupyter Notebook
- Git
- GitHub

Generated datasets include:

- artists_statistics.csv
- artists_all_fields_complete.csv
- artists_missing_dates.csv
- artists_prepared_for_wikidata.csv
- data_artists_enriched.csv

All notebooks and datasets are version-controlled and publicly documented.

---

# Tools & Technologies

| Tool | Purpose |
|------|---------|
| Anaconda | Development environment |
| Jupyter Notebook | Writing, testing and documenting Python code |
| Python | Programming language |
| Pandas | Data cleaning and analysis |
| Requests | HTTP requests to the Wikidata SPARQL endpoint |
| SPARQL | Query language for Wikidata |
| Wikidata | Metadata enrichment source |
| Git | Version control |
| GitHub | Open repository and reproducibility |
| ChatGPT (AI-assisted / Vibe Coding) | Assisted code generation, debugging, documentation and workflow design |

---

# Open Scholarship

This project follows Open Scholarship principles through:

- Open data (MoMA)
- Open knowledge graph (Wikidata)
- Open-source software (Python)
- Version control (GitHub)
- Transparent documentation
- Reproducible notebooks

---

# FAIR Principles

The project follows FAIR principles.

### Findable

The project is published on GitHub with a documented repository structure.

### Accessible

All datasets, notebooks and documentation are openly available.

### Interoperable

The dataset is linked with Wikidata using unique Wikidata identifiers.

### Reusable

The complete workflow is documented and reproducible using Jupyter Notebook.

---

# Results

The workflow produced the following outputs:

- Descriptive statistics
- Artists with complete metadata
- Artists requiring enrichment
- Enriched artist metadata linked to Wikidata
- Match status for every processed artist
- Reproducible notebooks
- GitHub repository

The final enriched dataset contains:

- Wikidata identifiers
- Birth Years recovered
- Death Years recovered
- Match Status
- Source information

---

# Key Findings

The project demonstrates that open knowledge graphs such as Wikidata can improve metadata quality for cultural heritage datasets.

The workflow successfully:

- Identified incomplete metadata
- Prepared the dataset for enrichment
- Retrieved missing metadata from Wikidata
- Applied entity matching
- Recorded match confidence
- Produced a reproducible Open Scholarship workflow

Remaining uncertain and not-found matches demonstrate the limitations of automatic entity matching and highlight opportunities for future improvements using additional authority files or more advanced disambiguation techniques.

---

# Future Work

Possible improvements include:

- Improving entity disambiguation
- Using additional authority files (e.g. VIAF, Getty ULAN)
- Expanding enrichment to additional metadata fields
- Improving matching confidence
- Automating validation of enriched metadata

---

# References

- Museum of Modern Art Collection Dataset
  https://www.kaggle.com/datasets/momanyc/museum-collection

- Wikidata
  https://www.wikidata.org/

- Wikidata SPARQL Endpoint
  https://query.wikidata.org/

- Python
  https://www.python.org/