---
title: R package
layout: default
parent: Getting Started
nav_order: 2
---

## R package

TIDAL can be used by installing the [TIDAL R package](https://github.com/TIDAL-modelling/TIDAL) and launching the R Shiny application locally (rather than using and uploading data to the tool online).

1. Install the statistical programing language [R](https://cran.rstudio.com/) 
2. We also reccomend installing [R Studio](https://posit.co/download/rstudio-desktop/)
3. Install the [TIDAL R package](https://github.com/TIDAL-modelling/TIDAL) by running the code below in your R console. 

	{: .highlight }
	If using R Studio it's recommended to restart your R session before installing.

	```r
	install.packages("remotes")
	remotes::install_github("TIDAL-modelling/TIDAL")
	# Note if prompted to update packages you can select option 3/None.
	# Updating all packages (option 1) might take a while to run.
	library("TIDAL")
	# Launch the R Shiny app
	launchTIDAL()
	# To get documentation for launchTIDAL()
	?launchTIDAL
	```

