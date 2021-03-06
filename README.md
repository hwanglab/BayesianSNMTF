# Bayeisan_SNMTF (BSNMTF)
Bayesian Semi-Nonnegative Matrix Tri-Factorization

BSNMTF is a semi-nonnegative matrix tri-factorization method in the framework of Bayesian learning to identify pathways associated with cancer phenotypes (e.g., cancer sub-types or treatment outcome) from a real-valued input matrix (e.g., copy number alterations or normalized/log transformed gene expression data). In contrast to non-negative factorization methods, which are limited to non-negative input only, our method takes a real-valued matrix as input and is able to find the up/down regulated patterns associated with the pathways from the data. We also place structured spike-and-slab priors (which are encoded with the pathways and a gene-gene interaction (GGI) network) on the centroid matrix so that even a set of genes that is not initially contained in the pathways (due to the incompleteness of the current pathway database) can be involved in the factorization in a stochastic way specifically, if those genes are connected to the member genes of the pathways on the GGI network. 

# Items
1. BSNMTF_supplementary_PSB2020.pdf (supplementary material): contains detailed derivations of the variational update rules and additional information

2. BSNMTF_top3_allcombined_geneset_enrichment.xlsx: cotains the pathway analysis in the main paper

3. MATLAB codes (./matlab_codes) <br/>
3-1 bsnmtf.m (Bayesian Semi-Nonnegative Matrix Tri-Factorization): the main Matlab function <br/>
3-2 script_BSNMTF_simulation_Z0_incomplete.m: the experiment on the simulation data in the main paper <br/>
3-3 script_BSNTMF_TCGA_STAD_Subtypes.m: the experiment on the TCGA gastric cancer dataset in the main paper <br/>
3-4 script_BSNTMF_ImmunotherapyResponse.m: the experiment on the metastatic gastric cancer immunotherapy clinical-trial dataset in the main paper <br/>
3-5 script_BSNMTF_supp_experiments.m: the experiments on the simulation dataset in the supplementary material

# Requirements
To test BSNMTF (on the simulation data in the main paper), run script_simulation_Z0_incomplete.m (Matlab or Octave, but we have tested our code only on Matlab)

call bsnmtf.m  (input arguments: X, U, Z0, A, options)

To rune the codes, you need the following optimziation toolbox: 
Limited memory BFGS: https://github.com/stephenbeckr/L-BFGS-B-C

The data files in the script files, script_BSNTMF_TCGA_STAD_Subtypes.m and script_BSNTMF_ImmunotherapyResponse.m, are not included in this repository. Please contact the authors if you want to run both scripts.

# Notes
This work is included in the Proceedings of Pacific Symposium on Biocomputing (PSB 2020), https://psb.stanford.edu/psb-online/proceedings/psb20/.

Contact information: Sunho Park (parks[nospam]@ccf.org) 

