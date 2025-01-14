# Type V Tn7 CAST Output

  - `canonical-pams.csv` PAM sequences from bona fide self-targeting systems
  - `cas12k-tns-minced-array.csv.gz` Putative Type V CASTs from the initial `gene_finder` run.
  - `other-pams.csv` PAM sequences from systems where we suspect the self-target annotation is an artifact and cannot be trusted
  - `reblasted-cas12k-with-sts-rules-deduped.csv.gz` Putative Type V CASTs after re-BLASTing with Cas12k as the seed.
  - `self-target-blastn-nt.csv` Results of running blastn with the NCBI nt database on target sequences.
  - `self-target-blastx-nr.csv` Results of running blastp with the NCBI nr database on target sequences.
  - `self-target-context-seqs.fa` DNA sequences 50 bp up/downstream of each target.
  - `unique-filenames.csv` Paths to raw sequence files for each CAST.
