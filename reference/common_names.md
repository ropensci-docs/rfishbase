# common names

Return a table of common names

## Usage

``` r
common_names(
  species_list = NULL,
  server = c("fishbase", "sealifebase"),
  version = "latest",
  db = NULL,
  Language = "English",
  fields = NULL
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

- Language:

  a string specifying the language for the common name, e.g. "English"

- fields:

  subset to these columns. (recommend to omit this and handle manually)

## Value

a data.frame of common names by species queried. If multiple species are
queried, The resulting data.frames are concatenated.

## Details

Note that there are many common names for a given sci name

## Examples

``` r
if (FALSE) { # interactive()
common_names("Bolbometopon muricatum")
}
```
