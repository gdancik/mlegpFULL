# mlegp 

## mlegp: Maximum Likelihood Estimates of Gaussian Processes (with sensitivity analysis)

Maximum likelihood Gaussian process modeling for univariate and multi-dimensional outputs with diagnostic plots following Santner et al (2003) <doi:10.1007/978-1-4757-3799-8> ([link](http://link-springer-com-443.webvpn.fjmu.edu.cn/book/10.1007%2F978-1-4757-3799-8)). 

- **This is the 'full' version of *mlegp* which implements sensitivity analysis.** This is no longer supported by CRAN and must be installed following the instructions below.
- The current version of *mlegp*, without sensitivity analysis, is available on [CRAN](https://cran.r-project.org/web/packages/mlegp/index.html). 

## Citation:

Dancik, GM and Dorman, KS (2008). mlegp: statistical analysis for
computer models of biological systems using R. Bioinformatics 24(17),
pp. 1966-1967. \[PMID: [18635570](http://www.ncbi.nlm.nih.gov/pubmed/18635570)\]

## Installation

**Note: In order to install *adapt*, you will need R 4.0.3 or lower**
 
In order to use the "full version" of mlegp you will need to download and install the package *adapt* from http://cran.r-project.org/src/contrib/Archive/adapt/. For adapt to work on R >=3.0 you will need to add a NAMESPACE file. Untar the *adapt* archive, and then add a file called NAMESPACE to the top directory that contains the DESCRIPTION and README files, among others.
 
The NAMESPACE file should contain the following 3 lines, which says to make all variables in the adapt package available:
 
~~~
# NAMESPACE file
useDynLib(adapt)
exportPattern("^[^\\.]")
~~~

Then rebuild adapt using `R CMD build` and install it. 

Then install the *mlegpFULL* package from the archive ([mlegpFULL_3.2.1.tar.gz](https://github.com/gdancik/mlegpFULL/raw/main/mlegpFULL_3.2.1.tar.gz)) available on this repository. Note that from within R you will load the full *mlegp* package (*mlegpFULL*) using the following:
 
~~~ 
library(mlegpFULL)
~~~

Make sure to use 'mlegpFULL' as the package name rather than 'mlegp'. However, the *mlegp* functions have the same names as they do in the standard package.

## Developers

The full version of *mlegp* depends on the *adapt* package, which is no longer supported by CRAN. However, the *cubature* package can be used instead (https://cran.r-project.org/web/packages/cubature/?/). Pull requests are welcome for anyone interested in updating the full version of *mlegp* to use *cubature* instead of *adapt*, or to implement any other features.
