---
title: Height
layout: default
parent: Synthetic Datasets
nav_order: 5
---

<div class="container">
    <h2 class="heading">Depressive symptoms synthetic dataset</h2>
    <a href="/assets/synthetic_data/height_simulated.csv" class="btn btn-blue">Download dataset</a>
</div>

* Sex and genetic differences in height trajetcories, measured across 8 time points across childhood and adolescence (ages 7 to 18).
* This dataset contains ~15000 people, based upon data from the [Avon Longitudinal Study of Parents and Children (ALSPAC)](https://https://www.bristol.ac.uk/alspac/) participants.
* You could use this dataset to examine sex differences in height trajetcories using the `female` for sex. Alternatively, you could explore how higher or lower polygenic risk score for height `hei_k_5e08_std` are associated with different height trajectories, adjusting for sex `female`.
* There is 1 sex variable one could use to split trajectories by: 
  *  `female`
* Alternatively, there is one geneic risk variable one could use to split trajectories by: 
  *  `hei_k_5e08_std`

### Variables (column names):
  * **Subject**
     * ID of simulated participant. 
     * Type: Character 
  * **height_t1, height_t2, height_t3, height_t4, height_t5, height_t6, height_t7, height_t8**
     * Height at each occasions (measured in cm)
     * Type: Numeric
  * **age_t1, age_t2, age_t3, age_t4, age_t5, age_t6, age_t7, age_t8**
     * Age at corresponding time points for the height variable (years)
     * Type: Numeric
  * **Female**
    * female is coded as 1. Male is coded as 0. 
    * Type: Categorical
  * **hei_k_5e08_std**
    * Polylgenic risk score for height where higher scores = greater genetic liability to height and lower scores = lower genetic liability for height. 
    * Type: Numeric
