# popchar

Table of maximum length (Lmax), weight (Wmax) and age (tmax)

## Usage

``` r
popchar(
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

## Details

See references for official documentation. From FishBase.org: This table
presents information on maximum length (Lmax), weight (Wmax) and age
(tmax) from various localities where a species occurs. The largest
values from this table are also entered in the SPECIES table. The
POPCHAR table also indicates whether the Lmax, Wmax and tmax values or
various combinations thereof refer to the same individual fish.

## References

http://www.fishbase.org/manual/english/fishbasethe_popchar_table.htm

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
popchar("Oreochromis niloticus")
} # }
}
```
