# Viral Genome Mutation Analysis  

## Project Overview  
This project focuses on analyzing the genome of **Nipah henipavirus isolate MCL-21-H-9808** to:  
1. Identify the genes present in the viral genome.  
2. Determine the function of those genes.  
3. Compare the viral genome with its closest relatives.  
4. Detect mutations in the viral genome.  
5. Predict the impact of mutations on gene function and protein structure.  

The genome, retrieved from **NCBI**, was analyzed for ORFs (Open Reading Frames), protein sequences, and structural changes due to mutations.  

---

## Problem Statement  
**Objective**: Analyze the viral genome to identify mutations and predict their potential impact on the viral properties, particularly the function and structure of critical proteins.  

---

## Data Sources  
- **Viral Genome Sequence**: NCBI Accession Number OM135495  
- **Protein Database**: UniProt and RCSB Protein Data Bank (PDB)  
- **Gene Finder Tools**: NCBI ORF Finder, BLAST, and UniProt Tools  

---

## Tools & Technologies  
- **ORF Identification**: NCBI ORF Finder  
- **Sequence Alignment**: BLASTn, MUSCLE, Clustal Omega  
- **Mutation Analysis**: Jalview  
- **Protein Visualization**: UniProt + 3D PDB Structures  
- **Programming**: Python (for data cleaning and processing)  

---

## Methodology  

### 1. Gene Identification  
- Retrieved the viral genome (18,005 bp) and identified **Open Reading Frames (ORFs)** using NCBI ORF Finder.  
- Parameters:  
   - Minimum ORF length: **150 bp**  
   - Start Codon: ATG (and alternative codons)  

### 2. Protein Functional Annotation  
- Verified ORFs by matching predicted proteins against **UniProtKB** using BLASTp.  
- Recorded the closest protein matches, functions, and structural details.  

### 3. Mutation Detection  
- Compared ORF sequences with related viral sequences using:  
   - **BLASTn** for sequence similarity  
   - **MUSCLE** and **Jalview** for multiple sequence alignment and mutation analysis.  
- Identified **substitution mutations** and analyzed their impact on amino acid charge, size, and polarity.  

### 4. Functional Impact of Mutations  
- Assessed the structural and functional changes due to mutations by examining:  
   - Changes in amino acid properties (charge, size, and shape).  
   - Their potential effect on protein stability and interactions.  

---

## Key Findings  

### Genes & Proteins Identified  
| **ORF** | **Protein Name**                   | **UniProt ID** | **Function**                                                                 |
|---------|-----------------------------------|---------------|-----------------------------------------------------------------------------|
| ORF 5   | RNA-directed RNA Polymerase       | Q997F0        | Transcribes viral mRNAs and replicates viral RNA.                           |
| ORF 2   | Phosphoprotein                    | Q9IK91        | Positions polymerase and inhibits host antiviral responses.                |
| ORF 4   | Glycoprotein G                    | Q9IH62        | Provides virion attachment to target cells.                                |
| ORF 3   | Fusion Glycoprotein F0            | Q9IH63        | Facilitates viral and cellular membrane fusion.                            |
| ORF 8   | Nucleoprotein                     | Q9IK92        | Protects the viral genome and serves as a replication template.            |
| ORF 9   | Matrix Protein                    | Q9IK90        | Mediates virion assembly and inhibits host immune response.                |

### Mutation Analysis  
- **ORF 5, 6, and 7**: Originally predicted to be part of the same protein, RNA polymerase, but broken into separate ORFs due to ambiguous regions (NNNN chains).  
- **Mutations Detected**:  
   - Substitution mutations affecting amino acid charge, size, and polarity.  
   - Potential changes in protein structure and functionality.  

---

## Results Summary  
1. **Overlapping ORFs**: Overlapping genes (ORF 5, 6, 7) were part of the same protein (RNA polymerase).  
2. **Mutation Effects**:  
   - Key mutations altered amino acid properties, potentially impacting protein interactions and stability.  
   - Some regions with missing data (N-values) caused issues in analysis.  
3. **Closest Relatives**: BLAST results identified the closest genome matches for comparison.  

---

## Conclusions  
- The project successfully identified and annotated genes within the Nipah virus genome.  
- Detected mutations in critical proteins and predicted their functional impact using sequence alignment and visualization tools.  
- The findings contribute to a deeper understanding of viral evolution and mutation-driven adaptations.  

---

## Future Directions  
- Conduct experimental validation of identified mutations and their impact on viral proteins.  
- Expand the analysis to other viral isolates for a comparative evolutionary study.  
- Use molecular modeling tools (e.g., PyMOL) to simulate structural changes caused by mutations.  

---

## File Organization  
- **data/**: Raw genome sequence, ORF tables, and protein sequences.  
- **results/**: Mutation tables, BLAST results, and functional annotations.  
- **scripts/**: Python scripts for data analysis and cleaning.  
- **docs/**: Report PDF and supplementary references.  

---

## Citation  
Please cite the following works:  
- NCBI ORF Finder: [https://www.ncbi.nlm.nih.gov/orffinder](https://www.ncbi.nlm.nih.gov/orffinder)  
- UniProtKB: [https://www.uniprot.org/](https://www.uniprot.org/)  
- Jalview: [https://www.jalview.org/](https://www.jalview.org/)  
