# Network Analysis Collaboration Repo

Here's one place for maintaining computational network integration methods, data, and results for the Cox and Hawn Labs and the TBRU.

### First Approach - Union of Unweighted Shortest Paths
Starting in a subnetwork of STRING limited to significant proteins from network propagation on any of the ataqseq, methylation, snp, rnaseq, and proteomics, calculate shortest paths from each Crispr KO/KD immune screen hit to each TB secreted factor PPI. Take the union of shortest paths as the subnetwork of interest and apply network analyses to it.

Crispr KO/KD data taken from [TBRU_integration_data](https://github.com/hawn-lab/TBRU_integration_data/tree/main/data_clean).

**Ideas To Implement**
- ~~Limit STRING Network to experimentally validated physical interactions~~
- ~~Change normalization method (dividing instead of subtracting)~~
- ~~Calc pvalues for each centrality score~~
- ~~Find KDs that are direct interactors of PPI and PPI and KD connected by only one hop~~
- Try simple normalization of centrality measures and simple pvalue fdr using the measure/degree of each gene in starting network
- ~~Track which start and end node for each path~~
- Run Weighted network with output heats as weights
- Track which data's network propagation each protein in the network was added from, and then enrich paths for clinical data types.
- Find dsd -> PAM clusters and enrich. *Try the same with network modularity clusters, see Cerami et al. 2010
- Complete suite of visualization, centrality hits, enrichment, modularization for ppi -> all KO and ppi -> each KO as well as ko to ppi
-  
- Compare Networks by generating S matrix for each and finding genes w greatest difference then doing gene enrichment (dor for allkd vs eachkd)
- Re-Run analysis for multiple underlying networks--look at https://pubmed.ncbi.nlm.nih.gov/29605183/ Evaluation of molecular networks (Huang et al 2018)
-

**Biological Lines of Inquiry**
### ESX-1
- lorum ipsum

### Menangitis and Mortality




### Future Approaches - Add TB Baits to Network
- Add TB baits; use this to find tb secreted factors likely responsible for development of meningitis from SNPS and patient data. Also explore enrichment for functions within shortest paths to/from interactors of individual baits.
- K shortest paths---unsure exactly how to best use this, look into PathLinker algorithm.
- Weight network based on features of experimental data ex: weight early timepoint regulation in rnaseq
