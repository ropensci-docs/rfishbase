# faoareas

return a table of species locations as reported in FishBASE.org FAO
location data

## Usage

``` r
faoareas(
  species_list = NULL,
  fields = NULL,
  server = getOption("FISHBASE_API", "fishbase"),
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

a tibble, empty tibble if no results found

## Examples

``` r
if (FALSE) { # interactive()
  faoareas()
}
```
