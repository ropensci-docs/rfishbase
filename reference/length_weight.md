# length_weight

The LENGTH-WEIGHT table presents the a and b values of over 5,000
length-weight relationships of the form W = a x Lb, pertaining to about
over 2,000 fish species.

## Usage

``` r
length_weight(
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

a table of length_weight information by species; see details

## Details

See references for official documentation. From FishBase.org:
Length-weight relationships are important in fisheries science, notably
to raise length-frequency samples to total catch, or to estimate biomass
from underwater length observations. The units of length and weight in
FishBase are centimeter and gram, respectively. Thus when length-weight
relationships are not in cm-g, the intercept 'a' is transformed as
follows:

a'(cm, g) = a (mm, g)\*10^b a'(cm, g) = a (cm, kg)\*1000 a'(cm, g) = a
(mm, mg)\*10^b/1000 a'(cm, g) = a (mm, kg)*10^b*1000

However, published length-weight relationships are sometimes difficult
to use, as they may be based on a length measurement type (e.g., fork
length) different from ones length measurements (expressed e.g., as
total length). Therefore, to facilitate conversion between length types,
an additional LENGTH-LENGTH table, \#' presented below, was devised
which presents linear regressions or ratios linking length types (e.g.,
FL vs. TL). We included a calculated field with the weight of a 10 cm
fish (which should be in the order of 10 g for normal, fusiform shaped
fish), to allow identification of gross errors, given knowledge of the
body form of a species.

## References

http://www.fishbase.org/manual/english/fishbasethe_length_weight_table.htm

## Examples

``` r
if (FALSE) { # interactive()
if (FALSE) { # \dontrun{
length_weight("Oreochromis niloticus")
} # }
}
```
