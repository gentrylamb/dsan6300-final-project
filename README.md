# Airline On-Time Statistics and Delay Causes Analysis

A multi-dataset exploration of U.S. airline delays using SQL, Python, and Quarto.

## Project Overview

This project analyzes patterns in commercial airline delays using derived SQL data, including flight performance, airports, airlines, weather, and aircraft metadata. Data is originially from the [Airline On-Time Statistics and Delay Causes](https://www.transtats.bts.gov/) data set, published by the United States Department of Transportation. The analysis is implemented in `code.ipynb`, and all narrative, interpretation, and visual outputs are integrated in a **Quarto website** using `{{< embed ... >}}` blocks to embed notebook-based charts.

## Key Questions Explored

* Which airports experience the worst delay patterns?
* Which airlines have the highest/lowest on-time performance?
* Do certain airlines consistently struggle at specific airports?
* How do departure delays differ from arrival delays?
* What relationships emerge when combining multiple datasets (weather, aircraft age, route distance, etc.)?

## Visualizations

All visualizations are produced in Python using `matplotlib`, `seaborn`, and notebook cell tags for embedding.

```markdown
{{< embed code.ipynb#airline-departure-delay >}}
```

## Tech Stack

* **Python** (pandas, matplotlib, seaborn)
* **SQL** for data extraction and preprocessing
* **Quarto** for website generation and narrative structure
* **Jupyter Notebook** for computation and visualization

## Repository Structure

```
├── README.md
├── data/                           # All seven CSV datasets from SQL queries
│   ├── Miniproject_Lamb_Gentry_gjl53_problem01.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem02.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem03.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem04.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem05.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem06a.csv
│   ├── Miniproject_Lamb_Gentry_gjl53_problem06b.csv
│   └── Miniproject_Lamb_Gentry_gjl53_problem07.csv
├── docs/                           # Rendered Quarto website (HTML output)
│   ├── index.html
│   ├── code.html
│   ├── story.html
│   └── site_libs/                  # Quarto assets (bootstrap, JS, CSS)
└── website/                        # Source files for the Quarto site
    ├── _quarto.yml                     # Site configuration
    ├── code.ipynb                      # Full analysis + visualizations
    ├── index.qmd                       # Home page
    └── story.qmd                       # Narrative and embedded charts
```