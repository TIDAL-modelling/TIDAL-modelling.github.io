---
title: R package
layout: default
parent: Getting Started
nav_order: 2
---

## R package

TIDAL can be used by installing the [TIDAL R package](https://github.com/TIDAL-modelling/TIDAL) and launching the R Shiny application locally (rather than using and uploading data to the tool online).

### Installation

1. Install the statistical programing language [R](https://cran.rstudio.com/) 
2. We also reccomend installing [R Studio](https://posit.co/download/rstudio-desktop/)
3. Install the [TIDAL R package](https://github.com/TIDAL-modelling/TIDAL) and launch the application by running the code below in your R console. Please see video and screenshot below for demo and function documentation.

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

<video width="100%" controls autoplay muted loop>
  <source src="/assets/video/TIDAL_demo.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

### Documentation for the function "launchTIDAL"


<style>
.bordered-box {
    border: 1px solid #ccc;       /* Light gray border */
    padding: 1em;                 /* Adds padding inside the box */
    border-radius: 5px;           /* Optional: rounds the corners */
    background-color: #f9f9f9;    /* Optional: light background color */
    margin: 1em 0;                /* Adds space around the box */
}
</style>

{::nomarkdown}
<div class="bordered-box">
{:/}

## Run Shiny app from local R environment

### Description
Opens an interactive Shiny GUI.

### Usage
~~~ r
launchTIDAL(display = "default")
~~~

### Arguments
- **display**:  
  Character vector. Can be either `"default"` or `"browser"`. Default is `"default"`.  
  - `"default"`: Opens the Shiny app in a pop-out window in RStudio.
  - `"browser"`: Opens the app in a web browser.

### Examples
**Run examples**

~~~ r
## Not run: 
# Launch Shiny app with default display
launchTIDAL()

# Launch Shiny app with browser display
launchTIDAL(display = "browser")
## End(Not run)
~~~

### Notes
You can also manually open a browser and copy and paste the URL after "Listening on" into the address bar. For example, if it says:

> Listening on http://127.0.0.1:4484

Copy and paste `http://127.0.0.1:4484` into your browser, such as Chrome or Firefox.  

Even though you are using a browser, the app is still running locally on your computer, the same as if the pop-out window was launched from RStudio.

{::nomarkdown}
</div>
{:/}
