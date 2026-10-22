# Access a fishbase or sealifebase table

Please note that rfishbase accesses static snapshots of the raw database
tables used by FishBase and Sealifebase websites. Because these are
static snapshots, they may lag behind the latest available information
on the web interface, but should provide stable results.

## Usage

``` r
fb_tbl(
  tbl,
  server = c("fishbase", "sealifebase"),
  version = "latest",
  db = NULL,
  collect = TRUE
)
```

## Arguments

- tbl:

  table name, as it appears in the database. See
  [`fb_tables()`](https://docs.ropensci.org/rfishbase/reference/fb_tables.md)
  for a list.

- server:

  Access data from fishbase or sealifebase?

- version:

  Version, see
  [`available_releases()`](https://docs.ropensci.org/rfishbase/reference/available_releases.md)

- db:

  database connection, deprecated

- collect:

  should we return an in-memory table? Generally best to leave as TRUE
  unless RAM is too limited. A remote table can be used with most dplyr
  functions (filter, select, joins, etc) to further refine.

## Details

Please also note that the website pages are not organized precisely
along the lines of these tables. A given page for a species may draw on
data from multiple tables, and sometimes presents the data in a
processed or summarized form. Following RDB design, it is often
necessary to join multiple tables. Other data cleaning steps are
sometimes necessary as well.

## Examples

``` r
if (FALSE) { # interactive()
fb_tbl("species")
}
```
