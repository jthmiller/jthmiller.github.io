---
layout: archive
title: "Results"
permalink: /results/
author_profile: true
---

### NERRs eDNA 

Metabarcoding analysis for NERRs sites sampled quarterly. Metadata for all sites [here](https://github.com/jthmiller/NERRs-18s-metabarcoding/blob/main/metadata.tsv), including SWMP data when available. Downloaded from https://cdmo.baruch.sc.edu


## OTU Abundance 
Interactive barplots of relative abundance can be found [here](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/NERRS_18s_taxa-barplot.qzv)
Non-interactive plots broken up by region can be found [here](https://github.com/jthmiller/NERRs-18s-metabarcoding/tree/main/images/barplots)
![gulf](https://github.com/jthmiller/NERRs-18s-metabarcoding/blob/main/images/sample-plots/gulf-barplots-sample.png?raw=true)


## Core diversity metrics 
PCoA is performed on distance matrices for the metrics below (seems to better handle missing data than PCA does). 
More complete descriptions here: https://docs.onecodex.com/en/articles/4150649-beta-diversity

* Alpha diversity 
    * [Rarefaction](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/alpha-rarefaction.qzv)
    * Shannon’s diversity index (a quantitative measure of community richness)  
    * Faith’s Phylogenetic Diversity (a qualitative measure of community richness that incorporates phylogenetic relationships between the features)[Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/faithspd-group-significance.qzv)
    * Observed OTUs (a qualitative measure of community richness) [Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/alpha-group-sig-obs-feats.qzv)
    * Evenness (or Pielou’s Evenness; a measure of community evenness)
    
* Beta diversity
    * Jaccard distance (a qualitative measure of community dissimilarity. Qualitative - presence / absence - percentage of taxa not found in both samples) [jaccard emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/jaccard_emperor.qzv)
    * Bray-Curtis distance (a quantitative measure of community dissimilarity. Takes into consideration abundance and presence absence) [bray curtis emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/bray_curtis_emperor.qzv)
    * Unweighted UniFrac distance (a qualitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Percentage of phylogenetic branch length not found in both samples)
    [unweighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/unweighted_unifrac_emperor.qzv)
    * Weighted UniFrac distance (a quantitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Similar to Bray-Curtis but takes into consideration phylogenetic relationships)
    [weighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/weighted_unifrac_emperor.qzv)

### Unifrac PCoA performed on Unweighted UniFrac distance matrix 
![unifrac](https://github.com/jthmiller/NERRs-18s-metabarcoding/blob/main/images/sample-plots/unifrac_salinity_all-sites.png?raw=true)
Samples colored by minimum salinity from SWMP collected data within X days of eDNA sample collection. This is an interactive plot that can be found [here](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/unweighted_unifrac_emperor.qzv)

## Classify samples from ASVs/OTUs (removed taxa with high 18s copy number)
[Qiime Sample Classification](https://docs.qiime2.org/2024.10/plugins/available/sample-classifier/classify-samples/) predicts a categorical sample metadata column using a supervised learning classifier. Splits input data into training and test sets. The training set is used to train and test the estimator using a stratified k-fold cross- validation scheme. This includes optional steps for automated feature extraction and hyperparameter optimization. The test set validates classification accuracy of the optimized estimator. Outputs classification results for test set. For more details on the learning algorithm, see http://scikit-learn.org/stable/supervised_learning.html

We used the default 'RandomForestRegressor' estimator. This works by building a collection of decision trees, each trained on a different random subset of the data (bagging) and a random subset of features. The final prediction is the average of the predictions made by all the individual decision trees. 

18s copy number in Bacillariophyta, Ciliophora, and Dinophyceae can be orders of magnitude higher than other taxa, resulting in extreme read counts for these taxa, which can swamp out the signals for other groups. One strategy to account for 18s copy number is to multiply read counts by a coefficent that was derived from the ratio between 18s copy number and biomass (as performed by Martin et al 2022, DOI 10.3897/mbmg.6.85794).

### PCoA on sample dissimilarity matricies: [bray curtis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/bray_curtis_emperor.qzv), [jaccard](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/jaccard_emperor.qzv)

### Phylogenetic PCoAs: [unweighted unifrac](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/unweighted_unifrac_emperor.qzv), [weighted unifrac](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/weighted_unifrac_emperor.qzv)

### Heatmaps of the ASVs that predict category: [Region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-ASVs/Region-heatmap.qzv), [NERR](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-ASVs/NERR-heatmap.qzv), [Site](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-ASVs/Site-heatmap.qzv)

### Heatmaps of the OTUs that predict category: [Region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/Region-heatmap.qzv), [NERR](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/NERR-heatmap.qzv), [Site](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/Site-heatmap.qzv)

### Heatmaps for each site: [SF](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/SF/heatmap.qzv), [GTM](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/GTM/heatmap.qzv)


### Heatmaps of the OTUs that predict continous data: [Sal_Min-Heatmap](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/Sal_Min-Sal_Min-important-feature-heatmap.qzv), [pH_Min-Heatmap](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/pH_Min-pH_Min-important-feature-heatmap.qzv)

### Accuracy Predictions: [Sal_Min-accuracy](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/Sal_Min-accuracy_results.qzv), [pH_Min-accuracy](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/copy-filtered/sample-classifier-OTUs/pH_Min-accuracy_results.qzv)  

### Predicting including diatoms? [OTUs Regions](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/genus-heatmap.qza), [ASVs Regions](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/heatmap.qzv). [ASVs Salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/important-feature-heatmap.qzv)

RPCA:  

CTF:  

GEMELLI: 




## Phylogenetic RPCA and CTF.
"In order to account for the correlation among samples from the same subject we will employ compositional tensor factorization (CTF). CTF builds on the ability to account for compositionality and sparsity using the robust center log-ratio transform ... but restructures and factors the data as a tensor."

"... robust principal-component analysis (RPCA) addresses sparsity and compositionality; compositional tensor factorization (CTF) addresses sparsity, compositionality, and repeated measure study designs; and UniFrac incorporates phylogenetic information. Here we introduce a strategy of incorporating phylogenetic information into RPCA and CTF. The resulting methods, phylo-RPCA, and phylo-CTF, provide substantial improvements over state-of-the-art methods in terms of discriminatory power of underlying clustering
https://pmc.ncbi.nlm.nih.gov/articles/PMC9238373/

For a tutorial on CTF with Qiime's Gemelli plugin, see [here](https://github.com/biocore/gemelli/blob/master/ipynb/tutorials/IBD-Tutorial-QIIME2-CLI.md)

The qurro interactive plots are to explore the log fold change abundance of the features loading on each axis of the PCoA. The features can be plotted for groups of samples (grouped by a meatadata column) or along a continous variable (eg: Salinity)

### Explore the phylogenetic tree of ASVs alongside the rpca ordination: [all-sites](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-empress.qzv), [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/SE.qzv), [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/NE.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/N-Pacific.qzv), [Pacific-Island](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/Pacific-Island_phylo-empress.qzv)     

### Explore the rpca feature loadings with qurro here:[all-sites](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-qurro_plot.qzv), [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/SE_phylo-qurro_plot.qzv), [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/NE_phylo-qurro_plot.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/N-Pacific_phylo-qurro_plot.qzv), [Pacific-Island](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/Pacific-Island_phylo-qurro_plot.qzv)

### Explore the features loading in CTF with Qurro: [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/ctf/NE_ctf-qurro_plot.qzv), [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/ctf/SE_ctf-qurro_plot.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/ctf/N-Pacific_ctf-qurro_plot.qzv), [Pacific-Island](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/ctf/Pacific-Island_ctf-qurro_plot.qzv), [NO-island](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/ctf/NO-island_ctf-qurro_plot.qzv)

## Longitudinal Volatility
Interactive line plots assess how volatile a dependent variable (ASV or taxonomic group) is over a continuous, independent variable (e.g., time) in one or more groups. Select which ASV or taxa to plot on the y-axis to examine how variance in diversity and other metadata changes across time (set with the state-column parameter) in groups of samples and in individual subjects (set with the individual-id-column parameter)

### Longitudinal volatility:[ASVs](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-filtered/volatility_plot.qzv), [genus](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-genus/volatility_plot.qzv), [family](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-family/volatility_plot.qzv)

### Regional ASV Volatility [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/SE_volatility_plot.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/N-Pacific_volatility_plot.qzv), [PacIsland](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/Pacific-Island_volatility_plot.qzv), [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/NE_volatility_plot.qzv)

### Regional Genus Volatility [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/SE_volatility-plot.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/N-Pacific_volatility-plot.qzv), [PacIsland](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/Pacific-Island_volatility-plot.qzv), [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/NE_volatility-plot.qzv)

## State Subject Volitility Ordination
Identify features that are predictive of a numeric metadata column, state_column (e.g., time), and plot their relative frequencies across states using interactive feature volatility plots. A supervised learning regressor is used to identify important features and assess their ability to predict sample states. state_column will typically be a measure of time, but any numeric metadata column can be used.

### With diatoms: [SE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/SE-ctf_state_subject_ordination_longitudinal-volatility.qzv), [N-Pacific](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/N-Pacific-ctf_state_subject_ordination_longitudinal-volatility.qzv), [PacIsland](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/Pacific-Island-ctf_state_subject_ordination_longitudinal-volatility.qzv), [NE](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/feat-volitility/NE-ctf_state_subject_ordination_longitudinal-volatility.qzv)







Accounts for the correlation among samples from the same subject (site within NERR). Points are instead sites. 
[rf-state_subject_ordination](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/longitudinal/rf-state_subject_ordination.qzv)

Here, points represent each site (subject) rather than each of the samples.  (to look for groupings by salinity or other features)
state-subject-ordination
















## beta-group-significance: Group samples by a metadata column to determine whether they are significantly different from one another using a permutation-based statistical test. At the national scale, 

beta-permanova[salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-salinity_significance.qzv), [region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-region_significance.qzv), [NERR](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-NERR_significance.qzv), [Quarter](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-Quarter_significance.qzv), [Site](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-Site_significance.qzv)

## Longitudinal pairwise distance
The pairwise-distances visualizer also assesses changes between paired samples from two different “states”, but instead of taking a metadata column or artifact as input, it operates on a distance matrix to assess the distance between “pre” and “post” sample pairs, and tests whether these paired differences are significantly different between different groups, as specified by the group-column parameter. (Qiime doc) For our data, this will test whether the effect of season differs between regions. We expect northern climates to have a greater seasonal effect. Each comparison was perfomed using the unweighted unifrac distance matrix  

[Region_1-3](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/Region_1-3_pairwise-distances.qzv)

[Region_2-4](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/Region_2-4_pairwise-distances.qzv)

These plots appears to support greater distances among norther samples over the 1 and 3rd quarter, compared to southern samples over that same timeframe
[North_South-1_3](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-1_3-pairwise-distances.qzv)

[North_South-2_4](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-2_4-pairwise-distances.qzv)

This comparison was perfomed using the gemelli ctf distance matrix (not sure if this is appropriate)  

[North_South-2_4-gemelli](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-2_4-gemelli_ctf_pairwise-distances.qzv)



### Mixed effects models
[linear-mixed-effects-by-region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/linear-mixed-effects-region.qzv)

[linear-mixed-effects-by-salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/linear-mixed-effects-salinity.qzv)

[phylo-salinity_significance](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/phylo-salinity_significance.qzv)





## Regional Analysis:
### New England
[NE_subject_biplot](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/regional/NE_with-repl/NE_gemelli-ctf/NE_subject_biplot.qzv)

[state_subject_ordination](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/regional/NE_with-repl/NE_gemelli-ctf/state_subject_ordination.qzv)

[accuracy_results](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/regional/NE_with-repl/NE_ecam-feat-volatility/accuracy_results.qzv)





### Results:  

Bar-plot images of sites broken up by regions [here](https://github.com/jthmiller/NERRs-18s-metabarcoding/blob/main/images/barplots)  

Network plots of sites broken up by regions [here](https://github.com/jthmiller/NERRs-18s-metabarcoding/blob/main/images/network-plots/)  




### Picocyanobacteria

[Bar plot](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/picocyano/111524-JM-Picocyanobacteria_taxa-barplot.qzv)



## [Gemelli](https://github.com/biocore/gemelli/tree/master)
For sparse compositional omics datasets. All these methods are unsupervised and aim to describe sample/subject variation and the biological features that separate them.
- Robust Aitchison PCA (RPCA)
- Compositional Tensor Factorization (CTF) 
The preprocessing transform for both RPCA and CTF is the robust centered log-ratio transform (rlcr) which accounts for sparse data (i.e. many missing/zero values). 