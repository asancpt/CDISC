
R4DSXML
=======

dataset-xml
-----------

``` r
# devtools::install_github("DataDrivenInc/R4DSXML/R4DSXML")

library(R4DSXML)
```

    ## Loading required package: XML

    ## Loading required package: methods

    ## Loading required package: stringr

``` r
define <- system.file("extdata", "SDTM",
                      "define2-0-0-example-sdtm(2013-11-09).xml", 
                       package="R4DSXML"
                       ) 
sds <- system.file("extdata", "SDTM",
                   "dm.xml", 
                    package="R4DSXML"
                    )

DM <- read.dataset.xml(dataset_xml=sds, define_xml=define)

knitr::kable(DM)
```

| STUDYID | DOMAIN | USUBJID        | SUBJID | RFSTDTC    | RFENDTC    | SITEID | BRTHDTC    |  AGE| AGEU  | SEX | RACE                      | ETHNIC                 | ARMCD    | ARM                | COUNTRY |
|:--------|:-------|:---------------|:-------|:-----------|:-----------|:-------|:-----------|----:|:------|:----|:--------------------------|:-----------------------|:---------|:-------------------|:--------|
| CDISC01 | DM     | CDISC01.100008 | 100008 | 2003-04-29 | 2003-10-12 | 100    | 1930-08-05 |   72| YEARS | M   | OTHER                     | NOT HISPANIC OR LATINO | WONDER10 | Miracle Drug 10 mg | USA     |
| CDISC01 | DM     | CDISC01.100014 | 100014 | 2003-10-15 | 2004-03-29 | 100    | 1936-11-01 |   66| YEARS | F   | WHITE                     | NOT HISPANIC OR LATINO | WONDER20 | Miracle Drug 20 mg | USA     |
| CDISC01 | DM     | CDISC01.200001 | 200001 | 2003-09-30 | 2004-02-02 | 200    | 1923-09-03 |   80| YEARS | F   | MULTIPLE                  | NOT HISPANIC OR LATINO | PLACEBO  | Placebo            | USA     |
| CDISC01 | DM     | CDISC01.200002 | 200002 | 2003-10-10 | 2004-03-28 | 200    | 1933-07-22 |   70| YEARS | F   | BLACK OR AFRICAN AMERICAN | NOT HISPANIC OR LATINO | WONDER10 | Miracle Drug 10 mg | USA     |
| CDISC01 | DM     | CDISC01.200005 | 200005 | NA         | NA         | 200    | 1937-02-22 |   66| YEARS | F   | WHITE                     | NOT HISPANIC OR LATINO | SCRNFAIL | Screen Failure     | USA     |
