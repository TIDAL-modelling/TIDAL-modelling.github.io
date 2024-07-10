---
title: Emotional regulation
layout: default
parent: Synthetic Datasets
nav_order: 1
---

<div class="container">
    <h2 class="heading">Emotional regulation synthetic dataset</h2>
    <a href="/assets/synthetic_data/emot_reg_simulated.csv" class="btn btn-blue">Download dataset</a>
</div>


 * Emotional regulation in childhood and emotional symptoms scores, measured by the Strengths & Difficulties Questionnaires (SDQ),  across 5 time points between childhoodand adolescence (ages 3 to 14).
 * This dataset contains ~13000 people, based upon data from the [Millennium Cohort Study (MCS)](https://cls.ucl.ac.uk/cls-studies/millennium-cohort-study/) participants.
 * You could use this example to look at the impact of poorer emotion regulation at baseline (t1) on later SDQ trajectories using the `er_t1_bin` variable or you could lookto see how changes in emotion regulation from baseline to the second wave (t2) have a long term impact on SDQ trajetcories using `er_bin`. You could even adjust thisanalysis by accounting for sex in the analysis using the variable `female`.
 * There are 3 categorical emotion dysregulation variables one could use to split trajectories by: 
    *  `er_t1_bin` , `er_t2_bin`, `er_bin`
 * There are 2 continuous emotion dysregulation variables one could use to split trajectories by: 
    *  `er_total_t1` , `er_total_t2`

### Variables (column names):
  * **Subject**
     * ID of simulated participant. 
     * Type: Character 
  * **sdq_t1, sdq_t2, sdq_t3, sdq_t4, sdq_t5**
     * Strengths & Difficulties Questionnaires Emotional Subscale (SDQ-E) scores from 0 to 10 at 5 time points. 
     * Type: Numeric
  * **age_t1, age_t2, age_t3, age_t4, age_t5**
     * Age at corresponding time points for the SDQ variable (years)
     * Type: Numeric
  * **Female**
    * Female is coded as 1. Male is coded as 0. 
    * Type: Categorical
  * **er_total_t1**
    * Emotional regulation scores from the emotional dysregulation component of the Child Social Behaviour Questionnaire at age 3 years.
    * Type: Numeric
    * Range: 0 to 10
  * **er_total_t2**
     * Emotional regulation scores from the emotional dysregulation component of the Child Social Behaviour Questionnaire at age 5 years.
    * Type: Numeric
    * Range: 0 to 10
  * **er_t1_bin**
    * When er_total_t1 is between 0 to 6 er_t1_bin is 0
    * When er_total_t1 is between 7 to 10 er_t1_bin is 1
  * **er_t2_bin**
    * When er_total_t2 is between 0 to 6 er_t2_bin is 0
    * When er_total_t2 is between 7 to 10 er_t2_bin is 1
  * **er_bin**
    * 0 = No emotional regulation (ER) problems at er_t1_bin & No ER problems at er_t2_bin
    * 1 = No ER problems at er_t1_bin & Yes ER problems at er_t2_bin
    * 2 = Yes ER problems at er_t1_bin & No ER problems at er_t2_bin 
    * 3 = Yes ER problems at er_t1_bin & Yes ER problems at er_t2_bin