# Pagerank_project

In this project, you will create a simple search engine for the website [https://www.lawfareblog.com](https://www.lawfareblog.com). This website provides legal analysis on U.S. national security issues. You will use **PageRank** to return only the most important results from this website in your search engine.

## Overview

This search engine applies the **PageRank algorithm** to rank pages on the Lawfare Blog website. PageRank assigns a score to each page based on the number and quality of links it receives from other pages, prioritizing the most authoritative content. Additionally, you can filter results by an **in-link ratio** or add a **personalization vector** to refine results based on specific search queries.

### Key Concepts

1. **PageRank Algorithm**: Measures the importance of pages based on their link structure, returning higher-ranked pages more prominently in search results.
2. **In-Link Ratio Filtering**: Filters out non-article pages by checking the number of links pointing to a page. Non-article pages, which typically appear in site menus, tend to have high in-link ratios and can be excluded from results.
3. **Personalization Vector**: Boosts the relevance of search results by personalizing PageRank based on specific keywords in the URLs.

## Getting Started

To get started, ensure you have Python installed along with the required dependencies, including `torch` for efficient tensor operations. The project uses compressed `.csv.gz` data for storing the website's link structure.

### Prerequisites

1. Python 3.6 or later
2. `torch` library

## Running the Search Engine

The program is executed through the command line with various flags to customize the search engine’s behavior. Here are some of the main flags:

- `--data`: Specifies the path to the input data file, typically a compressed CSV file representing the website's link structure.
- `--search_query`: Filters results based on specific terms found in the URLs.
- `--filter_ratio`: Filters out pages with an in-link ratio higher than a specified threshold.
- `--alpha`: Sets the damping factor for PageRank, with a typical value around 0.85.
- `--personalization_vector_query`: Uses a query to create a personalization vector, assigning higher PageRank scores to pages that satisfy the specified keywords.
