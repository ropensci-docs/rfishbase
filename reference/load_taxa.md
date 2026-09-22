# load_taxa

Show scientific classification of taxa Note: species_names() is an alias
for load taxa.

## Usage

``` r
load_taxa(server = c("fishbase", "sealifebase"), version = "latest", ...)
```

## Arguments

- server:

  Either "fishbase" (the default) or "sealifebase"

- version:

  the version of the database you want. Will default to the latest
  available; see
  [`available_releases()`](https://docs.ropensci.org/rfishbase/reference/available_releases.md).

- ...:

  for compatibility with previous versions

## Value

the taxa list
