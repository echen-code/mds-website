# mds-website

This is Ethan Chen's Quarto website, with posts written in Quarto with R and Python.

## Build from a fresh clone

Install Quarto, R 4.6.1, Python 3.14, and `uv` first. Then run:

```sh
git clone <repository-url>
cd mds-website

# Restore the R environment and activate it for this project.
Rscript -e 'renv::restore(prompt = FALSE)'

# Create the Python environment from pyproject.toml and uv.lock.
uv sync --locked

# Render the site into docs/ for GitHub Pages.
quarto render
```

The rendered site is written to `docs/`. Open `docs/index.html` locally to check the result, or publish the repository with GitHub Pages configured to serve from the `docs/` folder on the main branch.

The analysis data in both posts comes from [Gapminder](https://www.gapminder.org/data/) and is distributed under its [CC BY 4.0 licence](https://www.gapminder.org/license/).