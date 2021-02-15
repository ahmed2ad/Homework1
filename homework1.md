Homework \#1 – Pet Names Dataset
================
Ahmed adnan
2021-02-15

**Student ID:insert ID here** 2200000997

**Deadline:** 23:59 on Saturday, 13 February 2021

**Total Points:** 30

## Loading Packages

``` r
library(tidyverse)
library(openintro)
library(ggrepel)
```

\#\#Exercises

\`1.

(4 points)

``` r
seattlepets %>%
count(animal_name, sort = TRUE)
```

    ## # A tibble: 13,930 x 2
    ##    animal_name     n
    ##    <chr>       <int>
    ##  1 <NA>          483
    ##  2 Lucy          439
    ##  3 Charlie       387
    ##  4 Luna          355
    ##  5 Bella         331
    ##  6 Max           270
    ##  7 Daisy         261
    ##  8 Molly         240
    ##  9 Jack          232
    ## 10 Lily          232
    ## # … with 13,920 more rows

Write your narrative here

\`2.

(4 points)

``` r
seattlepets %>%
group_by(species) %>%
count(animal_name, sort = TRUE)
```

    ## # A tibble: 16,823 x 3
    ## # Groups:   species [4]
    ##    species animal_name     n
    ##    <chr>   <chr>       <int>
    ##  1 Cat     <NA>          406
    ##  2 Dog     Lucy          337
    ##  3 Dog     Charlie       306
    ##  4 Dog     Bella         249
    ##  5 Dog     Luna          244
    ##  6 Dog     Daisy         221
    ##  7 Dog     Cooper        189
    ##  8 Dog     Lola          187
    ##  9 Dog     Max           186
    ## 10 Dog     Molly         186
    ## # … with 16,813 more rows

Write your narrative below

\`3. Copy the code provided in the homework documentation and paste it
here.

(4 points)

``` r
seattlepets %>%
count(species, sort = TRUE)
```

    ## # A tibble: 4 x 2
    ##   species     n
    ##   <chr>   <int>
    ## 1 Dog     35181
    ## 2 Cat     17294
    ## 3 Goat       38
    ## 4 Pig         6

Write your narrative here

\`4.

(10 points)

``` r
seattlepets %>%
group_by(species) %>%
count(animal_name, sort = TRUE) %>%
slice_max(n, n = 5)
```

    ## # A tibble: 53 x 3
    ## # Groups:   species [4]
    ##    species animal_name     n
    ##    <chr>   <chr>       <int>
    ##  1 Cat     <NA>          406
    ##  2 Cat     Luna          111
    ##  3 Cat     Lucy          102
    ##  4 Cat     Lily           86
    ##  5 Cat     Max            83
    ##  6 Dog     Lucy          337
    ##  7 Dog     Charlie       306
    ##  8 Dog     Bella         249
    ##  9 Dog     Luna          244
    ## 10 Dog     Daisy         221
    ## # … with 43 more rows

\`5. What names are more common for cats than dogs? The ones above the
line or the ones below the line?

Answer here

(4 points)

\`6. Is the relationship between the two variables (proportion of cats
with a given name and proportion of dogs with a given name) positive or
negative? What does this mean in context of the data?

Answer here

(4 points)
