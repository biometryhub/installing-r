---
title: "<center>Installing and Configuring R and Rstudio with ASReml-R</center>"
author: 
- <center>Biometry Hub, University of Adelaide<center>
- <center>biometrytraining@adelaide.edu.au<center>
date: "<center>Last updated: March 2022</center>"
output:
  html_document:
    toc: yes
    toc_float: yes
    keep_md: true
    highlight: textmate
  pdf_document:
    fig_caption: yes
    toc: yes
    highlight: tango
linkcolor: blue
urlcolor: blue
---




---

# Introduction  

These instructions assume you already have a working version of R on your computer. If this is not yet the case, please follow these instructions: https://biometryhub.github.io/installing-r/installing-r.html

This guide does not assume any particular R development environment - it will work equally well with any option.

This guide assumes you are running a relatively recent version of Microsoft Windows, for example Windows 8 or later, or Mac OS X/macOS 10.11 (El Capitan) or later. The guide will likely work for Debian based Linux distributions as well (E.g. Ubuntu flavours), however it is not extensively tested under those scenarios.

# ASReml-R Installation

## biometryassist

You will need the `biometryassist` package, which can be installed from CRAN via


```r
if(!require(biometryassist)) install.packages("biometryassist")
```


## ASReml-R

Once `biometryassist` is installed, the latest version of ASReml-R can then be installed with the commands


```r
library(biometryassist)
install_asreml()
```

The `install_asreml()` function comes from the `biometryassist` package, hence the need to install and load that first.

All going well, you should get a confirmation that ASReml-R is installed successfully.

## Activate ASReml-R

After you have installed ASReml-R, you will need to activate it. To do this, you will need to provide a licence code from VSNi, and possibly open two ports on your computer to allow communication over the internet with the VSNi licence server. To enter the licence code, use the following commands:


```r
library(asreml)
asreml.license.activate()
```

This will result in a prompt such as:
```
Please enter your activation code (RET or 0 to exit): 
```

The licence code is usually in the format `AAAA-BBBB-CCCC-DDDD`. Once entered, your computer will connect to the VSNi licence server to check the code is correct, and you will be informed of the outcome. 

A successful licence activation will result in a message like the following:

```
Licensed to ABcDEfg
Ref: ABC12345 Expires: 2023-06-30, 487 days.
```

# Additional Packages (Optional)

If you are participating in an intership with the Biometry Hub, you may require additional packages installed, such as ASMap.

To install them, run the following command:


```r
install.packages("ASMap")
```

---


# Further resources {#Further}
The above will get your basic setup ready but here are some links if you are interested in reading a bit further.

- R project homepage: <https://www.r-project.org/>
- RStudio homepage: <https://www.rstudio.com/products/rstudio/>
- How to Use RStudio: <https://www.rstudio.com/ide/docs/>
- R Installation and Administration: <https://cran.r-project.org/doc/manuals/R-admin.html>
- R FAQ: <https://cran.r-project.org/doc/FAQ/R-FAQ.html>
- More about add-on packages in the R Installation and Administration Manual:  <https://cran.r-project.org/doc/manuals/R-admin.html#Add_002don-packages>
- ASReml-R package:  <https://vsni.co.uk/software/asreml-r>

