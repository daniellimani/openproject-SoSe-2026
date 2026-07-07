# Museum of Modern Art (MoMA) Artist Metadata Enrichment and Analysis using Wikidata

## Project Overview

This project investigates the completeness and quality of metadata describing artists in the Museum of Modern Art (MoMA) collection.

The original dataset contains demographic information about artists, including:

- Artist Name
- Nationality
- Gender
- Birth Year
- Death Year

However, many records contain missing metadata, limiting the quality of statistical analysis and reducing the usefulness of the dataset for Digital Humanities research.

To address this problem, missing metadata were enriched using the **Wikidata Knowledge Graph** through automated entity matching implemented in Python.

The project demonstrates a complete Digital Humanities workflow including data preparation, metadata enrichment, evaluation, visualization, documentation, and publication following FAIR and Open Science principles.

---

# Motivation

Cultural heritage datasets are only as useful as the quality of their metadata.

Missing values affect the reliability of historical analysis because researchers cannot accurately answer questions such as:

- How many artists were born during a particular period?
- How has artistic diversity changed over time?
- What is the gender distribution of artists represented in museums?
- Which nationalities are underrepresented?

Without complete metadata, statistical analyses become incomplete and may lead to misleading conclusions.

Metadata enrichment improves the completeness of the dataset by recovering missing information from trusted external knowledge bases such as Wikidata.

Rather than changing existing information, the enrichment process only fills missing values while preserving the original dataset.

This produces a richer dataset that supports more accurate Digital Humanities research and improves semantic interoperability.

---

# Research Questions

This project addresses the following research questions:

1. How complete is the original MoMA artist metadata?

2. Which artists require metadata enrichment?

3. Can Wikidata successfully recover missing metadata?

4. How does metadata enrichment improve dataset completeness?

5. How does metadata enrichment support more reliable Digital Humanities research?

---

# Dataset

Source:

https://www.kaggle.com/datasets/momanyc/museum-collection

Dataset:

artists.csv

License:

Creative Commons CC0 1.0 Universal

https://creativecommons.org/publicdomain/zero/1.0/

Date accessed:

11 May 2026

---

# Dataset Description

The dataset contains metadata describing artists represented in the Museum of Modern Art collection.

Main variables include:

- Artist ID
- Name
- Nationality
- Gender
- Birth Year
- Death Year

Original dataset size:

**15,091 artists**

---

# Project Workflow

The project follows a complete Digital Humanities data lifecycle.

```
Original MoMA Dataset
        │
        ▼
Data Cleaning
        │
        ▼
Missing Value Detection
        │
        ▼
Dataset Preparation
        │
        ▼
Entity Matching with Wikidata
        │
        ▼
Metadata Enrichment
        │
        ▼
Impact Analysis
        │
        ▼
Visualisation
        │
        ▼
Documentation & GitHub Publication
```

---

# Methodology

## 1. Data Cleaning

The original dataset was inspected using Python and Pandas.

Cleaning included:

- detecting missing values
- checking dataset completeness
- descriptive statistics
- exporting clean subsets

---

## 2. Dataset Preparation

Artists missing one or more metadata fields were extracted into a new dataset.

Prepared dataset:

**10,525 artists**

These records became candidates for Wikidata enrichment.

---

## 3. Entity Matching

Each artist name was queried against the Wikidata API.

Potential matches were evaluated using:

- Name
- Birth Year
- Death Year
- Nationality
- Gender
- Occupation

Each record received one of four labels:

- matched
- uncertain
- not_found
- error

This process minimizes incorrect entity linking while maintaining high metadata quality.

---

## 4. Metadata Enrichment

Only missing metadata were filled.

Existing information was never overwritten.

Recovered metadata include:

- Wikidata ID
- Birth Year
- Death Year

---

## 5. Evaluation

The enriched dataset was compared against the original dataset to evaluate the overall impact of metadata enrichment.

Evaluation focused on:

- successful entity matches
- recovered metadata
- completeness improvement
- dataset quality

---

# Tools and Technologies

| Tool | Purpose |
|------|----------|
| Python | Data cleaning, enrichment and analysis |
| Pandas | Data manipulation |
| Requests | Wikidata API communication |
| Matplotlib | Data visualisation |
| Jupyter Notebook | Reproducible research |
| Git | Version control |
| GitHub | Repository hosting |
| Wikidata API | Metadata enrichment |
| Anaconda | Python environment |
| ChatGPT (Vibe Coding) | Assisted development, debugging and documentation |

