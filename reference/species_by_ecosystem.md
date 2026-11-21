# Species list by ecosystem

Species list by ecosystem

## Usage

``` r
species_by_ecosystem(
  ecosystem,
  species_list = NULL,
  server = getOption("FISHBASE_API", "fishbase"),
  version = "latest",
  db = NULL,
  ...
)
```

## Arguments

- ecosystem:

  (character) an ecosystem name

- species_list:

  A vector of scientific names (each element as "genus species"). If
  empty, a table for all fish will be returned.

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

a table of species ecosystems data

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
species_by_ecosystem(ecosystem = "Arctic", server = "sealifebase")
} # }
}
```
