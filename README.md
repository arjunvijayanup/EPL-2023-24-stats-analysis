# EPL 2023/24 Premier League Stats Analysis

&#x20;

## Overview

This repository contains an in-depth statistical analysis of the 2023–24 Premier League season, conducted in R using Quarto. The analysis covers player performance, club-level distributions, and includes a custom R package with S3 methods to facilitate further exploration.

## Table of Contents

- [Installation](#installation)
- [Data Source](#data-source)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Analysis Overview](#analysis-overview)
  - [Part 1: Exploratory Analysis](#part-1-exploratory-analysis)
  - [Part 2: R Package Development](#part-2-r-package-development)
  - [Part 3: Custom Functions and S3 Methods](#part-3-custom-functions-and-s3-methods)
- [Results and Outputs](#results-and-outputs)
- [References](#references)
- [Author](#author)
- [License](#license)

## Installation

1. **Install R (>= 4.0)** and [**Quarto**](https://quarto.org/).
2. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/epl-2023-24-stats-analysis.git
   cd epl-2023-24-stats-analysis
   ```
3. Install required R packages:
   ```r
   install.packages(c(
     "tidyverse", "readxl", "countrycode",
     "ggplot2", "summarytools", "devtools"
   ))
   ```

## Data Source

- Player statistics for the 2023–24 season were sourced from [FBref](https://fbref.com/en/) and saved in `data/2023_24_PL_Player_Stats.xlsx`.

## Usage

Render the analysis document in HTML or PDF:

```bash
quarto render EPL-2023-24-stats-analysis.qmd --to html
```

Or for PDF:

```bash
quarto render EPL-2023-24-stats-analysis.qmd --to pdf
```

## Project Structure

```
├── data/
│   └── 2023_24_PL_Player_Stats.xlsx
├── R/
├── figures/             # Generated plots
├── EPL-2023-24-stats-analysis.qmd
└── README.md
```

## Analysis Overview

### Part 1: Exploratory Analysis

- **Top 10 Countries with Most Players**: Table of countries by player count.
- **Top Under-22 Players by Efficiency**: Comparison of goal contributions vs expected goal contributions.
- **Expected Assists vs Non-Penalty Goals (Liverpool)**: Scatter plot analysis for Liverpool players.
- **Club-Wise Distribution of Goals and Assists**: Barplot of total contributions by club.

### Part 2: R Package Development

- **Purpose**: Offer streamlined functions for data summarization and descriptive statistics.
- **Main Functions**:
  - `summarize_stats()`: Generate descriptive statistics.
  - `distribution_stats()`: Create frequency distributions.
  - `group_stats()`: Compute grouped summaries by player position.

### Part 3: Custom Functions and S3 Methods

- **Function**: Constructs an S3 object encapsulating player data.
  - **Methods**:
    - `print()`: Nicely formatted console output.
    - `summary()`: Summary statistics for the S3 object.
    - `plot()`: Visual comparison of player performance per 90 minutes.

## Results and Outputs

All tables and figures are generated in the `figures/` directory. Please view the rendered `.html` or `.pdf` output for detailed insights.

## References

- FBref: [https://fbref.com/en/](https://fbref.com/en/)
- Quarto: [https://quarto.org/](https://quarto.org/)

## Author

Arjun Vijay Anup
