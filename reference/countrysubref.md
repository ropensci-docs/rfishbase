# countrysubref

return a table of countrysubref

## Usage

``` r
countrysubref(
  server = getOption("FISHBASE_API", "fishbase"),
  version = get_latest_release(),
  db = default_db(),
  ...
)
```

## Arguments

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

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
countrysubref()
} # }
}
```
