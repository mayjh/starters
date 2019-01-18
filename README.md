Project health
================
18 January, 2019 10:24:11

# Good practice

``` r
if(!require("goodpractice")){
  install.packages("goodpractice")
}
checks <- goodpractice::all_checks()
gp <- goodpractice::gp(fs::path_dir(getwd()),
                       checks[!grepl("rcmdcheck", checks)])
```

    ## 
    ##   
       checking for file ‘/tmp/RtmpVQsrv7/remotes3bae1b2025a1/starters/DESCRIPTION’ ...
      
    ✔  checking for file ‘/tmp/RtmpVQsrv7/remotes3bae1b2025a1/starters/DESCRIPTION’
    ## 
      
    ─  preparing ‘starters’:
    ## 
      
       checking DESCRIPTION meta-information ...
      
    ✔  checking DESCRIPTION meta-information
    ## 
      
       checking vignette meta-information ...
      
    ✔  checking vignette meta-information
    ## 
      
    ─  checking for LF line-endings in source and make files and shell scripts
    ## 
      
    ─  checking for empty or unneeded directories
    ## 
      
    ─  building ‘starters_0.0.2.tar.gz’
    ## 
      
       
    ## 

``` r
print(gp)
```

    ## ── GP starters ────────────────────────────────────────────────────────────
    ## 
    ## It is good practice to
    ## 
    ##   ✖ write unit tests for all functions, and all package code in
    ##     general. 61% of code lines are covered by test cases.
    ## 
    ##     R/createBasicProject.R:108:NA
    ##     R/createBasicProject.R:109:NA
    ##     R/createBasicProject.R:110:NA
    ##     R/createBasicProject.R:111:NA
    ##     R/createBasicProject.R:112:NA
    ##     ... and 210 more lines
    ## 
    ##   ✖ use '<-' for assignment instead of '='. '<-' is the standard,
    ##     and R users and developers are used it and it is easier to
    ##     read your code for them if you use '<-'.
    ## 
    ##     R/createAnalysisProject.R:75:25
    ##     R/createBasicProject.R:141:22
    ##     R/createPackageProject.R:178:24
    ##     R/createTrainingProject.R:156:25
    ## 
    ## ───────────────────────────────────────────────────────────────────────────

# Typos

``` r
devtools::spell_check()
```

    ##   WORD              FOUND IN
    ## addin             README.md:25
    ##                   README.Rmd:36
    ## browseVignettes   starters.Rd:15
    ## codecov           createPackageProject.Rd:34
    ## config            createPackageProject.Rd:38
    ## flavours          BasicProjects.Rmd:12
    ## https             createAnalysisProject.Rd:46
    ##                   createBasicProject.Rd:42
    ##                   createPackageProject.Rd:47
    ##                   createTrainingProject.Rd:52
    ## md                BasicProjects.Rmd:28
    ## packrat           README.md:14,15
    ##                   README.Rmd:26,27
    ##                   TrainingProjects.Rmd:33
    ## Packrat           BasicProjects.Rmd:51
    ## PACKRAT           BasicProjects.Rmd:53
    ## pkgdown           createPackageProject.Rd:38
    ## pRoject           README.md:25
    ##                   README.Rmd:36
    ## pRojects          NEWS.md:5
    ## README            createAnalysisProject.Rd:31,49
    ##                   createBasicProject.Rd:29,45
    ##                   createPackageProject.Rd:30,50
    ##                   createTrainingProject.Rd:33,55
    ##                   BasicProjects.Rmd:25,26,28
    ##                   RPackages.Rmd:23
    ## repo              createAnalysisProject.Rd:44,45
    ##                   createBasicProject.Rd:40,41
    ##                   createPackageProject.Rd:45,46
    ##                   createTrainingProject.Rd:50,51
    ## repostatus        createAnalysisProject.Rd:30
    ##                   createBasicProject.Rd:28
    ##                   createPackageProject.Rd:29
    ##                   createTrainingProject.Rd:32
    ## reproducibility   createAnalysisProject.Rd:35
    ##                   createBasicProject.Rd:31
    ##                   createTrainingProject.Rd:41
    ##                   README.md:14,15
    ##                   README.Rmd:26,27
    ## Reproducibility   BasicProjects.Rmd:48
    ## Rmd               BasicProjects.Rmd:25,28
    ## RStudio           README.md:22,25,25
    ##                   README.Rmd:35,36,36
    ##                   BasicProjects.Rmd:20,37
    ##                   TrainingProjects.Rmd:31
    ## travis            createAnalysisProject.Rd:47,48
    ##                   createBasicProject.Rd:43,44
    ##                   createPackageProject.Rd:48,49
    ##                   createTrainingProject.Rd:53,54
    ## usethis           createPackageProject.Rd:6,56
