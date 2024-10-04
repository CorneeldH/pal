
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Your pal <img src="man/figures/logo.png" align="right" height="200" alt="" />

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/pal)](https://CRAN.R-project.org/package=pal)
<!-- badges: end -->

Pals are persistent LLM-driven helpers designed to help you complete
common tasks in interactive data analysis, authoring, and package
development. Once created, they can be attached to a keybinding and
immediately get to work on repetitive but hard-to-automate tasks.

To create a pal, simply pass `pal()` the ID of a pre-defined pal and a
keybinding you’d like it attached to. For example, to use the cli pal:

``` r
pal("cli", "Ctrl+Shift+C")
```

> \[!CAUTION\] Much of the documentation in this package is aspirational
> and its interface is likely to change rapidly.

## Installation

You can install pal like so:

``` r
pak::pak("simonpcouch/pal")
```

Then, ensure that you have an `ANTHROPIC_API_KEY` set in your
[`.env`](https://github.com/gaborcsardi/dotenv). If you’d like to use an
LLM other than Anthropic’s Claude 3.5 Sonnet to power the pal, see
`?pal()` to set default metadata on that model.

## Example

For example, the cli pal created above with `pal("cli", "Ctrl+Shift+C")`
provides an RStudio add-in “Convert to cli” registered with the
keybinding “Ctrl+Shift+C”. After selecting some code, press the keyboard
shortcut and wait a moment:

![](inst/figs/addin.gif)

## Available Pals

There are pre-engineered pals for all sorts of tasks in R:

**Interactive Data Analysis**

- …

**Quarto / Authoring**

- `"label"`: Label code chunks

**Package development**

- `"cli"`: Convert to cli
- `"testthat"`: Convert to testthat 3
- `"roxygen"`: Document functions with roxygen

You can also create your own pals by passing a custom prompt to
`pal(role)`.
