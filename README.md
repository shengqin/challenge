# Visium Spatial Transcriptomics: Spot Pre-filtering for Deconvolution

Pre-processing notebook from my 2023 work on Hodgkin lymphoma spatial transcriptomics, started at the Stanford Data Science (SSDS) bootcamp.

## What `052323_Visium.Rmd` does
For each 10x Visium sample (Space Ranger outputs: `matrix.mtx.gz`, `barcodes.tsv.gz`, `features.tsv.gz`, `tissue_positions_list.csv`), it:
1. Loads the sparse count matrix and maps spots to tissue coordinates.
2. Keeps the genes in a single-cell-derived Hodgkin lymphoma signature matrix.
3. Drops spots with no signature-gene expression.
4. Writes a filtered, Space Ranger–formatted sample folder (`<id>_min1sig/`) that is ready for cell-state deconvolution (EcoTyper).

**Stack:** R (Matrix, stringr)

Input data are not included. Paths in the notebook point to local and lab storage, so edit them to run elsewhere.
