# Network Analysis Collaboration Repo

Here's one place for maintaining computational network integration methods, data, and results for the Cox and Hawn Labs and the TBRU.

### First Approach - Union of Unweighted Shortest Paths
Starting in a subnetwork of STRING limited to significant proteins from network propagation on any of the ataqseq, methylation, snp, rnaseq, and proteomics, calculate shortest paths from each Crispr KO/KD immune screen hit to each TB secreted factor PPI. Take the union of shortest paths as the subnetwork of interest and apply network analyses to it.

Crispr KO/KD data taken from [TBRU_integration_data](https://github.com/hawn-lab/TBRU_integration_data/tree/main/data_clean).

**Ideas To Implement**
- Limit STRING Network to experimentally validated physical interactions
- Change normalization method (dividing instead of subtracting)
- Calc pvalues for each centrality score
- Track which data's network propagation each protein in the network was added from, and then enrich paths for clinical data types.
- Find dsd modules and enrich
- Complete suite of visualization, centrality hits, enrichment, modularization for ppi -> all KO and ppi -> each KO as well as ko to ppi

### Future Approaches - Add TB Baits to Network
- Add TB baits; use this to find tb secreted factors likely responsible for development of meningitis from SNPS and patient data. Also explore enrichment for functions within shortest paths to/from interactors of individual baits.
- K shortest paths---unsure exactly how to best use this, look into PathLinker algorithm.
- Weight network based on features of experimental data ex: weight early timepoint regulation in rnaseq
