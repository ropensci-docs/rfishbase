# validate_names

Check for alternate versions of a scientific name and return the
scientific names FishBase recognizes as valid

## Usage

``` r
validate_names(
  species_list,
  server = getOption("FISHBASE_API", "fishbase"),
  version = get_latest_release(),
  db = default_db(),
  ...
)
```

## Arguments

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

a string of the validated names

## Examples

``` r
if (FALSE) { # interactive()

  # \donttest{
validate_names("Abramites ternetzi")
# }
}
```
