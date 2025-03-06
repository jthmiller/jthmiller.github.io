---
layout: archive
title: "hidden"
permalink: /hidden/
author_profile: true
---

### Aquafort eDNA 


## OTU Abundance 
For this barplot, change the 'level' dropdown to '6'. Use the other drop down to sort the columns (samples) by date, stocked/not-stocked, ect. Click on the square on the taxonomy key to visualized only selected taxa. 

Interactive barplots of relative abundance can be found [here](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/Coogan_taxa-barplot.qzv)


## Core diversity metrics 
PCoA is performed on distance matrices for the metrics below (seems to better handle missing data than PCA does). 
More complete descriptions here: https://docs.onecodex.com/en/articles/4150649-beta-diversity

* Alpha diversity 
    * [Rarefaction](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/   )
    * Shannon’s diversity index (a quantitative measure of community richness)  
    * Faith’s Phylogenetic Diversity (a qualitative measure of community richness that incorporates phylogenetic relationships between the features)[Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/faithspd-group-significance.qzv)
    * Observed OTUs (a qualitative measure of community richness) [Kruskal-Wallis](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/alpha-group-sig-obs-feats.qzv)
    * Evenness (or Pielou’s Evenness; a measure of community evenness)
    
* Beta diversity
    * Jaccard distance (a qualitative measure of community dissimilarity. Qualitative - presence / absence - percentage of taxa not found in both samples) [jaccard emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/jaccard_emperor.qzv)
    * Bray-Curtis distance (a quantitative measure of community dissimilarity. Takes into consideration abundance and presence absence) [bray curtis emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/bray_curtis_emperor.qzv)
    * Unweighted UniFrac distance (a qualitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Percentage of phylogenetic branch length not found in both samples)
    [unweighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/unweighted_unifrac_emperor.qzv)
    * Weighted UniFrac distance (a quantitative measure of community dissimilarity that incorporates phylogenetic relationships between the features. Similar to Bray-Curtis but takes into consideration phylogenetic relationships)
    [weighted unifrac emperor](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/weighted_unifrac_emperor.qzv)



## Descriptons Coming Soon...
[phylo-empress](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/phylo-empress.qzv)

[beta-permanova-salinity](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/phylo-salinity_significance.qzv)

[beta-permanova-region](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/phylo-region_significance.qzv)

[beta-permanova-NERR](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/phylo-NERR_significance.qzv)

[longitudinal_volatility_ASVs](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/longitudinal-filtered/volatility_plot.qzv)

[longitudinal_volatility_genus](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/longitudinal-genus/volatility_plot.qzv)

[longitudinal_volatility_family](https://view.qiime2.org/visualization/?src=https://jthmiller.github.io/files/results/aquafort/phylogenetic/longitudinal-family/volatility_plot.qzv)






