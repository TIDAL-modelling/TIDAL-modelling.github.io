---
title: Anxiety symptoms
layout: default
parent: Synthetic Datasets
nav_order: 3
---

<div class="container">
    <h2 class="heading">Anxiety symptoms synthetic dataset</h2>
    <a href="/assets/synthetic_data/fp_anx_simulated.csv" class="btn btn-blue">Download dataset</a>
</div>

* Pre-pandemic financial problems and subsequent measures of anxiety symptoms across COVID-19, measured by the Generalised Anxiety Disorder 7 scale (GAD-7),  across 5 time points in early adulthood (ages 28 to 30).
* This dataset contains ~4100 people, based upon data from the [Avon Longitudinal Study of Parents and Children (ALSPAC)](https://www.bristol.ac.uk/alspac/) participants.
* You could use this dataset to explore the impact of pre-pandemic financial problems on later anxiety trajectories across COVID-19. You could use the fin_probs variable `fin_probs` to see how trajectories differ, and even see how these trajectories might look after adjusting for by pre-pandemic levels of anxiety `anx_pp`. 
* There is 1 finacial problems variable one could use to split trajectories by: 
  *  `fin_probs`
* Alternatively, there is 1 pre-pandemic anxiety variable one could use to split trajectories by: 
  *  `anx_pp`

### Variables (column names):
  * **Subject**
     * ID of simulated participant. 
     * Type: Character 
  * **gad7_t2, gad7_t3, gad7_t4, gad7_t5, gad7_t6**
     * Generalised Anxiety Disorder 7 scale (GAD-7) scores from 0 to 21 at 5 time points. 
     * Type: Numeric
  * **age_t2, age_t3, age_t4, age_t5, age_t6**
     * Age at corresponding time points for the SDQ variable (years)
     * Type: Numeric
  * **fin_probs**
    * Pre-pandemic finacial problems is coded as 1. No pre-pandemic finacial problems is coded as 0. 
    * Type: Categorical
  * **anx_pp**
    * Pre-pandemic GAD-7 scores 
    * Type: Numeric