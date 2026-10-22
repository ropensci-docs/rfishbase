# species

Provide wrapper to work with species lists.

## Usage

``` r
species(
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

a data.frame with rows for species and columns for the fields returned
by the query (FishBase 'species' table)

## Details

The Species table is the heart of FishBase. This function provides a
convenient way to query, tidy, and assemble data from that table given
an entire list of species. For details, see:
http://www.fishbase.org/manual/english/fishbasethe_species_table.htm

Species scientific names are defined according to fishbase taxonomy and
nomenclature.

## Examples

``` r
if (FALSE) { # \dontrun{

species(c("Labroides bicolor", "Bolbometopon muricatum")) 

} # }
```
