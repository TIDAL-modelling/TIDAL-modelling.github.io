---
title: FAQs and Troubleshooting
layout: default
nav_order: 7
---

## FAQs and Troubleshooting

If you run into any bugs or issues not listed below, please email TIDAL@ed.ac.uk or raise a new [GitHub issue](https://github.com/TIDAL-modelling/TIDAL/issues).

- **Can I upload my own data to use with TIDAL?**

If you are using the [online version](https://tidal.shinyapps.io/tidalapp/) then please do not upload *any sensitive data*. You can explore the tool online using the [synthetic data](/docs/synthetic_data).

You *must* install TIDAL on your computer if you wish to analyse sensitive data. To do this, you need to first install R and RStudio (though if you prefer to work in the R terminal, you could use a X window system to display the GUI instead). Then run the following code to install and launch TIDAL:

```r
install.packages("remotes")
remotes::install_github("TIDAL-modelling/TIDAL")
library("TIDAL")
# Launch the R Shiny app
launchTIDAL()
# To get documentation for launchTIDAL()
?launchTIDAL
```

- **What format should my data I want to upload be in?**

Comma delimited *.csv file or a Tab delimited *.tsv or *.txt files can be used to upload data. Missing data should be coded as "NA". Column names should ideally have no spaces or special characters in them.


When I select columns from my uploaded data, they have strange names

It's likely that you have uploaded an .xlsx file or another unsupported file format. Please save your data as a Comma delimited *.csv file or a Tab delimited *.tsv or *.txt file and try again.



- **The download results feature is not working**

If you are a Mac user, when you click "download results" your results PDF will open in a pop-out window in your default PDF program. You need to save this report manually (CMD+S) or the file will be lost when closed.

If you are trying to download results and the resulting file is not a .pdf or the file name begins with something other than "Explore_Data", it is likely that you do not have LaTeX installed on your computer. LaTeX is a free software needed to make PDF files in R, and can be downloaded for Linux, MacOS and Windows from [The LaTeX Project](https://www.latex-project.org/get). 

Try running the following in your R console:
```r
install.packages("tinytex")
tinytex::install_tinytex()
```

- **My model isn't running**

If you are *only* running a linear model, ensure that there are at least 3 time points in your data. If you wish to run quadratic, cubic and/or quartic models, ensure that there are at least 4 time points in your data. If you are uploading your own long format data, also check that column names do not have spaces in them, and that no column names are duplicated.

- **I am having problems installing TIDAL**

Check that your R version is up-to-date. TIDAL requires you to have R version 2.10 or newer. If you are a Mac user or installing TIDAL within the terminal/command line, you may need to install the compiler [CMake](https://cmake.org/) which should solve any issues with compiling R packages from source. It is easier to install TIDAL within RStudio, however if you are accustomed to using R in the terminal or command line, be aware that you may need an X window system to display the GUI.

- **The "?" icons for more information are not working**

Hover over the icon with your cursor to display the additional information. Clicking the icon will not display the text.

- **The Shiny app fails to launch on Linux from the R console**

If this happens a work around may be to view the app running locally in your browser. This can be done by copying and pasting the URL after "Listening on" (see the yellow box in the screenshot below for an example). Here, for "Listening on http://127.0.0.1:4484" copy and paste "http://127.0.0.1:4484" into your browser, eg. in Chrome or Firefox. Even though you are using a browser the app is still running locally on your computer, the same as if the pop-out window was launched from RStudio.

![../../assets/images/localhost.png](../../assets/images/localhost.png)
