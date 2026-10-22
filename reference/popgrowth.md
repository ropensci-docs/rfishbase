# popgrowth

This table contains information on growth, natural mortality and length
at first maturity, which serve as inputs to many fish stock assessment
models. The data can also be used to generate empirical relationships
between growth parameters or natural mortality estimates, and their
correlates (e.g., body shape, temperature, etc.), a line of research
that is useful both for stock assessment and for increasing
understanding of the evolution of life-history strategies

## Usage

``` r
popgrowth(
  species_list = NULL,
  fields = NULL,
  server = c("fishbase", "sealifebase"),
  version = "latest",
  db = NULL,
  ...
)
```

## Arguments

- species_list:

  A vector of scientific names (each element as "genus species"). If
  empty, a table for all fish will be returned.

- fields:

  subset to these columns. (recommend to omit this and handle manually)

- server:

  Either "fishbase" or "sealifebase".

- version:

  a version string for the database. See
  [`available_releases()`](https://docs.ropensci.org/rfishbase/reference/available_releases.md)
  for details.

- db:

  database connection, now deprecated.

- ...:

  additional arguments, currently ignored

## Value

a table of population growth information by species; see details

## References

http://www.fishbase.org/manual/english/fishbasethe_popgrowth_table.htm

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
popgrowth("Oreochromis niloticus")
} # }
}
```
