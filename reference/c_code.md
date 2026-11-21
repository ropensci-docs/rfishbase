# c_code

return a table of country information for the requested c_code, as
reported in FishBASE.org

## Usage

``` r
c_code(
  c_code = NULL,
  server = getOption("FISHBASE_API", "fishbase"),
  version = get_latest_release(),
  db = default_db(),
  ...
)
```

## Arguments

- c_code:

  a C_Code or list of C_Codes (FishBase country code)

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
c_code(440)
}
```
