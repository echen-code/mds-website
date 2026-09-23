# echen-code.github.io

Personal data science blog built with Quarto, including two reproducible
computational posts (Python and R) comparing GDP per capita in Taiwan and
Canada, using Gapminder dataset.

## Prerequisites

- Quarto >= 1.5
- uv >= 0.5
- R >= 4.4
- renv bootstraps itself on first `quarto render`

## Build instructions (from a clean clone)

Run all commands from the repository top level.

```bash
git clone https://github.com/echen-code/mds-website.git
cd ~/mds-website

# Python environment
uv sync
```
```r
# R environment — start R at the repo top level (e.g. `R` in this directory)
renv::restore()
```
```bash
# Render the whole site from top level 
uv run quarto render
```

## Viewing the built site
Live site: https://echen-code.github.io/mds-website/

## Data

Both posts use `gapminder.csv`, downloaded from the Software Carpentry
r-novice-gapminder lesson materials
(https://raw.githubusercontent.com/swcarpentry/r-novice-gapminder/main/episodes/data/gapminder_data.csv),
itself an excerpt of Gapminder.org data (CC BY 4.0).
