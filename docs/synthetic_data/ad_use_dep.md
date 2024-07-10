---
title: Depressive symptoms
layout: default
parent: Synthetic Datasets
nav_order: 2
---

<div class="container">
    <h2 class="heading">Depressive symptoms synthetic dataset</h2>
    <a href="/assets/synthetic_data/ad_use_dep_simulated.csv" class="btn btn-blue">Download dataset</a>
</div>


* Long term antidepressant adherence and subsequent measures of depressive symptoms, measured by the Short Mood and Feelings Questionnaire (SMFQ),  across 7 time pointsbetween in early adulthood (ages 23 to 30).
* This dataset contains ~800 people, based upon data from the [Avon Longitudinal Study of Parents and Children (ALSPAC)](https://https://www.bristol.ac.uk/alspac/)participants.
* You could use this dataset to look at long term depression trajetcories split by adherence to antidepressants. 
* There is 1 antidepressant variable one could use to split trajectories by: 
   *  `meds`

### Variables (column names):
  * **Subject**
     * ID of simulated participant. 
     * Type: Character 
  * **mfq_t1, mfq_t2, mfq_t3, mfq_t4, mfq_t5, mfq_t6, mfq_t7**
     * Short Mood and Feelings Questionnaire (SMFQ) scores from 0 to 26 at 7 time points. 
     * Type: Numeric
  * **age_t1, age_t2, age_t3, age_t4, age_t5, age_t6, age_t7**
     * Age at corresponding time points for the SDQ variable (years)
     * Type: Numeric
  * **meds**
    * Adherence to AD medication is coded as 1. Non-adherence to AD medication is coded as 0. 
    * Type: Categorical
