# Quarto Learning Repo

### Quarto Dashboards Learning Materials

- [PositPBC](https://www.youtube.com/@PositPBC)
- [Quarto Dashboards 1: Hello, Dashboards!](https://www.youtube.com/watch?v=HW7QbqI4fH0)
  - [Slides: 1-hello-dashboards](https://mine.quarto.pub/quarto-dashboards/1-hello-dashboards)
- [Quarto Dashboards 2: Components](https://www.youtube.com/watch?v=KdsQgwaY950)
  - [Slides: 2-dashboard-components](https:///mine.quarto.pub/quarto-dashboards/2-dashboard-components)
- [Quarto Dashboards 3: Theming and Styling](https://www.youtube.com/watch?v=NigWSB-jG4Y)
- [GitHub: quarto-dashboards](https://github.com/mine-cetinkaya-rundel/quarto-dashboards)
- [GitHub: olympicdash](https://github.com/mine-cetinkaya-rundel/olympicdash)
- [Dashboards with Shiny for R](https://quarto.org/docs/dashboards/interactivity/shiny-r.html)
- [Quarto GitHub Pages](https://quarto.org/docs/publishing/github-pages.html)
### My Repos

- [olympicdash](https://github.com/byandell/olympicdash)
- ([olympicdash-r-1.qmd](https://github.com/byandell/olympicdash/blob/main/olympicdash-r-1.qmd))
- ([olympicdash-r-2.qmd](https://github.com/byandell/olympicdash/blob/main/olympicdash-r-2.qmd))

Also python alternatives.

### Notes and Resources

- <https://quarto.org/>
- <https://quarto.org/docs/websites/>.
- <https://plotnine.org/> for Python version of ggplot.
- top bar
  - [_quarto.yml](https://github.com/byandell/quarto/blob/main/_quarto.yml)
  - [index.qmd](https://github.com/byandell/quarto/blob/main/index.qmd)
  - [about.qmd](https://github.com/byandell/quarto/blob/main/about.qmd)
  - navigation buttons on far right (see YAML)
- second bar
  - title (see YAML)
  - first level headings (`#`) map onto tabs in second bar
- body
  - second level headings (`##`) map onto major `rows` (default) or `columns` via YAML
  - third level headings (`###`) map onto minor `columns` (default) or `rows`
  - titles in magic comments inside code chunks (`#| title: Blah`)
  - alter sizes for column `{width="70%"}` and/or row `{height="60%"}`
  - tabsets within major rows via `{.tabset}`
- component fill `{.fill}` (default) or flow `{.flow}` (markdown default)
- scrolling sub to dashboard (`scrolling: true`)
- orientation and scrolling can be set at dashboard or page component level
  - `## Blah {orientation="rows"}`
  - `## Blah {orientation="columns" scrolling="true"}`
- cards placed in page components (rows or columns)
  - code chunks or markdowns that have output create cards
  - manually create with fench div paragraph from `::: {.card title="Title"}` through `:::`
  - `#| output: false` hide code chunk
  - multiple outputs in code chunk end up in one card
    - use `#| layout-ncol: 2` to layout plots in columns
- value boxes
  - use Bootstrap icons (<https://icons.getbootstrap.com>)
  - default colors can be changed
  - expand button
  - see [componentValue-r.qmd](https://github.com/byandell/quarto/blob/main/componentValue-r.qmd)
- markdown text
  - 
### Sidebar

```

# {.sidebar}

Main Sidebar.

# Scatter

## {.sidebar}

Sidebar for Scatter.

##
```

### YAML

YAML is its own language.
It is situated between lines with three dashes (`---`).
Components can be on same line (`format: dashbard`) or indented.

#### title

```
title: "Pages"
```

```
cat("title=", "Blah", myvar)
<more code>
```

#### dashboard

with orientation and nav-buttons

```
format:
  dashboard:
    orientation: columns
    nav-buttons: [github]
    github: https://github.com/byandell/olympicdash
```

logo (can be sub to `dashboard`)

```
logo: images/olympics-logo.svg
logo-alt: Olympics logo with multicolored circles.
```

navigation buttons

```
format:
  dashboard:
    logo: images/beetle.png
    nav-buttons:
      - icon: github
        href: https://github.com/quarto-dev/quarto-cli
        aria-label: GitHub
      - icon: linkedin
        href: https://www.linkedin.com/company/posit-software/
        aria-label: LinkedIn
      - icon: youtube
        href: https://youtube.com]
        aria-label: YouTube

```
