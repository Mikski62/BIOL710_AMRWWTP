---
YAML tags:
  pretty_name: "Metagenomic Insights into AMR Gene Prevalence in Municipal Wastewater: A One Health Approach"
  task_categories:
    - structured-data-classification
    - other:metagenomic-annotation
  language:
    - en
  license: mit
  size_categories:
    - n<1K
  source_datasets:
    - original
  annotations_creators:
    - found
  multilinguality: monolingual
---

# Metagenomic Insights into AMR Gene Prevalence in Municipal Wastewater: A One Health Approach

## Table of Contents
- [Dataset Description](#dataset-description)
- [Dataset Structure](#dataset-structure)
- [Dataset Creation](#dataset-creation)
- [Considerations for Using the Data](#considerations-for-using-the-data)
- [Additional Information](#additional-information)

## Dataset Description

- **Homepage:** N/A
- **Repository:** https://github.com/Mikski62/BIOL710_AMRWWTP
- **Paper:** https://doi.org/10.1101/2024.11.06.24316840
- **Leaderboard:** N/A
- **Point of Contact:** Michael Hajkowski – mhajkowski@sfsu.edu

### Dataset Summary

This dataset includes metagenomic data from influent samples collected at a municipal wastewater treatment plant. It documents microbial community structure and antimicrobial resistance (AMR) gene presence, supporting One Health-oriented research. It was created to apply and evaluate the Resistance Persistence Index (RPI) for AMR gene burden. The dataset is in English and formatted for classification and annotation tasks.

### Supported Tasks and Leaderboards

- `structured-data-classification`: Enables modeling microbial or AMR gene presence using structured tabular data.
- `other:metagenomic-annotation`: Supports annotation or unsupervised exploration of microbial sequences and AMR gene presence.

### Languages

English (`en`) metadata with Latin taxonomic annotations for microbial taxa.

## Dataset Structure

### Data Instances

```json
{
  "SampleID": "Influent_01",
  "CollectionDate": "2023-08-10",
  "Location": "WWTP",
  "ReadCount": 384710,
  "Taxa_Proteobacteria": 0.45,
  "Taxa_Bacteroidetes": 0.22,
  "AMR_Genes_Detected": ["tetA", "blaTEM", "sul1"]
}
```

### Data Fields

- `SampleID`: (string) Unique ID per sample.
- `CollectionDate`: (date) Sample collection date.
- `Location`: (string) Generalized WWTP label.
- `ReadCount`: (int) Sequencing depth post-QC.
- `Taxa_*`: (float) Relative microbial abundance.
- `AMR_Genes_Detected`: (list) AMR genes present in each sample.

### Data Splits

| Split | Samples |
|-------|---------|
| main  | 8       |

## Dataset Creation

### Curation Rationale

The dataset was created to evaluate AMR risk using a newly proposed RPI framework and to contribute to wastewater-based surveillance of public health threats.

### Source Data

#### Initial Data Collection and Normalization

Samples were collected, concentrated with Nanotrap particles, DNA-extracted (NucleoMag), and sequenced with Illumina. CZ-ID pipeline was used for bioinformatic analysis.

#### Who are the source language producers?

Microbial taxa in environmental wastewater. Metadata and interpretation by the researchers.

### Annotations

#### Annotation process

CZ-ID and CARD used for computational annotation. Manual curation where appropriate.

#### Who are the annotators?

Annotations were generated computationally and reviewed by the research team, led by Michael Hajkowski.

### Personal and Sensitive Information

No human-identifiable information is present. All data are derived from anonymized environmental sampling.

## Considerations for Using the Data

### Social Impact of Dataset

Helps track AMR trends at a community level through environmental surveillance. Supports public health interventions via the One Health framework.

### Discussion of Biases

May be biased by database limitations or sequencing method bias. Small sample size also limits generalization.

### Other Known Limitations

Limited sample size and lack of temporal scope. Future work should include seasonal variation.

## Additional Information

### Dataset Curators

Michael Hajkowski 

### Licensing Information

MIT License: https://opensource.org/licenses/MIT

### Citation Information

```
@article{hajkowski2024rpi,
  author    = {Hajkowski, M. et al.},
  title     = {A Resistance Persistence Index (RPI) for antimicrobial resistance in wastewater},
  journal   = {medRxiv},
  year      = {2024},
  doi       = {10.1101/2024.11.06.24316840}
}
```

### Contributions

Thanks to [@Mikski62](https://github.com/Mikski62) for compiling and sharing this dataset.