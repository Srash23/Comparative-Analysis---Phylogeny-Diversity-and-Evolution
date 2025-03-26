# Comparative Analysis - Phylogeny Diversity and Evolution

## Overview
This project explores fungal diversity through a comparative analysis of the Internal Transcribed Spacer (ITS) region — a well-established molecular barcode for fungi. The framework presented here is modular, reproducible, and designed to scale for use across fungal species, strains, and environments.

1. Whether you're interested in taxonomy, evolutionary biology, industrial microbiology, or bioinformatics workflows, this project gives you a ready-to-use pipeline for:

2. Visualizing taxonomic distributions

3. Performing multiple sequence alignments

4. Building phylogenetic trees

5. Exploring evolutionary distances via PCoA/MDS

6. Measuring sequence conservation across aligned regions

## Introduction
The Internal Transcribed Spacer (ITS) region is one of the most widely used molecular markers in fungal phylogenetics and taxonomy. Its high variability across species, combined with conserved flanking regions, makes it ideal for identifying and differentiating fungal taxa.

This project presents a comparative genomics framework that uses ITS sequences to analyze phylogeny, diversity, and evolutionary patterns among key fungal genera. The focus is on industrially and medically relevant fungi, _Aspergillus_, _Penicillium_, and _Saccharomyces_, enabling insights into their genetic relationships, divergence, and potential evolutionary constraints.

In a broader context, this analysis sets the foundation for scaling up to full-genome comparisons, environmental sampling, and strain-level epidemiology.

## What This Project Does
#### Input
A .fna or .fasta file containing ITS sequences (e.g., fungi.ITS.fna from NCBI or UNITE)

#### Output
1. Cleaned and annotated sequence metadata

2. Aligned sequences using MAFFT

3. Maximum likelihood tree with FastTree

4. Interactive PCA-style PCoA visualization

5. Sequence conservation profile

## Workflow
**Data Collection**

1. Retrieved ITS sequences from public databases (e.g., NCBI RefSeq, UNITE).

2. Focused on a curated list of 14 well-known fungal species across Aspergillus, Penicillium, and Saccharomyces.

**Preprocessing & Metadata Annotation**

1. Extracted scientific names and cleaned FASTA headers.

2. Mapped genus and species information for downstream grouping.

**Sequence Alignment**

1. Used MAFFT for multiple sequence alignment (MSA) to ensure structural consistency and gap management.

2. Alignment file saved in FASTA format for reuse and reproducibility.

**Phylogenetic Tree Construction**

1. Employed FastTree to infer a maximum-likelihood tree from aligned sequences.

2. Exported tree in Newick format and visualized using Biopython’s Phylo module.

**Evolutionary Distance and Dimensionality Reduction**

1. Calculated pairwise Hamming distances from aligned sequences (excluding gaps).

2. Used MDS (Multi-Dimensional Scaling) to project distances into 2D space for visualization of evolutionary clusters.

**Sequence Conservation Analysis**

1. Used skbio’s TabularMSA to compute positional conservation across the alignment.

2. Plotted conservation scores to identify hotspots of variation and conserved motifs.

![You can visualize the results using a three-panel figure showing the following_ - visual selection](https://github.com/user-attachments/assets/01985834-76a1-4876-8ff2-0e31b0ed920b)


## Main Results (from Current Notebook)
**1. Top Genera:**	Dominance of Aspergillus, Penicillium, and Saccharomyces

**2. Tree:**	Well-separated clades, Some intra-genus diversity observed in Aspergillus and Penicillium.

**3. PCoA Plot:**	Distinct clusters per genus — supports evolutionary divergence. Saccharomyces species cluster tightly — consistent with low variability. Aspergillus and Penicillium show wider spread.

**4. Conservation:**	ITS has high variability — Key regions of high variation useful for species delimitation.

## Tools & Libraries Used
1. BioPython (SeqIO, AlignIO, Phylo, MAFFT & FastTree interfaces)

2. skbio (TabularMSA, distance metrics)

3. matplotlib, pandas, numpy, scikit-learn

## Conclusion
This project demonstrates the power of ITS-based comparative analysis in uncovering fungal diversity, evolutionary relationships, and taxonomic structure. With scalable components and flexible visualization, the framework is ready to be deployed on broader datasets — from environmental sequencing to fungal pathogen surveillance.

As sequencing technologies and databases continue to grow, this pipeline can serve as a foundational tool for researchers, educators, and enthusiasts diving into the fascinating world of fungal genomics.

