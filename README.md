# Google Search Results Scraper

## Description

This repository contains a Python-based scraper that extracts data from Google Search Results (SERP) using the [Crawlbase Crawling API](https://crawlbase.com/crawling-api-avoid-captchas-blocks). The scraper uses the **Google SERP Scraper** provided by Crawlbase, which bypasses CAPTCHA challenges, anti-bot protections, and handles JavaScript-rendered content seamlessly.

The extracted data is parsed and saved in JSON format, including relevant information such as search result titles, URLs, snippets, related searches, and ads.

➡ For detailed instructions, visit the full blog [here](https://crawlbase.com/blog/scrape-google-search-results-with-python/).

## Features

The scraper extracts the following information from Google Search Results:

1. **Search Results** – Includes the position, title, URL, and description for each result.
2. **Related Searches** – Suggestions for related searches on Google.
3. **Ads** – Paid advertisements appearing on the results page (if available).
4. **People Also Ask** – FAQs related to the search query (if available).
5. **Snack Pack** – Local business listings or other special results (if available).

The scraper also handles pagination and saves the results in a clean JSON file for easy further processing.

## Requirements

- **Python 3.x** (check your version with python --version)
- **Required libraries:**

  - **crawlbase** – For handling JavaScript-rendered content and bypassing CAPTCHAs
  - **json** – For parsing and saving data in JSON format.

  To install the required libraries, run:

  ```bash
  pip install crawlbase
  ```

## Environment Setup

1. **Get Your Crawlbase Access Token**

- Sign up for Crawlbase [here](https://crawlbase.com/signup) to obtain your API token.
- Use the **JavaScript (JS) token** since Google uses JavaScript-rendered content.

2. **Update the Scraper with Your Token**

- In the `google_serp_scraper.py` script, replace `"YOUR_CRAWLBASE_TOKEN"` with your Crawlbase API token.

## Running the Scraper

1. Clone this repository or download the script.
2. Open a terminal and navigate to the folder containing the script.
3. Run the scraper:

```bash
python google_serp_scraper.py
```

This will scrape the Google Search results for the query specified in the script (e.g., `"web scraping tools"`) and save the results in a JSON file (`google_search_results.json`).

## Customization

You can customize the scraper by changing the search query and adjusting the maximum number of pages to scrape.

- Change the query by modifying the query variable in the script.
- Adjust the number of pages to scrape by modifying the max_pages variable.

## To-Do List

- Handle more complex Google result types (e.g., images, videos).
- Implement better error handling for failed requests.
- Add support for saving data in additional formats like CSV or databases.

## Why Use This Scraper?

- **Bypasses CAPTCHAs and anti-bot protections** with Crawlbase.
- **Handles JavaScript-rendered content** seamlessly.
- **Extracts structured Google Search results** efficiently.
- **Supports easy pagination** for scraping multiple pages.
