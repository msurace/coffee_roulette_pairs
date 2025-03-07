
<!-- README.md is generated from README.Rmd. Please edit that file -->

# coffeeroulettepairs

<!-- badges: start -->
<!-- badges: end -->

Save time when organising a round of coffee roulette chats, in which
people who sign up are paired up randomly with each other! The code
generates the random pairs for you, and ensures each person appears only
once per round.

## Installation

You can install coffeeroulettepairs like so:

``` r
devtools::install_github("moj-analytical-services/coffee_roulette_pairs")
```

## Usage

-   Create a one column csv file containing the list of names, and if
    required a two column csv file containing pairs of names which you
    don’t want to appear in the random matches.
-   Run the `main` function, which writes a new csv file called
    `randompairs.csv` containing the random pairs of names, and appends
    to or creates a two column csv file called `unwantedpairs.csv`,
    containing the pairs which have just been matched, in addition to
    any pre-existing ones.

## Example

You can find an example list of names and unwanted pairs in the
`inst/extdata` directory. The example below uses those files as an
illustration.

``` r
library(coffeeroulettepairs)

# Specify the path to the file containing a list of names in one column
names <- system.file("extdata", "names.csv", package = "coffeeroulettepairs")

# Specify the path to the file containing the unwanted pairs of names in two columns, one pair per row
uwp <- system.file("extdata", "unwantedpairs.csv", package = "coffeeroulettepairs")

# Run the main function. NB the output will be saved in your current working directory
main(names_file = names, unwantedpairs_file = uwp)
#> 
#> ── Column specification ────────────────────────────────────────────────────────
#> cols(
#>   X1 = col_character()
#> )
#> 
#> ── Column specification ────────────────────────────────────────────────────────
#> cols(
#>   P1 = col_character(),
#>   P2 = col_character()
#> )
```
