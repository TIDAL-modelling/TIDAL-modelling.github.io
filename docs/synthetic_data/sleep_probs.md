---
title: Sleep problems
layout: default
parent: Synthetic Datasets
nav_order: 4
---

<div class="container">
    <h2 class="heading">Sleep problems synthetic dataset</h2>
    <a href="/assets/synthetic_data/sleep_probs_mh_simulated.csv" class="btn btn-blue">Download dataset</a>
</div>

* Sleep problems in childhood and subsequent measures of depressive symptoms, measured by the Short Mood and Feelings Questionnaire (SMFQ), and the Strengths & Difficulties Questionnaires Emotional Subscale (SDQ-E) across 4 time points in childhood and adolescence (ages 9 to 16).
* This dataset contains ~8900 people, based upon data from the [Avon Longitudinal Study of Parents and Children (ALSPAC)](https://https://www.bristol.ac.uk/alspac/) participants.
* You could use this dataset to examine the impact of childhood sleep problems on later mental health trajectories using either the MFQ or SDQ data as outcomes. For example you could see how MFQ trajectories differ by `sleep_bin` and even adjust for baseline SDQ scores `emot_t1` and vice versa.
* There is 1 sleep problems variable one could use to split trajectories by: 
  *  `sleep_bin`
* Alternatively, there are two mental health variables one could use to split trajectories by: 
  *  `mfq_t1` if looking at SDQ trajetcories
  *  `emot` if looking at SMFQ trajetcories

### Variables (column names):
  * **Subject**
     * ID of simulated participant. 
     * Type: Character 
  * **mfq_t1, mfq_t2, mfq_t3, mfq_t4**
     * Short Mood and Feelings Questionnaire (SMFQ) scores from 0 to 26 at 4 time points. 
     * Type: Numeric
  * **emot_t1, emot_t2, emot_t3, emot_t4**
     * Strengths & Difficulties Questionnaires Emotional Subscale (SDQ-E) scores from 0 to 10 at 4 time points. 
     * Type: Numeric
  * **age_t1, age_t2, age_t3, age_t4**
     * Age at corresponding time points for the SMFQ/SDQ variable (years)
     * Type: Numeric
  * **sleep_bin**
    * Sleep problems in childhood are coded as 1. No sleep problems in childhood are coded as 0. 
    * Type: Categorical
