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
Samples colored by minimum salinity from SWMP collected data within X days of eDNA sample collection. This is an interactive plot that can be found [here](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-diversity-phylogenetic/weighted_unifrac_emperor.qzv)

## Descriptons Coming Soon...
[phylo-empress](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-empress.qzv)


## Description
[beta-permanova-salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-salinity_significance.qzv)

[beta-permanova-region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-region_significance.qzv)

[beta-permanova-NERR](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-NERR_significance.qzv)

[beta-permanova-Quarter](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/phylo-Quarter_significance.qzv)

### Longitudinal pairwise distance
The pairwise-distances visualizer also assesses changes between paired samples from two different “states”, but instead of taking a metadata column or artifact as input, it operates on a distance matrix to assess the distance between “pre” and “post” sample pairs, and tests whether these paired differences are significantly different between different groups, as specified by the group-column parameter. (Qiime doc) For our data, this will test whether the effect of season differs between regions. We expect northern climates to have a greater seasonal effect. Each comparison was perfomed using the unweighted unifrac distance matrix  

[Region_1-3](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/Region_1-3_pairwise-distances.qzv)

[Region_2-4](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/Region_2-4_pairwise-distances.qzv)

These plots appears to support greater distances among norther samples over the 1 and 3rd quarter, compared to southern samples over that same timeframe
[North_South-1_3](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-1_3-pairwise-distances.qzv)

[North_South-2_4](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-2_4-pairwise-distances.qzv)


This comparison was perfomed using the gemelli ctf distance matrix (not sure if this is appropriate)  

[North_South-2_4-gemelli](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-pairwise-dis/North_South-2_4-gemelli_ctf_pairwise-distances.qzv)

### Longitudinal Volatility
Interactive line plots assess how volatile a dependent variable (ASV or taxonomic group) is over a continuous, independent variable (e.g., time) in one or more groups. Select which ASV or taxa to plot on the y-axis to examine how variance in diversity and other metadata changes across time (set with the state-column parameter) in groups of samples and in individual subjects (set with the individual-id-column parameter).

[longitudinal_volatility_ASVs](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-filtered/volatility_plot.qzv)

[longitudinal_volatility_genus](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-genus/volatility_plot.qzv)

[longitudinal_volatility_family](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/core-metrics-results/phylogenetic/longitudinal-family/volatility_plot.qzv)

### Regional Longitudinal Volatility

### Mixed effects models
[linear-mixed-effects-by-region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/linear-mixed-effects-region.qzv)

[linear-mixed-effects-by-salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/linear-mixed-effects-salinity.qzv)

[phylo-salinity_significance](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/phylo-salinity_significance.qzv)




[rf-state_subject_ordination](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/longitudinal/rf-state_subject_ordination.qzv)




[volatility_plot](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/volatility_plot.qzv)

[genus-level_volatility](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/genus-level_volatility_plot.qzv)

[ASV-level_volatility](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/nerrs/all-sites/asv-level_volatility_plot.qzv)

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
