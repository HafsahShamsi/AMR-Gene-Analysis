# Antibiotic Resistance Gene Analysis
### Detecting AMR genes in bacterial genomes using Biopython and NCBI data

**Tools:** Python · Biopython · Pandas · Matplotlib · NCBI Entrez  
**Data:** NCBI public genomic sequences (fetched via Biopython)  
**Author:** Hafsah Shamsi · Microbiology + Data Science · Mithibai College, Mumbai

---

## Overview

This project analyses publicly available bacterial genome sequences from NCBI to identify and characterise antibiotic resistance (AMR) genes — sequences that allow bacteria to survive exposure to antibiotics.

Antimicrobial resistance is one of the most significant global health threats. Understanding which resistance genes are present in which bacterial strains, and how they are distributed, is foundational to both clinical microbiology and drug discovery research.

This is the project where the two halves of my degree directly meet: microbiology domain knowledge about resistance mechanisms, and computational tools (Biopython, sequence parsing, NCBI API) to analyse genomic data at scale.

---

## What this project does

- Fetches bacterial genome sequences from NCBI using the Entrez API
- Parses GenBank records with Biopython to extract annotated features
- Identifies resistance-associated genes by keyword and annotation
- Visualises gene distribution across strains
- Produces a summary of resistance profiles

---

## Charts produced

| File | Description |
|---|---|
| `amr_gene_distribution.png` | Frequency of AMR gene families across analysed sequences |
| `resistance_profile.png` | Antibiotic class coverage by strain |
| `gc_content.png` | GC content analysis of identified resistance genes |

---

## How to run

```bash
git clone https://github.com/HafsahShamsi/amr-gene-analysis.git
cd amr-gene-analysis
pip install biopython pandas matplotlib seaborn jupyter
```

Set your NCBI email in the notebook (required for Entrez API access), then:

```bash
jupyter notebook amr_gene_analysis.ipynb
```

---

## Biological context

AMR genes encode proteins that neutralise antibiotics through several mechanisms:
- **Efflux pumps** — actively pump antibiotics out of the cell
- **Enzymatic degradation** — enzymes like beta-lactamases break down antibiotics
- **Target modification** — altering the antibiotic's binding site
- **Reduced permeability** — modified cell wall prevents antibiotic entry

The genes identified in this project map to these known resistance mechanisms, connecting sequence-level analysis to clinical microbiology outcomes.

---

## What I learned

- Biopython's `Entrez` module for programmatic NCBI access
- GenBank record parsing and feature extraction
- Sequence analysis and annotation in Python
- Connecting genomic data to biological function
- Building a bioinformatics pipeline from data fetch to visualisation

---

## Next steps

- [ ] Expand to larger genome datasets
- [ ] Add phylogenetic analysis — how are resistance genes distributed evolutionarily?
- [ ] Compare resistance profiles across clinical vs environmental isolates
- [ ] Extend toward autoimmune-related genomic analysis pipelines
