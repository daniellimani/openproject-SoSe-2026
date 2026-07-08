# Museum of Modern Art (MoMA) Artist Metadata Enrichment and Analysis using Wikidata

## Project Overview

This project enriches the **Museum of Modern Art (MoMA) Artist Dataset** using **Wikidata** to improve the completeness and reliability of artist metadata.

Rather than simply filling missing values, the project demonstrates how **Linked Open Data (LOD)** can enhance cultural heritage datasets while preserving their original integrity.

The enrichment process automatically retrieves and validates missing information such as:

- Birth Year
- Death Year
- Nationality
- Gender
- Wikidata Identifier (Q-ID)

Only missing metadata is updated, ensuring that existing records remain unchanged.

The resulting enriched dataset enables more accurate demographic and historical analyses of the MoMA artist collection.

---

# Project Highlights

| Metric | Value |
|---------|------:|
| Original Artists | **15,091** |
| Artists Prepared for Enrichment | **10,525** |
| Successfully Matched | **5,186** |
| Not Found | **3,375** |
| Uncertain Matches | **1,944** |
| API Errors | **20** |

---

# Motivation

Museum collections are increasingly used in research within **Digital Humanities**, **Data Science**, **Art History**, and **Cultural Heritage**. However, many publicly available datasets contain incomplete or missing metadata.

Missing information makes it difficult to answer important research questions such as:

- Which nationalities are most represented?
- What is the gender distribution of artists?
- Which historical periods are most represented?
- How diverse is the museum collection?

Without complete metadata, visualisations often represent **missing information rather than reality**, producing incomplete or misleading conclusions.

Linked Open Data resources such as **Wikidata** provide a scalable solution for enriching existing datasets while maintaining their original information.

The objective of this project is therefore not simply to increase completeness, but to improve the quality and reliability of future analyses.

---

# Research Questions

This project investigates the following questions:

1. How complete is the original MoMA artist dataset?
2. Can Wikidata successfully enrich missing artist metadata?
3. How many artists can be confidently matched automatically?
4. Which metadata fields benefit the most from enrichment?
5. How does metadata enrichment improve downstream analyses?
6. What limitations remain after enrichment?

---

# Dataset

## Source

Museum of Modern Art (MoMA)

https://www.moma.org/

Dataset

https://www.kaggle.com/datasets/momanyc/museum-collection

External Knowledge Base

https://www.wikidata.org/

Wikidata API

https://www.wikidata.org/w/api.php

---

# Dataset Description

The dataset contains metadata describing artists represented in the Museum of Modern Art collection.

Important attributes include:

- Artist ID
- Artist Name
- Nationality
- Gender
- Birth Year
- Death Year

Several records contain missing metadata, motivating the enrichment process.

---

# Project Workflow

```text
Original MoMA Dataset
        │
        ▼
Data Cleaning
        │
        ▼
Prepare Artists
        │
        ▼
Query Wikidata API
        │
        ▼
Entity Matching
        │
        ├── Matched
        ├── Uncertain
        ├── Not Found
        └── Error
        │
        ▼
Update Missing Metadata
        │
        ▼
Generate Enriched Dataset
        │
        ▼
Analysis & Visualisation
```

---

# Methodology

## 1. Data Cleaning

The original dataset was inspected and prepared by:

- removing invalid values
- checking missing metadata
- standardising artist names
- preparing records for API queries

---

## 2. Metadata Enrichment

Each artist name was queried using the Wikidata API.

Candidate entities were evaluated using available metadata including:

- Name
- Nationality
- Gender
- Birth Year
- Death Year

The best candidate was automatically selected whenever possible.

---

## 3. Entity Matching

Each artist was assigned one of four matching outcomes.

| Status | Description |
|---------|-------------|
| Matched | Reliable Wikidata entity identified |
| Uncertain | Multiple candidate entities remained |
| Not Found | No suitable Wikidata entity available |
| Error | API or processing error |


---

## 4. Dataset Update

Only missing metadata was enriched.

Existing values were preserved, ensuring that the original dataset remained unchanged.

---

<img width="763" height="361" alt="image" src="https://github.com/user-attachments/assets/c8de97d1-1475-4e9d-adae-05fe35ab2650" />


# Results

## Entity Matching Performance

<img width="784" height="484" alt="image" src="https://github.com/user-attachments/assets/c95fd964-0a58-46c1-84ac-1af038929081" />


