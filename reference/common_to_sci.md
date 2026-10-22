# common_to_sci

Return a list of scientific names corresponding to given the common
name(s).

## Usage

``` r
common_to_sci(
  x,
  Language = "English",
  server = c("fishbase", "sealifebase"),
  version = "latest",
  db = NULL
)
```

## Arguments

- x:

  a common name or list of common names

- Language:

  a string specifying the language for the common name, e.g. "English"

- server:

  Either "fishbase" or "sealifebase".

- version:

  a version string for the database. See
  [`available_releases()`](https://docs.ropensci.org/rfishbase/reference/available_releases.md)
  for details.

- db:

  database connection, now deprecated.

## Value

a character vector of scientific names

## Details

If more than one scientific name matches the common name (e.g. "trout"),
the function will simply return a list of all matching scientific names.
If given more than one common name, the resulting strings of matching
scientific names are simply concatenated.

## See also

[`synonyms`](https://docs.ropensci.org/rfishbase/reference/synonyms.md)

## Examples

``` r
if (FALSE) { # interactive()
# \donttest{
common_to_sci(c("Bicolor cleaner wrasse", "humphead parrotfish"), Language="English")
common_to_sci(c("Coho Salmon", "trout"))
# }
}
```
