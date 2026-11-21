# references

references

## Usage

``` r
references(
  codes = NULL,
  fields = NULL,
  server = getOption("FISHBASE_API", "fishbase"),
  version = get_latest_release(),
  db = default_db(),
  ...
)
```

## Arguments

- codes:

  One or more Fishbase reference numbers, matching the RefNo field

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

a tibble (data.frame) of reference data

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
references(codes = 1)
references(codes = 1:6)
references(codes = 1:6, fields = c('Author', 'Year', 'Title'))
references() # all references
} # }
}
```
