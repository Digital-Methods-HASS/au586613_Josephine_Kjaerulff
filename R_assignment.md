Start with R
================

1)  Use R to figure out how many elements in the vector below are
    greater than 2 . (You need to filter out the NAs first)

<!-- end list -->

``` r
rooms <- c(1, 2, 1, 3, 1, NA, 3, 1, 3, 2, 1, NA, 1, 8, 3, 1, 4, NA, 1, 3, 1, 2, 1, 7, 1, NA)
rooms <- na.omit(rooms) #this removes na and cleans my data
length(rooms[rooms>2]) #this will tell me how many elements in the rooms vector are greater than two
```

    ## [1] 8

There are 8 elements that are greater than 2.

2)  What is the result of running median() function on the above ‘rooms’
    vector? (again, best remove the NAs)

<!-- end list -->

``` r
median(rooms)
```

    ## [1] 1.5

The median is 1.5

3)  Inside your R Project (.Rproj), install the ‘tidyverse’ package and
    use the download.file() and read\_csv() function to read the
    SAFI\_clean.csv dataset into your R project as ‘interviews’ digital
    object (see instructions in
    <https://datacarpentry.org/r-socialsci/setup.html> and ‘Starting
    with Data’ section).

<!-- end list -->

``` r
getwd()
```

    ## [1] "/Users/josephinekjaerulff/Documents/au586613_Kjaerulff_Josephine"

``` r
library(tidyverse)
```

    ## ── Attaching packages ──────────────────────────────────────────────────────────── tidyverse 1.3.0 ──

    ## ✓ ggplot2 3.3.2     ✓ purrr   0.3.4
    ## ✓ tibble  3.0.3     ✓ dplyr   1.0.2
    ## ✓ tidyr   1.1.2     ✓ stringr 1.4.0
    ## ✓ readr   1.3.1     ✓ forcats 0.5.0

    ## ── Conflicts ─────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

``` r
interviews <- read_csv("/Users/josephinekjaerulff/Documents/RStudio Cultural Data Science/data/SAFI_clean.csv", na = "NULL")
```

    ## Parsed with column specification:
    ## cols(
    ##   key_ID = col_double(),
    ##   village = col_character(),
    ##   interview_date = col_datetime(format = ""),
    ##   no_membrs = col_double(),
    ##   years_liv = col_double(),
    ##   respondent_wall_type = col_character(),
    ##   rooms = col_double(),
    ##   memb_assoc = col_character(),
    ##   affect_conflicts = col_character(),
    ##   liv_count = col_double(),
    ##   items_owned = col_character(),
    ##   no_meals = col_double(),
    ##   months_lack_food = col_character(),
    ##   instanceID = col_character()
    ## )
