---
layout: archive
title: "hidden"
permalink: /hidden/
author_profile: true
---

# Aquafort eDNA 

## OTU Abundance 
For this barplot, change the 'level' dropdown to '6'. Use the other drop down to sort the columns (samples) by date, stocked/not-stocked, ect. Click on the square on the taxonomy key to visualized only selected taxa. Interactive barplots of relative abundance can be found [here](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/Coogan_taxa-barplot.qzv)


## Core diversity metrics 
PCoA is performed on distance matrices for the metrics below (seems to better handle missing data than PCA does). 
More complete descriptions here: https://docs.onecodex.com/en/articles/4150649-beta-diversity

* Alpha diversity 
    * [Rarefaction](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/alpha-rarefaction.qzv)
    * Shannon’s diversity index (a quantitative measure of community richness)  
    * Faith’s Phylogenetic Diversity (a qualitative measure of community richness that incorporates phylogenetic relationships between the features)[Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/faith_pd_alpha-group-significance.qzv)
    * Observed OTUs (a qualitative measure of community richness) [Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/alpha-group-sig-obs-feats.qzv)
    
* Beta diversity
    * Jaccard distance (a qualitative measure of community dissimilarity. Qualitative - presence / absence - percentage of taxa not found in both samples) [jaccard emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/jaccard_emperor.qzv)
    * Bray-Curtis distance (a quantitative measure of community dissimilarity. Takes into consideration abundance and presence absence) [bray curtis emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/bray_curtis_emperor.qzv)
    * Unweighted UniFrac distance (a qualitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Percentage of phylogenetic branch length not found in both samples)
    [unweighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/unweighted_unifrac_emperor.qzv)
    * Weighted UniFrac distance (a quantitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Similar to Bray-Curtis but takes into consideration phylogenetic relationships)
    [weighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/weighted_unifrac_emperor.qzv)

## Descriptons Coming Soon...
[phylo-empress](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylo-empress.qzv)


### gemelli phylogenetic-rpca-with-taxonomy
Performs phylogenetic robust center log-ratio transform robust PCA and ranks the features by the loadings of the resulting SVD. One-way PERMANOVA: Determine whether groups of samples are significantly different from one another using a permutation-based statistical test. Tested here when grouping by pre- and post stocked, as well as tide. Test performed on the Aitchison distance of the sample loadings from RPCA.

[beta-permanova-stocked](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylo-stocked_significance.qzv)

[pairwise-beta-permanova-stocked](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/pairwise_phylo-stocked_significance.qzv)

[beta-permanova-tide](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylo-tide_significance.qzv)








