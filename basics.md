---
layout: default
title: Basic Commands
nav_order: 2
description:
---

# Basic Commands

<img src="{{site.baseurl}}/jupyter/figures/learning_objectives.png">

***

### R packages

R package is a library of prewritten code designed for a particular task or a collection of tasks

<img src="{{site.baseurl}}/jupyter/figures/R_packages.png">

***

### Installing a new package (2 options)



#### Under Tools -> Packages tab -> Search for “psych” and “dplyr”

<img src="{{site.baseurl}}/jupyter/figures/install_packages.png">

***

#### Using code: install.packages( ) and library( ) functions

```
install.packages(c("ggplot2", "dplyr", "readr", "psych"))

library("ggplot2")
library("dplyr")
library("readr")
library("psych")
```

***


```R
install.packages(c("ggplot2", "dplyr", "readr", "psych"))

library("ggplot2")
library("dplyr")
library("readr")
```

    Installing packages into 'C:/Users/17783/Documents/R/win-library/3.6'
    (as 'lib' is unspecified)
    
    

    package 'ggplot2' successfully unpacked and MD5 sums checked
    package 'dplyr' successfully unpacked and MD5 sums checked
    package 'readr' successfully unpacked and MD5 sums checked
    package 'psych' successfully unpacked and MD5 sums checked
    
    The downloaded binary packages are in
    	C:\Users\17783\AppData\Local\Temp\Rtmpo3klau\downloaded_packages
    

    Warning message:
    "package 'ggplot2' was built under R version 3.6.3"
    Warning message:
    "package 'dplyr' was built under R version 3.6.3"
    
    Attaching package: 'dplyr'
    
    
    The following objects are masked from 'package:stats':
    
        filter, lag
    
    
    The following objects are masked from 'package:base':
    
        intersect, setdiff, setequal, union
    
    
    Warning message:
    "package 'readr' was built under R version 3.6.3"
    

#### Tips

**On the editor**

<kbd>CTRL</kbd>+<kbd>enter</kbd> runs the command in the current line (<kbd>cmd</kbd>+<kbd>enter</kbd> on MacOS)

<kbd>CTRL</kbd>+<kbd>w</kbd> closes current tab (<kbd>cmd</kbd>+<kbd>w</kbd> on MacOS)

After typing the first few lines of a command, <kbd>tab</kbd> auto-completes the command

**On the console**

<kbd>↑</kbd> shows the last command (useful to rerun the command of fix errors)

***
