Lab 03 - Nobel laureates
================
Heather Hawkins
01/23/23

### Load packages and data

``` r
library(tidyverse) 
```

``` r
nobel <- read_csv("data/nobel.csv")
```

## Exercises

### Exercise 1

``` r
nobel <- read_csv("data/nobel.csv")
dim(nobel)
```

    ## [1] 935  26

``` r
#to specify columns and rows
```

26 variables and 935 observations, each observation is a Noble Laureate

### Exercise 2

``` r
nobel_living <- nobel %>%
  filter(!is.na(country), gender!="org",is.na(died_date),)

dim(nobel_living)
```

    ## [1] 228  26

Got it! ☺️

``` r
nobel_living <- nobel_living %>%
  mutate(
    country_us = if_else(country == "USA", "USA", "Other")
  )
```

``` r
nobel_living_science <- nobel_living %>%
  filter(category %in% c("Physics", "Medicine", "Chemistry", "Economics"))

dim(nobel_living)
```

    ## [1] 228  27

### Exercise 3

### Exercise 4

…

### Exercise 5

…

### Exercise 6

…
