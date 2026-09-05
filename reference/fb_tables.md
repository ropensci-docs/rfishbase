# List the tables available on fishbase/sealifebase

These table names can be used to access each of the corresponding tables
using `[fb_tbl()]`. Please note that following RDB design, it is often
necessary to join multiple tables. Other data cleaning steps are
sometimes necessary as well.

## Usage

``` r
fb_tables(server = c("fishbase", "sealifebase"), version = "latest")
```

## Arguments

- server:

  Access data from fishbase or sealifebase?

- version:

  Version, see
  [`available_releases()`](https://docs.ropensci.org/rfishbase/reference/available_releases.md)

## Examples

``` r
if (FALSE) { # interactive()
fb_tables()
}
```
