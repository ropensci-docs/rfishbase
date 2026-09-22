# synonyms

Check for alternate versions of a scientific name

## Usage

``` r
synonyms(
  species_list = NULL,
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

A table with information about the synonym. Will generally be only a
single row if a species name is given. If a FishBase SpecCode is given,
all synonyms matching that SpecCode are shown, and the table indicates
which one is Valid for FishBase. This may or may not match the valid
name for Catalog of Life (Col), also shown in the table. See examples
for details.

## Details

For further information on fields returned, see:
http://www.fishbase.org/manual/english/fishbasethe_synonyms_table.htm
