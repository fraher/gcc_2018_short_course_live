README
================
Chris Fraher
June 6, 2018

-   [Seting Up a Project](#seting-up-a-project)
    -   [The Folders](#the-folders)
-   [Write a README First](#write-a-readme-first)
    -   [The Process](#the-process)

Seting Up a Project
===================

The Folders
-----------

R/ data/ results/ reports/ README.Rmd., .md

Sometimes: figures/ LICENSE.Rmd, TODO.Rmd CITATION.Rmd etc...

Write a README First
====================

1.  Write a README first

-   Put the goal of the project before starting analysis, confirm with others
-   Prevents project creep over time, where ideas of analysis differ from goals
-   Tells a new person everything that needs to be done from getting the data to cleaning to running the analysis

The Process
-----------

Files in the R folder:

1.  01\_gather\_data.R - Used to get the same dataset everytime
2.  3.  95\_make\_clean.R - Cleans all data from workspace clean slate before running all scripts

-   Loops through folders such as "results" and "data" directories and delete it all

1.  99\_make\_all.R - This contains the entire workflow to run in order

Write a funcioning R package in &lt; 15 min

Thesee packages shift bookkeeping from frustrated mortals to laconic computers:

devtools roxygen2 knitr rmarkdown

To generate an R Pakcage

Start a new R Project

Create a license file

file.edit("LICENSE") library(devtools) library(roxygen2) library(knitr) library(rmarkdown) document() - this will generate man pages if necessary build() install() check() - would this be accepted by CRAN

at this point you have created a valid package

.rs.restartR() - if you have edited the code for a packaged, it will try to reload from last time R was loaded... so edits require this to install it will also reload packages that were already reloaded

library(gcc2018pck2) to load your package

first add a script that describes the pacakge

Every function should have a few typse of documentation, 1. Title 2. Description 3. doctype 4. name

rerun through all the same steps as earlier Now can load the document file ?gcc2018pck2

Make sure to follow "A Trivial Function" template use @examples not @example Then be sure to @export
