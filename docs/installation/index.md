---
title: Installation
layout: default
nav_order: 2
has_children: true
---

## Installation and usage

### Locally

Please install the R package and launch the Shiny app locally if you want to upload sensitive data. If using R Studio it's recommended to restart your R session before installing.

```r
# install.packages("remotes")
remotes::install_github("TIDAL-modelling/TIDAL")
# Note if prompted to update packages you can select option 3/None.
# Updating all packages (option 1) might take a while to run.
library("TIDAL")
# Launch the R Shiny app
launchTIDAL()
# To get documentation for launchTIDAL()
?launchTIDAL
```

### Online

[https://tidal.shinyapps.io/tidalapp/](https://tidal.shinyapps.io/tidalapp/)

To use this tool online please do not upload any sensitive data. Only use the [synthetic datasets](/docs/installation/synthetic_data).

