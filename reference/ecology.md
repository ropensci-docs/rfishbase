# ecology

ecology

## Usage

``` r
ecology(
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

a table of species ecology data

## Details

By default, will only return one entry (row) per species. Increase limit
to get multiple returns for different stocks of the same species, though
often data is either identical to the first or simply missing in the
additional stocks.

## References

http://www.fishbase.org/manual/english/fishbasethe_ecology_table.htm

## Examples

``` r
if (FALSE) { # interactive()

if (FALSE) { # \dontrun{
ecology("Oreochromis niloticus")

## trophic levels and standard errors for a list of species
ecology(c("Oreochromis niloticus", "Salmo trutta"),
        fields=c("SpecCode", "FoodTroph", "FoodSeTroph", "DietTroph", "DietSeTroph"))
} # }
}
```
