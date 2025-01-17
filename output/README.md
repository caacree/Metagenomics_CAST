This folder contains the following: 

  - `nontn7` Intermediate data files for non-Tn7 CASTs
  - `tn7` Intermediate data files for Type I and Type IV Tn7 CASTs
  - `tn7-type-v` Intermediate data files for Type V Tn7 CASTs

Intermediate data files representing CAST systems are in a format used by our custom-built [pipeline](https://github.com/wilkelab/Opfi), where each row represents one annotated feature in a candidate CAST system. Column descriptions are given in the table below. 

| index | field name      | data type  | description                                                                                                                                        |
|-------|-----------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Contig          | string     | ID/accession for the parent contig/genome sequence.                                                                                                |
| 1     | Loc_coordinates | string     | Start and end position of the candidate locus (relative to the parent sequence).                                                                   |
| 2     | Name            | string     | Feature name/label. This is will be identical to “Description” (index 8) if ``parse_descriptions`` is ``True``.                                    |
| 3     | Coordinates     | string     | Start and end position of this feature, relative to the parent sequence.                                                                           |
| 4     | ORFID           | string     | A unique ID given to this feature, primarily for internal use. Only applies to features that are genes.                                            |
| 5     | Strand          | signed int | Specifies if the feature was found in the forward (1) or backward (-1) direction. Only applied to features that are genes.                         |
| 6     | Accession       | string     | ID/accession for the reference sequence that had the best alignment (by e-value) with this feature’s translated sequence.                          |
| 7     | E_val           | float      | The e-value score for the best alignment for this feature.                                                                                         |
| 8     | Description     | string     | A description of this putative feature, parsed from the defline of best aligned reference sequence.                                                |
| 9     | Sequence        | string     | The (translated) amino acid sequence for this feature.                                                                                             |
| 10    | Bitscore        | float      | The bitscore for the best alignment for this feature.                                                                                              |
| 11    | Rawscore        | int        | The raw score for the best alignment for this feature.                                                                                             |
| 12    | Aln_len         | int        | The length of the best scoring alignment, in base pairs.                                                                                           |
| 13    | Pident          | float      | The fraction of identical positions in the best alignment.                                                                                         |
| 14    | Nident          | int        | The number of identical positions in the best alignment.                                                                                           |
| 15    | Mismatch        | int        | The number of mismatched positions in the best alignment.                                                                                          |
| 16    | Positive        | int        | The number of positive-scoring matches in the best alignment.                                                                                      |
| 17    | Gapopen         | int        | The number of gap openings.                                                                                                                        |
| 18    | Gaps            | int        | Total number of gaps in the alignment.                                                                                                             |
| 19    | Ppos            | float      | Percentage of positive scoring matches.                                                                                                            |
| 20    | Qcovhsp         | int        | Query coverage per HSP. That is, the fraction of the query (this feature’s translated amino acid sequence) that was covered in the best alignment. |
| 21    | Contig_filename | string     | The input data (genomic sequence(s)) file path.                                                                                                    |