---

# Results

## Original dataset

**15,091 artists**

---

## Artists requiring enrichment

**10,525 artists**

---

## Entity Matching Results

| Status | Artists |
|---------|---------:|
| Matched | 5,186 |
| Uncertain | 1,944 |
| Not Found | 3,375 |
| Error | 20 |

Overall successful match rate:

**49.3%**

<<<<<<< HEAD
=======
<img width="587" height="579" alt="image" src="https://github.com/user-attachments/assets/03714db5-18a4-4bf9-a506-b31978cb72a2" />


>>>>>>> 9e7a2169cd5a73b2174d3a26658331cb77089869
---

## Metadata Recovery

The enrichment workflow successfully recovered thousands of missing metadata values including:

- Birth Years
- Death Years
- Wikidata Identifiers

This substantially improves dataset completeness while preserving the original metadata.

---

# Why Metadata Enrichment Matters

Consider the following research question:

> **How many artists born between 1900 and 1950 are represented in the MoMA collection?**

### Before enrichment

Many artists had missing birth years.

These artists could not be included in chronological analyses.

Result:

<<<<<<< HEAD
❌ Incomplete statistics
=======
Incomplete statistics
>>>>>>> 9e7a2169cd5a73b2174d3a26658331cb77089869

---

### After enrichment

Thousands of missing birth years were recovered using Wikidata.

More artists can now be placed on historical timelines.

Result:

<<<<<<< HEAD
✅ More complete and reliable analyses.

Rather than claiming absolute truth, the enriched dataset provides a **more complete representation** of the available knowledge.

=======
More complete and reliable analyses.

Rather than claiming absolute truth, the enriched dataset provides a **more complete representation** of the available knowledge.

<img width="784" height="484" alt="image" src="https://github.com/user-attachments/assets/e1c9c81c-2e39-495d-b52b-7a22e02c0fbe" />


>>>>>>> 9e7a2169cd5a73b2174d3a26658331cb77089869
---

# Key Outcomes

The project demonstrates that metadata enrichment significantly improves cultural heritage datasets.

Main achievements include:

- Automated entity matching using Wikidata
- Recovery of missing metadata
- Improved dataset completeness
- More reliable demographic analysis
- Better support for Digital Humanities research
- Fully reproducible workflow
- Public GitHub repository with documentation

<<<<<<< HEAD
=======
<img width="683" height="384" alt="image" src="https://github.com/user-attachments/assets/5a39c86b-51a1-439b-97d0-0079ead6ea01" />


>>>>>>> 9e7a2169cd5a73b2174d3a26658331cb77089869
---

# FAIR Principles

The project follows the FAIR principles.

### Findable

- GitHub repository
- Structured documentation

### Accessible

- Open dataset
- Open-source code

### Interoperable

- Wikidata identifiers enable semantic interoperability

### Reusable

- Documented workflow
- Version-controlled repository
- Reproducible notebooks

---

# Open Science

The project promotes Open Science by providing:

- Open-source code
- Public documentation
- Reproducible notebooks
- Public datasets
- Version control using Git
- Transparent methodology

---

# Repository Structure

```
project/

│

├── data/

│   ├── artists.csv

│   ├── artists_statistics.csv

│   ├── artists_all_fields_complete.csv

│   ├── artists_missing_dates.csv

│   ├── artists_prepared_for_wikidata.csv

│   ├── data_artists_enriched.csv

│   ├── enrichment_summary.csv

│   └── project_summary.csv

│

├── notebook/

│   ├── create_update_notebook.ipynb

│   ├── Data_enrichment.ipynb

│   └── Results_analysis.ipynb

│

├── README.md

└── .gitignore
```

---

# Future Work

Possible future improvements include:

- SPARQL-based semantic queries
- Additional metadata fields
- Occupation enrichment
- Place of birth enrichment
- Museum collection comparison
- Improved entity disambiguation using machine learning
- Integration with Linked Open Data resources

---

# References

Museum of Modern Art Collection

https://www.moma.org/

MoMA Dataset

https://www.kaggle.com/datasets/momanyc/museum-collection

Wikidata

https://www.wikidata.org/

Wikidata API

https://www.wikidata.org/w/api.php

FAIR Principles

<<<<<<< HEAD
https://www.go-fair.org/fair-principles/
=======
https://www.go-fair.org/fair-principles/
>>>>>>> 9e7a2169cd5a73b2174d3a26658331cb77089869
