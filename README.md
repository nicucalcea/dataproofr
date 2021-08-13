dataproofr
================

dataproofr is a wrapper for the excellent
[dataproofer](https://github.com/dataproofer/Dataproofer) package. It
automatically checks for a series of potential errors and mistakes in a
dataset.

## Installation

You can install `dataproofr` with the following command:

``` r
remotes::install_github("nicucalcea/dataproofr")
```

dataproofr uses the
[dataproofer](https://github.com/dataproofer/Dataproofer) NodeJS package
under the hood, so it will need NodeJS and npm installed on your device.

After installing the library, you can run `node_available()` to check
whether the necessary software is installed. If it’s not, install it to
use `dataproofr`.

After you’ve confirmed that NodeJS and npm are installed, run the
following command to install
[dataproofer](https://github.com/dataproofer/Dataproofer):

``` r
dataproofer_install()
```

## Using dataproofr

The most straightforward to use the library is this:

``` r
proof(iris)
```

There are a few optional arguments you can use. Among other things, you
can specify which tests to run with `tests` or you can output the result
of the tests with `out`.

``` r
proof(iris, tests = "core", verbose = TRUE)
```

Alternatively, you can use `proof_custom()` with the arguments from the
[original NodeJS library](https://github.com/dataproofer/Dataproofer):

``` r
proof_custom(iris, options = "--core --summary")
```

You can run `proof_custom(iris, options = "--help")` for a full list of
commands.