### Interpretation

The enrichment pipeline successfully matched approximately half of all queried artists.

Only a very small number of API errors occurred.

Remaining unmatched artists were mainly due to ambiguous names or unavailable Wikidata records.

The results demonstrate that Linked Open Data can substantially improve metadata completeness while maintaining data quality.

---

# Why Metadata Enrichment Matters

Completeness is not the final objective.

The real objective is obtaining **more reliable analyses**.

> **What is the gender distribution of artists represented in the MoMA collection?**

### Before enrichment

Many artists contained missing gender information.

Any analysis underestimated the true number of male and female artists, resulting in biased conclusions.

### After enrichment

Thousands of missing values were completed using Wikidata.

The resulting visualisation provides a much more realistic representation of the museum collection.

Instead of analysing missing information, I am analysing the artists themselves.

This illustrates the practical value of metadata enrichment.

<img width="784" height="484" alt="image" src="https://github.com/user-attachments/assets/025328d4-774d-4f5e-8ca7-f3416868a524" />


---

# Key Findings

### Interpretation

Metadata enrichment significantly reduced missing gender values.

As a conclusion:

- demographic analyses became more reliable;
- the proportion of unknown values decreased;
- visualisations better reflected the actual museum collection;
- conclusions drawn from the dataset became more representative of reality.

<img width="683" height="384" alt="image" src="https://github.com/user-attachments/assets/025d0159-5487-4d29-9eff-30019a647f97" />


---

# Key Outcomes

This project demonstrates that:

- Linked Open Data can significantly improve museum datasets.
- Automatic entity matching can successfully enrich thousands of records.
- Existing metadata can be preserved while enriching only missing values.
- Enriched datasets produce analyses that are considerably closer to reality.
- Reproducible enrichment pipelines can support future cultural heritage research.

---

# Tools & Technologies

| Tool | Purpose |
|-------|---------|
| Python | Data Processing |
| Pandas | Data Manipulation |
| Requests | Wikidata API |
| Matplotlib | Visualisation |
| Jupyter Notebook | Analysis |
| Git | Version Control |
| GitHub | Repository Hosting |

---

# FAIR Principles

This project follows the FAIR principles.

### Findable

- Public GitHub repository
- Public dataset License - CC0: Public Domain https://creativecommons.org/publicdomain/zero/1.0/ 
- Wikidata identifiers

### Accessible

- Open APIs
- Open datasets
- Public documentation

### Interoperable

- CSV files
- Standard metadata
- Wikidata identifiers

### Reusable

- Open-source implementation
- Reproducible workflow
- Well-documented notebooks

---

# Open Scholarship

This project promotes Open Scholarship through:

- Open-source implementation
- Reproducible analyses
- Public datasets
- Open APIs
- Transparent methodology
- Version-controlled development

---

# Repository Structure

```text
openproject-SoSe-2026/
│
├── data/
│   ├── artists.csv
│   ├── artists_prepared_for_wikidata.csv
│   ├── data_artists_enriched.csv
│   ├── artists_statistics.csv
│   ├── enrichment_summary.csv
│   ├── artists_missing_dates.csv
│   └── artists_all_fields_complete.csv
│
├── notebook/
│   ├── create_update_notebook.ipynb
│   ├── Data_enrichment.ipynb
│   ├── impacts_and_results.ipynb
│   └── results_and_analysis.ipynb
│
├── images/
│   ├── entity_matching_results.png
│   ├── gender_results.png
│   └── ...
│
├── README.md
└── .gitignore
```

---

# Limitations

Although the enrichment pipeline significantly improves metadata completeness, several limitations remain.

- Ambiguous artist names cannot always be resolved automatically.
- Wikidata itself may contain incomplete or outdated information.
- API rate limits affect processing speed.
- Some uncertain matches still require manual verification.

---

# Future Work

Future improvements may include:

- SPARQL-based semantic enrichment
- Occupation enrichment
- Place of birth and death enrichment
- Artistic movement enrichment
- Integration with additional Linked Open Data sources
- Machine Learning for entity disambiguation
- Compare the MoMA dataset with other museum collections
- Improve matching by incorporating additional metadata fields


---

# References

Museum of Modern Art

https://www.moma.org/

MoMA Dataset

https://www.kaggle.com/datasets/momanyc/museum-collection

Wikidata

https://www.wikidata.org/

Wikidata API

https://www.wikidata.org/w/api.php
