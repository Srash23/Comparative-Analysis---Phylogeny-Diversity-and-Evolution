# Comparative Genomics and Phylogenetic Analysis of Fungal ITS and Bacterial Genomes

This repository presents a comprehensive bioinformatics pipeline for comparative genome analysis using fungal ITS sequences and bacterial genome annotations. We combine sequence annotation, codon usage evaluation, GC skew analysis, genome visualization, protein metadata retrieval, and phylogenetic modeling to extract evolutionary and structural insights.

## Project Overview
The goal of this project is to integrate functional and evolutionary genomics through:
- Genomic sequence parsing and annotation (E. coli)
- GC content and coding distribution profiling
- Protein function exploration via SwissProt and PDB
- ITS region analysis and comparative phylogeny of industrially relevant fungi

We leverage Biopython, MAFFT, FastTree, and scikit-bio for data processing, alignment, and visualization.

## Objectives
- Annotate CDS and non-coding regions of bacterial genomes
- Perform GC skew and cumulative skew analysis to locate replication origin and terminus
- Compare GC content between CDS and intergenic regions
- Explore protein metadata via ExPASy/SwissProt
- Analyze and align ITS sequences of 15 fungal species
- Construct and visualize a phylogenetic tree using FastTree
- Evaluate sequence conservation, positional entropy, and pairwise distance matrices

## Dataset Description
**Input Files:**
- `fungi.ITS.fna`: Fungal ITS sequences from NCBI RefSeq
- `GCF_000005845.2_ASM584v2_genomic.fna`: E. coli genome
- `GCF_000005845.2_ASM584v2_genomic.gbff`: E. coli GenBank annotation
- `e_coli_plasmid.gb`: Plasmid file for genome diagram

**Tools and Packages:**
- Biopython, MAFFT, FastTree, scikit-bio, reportlab, NGLView

## Pipeline Summary

### 1. Genome Annotation and CDS Analysis
- Parse GenBank files to extract CDS, gene, and replication origin features
- Quantify coding coverage and perform GC content analysis (CDS vs non-CDS)

### 2. Functional Exploration
- Use ExPASy and SwissProt to retrieve function metadata
- Fetch and view 3D PDB protein structures with NGLView

### 3. ITS Sequence Processing and Alignment
- Parse fungal ITS sequences and extract metadata
- Select 15 industrially relevant fungal species (e.g., *Aspergillus*, *Penicillium*, *Saccharomyces*)
- Multiple sequence alignment using MAFFT

### 4. Phylogenetic Tree Construction
- Build Newick tree using FastTree
- Visualize annotated phylogenetic trees with Biopython

### 5. Conservation and Distance Metrics
- Calculate sequence conservation (Shannon entropy)
- Compute pairwise Hamming distance matrix
- Perform Principal Coordinate Analysis (PCoA)

## Key Results
- E. coli genome: 4.6 Mb with >86% coding density
- GC skew infers origin and terminus of replication
- CDS GC content is significantly higher than non-CDS
- Annotated tree reveals phylogenetic separation of toxic, industrial, and food-related fungi
- Sequence conservation metrics distinguish conserved vs variable ITS positions

## Visualizations

### 1. Circular Genome Diagram
Depicts annotated genes from the E. coli plasmid GenBank file with labeled directionality.
<img width="741" alt="Screenshot 2025-04-21 at 3 39 05 PM" src="https://github.com/user-attachments/assets/c59450f7-fc26-460a-8786-65aa756bffa7" />

### 2. GC Content Distribution Histogram
Shows the contrast in GC content between coding and non-coding regions.
<img width="549" alt="Screenshot 2025-04-21 at 3 39 58 PM" src="https://github.com/user-attachments/assets/34b2484d-8174-4d34-828f-46268880a847" />

### 3. Phylogenetic Tree (Annotated)
Visualizes fungal evolutionary relationships with genus/species annotations.
<img width="791" alt="Screenshot 2025-04-21 at 3 55 58 PM" src="https://github.com/user-attachments/assets/7b95215a-8595-43f7-aa1d-a408e0603599" />

### 4. PCoA Plot of Fungal ITS Sequences
Demonstrates clustering by genus using principal coordinate analysis of Hamming distances.
<img width="581" alt="Screenshot 2025-04-21 at 3 40 53 PM" src="https://github.com/user-attachments/assets/49207904-befb-4d8d-b89e-363e7bc6e582" />
<img width="393" alt="Screenshot 2025-04-21 at 3 41 18 PM" src="https://github.com/user-attachments/assets/0207f0b4-4b11-41e3-992e-7a28ab4dcae4" />

### 5. Sequence Conservation Profile
Plots conservation across aligned ITS regions using inverse Shannon entropy.
<img width="432" alt="Screenshot 2025-04-21 at 3 56 47 PM" src="https://github.com/user-attachments/assets/1551861e-f6b5-4ea4-b8eb-0d65a9142106" />

## Tech Stack
- **Languages**: Python (Biopython, pandas, matplotlib)
- **Alignment Tools**: MAFFT, FastTree
- **Structural Viz**: NGLView, ReportLab GenomeDiagram
- **Distance & Tree Analysis**: scikit-bio, ete3, skbio.stats

## Scalability
This pipeline is designed for cross-species analysis and genome exploration:
- Easily extendable to other genomic formats and organisms
- Modular code blocks for integration into larger workflows
- Scalable to hundreds of sequences via optimized alignment and tree-building tools

## Example Applications
- Functional annotation of microbial genomes
- Phylogenetic clustering of fungi for industrial relevance
- Codon usage and genome structural insights
- Educational pipeline for teaching comparative genomics

## Acknowledgements
- NCBI RefSeq for genomic and ITS sequence data
- SwissProt and ExPASy for protein metadata
- BioPython community and scikit-bio developers

## License
MIT License
